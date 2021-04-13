---
description: Il \_ PCVIDEOCONTROLLER CIM rappresenta le funzionalità e la gestione di un personal computer controller video, un sottotipo di un controller video.
ms.assetid: bf937727-a332-445b-9397-7d87d58c4a5b
ms.tgt_platform: multiple
title: Classe CIM_PCVideoController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PCVideoController
- CIM_PCVideoController.AcceleratorCapabilities
- CIM_PCVideoController.Availability
- CIM_PCVideoController.CapabilityDescriptions
- CIM_PCVideoController.Caption
- CIM_PCVideoController.ConfigManagerErrorCode
- CIM_PCVideoController.ConfigManagerUserConfig
- CIM_PCVideoController.CreationClassName
- CIM_PCVideoController.CurrentBitsPerPixel
- CIM_PCVideoController.CurrentHorizontalResolution
- CIM_PCVideoController.CurrentNumberOfColors
- CIM_PCVideoController.CurrentNumberOfColumns
- CIM_PCVideoController.CurrentNumberOfRows
- CIM_PCVideoController.CurrentRefreshRate
- CIM_PCVideoController.CurrentScanMode
- CIM_PCVideoController.CurrentVerticalResolution
- CIM_PCVideoController.Description
- CIM_PCVideoController.DeviceID
- CIM_PCVideoController.ErrorCleared
- CIM_PCVideoController.ErrorDescription
- CIM_PCVideoController.InstallDate
- CIM_PCVideoController.LastErrorCode
- CIM_PCVideoController.MaxMemorySupported
- CIM_PCVideoController.MaxNumberControlled
- CIM_PCVideoController.MaxRefreshRate
- CIM_PCVideoController.MinRefreshRate
- CIM_PCVideoController.Name
- CIM_PCVideoController.NumberOfColorPlanes
- CIM_PCVideoController.NumberOfVideoPages
- CIM_PCVideoController.PNPDeviceID
- CIM_PCVideoController.PowerManagementCapabilities
- CIM_PCVideoController.PowerManagementSupported
- CIM_PCVideoController.ProtocolSupported
- CIM_PCVideoController.Status
- CIM_PCVideoController.StatusInfo
- CIM_PCVideoController.SystemCreationClassName
- CIM_PCVideoController.SystemName
- CIM_PCVideoController.TimeOfLastReset
- CIM_PCVideoController.VideoArchitecture
- CIM_PCVideoController.VideoMemoryType
- CIM_PCVideoController.VideoMode
- CIM_PCVideoController.VideoProcessor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 94465862c34cc9c6fb645f63c0add48d0fded56b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401456"
---
# <a name="cim_pcvideocontroller-class"></a><span data-ttu-id="257dc-103">CIM \_ PCVideoController (classe)</span><span class="sxs-lookup"><span data-stu-id="257dc-103">CIM\_PCVideoController class</span></span>

<span data-ttu-id="257dc-104">Il **\_ PCVideoController CIM** rappresenta le funzionalità e la gestione di un personal computer controller video, un sottotipo di un controller video.</span><span class="sxs-lookup"><span data-stu-id="257dc-104">The **CIM\_PCVideoController** represents the capabilities and management of a personal computer video controller, a subtype of a video controller.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="257dc-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="257dc-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="257dc-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="257dc-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="257dc-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="257dc-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="257dc-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="257dc-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="257dc-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="257dc-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCE6-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_PCVideoController : CIM_VideoController
{
  uint16   AcceleratorCapabilities[];
  uint16   Availability;
  string   CapabilityDescriptions[];
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint32   CurrentBitsPerPixel;
  uint32   CurrentHorizontalResolution;
  uint64   CurrentNumberOfColors;
  uint32   CurrentNumberOfColumns;
  uint32   CurrentNumberOfRows;
  uint32   CurrentRefreshRate;
  uint16   CurrentScanMode;
  uint32   CurrentVerticalResolution;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxMemorySupported;
  uint32   MaxNumberControlled;
  uint32   MaxRefreshRate;
  uint32   MinRefreshRate;
  string   Name;
  uint16   NumberOfColorPlanes;
  uint32   NumberOfVideoPages;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtocolSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
  uint16   VideoArchitecture;
  uint16   VideoMemoryType;
  uint16   VideoMode;
  string   VideoProcessor;
};
```

## <a name="members"></a><span data-ttu-id="257dc-110">Members</span><span class="sxs-lookup"><span data-stu-id="257dc-110">Members</span></span>

<span data-ttu-id="257dc-111">La classe **CIM \_ PCVideoController** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="257dc-111">The **CIM\_PCVideoController** class has these types of members:</span></span>

-   [<span data-ttu-id="257dc-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="257dc-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="257dc-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="257dc-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="257dc-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="257dc-114">Methods</span></span>

<span data-ttu-id="257dc-115">La classe **CIM \_ PCVideoController** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="257dc-115">The **CIM\_PCVideoController** class has these methods.</span></span>



| <span data-ttu-id="257dc-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="257dc-116">Method</span></span>                                                                       | <span data-ttu-id="257dc-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="257dc-117">Description</span></span>                                                                                                                              |
|:-----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="257dc-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="257dc-118">**Reset**</span></span>](reset-method-in-class-cim-pcvideocontroller.md)                 | <span data-ttu-id="257dc-119">Richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="257dc-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="257dc-120">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="257dc-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="257dc-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="257dc-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-pcvideocontroller.md) | <span data-ttu-id="257dc-122">Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="257dc-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="257dc-123">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="257dc-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="257dc-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="257dc-124">Properties</span></span>

<span data-ttu-id="257dc-125">La classe **CIM \_ PCVideoController** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="257dc-125">The **CIM\_PCVideoController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="257dc-126">**AcceleratorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="257dc-126">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-127">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="257dc-127">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="257dc-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="257dc-129">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="257dc-129">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="257dc-130">Grafica e funzionalità 3D del controller video.</span><span class="sxs-lookup"><span data-stu-id="257dc-130">Graphics and 3-D capabilities of the video controller.</span></span>

<span data-ttu-id="257dc-131">Questa proprietà viene ereditata da [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="257dc-131">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="257dc-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="257dc-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="257dc-133"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="257dc-133"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>

<span data-ttu-id="257dc-134"><span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>**Acceleratore grafico** (2)</span><span class="sxs-lookup"><span data-stu-id="257dc-134"><span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>**Graphics Accelerator** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>

<span data-ttu-id="257dc-135"><span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>**acceleratore 3D** (3)</span><span class="sxs-lookup"><span data-stu-id="257dc-135"><span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>**3D Accelerator** (3)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-136">acceleratore 3D</span><span class="sxs-lookup"><span data-stu-id="257dc-136">3-D accelerator</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="257dc-137">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="257dc-137">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-138">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="257dc-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="257dc-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="257dc-140">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="257dc-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="257dc-141">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="257dc-141">Availability and status of the device.</span></span>

<span data-ttu-id="257dc-142">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="257dc-142">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="257dc-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="257dc-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="257dc-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="257dc-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="257dc-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="257dc-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-146">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="257dc-146">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="257dc-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="257dc-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="257dc-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="257dc-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="257dc-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="257dc-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="257dc-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="257dc-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="257dc-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="257dc-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="257dc-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="257dc-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="257dc-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="257dc-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="257dc-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="257dc-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="257dc-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="257dc-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="257dc-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="257dc-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-157">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="257dc-157">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="257dc-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="257dc-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-159">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="257dc-159">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="257dc-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="257dc-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-161">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="257dc-161">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="257dc-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="257dc-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="257dc-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="257dc-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-164">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="257dc-164">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="257dc-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="257dc-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-166">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="257dc-166">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="257dc-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="257dc-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-168">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="257dc-168">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="257dc-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="257dc-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-170">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="257dc-170">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="257dc-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="257dc-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-172">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="257dc-172">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="257dc-173">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="257dc-173">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-174">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="257dc-174">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="257dc-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="257dc-176">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**AcceleratorCapabilities**")</span><span class="sxs-lookup"><span data-stu-id="257dc-176">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**AcceleratorCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="257dc-177">Stringhe in formato libero che forniscono spiegazioni dettagliate per le funzionalità di accelerazione video indicate nella matrice **AcceleratorCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="257dc-177">Free-form strings that provide detailed explanations for video accelerator features indicated in the **AcceleratorCapabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="257dc-178">Ogni voce della matrice è correlata alla voce nella matrice **AcceleratorCapabilities** che si trova nello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="257dc-178">Each array entry is related to the entry in the **AcceleratorCapabilities** array that is located at the same index.</span></span>

 

<span data-ttu-id="257dc-179">Questa proprietà viene ereditata da [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="257dc-179">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="257dc-180">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="257dc-180">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-181">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="257dc-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="257dc-182">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="257dc-183">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="257dc-183">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="257dc-184">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="257dc-184">Short textual description of the object.</span></span>

<span data-ttu-id="257dc-185">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="257dc-185">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="257dc-186">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="257dc-186">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-187">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="257dc-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="257dc-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="257dc-189">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="257dc-189">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="257dc-190">Codice di errore di Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="257dc-190">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="257dc-191">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="257dc-191">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="257dc-192"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="257dc-192"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="257dc-193"> (0)</span><span class="sxs-lookup"><span data-stu-id="257dc-193">(0)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-194">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="257dc-194">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="257dc-195"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="257dc-195"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="257dc-196">(1)</span><span class="sxs-lookup"><span data-stu-id="257dc-196">(1)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-197">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="257dc-197">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="257dc-198"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="257dc-198"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="257dc-199">(2)</span><span class="sxs-lookup"><span data-stu-id="257dc-199">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="257dc-200"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="257dc-200"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="257dc-201">(3)</span><span class="sxs-lookup"><span data-stu-id="257dc-201">(3)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-202">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="257dc-202">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="257dc-203"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="257dc-203"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="257dc-204">(4)</span><span class="sxs-lookup"><span data-stu-id="257dc-204">(4)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-205">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="257dc-205">Device is not working properly.</span></span> <span data-ttu-id="257dc-206">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="257dc-206">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="257dc-207"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="257dc-207"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="257dc-208">(5)</span><span class="sxs-lookup"><span data-stu-id="257dc-208">(5)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-209">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="257dc-209">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="257dc-210"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="257dc-210"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="257dc-211"> (6)</span><span class="sxs-lookup"><span data-stu-id="257dc-211">(6)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-212">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="257dc-212">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="257dc-213"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="257dc-213"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="257dc-214">(7)</span><span class="sxs-lookup"><span data-stu-id="257dc-214">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="257dc-215"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="257dc-215"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="257dc-216">(8)</span><span class="sxs-lookup"><span data-stu-id="257dc-216">(8)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-217">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="257dc-217">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="257dc-218"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="257dc-218"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="257dc-219">(9)</span><span class="sxs-lookup"><span data-stu-id="257dc-219">(9)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-220">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="257dc-220">Device is not working properly.</span></span> <span data-ttu-id="257dc-221">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="257dc-221">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="257dc-222"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="257dc-222"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="257dc-223">(10)</span><span class="sxs-lookup"><span data-stu-id="257dc-223">(10)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-224">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="257dc-224">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="257dc-225"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="257dc-225"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="257dc-226">(11)</span><span class="sxs-lookup"><span data-stu-id="257dc-226">(11)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-227">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="257dc-227">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="257dc-228"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="257dc-228"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="257dc-229">12</span><span class="sxs-lookup"><span data-stu-id="257dc-229">(12)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-230">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="257dc-230">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="257dc-231"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="257dc-231"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="257dc-232">(13)</span><span class="sxs-lookup"><span data-stu-id="257dc-232">(13)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-233">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="257dc-233">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="257dc-234"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="257dc-234"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="257dc-235">(14)</span><span class="sxs-lookup"><span data-stu-id="257dc-235">(14)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-236">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="257dc-236">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="257dc-237"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="257dc-237"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="257dc-238">(15)</span><span class="sxs-lookup"><span data-stu-id="257dc-238">(15)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-239">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="257dc-239">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="257dc-240"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="257dc-240"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="257dc-241">(16)</span><span class="sxs-lookup"><span data-stu-id="257dc-241">(16)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-242">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="257dc-242">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="257dc-243"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="257dc-243"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="257dc-244">(17)</span><span class="sxs-lookup"><span data-stu-id="257dc-244">(17)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-245">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="257dc-245">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="257dc-246"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="257dc-246"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="257dc-247">(18)</span><span class="sxs-lookup"><span data-stu-id="257dc-247">(18)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-248">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="257dc-248">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="257dc-249"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="257dc-249"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="257dc-250">(19)</span><span class="sxs-lookup"><span data-stu-id="257dc-250">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="257dc-251"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="257dc-251"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="257dc-252">(20)</span><span class="sxs-lookup"><span data-stu-id="257dc-252">(20)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-253">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="257dc-253">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="257dc-254"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="257dc-254"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="257dc-255">(21)</span><span class="sxs-lookup"><span data-stu-id="257dc-255">(21)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-256">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="257dc-256">System failure.</span></span> <span data-ttu-id="257dc-257">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="257dc-257">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="257dc-258">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="257dc-258">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="257dc-259"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="257dc-259"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="257dc-260">(22)</span><span class="sxs-lookup"><span data-stu-id="257dc-260">(22)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-261">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="257dc-261">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="257dc-262"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="257dc-262"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="257dc-263">(23)</span><span class="sxs-lookup"><span data-stu-id="257dc-263">(23)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-264">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="257dc-264">System failure.</span></span> <span data-ttu-id="257dc-265">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="257dc-265">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="257dc-266"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="257dc-266"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="257dc-267">(24)</span><span class="sxs-lookup"><span data-stu-id="257dc-267">(24)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-268">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="257dc-268">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="257dc-269"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="257dc-269"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="257dc-270">(25)</span><span class="sxs-lookup"><span data-stu-id="257dc-270">(25)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-271">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="257dc-271">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="257dc-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="257dc-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="257dc-273">(26)</span><span class="sxs-lookup"><span data-stu-id="257dc-273">(26)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-274">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="257dc-274">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="257dc-275"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="257dc-275"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="257dc-276">(27)</span><span class="sxs-lookup"><span data-stu-id="257dc-276">(27)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-277">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="257dc-277">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="257dc-278"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="257dc-278"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="257dc-279">(28)</span><span class="sxs-lookup"><span data-stu-id="257dc-279">(28)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-280">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="257dc-280">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="257dc-281"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="257dc-281"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="257dc-282">(29)</span><span class="sxs-lookup"><span data-stu-id="257dc-282">(29)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-283">Il dispositivo è disabilitato; il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="257dc-283">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="257dc-284"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="257dc-284"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="257dc-285">(30)</span><span class="sxs-lookup"><span data-stu-id="257dc-285">(30)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-286">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="257dc-286">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="257dc-287"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="257dc-287"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="257dc-288">31</span><span class="sxs-lookup"><span data-stu-id="257dc-288">(31)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-289">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="257dc-289">Device is not working properly.</span></span> <span data-ttu-id="257dc-290">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="257dc-290">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="257dc-291">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="257dc-291">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-292">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="257dc-292">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="257dc-293">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="257dc-294">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="257dc-294">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="257dc-295">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="257dc-295">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="257dc-296">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="257dc-296">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="257dc-297">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="257dc-297">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-298">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="257dc-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="257dc-299">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="257dc-300">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="257dc-300">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="257dc-301">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="257dc-301">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="257dc-302">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="257dc-302">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="257dc-303">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="257dc-303">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="257dc-304">**CurrentBitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="257dc-304">**CurrentBitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-305">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="257dc-305">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="257dc-306">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="257dc-307">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video \| 003,12 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="257dc-307">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="257dc-308">Numero di bit utilizzati per visualizzare ogni pixel.</span><span class="sxs-lookup"><span data-stu-id="257dc-308">Number of bits used to display each pixel.</span></span>

<span data-ttu-id="257dc-309">Questa proprietà viene ereditata da [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="257dc-309">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="257dc-310">**CurrentHorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="257dc-310">**CurrentHorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-311">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="257dc-311">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="257dc-312">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="257dc-313">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video \| 003,11 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" pixel ")</span><span class="sxs-lookup"><span data-stu-id="257dc-313">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="257dc-314">Numero corrente di pixel orizzontali.</span><span class="sxs-lookup"><span data-stu-id="257dc-314">Current number of horizontal pixels.</span></span>

<span data-ttu-id="257dc-315">Questa proprietà viene ereditata da [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="257dc-315">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="257dc-316">**CurrentNumberOfColors**</span><span class="sxs-lookup"><span data-stu-id="257dc-316">**CurrentNumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-317">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="257dc-317">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="257dc-318">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="257dc-319">Numero di colori supportati per le risoluzioni correnti.</span><span class="sxs-lookup"><span data-stu-id="257dc-319">Number of colors supported at the current resolutions.</span></span>

<span data-ttu-id="257dc-320">Questa proprietà viene ereditata da [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="257dc-320">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<span data-ttu-id="257dc-321">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="257dc-321">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="257dc-322">**CurrentNumberOfColumns**</span><span class="sxs-lookup"><span data-stu-id="257dc-322">**CurrentNumberOfColumns**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-323">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="257dc-323">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="257dc-324">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="257dc-325">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Video di DMTF \| \| 003,14 ")</span><span class="sxs-lookup"><span data-stu-id="257dc-325">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.14")</span></span>
</dt> </dl>

<span data-ttu-id="257dc-326">Se è in modalità carattere, numero di colonne per il controller video; in caso contrario, immettere 0.</span><span class="sxs-lookup"><span data-stu-id="257dc-326">If in character mode, number of columns for the video controller; otherwise, enter 0.</span></span>

<span data-ttu-id="257dc-327">Questa proprietà viene ereditata da [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="257dc-327">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="257dc-328">**CurrentNumberOfRows**</span><span class="sxs-lookup"><span data-stu-id="257dc-328">**CurrentNumberOfRows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-329">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="257dc-329">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="257dc-330">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="257dc-331">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Video di DMTF \| \| 003,13 ")</span><span class="sxs-lookup"><span data-stu-id="257dc-331">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.13")</span></span>
</dt> </dl>

<span data-ttu-id="257dc-332">Se è in modalità carattere, numero di righe per il controller video; in caso contrario, immettere 0.</span><span class="sxs-lookup"><span data-stu-id="257dc-332">If in character mode, number of rows for this video controller; otherwise, enter 0.</span></span>

<span data-ttu-id="257dc-333">Questa proprietà viene ereditata da [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="257dc-333">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="257dc-334">**CurrentRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="257dc-334">**CurrentRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-335">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="257dc-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="257dc-336">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="257dc-337">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video \| 003,15 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="257dc-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="257dc-338">Frequenza di aggiornamento corrente in Hertz.</span><span class="sxs-lookup"><span data-stu-id="257dc-338">Current refresh rate in hertz.</span></span>

<span data-ttu-id="257dc-339">Questa proprietà viene ereditata da [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="257dc-339">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="257dc-340">**CurrentScanMode**</span><span class="sxs-lookup"><span data-stu-id="257dc-340">**CurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-341">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="257dc-341">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="257dc-342">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="257dc-343">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Video di DMTF \| \| 003,8 ")</span><span class="sxs-lookup"><span data-stu-id="257dc-343">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.8")</span></span>
</dt> </dl>

<span data-ttu-id="257dc-344">Modalità di analisi corrente.</span><span class="sxs-lookup"><span data-stu-id="257dc-344">Current scan mode.</span></span> <span data-ttu-id="257dc-345">Questa proprietà viene ereditata da [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="257dc-345">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="257dc-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="257dc-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="257dc-347"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="257dc-347"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>

<span data-ttu-id="257dc-348"><span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>**Interlacciato** (3)</span><span class="sxs-lookup"><span data-stu-id="257dc-348"><span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>**Interlaced** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>

<span data-ttu-id="257dc-349"><span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>**Non interlacciato** (4)</span><span class="sxs-lookup"><span data-stu-id="257dc-349"><span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>**Non Interlaced** (4)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-350">Non interlacciato</span><span class="sxs-lookup"><span data-stu-id="257dc-350">Non-interlaced</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="257dc-351">**CurrentVerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="257dc-351">**CurrentVerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-352">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="257dc-352">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="257dc-353">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="257dc-354">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video \| 003,10 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" pixel ")</span><span class="sxs-lookup"><span data-stu-id="257dc-354">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="257dc-355">Numero corrente di pixel verticali.</span><span class="sxs-lookup"><span data-stu-id="257dc-355">Current number of vertical pixels.</span></span>

<span data-ttu-id="257dc-356">Questa proprietà viene ereditata da [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="257dc-356">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="257dc-357">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="257dc-357">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-358">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="257dc-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="257dc-359">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="257dc-360">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="257dc-360">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="257dc-361">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="257dc-361">Textual description of the object.</span></span>

<span data-ttu-id="257dc-362">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="257dc-362">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="257dc-363">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="257dc-363">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-364">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="257dc-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="257dc-365">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="257dc-366">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="257dc-366">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="257dc-367">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="257dc-367">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="257dc-368">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="257dc-368">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="257dc-369">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="257dc-369">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-370">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="257dc-370">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="257dc-371">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="257dc-372">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="257dc-372">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="257dc-373">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="257dc-373">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="257dc-374">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="257dc-374">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-375">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="257dc-375">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="257dc-376">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="257dc-377">Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.</span><span class="sxs-lookup"><span data-stu-id="257dc-377">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="257dc-378">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="257dc-378">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="257dc-379">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="257dc-379">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-380">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="257dc-380">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="257dc-381">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="257dc-382">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="257dc-382">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="257dc-383">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="257dc-383">Date and time the object was installed.</span></span> <span data-ttu-id="257dc-384">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="257dc-384">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="257dc-385">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="257dc-385">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="257dc-386">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="257dc-386">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-387">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="257dc-387">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="257dc-388">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="257dc-389">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="257dc-389">Last error code reported by the logical device.</span></span>

<span data-ttu-id="257dc-390">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="257dc-390">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="257dc-391">**MaxMemorySupported**</span><span class="sxs-lookup"><span data-stu-id="257dc-391">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-392">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="257dc-392">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="257dc-393">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="257dc-394">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="257dc-394">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="257dc-395">Quantità massima di memoria supportata, in byte.</span><span class="sxs-lookup"><span data-stu-id="257dc-395">Maximum amount of memory supported, in bytes.</span></span>

<span data-ttu-id="257dc-396">Questa proprietà viene ereditata da [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="257dc-396">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="257dc-397">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="257dc-397">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-398">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="257dc-398">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="257dc-399">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="257dc-400">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta bus DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="257dc-400">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="257dc-401">Numero massimo di entità indirizzabili direttamente supportate dal controller.</span><span class="sxs-lookup"><span data-stu-id="257dc-401">Maximum number of directly addressable entities supported by the controller.</span></span> <span data-ttu-id="257dc-402">Se il numero è sconosciuto o illimitato, è necessario utilizzare il valore 0.</span><span class="sxs-lookup"><span data-stu-id="257dc-402">A value of 0 should be used if the number is unknown or unlimited.</span></span>

<span data-ttu-id="257dc-403">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="257dc-403">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="257dc-404">**MaxRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="257dc-404">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-405">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="257dc-405">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="257dc-406">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-406">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="257dc-407">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video \| 003,5 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="257dc-407">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="257dc-408">Frequenza di aggiornamento massima del controller video in Hertz.</span><span class="sxs-lookup"><span data-stu-id="257dc-408">Maximum refresh rate of the video controller in hertz.</span></span>

<span data-ttu-id="257dc-409">Questa proprietà viene ereditata da [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="257dc-409">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="257dc-410">**MinRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="257dc-410">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-411">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="257dc-411">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="257dc-412">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-412">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="257dc-413">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video \| 003,4 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="257dc-413">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="257dc-414">Frequenza di aggiornamento minima del controller video in Hertz.</span><span class="sxs-lookup"><span data-stu-id="257dc-414">Minimum refresh rate of the video controller in hertz.</span></span>

<span data-ttu-id="257dc-415">Questa proprietà viene ereditata da [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="257dc-415">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="257dc-416">**Nome**</span><span class="sxs-lookup"><span data-stu-id="257dc-416">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-417">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="257dc-417">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="257dc-418">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="257dc-419">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="257dc-419">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="257dc-420">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="257dc-420">Label by which the object is known.</span></span> <span data-ttu-id="257dc-421">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="257dc-421">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="257dc-422">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="257dc-422">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="257dc-423">**NumberOfColorPlanes**</span><span class="sxs-lookup"><span data-stu-id="257dc-423">**NumberOfColorPlanes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-424">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="257dc-424">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="257dc-425">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="257dc-426">Numero corrente di piani di colore.</span><span class="sxs-lookup"><span data-stu-id="257dc-426">Current number of color planes.</span></span> <span data-ttu-id="257dc-427">Se questo valore non è applicabile per la configurazione video corrente, immettere 0.</span><span class="sxs-lookup"><span data-stu-id="257dc-427">If this value is not applicable for the current video configuration, enter 0.</span></span>

</dd> <dt>

<span data-ttu-id="257dc-428">**NumberOfVideoPages**</span><span class="sxs-lookup"><span data-stu-id="257dc-428">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-429">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="257dc-429">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="257dc-430">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="257dc-431">Numero di pagine video supportate in base alle risoluzioni correnti e alla memoria disponibile.</span><span class="sxs-lookup"><span data-stu-id="257dc-431">Number of video pages supported given the current resolutions and available memory.</span></span>

<span data-ttu-id="257dc-432">Questa proprietà viene ereditata da [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="257dc-432">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="257dc-433">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="257dc-433">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-434">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="257dc-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="257dc-435">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="257dc-436">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="257dc-436">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="257dc-437">Win32 Plug and Play identificatore dispositivo del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="257dc-437">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="257dc-438">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="257dc-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="257dc-439">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="257dc-439">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="257dc-440">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="257dc-440">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-441">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="257dc-441">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="257dc-442">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="257dc-443">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="257dc-443">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="257dc-444">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="257dc-444">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="257dc-445"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="257dc-445"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="257dc-446"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="257dc-446"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="257dc-447"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="257dc-447"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="257dc-448"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="257dc-448"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-449">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="257dc-449">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="257dc-450"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="257dc-450"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-451">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="257dc-451">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="257dc-452"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="257dc-452"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-453">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="257dc-453">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="257dc-454">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="257dc-454">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="257dc-455">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="257dc-455">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="257dc-456"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="257dc-456"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-457">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="257dc-457">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="257dc-458"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="257dc-458"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="257dc-459">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="257dc-459">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="257dc-460">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="257dc-460">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-461">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="257dc-461">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="257dc-462">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-462">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="257dc-463">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="257dc-463">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="257dc-464">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="257dc-464">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="257dc-465">Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="257dc-465">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="257dc-466">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="257dc-466">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="257dc-467">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="257dc-467">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="257dc-468">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="257dc-468">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-469">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="257dc-469">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="257dc-470">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-470">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="257dc-471">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta bus DMTF \| 001,2 "," MIF. \|Dischi DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="257dc-471">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="257dc-472">Protocollo usato dal controller per accedere ai dispositivi "controllati".</span><span class="sxs-lookup"><span data-stu-id="257dc-472">Protocol used by the controller to access 'controlled' devices.</span></span>

<span data-ttu-id="257dc-473">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="257dc-473">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="257dc-474">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="257dc-474">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="257dc-475">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="257dc-475">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="257dc-476">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="257dc-476">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="257dc-477">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="257dc-477">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="257dc-478">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="257dc-478">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="257dc-479">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="257dc-479">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="257dc-480">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="257dc-480">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="257dc-481">**Dischetto flessibile** (7)</span><span class="sxs-lookup"><span data-stu-id="257dc-481">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="257dc-482">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="257dc-482">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="257dc-483">**Interfaccia parallela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="257dc-483">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="257dc-484">**Protocollo di Fibre Channel SCSI** (10)</span><span class="sxs-lookup"><span data-stu-id="257dc-484">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="257dc-485">**Protocollo bus seriale SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="257dc-485">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="257dc-486">**Protocollo bus seriale SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="257dc-486">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="257dc-487">**Architettura di archiviazione seriale SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="257dc-487">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="257dc-488">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="257dc-488">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="257dc-489">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="257dc-489">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="257dc-490">**Bus seriale universale** (16)</span><span class="sxs-lookup"><span data-stu-id="257dc-490">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="257dc-491">**Protocollo parallelo** (17)</span><span class="sxs-lookup"><span data-stu-id="257dc-491">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="257dc-492">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="257dc-492">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="257dc-493">**Diagnostica** (19)</span><span class="sxs-lookup"><span data-stu-id="257dc-493">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="257dc-494">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="257dc-494">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="257dc-495">**Potenza** (21)</span><span class="sxs-lookup"><span data-stu-id="257dc-495">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="257dc-496">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="257dc-496">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="257dc-497">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="257dc-497">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="257dc-498">**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="257dc-498">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="257dc-499">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="257dc-499">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="257dc-500">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="257dc-500">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="257dc-501">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="257dc-501">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="257dc-502">**IEEE 802,3 10Base5** (28)</span><span class="sxs-lookup"><span data-stu-id="257dc-502">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="257dc-503">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="257dc-503">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="257dc-504">**IEEE 802,3 1Base5** (30)</span><span class="sxs-lookup"><span data-stu-id="257dc-504">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="257dc-505">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="257dc-505">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="257dc-506">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="257dc-506">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="257dc-507">**Token-ring IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="257dc-507">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="257dc-508">**ANSI X3T 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="257dc-508">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="257dc-509">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="257dc-509">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="257dc-510">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="257dc-510">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="257dc-511">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="257dc-511">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="257dc-512">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="257dc-512">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="257dc-513">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="257dc-513">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="257dc-514">**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="257dc-514">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="257dc-515">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="257dc-515">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="257dc-516">**ATA/IDE avanzato** (42)</span><span class="sxs-lookup"><span data-stu-id="257dc-516">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="257dc-517">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="257dc-517">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="257dc-518">**TWIRP (infrarossi bidirezionali)** (44)</span><span class="sxs-lookup"><span data-stu-id="257dc-518">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="257dc-519">**FIR (infrarossi veloci)** (45)</span><span class="sxs-lookup"><span data-stu-id="257dc-519">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="257dc-520">**Sir (Serial Infrared)** (46)</span><span class="sxs-lookup"><span data-stu-id="257dc-520">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="257dc-521">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="257dc-521">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="257dc-522">**Status**</span><span class="sxs-lookup"><span data-stu-id="257dc-522">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-523">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="257dc-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="257dc-524">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="257dc-525">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="257dc-525">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="257dc-526">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="257dc-526">Current status of the object.</span></span> <span data-ttu-id="257dc-527">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="257dc-527">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="257dc-528">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="257dc-528">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="257dc-529">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="257dc-529">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="257dc-530">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="257dc-530">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="257dc-531">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="257dc-531">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="257dc-532">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="257dc-532">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="257dc-533">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="257dc-533">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="257dc-534">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="257dc-534">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="257dc-535">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="257dc-535">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="257dc-536">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="257dc-536">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="257dc-537">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="257dc-537">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="257dc-538">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="257dc-538">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="257dc-539">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="257dc-539">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="257dc-540">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="257dc-540">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="257dc-541">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="257dc-541">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-542">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="257dc-542">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="257dc-543">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-543">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="257dc-544">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="257dc-544">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="257dc-545">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="257dc-545">State of the logical device.</span></span> <span data-ttu-id="257dc-546">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="257dc-546">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="257dc-547">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="257dc-547">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="257dc-548">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="257dc-548">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="257dc-549">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="257dc-549">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="257dc-550">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="257dc-550">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="257dc-551">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="257dc-551">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="257dc-552">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="257dc-552">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="257dc-553">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="257dc-553">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-554">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="257dc-554">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="257dc-555">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-555">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="257dc-556">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="257dc-556">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="257dc-557">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="257dc-557">Scoping system's creation class name.</span></span>

<span data-ttu-id="257dc-558">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="257dc-558">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="257dc-559">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="257dc-559">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-560">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="257dc-560">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="257dc-561">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-561">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="257dc-562">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="257dc-562">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="257dc-563">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="257dc-563">Scoping system's name.</span></span>

<span data-ttu-id="257dc-564">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="257dc-564">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="257dc-565">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="257dc-565">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-566">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="257dc-566">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="257dc-567">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-567">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="257dc-568">Data e ora dell'ultima reimpostazione del controller che indica che il controller è stato spento o reinizializzato.</span><span class="sxs-lookup"><span data-stu-id="257dc-568">Date and time this controller was last reset meaning the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="257dc-569">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="257dc-569">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="257dc-570">**VideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="257dc-570">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-571">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="257dc-571">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="257dc-572">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="257dc-573">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Video di DMTF \| \| 003,2 ")</span><span class="sxs-lookup"><span data-stu-id="257dc-573">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.2")</span></span>
</dt> </dl>

<span data-ttu-id="257dc-574">Architettura video.</span><span class="sxs-lookup"><span data-stu-id="257dc-574">Video architecture.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="257dc-575">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="257dc-575">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="257dc-576">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="257dc-576">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="CGA"></span><span id="cga"></span>

<span data-ttu-id="257dc-577">**CGA** (3)</span><span class="sxs-lookup"><span data-stu-id="257dc-577">**CGA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="EGA"></span><span id="ega"></span>

<span data-ttu-id="257dc-578">**EGA** (4)</span><span class="sxs-lookup"><span data-stu-id="257dc-578">**EGA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VGA"></span><span id="vga"></span>

<span data-ttu-id="257dc-579">**VGA** (5)</span><span class="sxs-lookup"><span data-stu-id="257dc-579">**VGA** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SVGA"></span><span id="svga"></span>

<span data-ttu-id="257dc-580">**SVGA** (6)</span><span class="sxs-lookup"><span data-stu-id="257dc-580">**SVGA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="MDA"></span><span id="mda"></span>

<span data-ttu-id="257dc-581">**MDA** (7)</span><span class="sxs-lookup"><span data-stu-id="257dc-581">**MDA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="HGC"></span><span id="hgc"></span>

<span data-ttu-id="257dc-582">**HGC** (8)</span><span class="sxs-lookup"><span data-stu-id="257dc-582">**HGC** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="MCGA"></span><span id="mcga"></span>

<span data-ttu-id="257dc-583">**MCGA** (9)</span><span class="sxs-lookup"><span data-stu-id="257dc-583">**MCGA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="8514A"></span><span id="8514a"></span>

<span data-ttu-id="257dc-584">**8514a** (10)</span><span class="sxs-lookup"><span data-stu-id="257dc-584">**8514A** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="XGA"></span><span id="xga"></span>

<span data-ttu-id="257dc-585">**XGA** (11)</span><span class="sxs-lookup"><span data-stu-id="257dc-585">**XGA** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>

<span data-ttu-id="257dc-586">**Buffer frame lineare** (12)</span><span class="sxs-lookup"><span data-stu-id="257dc-586">**Linear Frame Buffer** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="257dc-587">**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="257dc-587">**PC-98** (160)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="257dc-588">**VideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="257dc-588">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-589">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="257dc-589">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="257dc-590">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-590">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="257dc-591">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Video di DMTF \| \| 003,6 ")</span><span class="sxs-lookup"><span data-stu-id="257dc-591">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.6")</span></span>
</dt> </dl>

<span data-ttu-id="257dc-592">Tipo di memoria video.</span><span class="sxs-lookup"><span data-stu-id="257dc-592">Type of video memory.</span></span>

<span data-ttu-id="257dc-593">Questa proprietà viene ereditata da [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="257dc-593">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="257dc-594">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="257dc-594">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="257dc-595">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="257dc-595">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="257dc-596">**VRAM** (3)</span><span class="sxs-lookup"><span data-stu-id="257dc-596">**VRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="257dc-597">**DRAM** (4)</span><span class="sxs-lookup"><span data-stu-id="257dc-597">**DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="257dc-598">**SRAM** (5)</span><span class="sxs-lookup"><span data-stu-id="257dc-598">**SRAM** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WRAM"></span><span id="wram"></span>

<span data-ttu-id="257dc-599">**WRAM** (6)</span><span class="sxs-lookup"><span data-stu-id="257dc-599">**WRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO_RAM"></span><span id="edo_ram"></span>

<span data-ttu-id="257dc-600">**RAM EDO** (7)</span><span class="sxs-lookup"><span data-stu-id="257dc-600">**EDO RAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst_Synchronous_DRAM"></span><span id="burst_synchronous_dram"></span><span id="BURST_SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="257dc-601">**DRAM sincrona a impulsi** (8)</span><span class="sxs-lookup"><span data-stu-id="257dc-601">**Burst Synchronous DRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipelined_Burst_SRAM"></span><span id="pipelined_burst_sram"></span><span id="PIPELINED_BURST_SRAM"></span>

<span data-ttu-id="257dc-602">**SRAM di impulso in pipeline** (9)</span><span class="sxs-lookup"><span data-stu-id="257dc-602">**Pipelined Burst SRAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="257dc-603">**CDRAM** (10)</span><span class="sxs-lookup"><span data-stu-id="257dc-603">**CDRAM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="257dc-604">**3DRAM** (11)</span><span class="sxs-lookup"><span data-stu-id="257dc-604">**3DRAM** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="257dc-605">**SDRAM** (12)</span><span class="sxs-lookup"><span data-stu-id="257dc-605">**SDRAM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="257dc-606">**SGRAM** (13)</span><span class="sxs-lookup"><span data-stu-id="257dc-606">**SGRAM** (13)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="257dc-607">**VideoMode**</span><span class="sxs-lookup"><span data-stu-id="257dc-607">**VideoMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-608">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="257dc-608">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="257dc-609">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-609">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="257dc-610">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Video di DMTF \| \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="257dc-610">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="257dc-611">Modalità video corrente.</span><span class="sxs-lookup"><span data-stu-id="257dc-611">Current video mode.</span></span>

</dd> <dt>

<span data-ttu-id="257dc-612">**VideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="257dc-612">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="257dc-613">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="257dc-613">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="257dc-614">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="257dc-614">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="257dc-615">Stringa in formato libero che descrive il processore/controller video.</span><span class="sxs-lookup"><span data-stu-id="257dc-615">Free-form string that describes the video processor/controller.</span></span>

<span data-ttu-id="257dc-616">Questa proprietà viene ereditata da [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="257dc-616">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="257dc-617">Commenti</span><span class="sxs-lookup"><span data-stu-id="257dc-617">Remarks</span></span>

<span data-ttu-id="257dc-618">La classe **CIM \_ PCVideoController** è derivata da [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="257dc-618">The **CIM\_PCVideoController** class is derived from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<span data-ttu-id="257dc-619">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="257dc-619">WMI does not implement this class.</span></span> <span data-ttu-id="257dc-620">Per le classi WMI derivate da [**CIM \_ PCVideoController**](cim-videocontroller.md), vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="257dc-620">For WMI classes derived from [**CIM\_PCVideoController**](cim-videocontroller.md), see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="257dc-621">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="257dc-621">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="257dc-622">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="257dc-622">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="257dc-623">Requisiti</span><span class="sxs-lookup"><span data-stu-id="257dc-623">Requirements</span></span>



| <span data-ttu-id="257dc-624">Requisito</span><span class="sxs-lookup"><span data-stu-id="257dc-624">Requirement</span></span> | <span data-ttu-id="257dc-625">Valore</span><span class="sxs-lookup"><span data-stu-id="257dc-625">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="257dc-626">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="257dc-626">Minimum supported client</span></span><br/> | <span data-ttu-id="257dc-627">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="257dc-627">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="257dc-628">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="257dc-628">Minimum supported server</span></span><br/> | <span data-ttu-id="257dc-629">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="257dc-629">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="257dc-630">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="257dc-630">Namespace</span></span><br/>                | <span data-ttu-id="257dc-631">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="257dc-631">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="257dc-632">MOF</span><span class="sxs-lookup"><span data-stu-id="257dc-632">MOF</span></span><br/>                      | <dl> <span data-ttu-id="257dc-633"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="257dc-633"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="257dc-634">DLL</span><span class="sxs-lookup"><span data-stu-id="257dc-634">DLL</span></span><br/>                      | <dl> <span data-ttu-id="257dc-635"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="257dc-635"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="257dc-636">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="257dc-636">See also</span></span>

<dl> <dt>

[<span data-ttu-id="257dc-637">**\_VIDEOCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="257dc-637">**CIM\_VideoController**</span></span>](cim-videocontroller.md)
</dt> </dl>

 


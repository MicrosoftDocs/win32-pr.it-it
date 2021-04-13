---
description: Rappresenta le funzionalità e la capacità di gestione del controller video in un sistema di computer che esegue Windows.
ms.assetid: 5c81994b-4a84-46ff-8689-09998dc66f91
ms.tgt_platform: multiple
title: Classe Win32_VideoController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VideoController
- Win32_VideoController.Reset
- Win32_VideoController.SetPowerState
- Win32_VideoController.AcceleratorCapabilities
- Win32_VideoController.AdapterCompatibility
- Win32_VideoController.AdapterDACType
- Win32_VideoController.AdapterRAM
- Win32_VideoController.Availability
- Win32_VideoController.CapabilityDescriptions
- Win32_VideoController.Caption
- Win32_VideoController.ColorTableEntries
- Win32_VideoController.ConfigManagerErrorCode
- Win32_VideoController.ConfigManagerUserConfig
- Win32_VideoController.CreationClassName
- Win32_VideoController.CurrentBitsPerPixel
- Win32_VideoController.CurrentHorizontalResolution
- Win32_VideoController.CurrentNumberOfColors
- Win32_VideoController.CurrentNumberOfColumns
- Win32_VideoController.CurrentNumberOfRows
- Win32_VideoController.CurrentRefreshRate
- Win32_VideoController.CurrentScanMode
- Win32_VideoController.CurrentVerticalResolution
- Win32_VideoController.Description
- Win32_VideoController.DeviceID
- Win32_VideoController.DeviceSpecificPens
- Win32_VideoController.DitherType
- Win32_VideoController.DriverDate
- Win32_VideoController.DriverVersion
- Win32_VideoController.ErrorCleared
- Win32_VideoController.ErrorDescription
- Win32_VideoController.ICMIntent
- Win32_VideoController.ICMMethod
- Win32_VideoController.InfFilename
- Win32_VideoController.InfSection
- Win32_VideoController.InstallDate
- Win32_VideoController.InstalledDisplayDrivers
- Win32_VideoController.LastErrorCode
- Win32_VideoController.MaxMemorySupported
- Win32_VideoController.MaxNumberControlled
- Win32_VideoController.MaxRefreshRate
- Win32_VideoController.MinRefreshRate
- Win32_VideoController.Monochrome
- Win32_VideoController.Name
- Win32_VideoController.NumberOfColorPlanes
- Win32_VideoController.NumberOfVideoPages
- Win32_VideoController.PNPDeviceID
- Win32_VideoController.PowerManagementCapabilities
- Win32_VideoController.PowerManagementSupported
- Win32_VideoController.ProtocolSupported
- Win32_VideoController.ReservedSystemPaletteEntries
- Win32_VideoController.SpecificationVersion
- Win32_VideoController.Status
- Win32_VideoController.StatusInfo
- Win32_VideoController.SystemCreationClassName
- Win32_VideoController.SystemName
- Win32_VideoController.SystemPaletteEntries
- Win32_VideoController.TimeOfLastReset
- Win32_VideoController.VideoArchitecture
- Win32_VideoController.VideoMemoryType
- Win32_VideoController.VideoMode
- Win32_VideoController.VideoModeDescription
- Win32_VideoController.VideoProcessor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: deb6903ba6cf27170539281da90569a14471999c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482772"
---
# <a name="win32_videocontroller-class"></a><span data-ttu-id="f1530-103">Win32 \_ VideoController (classe)</span><span class="sxs-lookup"><span data-stu-id="f1530-103">Win32\_VideoController class</span></span>

<span data-ttu-id="f1530-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ VideoController Win32** rappresenta le funzionalità e la capacità di gestione del controller video in un computer che esegue Windows.</span><span class="sxs-lookup"><span data-stu-id="f1530-104">The **Win32\_VideoController** [WMI class](../wmisdk/retrieving-a-class.md) represents the capabilities and management capacity of the video controller on a computer system running Windows.</span></span>

<span data-ttu-id="f1530-105">L'hardware non compatibile con Windows Display Driver Model (WDDM) restituisce valori di proprietà non accurati per le istanze di questa classe.</span><span class="sxs-lookup"><span data-stu-id="f1530-105">Hardware that is not compatible with Windows Display Driver Model (WDDM) returns inaccurate property values for instances of this class.</span></span>

<span data-ttu-id="f1530-106">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f1530-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="f1530-107">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="f1530-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1530-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f1530-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{1008CCF1-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class Win32_VideoController : CIM_PCVideoController
{
  uint16   AcceleratorCapabilities[];
  string   AdapterCompatibility;
  string   AdapterDACType;
  uint32   AdapterRAM;
  uint16   Availability;
  string   CapabilityDescriptions[];
  string   Caption;
  uint32   ColorTableEntries;
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
  uint32   DeviceSpecificPens;
  uint32   DitherType;
  datetime DriverDate;
  string   DriverVersion;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   ICMIntent;
  uint32   ICMMethod;
  string   InfFilename;
  string   InfSection;
  datetime InstallDate;
  string   InstalledDisplayDrivers;
  uint32   LastErrorCode;
  uint32   MaxMemorySupported;
  uint32   MaxNumberControlled;
  uint32   MaxRefreshRate;
  uint32   MinRefreshRate;
  boolean  Monochrome;
  string   Name;
  uint16   NumberOfColorPlanes;
  uint32   NumberOfVideoPages;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtocolSupported;
  uint32   ReservedSystemPaletteEntries;
  uint32   SpecificationVersion;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   SystemPaletteEntries;
  datetime TimeOfLastReset;
  uint16   VideoArchitecture;
  uint16   VideoMemoryType;
  uint16   VideoMode;
  string   VideoModeDescription;
  string   VideoProcessor;
};
```

## <a name="members"></a><span data-ttu-id="f1530-109">Members</span><span class="sxs-lookup"><span data-stu-id="f1530-109">Members</span></span>

<span data-ttu-id="f1530-110">La classe **Win32 \_ VideoController** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f1530-110">The **Win32\_VideoController** class has these types of members:</span></span>

-   [<span data-ttu-id="f1530-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="f1530-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="f1530-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f1530-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f1530-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="f1530-113">Methods</span></span>

<span data-ttu-id="f1530-114">La classe **Win32 \_ VideoController** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="f1530-114">The **Win32\_VideoController** class has these methods.</span></span>



| <span data-ttu-id="f1530-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="f1530-115">Method</span></span>            | <span data-ttu-id="f1530-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1530-116">Description</span></span>                                                                                                                                                                                            |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1530-117">**Reimpostazione**</span><span class="sxs-lookup"><span data-stu-id="f1530-117">**Reset**</span></span>         | <span data-ttu-id="f1530-118">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="f1530-118">Not implemented.</span></span> <span data-ttu-id="f1530-119">Per implementare questo metodo, vedere il metodo [**Reset**](reset-method-in-class-cim-controller.md) in [**CIM \_ PCVideoController**](cim-pcvideocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-119">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span><br/>                 |
| <span data-ttu-id="f1530-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="f1530-120">**SetPowerState**</span></span> | <span data-ttu-id="f1530-121">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="f1530-121">Not implemented.</span></span> <span data-ttu-id="f1530-122">Per implementare questo metodo, vedere il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) in [**CIM \_ PCVideoController**](cim-pcvideocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-122">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f1530-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f1530-123">Properties</span></span>

<span data-ttu-id="f1530-124">La classe **Win32 \_ VideoController** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f1530-124">The **Win32\_VideoController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f1530-125">**AcceleratorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="f1530-125">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-126">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1530-126">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f1530-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-128">Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="f1530-128">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_VideoController**](cim-videocontroller.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-129">Matrice di elementi grafici e funzionalità 3D del controller video.</span><span class="sxs-lookup"><span data-stu-id="f1530-129">Array of graphics and 3-D capabilities of the video controller.</span></span>

<span data-ttu-id="f1530-130">Questa proprietà viene ereditata da [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-130">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f1530-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="f1530-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f1530-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="f1530-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>

<span data-ttu-id="f1530-133"><span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>**Acceleratore grafico** (2)</span><span class="sxs-lookup"><span data-stu-id="f1530-133"><span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>**Graphics Accelerator** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>

<span data-ttu-id="f1530-134"><span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>**acceleratore 3D** (3)</span><span class="sxs-lookup"><span data-stu-id="f1530-134"><span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>**3D Accelerator** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-135">Acceleratore 3D</span><span class="sxs-lookup"><span data-stu-id="f1530-135">3-D Accelerator</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f1530-136">**AdapterCompatibility**</span><span class="sxs-lookup"><span data-stu-id="f1530-136">**AdapterCompatibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f1530-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-139">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="f1530-139">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-140">Chipset generale utilizzato per il controller per confrontare le compatibilità con il sistema.</span><span class="sxs-lookup"><span data-stu-id="f1530-140">General chipset used for this controller to compare compatibilities with the system.</span></span>

</dd> <dt>

<span data-ttu-id="f1530-141">**AdapterDACType**</span><span class="sxs-lookup"><span data-stu-id="f1530-141">**AdapterDACType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f1530-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-144">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HardwareInformation. DACType")</span><span class="sxs-lookup"><span data-stu-id="f1530-144">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HardwareInformation.DACType")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-145">Nome o identificatore del chip del convertitore da digitale a analogico (DAC).</span><span class="sxs-lookup"><span data-stu-id="f1530-145">Name or identifier of the digital-to-analog converter (DAC) chip.</span></span> <span data-ttu-id="f1530-146">Il set di caratteri di questa proprietà è alfanumerico.</span><span class="sxs-lookup"><span data-stu-id="f1530-146">The character set of this property is alphanumeric.</span></span>

</dd> <dt>

<span data-ttu-id="f1530-147">**AdapterRAM**</span><span class="sxs-lookup"><span data-stu-id="f1530-147">**AdapterRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-148">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1530-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-150">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HardwareInformation. MemorySize"), [**unità**](../wmisdk/standard-qualifiers.md) ("byte")</span><span class="sxs-lookup"><span data-stu-id="f1530-150">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HardwareInformation.MemorySize"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-151">Dimensioni della memoria della scheda video.</span><span class="sxs-lookup"><span data-stu-id="f1530-151">Memory size of the video adapter.</span></span>

<span data-ttu-id="f1530-152">Esempio: 64000</span><span class="sxs-lookup"><span data-stu-id="f1530-152">Example: 64000</span></span>

</dd> <dt>

<span data-ttu-id="f1530-153">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="f1530-153">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-154">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1530-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-156">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="f1530-156">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-157">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f1530-157">Availability and status of the device.</span></span>

<span data-ttu-id="f1530-158">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-158">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f1530-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="f1530-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f1530-160"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="f1530-160"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="f1530-161"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="f1530-161"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-162">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="f1530-162">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="f1530-163"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="f1530-163"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="f1530-164"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="f1530-164"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f1530-165"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="f1530-165"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="f1530-166"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="f1530-166"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="f1530-167"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="f1530-167"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-168">Offline</span><span class="sxs-lookup"><span data-stu-id="f1530-168">Offline</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="f1530-169"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="f1530-169"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f1530-170"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="f1530-170"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="f1530-171"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="f1530-171"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="f1530-172"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="f1530-172"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="f1530-173"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="f1530-173"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-174">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="f1530-174">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="f1530-175"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="f1530-175"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-176">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="f1530-176">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="f1530-177"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="f1530-177"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-178">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="f1530-178">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="f1530-179"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="f1530-179"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="f1530-180"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="f1530-180"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-181">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="f1530-181">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="f1530-182"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="f1530-182"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-183">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="f1530-183">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="f1530-184"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="f1530-184"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-185">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="f1530-185">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="f1530-186"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="f1530-186"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-187">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="f1530-187">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="f1530-188"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="f1530-188"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-189">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="f1530-189">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f1530-190">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="f1530-190">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-191">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="f1530-191">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f1530-192">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-193">Qualificatori: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ VideoController**](cim-videocontroller.md).**AcceleratorCapabilities**")</span><span class="sxs-lookup"><span data-stu-id="f1530-193">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_VideoController**](cim-videocontroller.md).**AcceleratorCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-194">Stringhe in formato libero che forniscono spiegazioni più dettagliate per tutte le funzionalità di accelerazione video indicate nella matrice **AcceleratorCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="f1530-194">Free-form strings providing more detailed explanations for any of the video accelerator features indicated in the **AcceleratorCapabilities** array.</span></span> <span data-ttu-id="f1530-195">Si noti che ogni voce di questa matrice è correlata alla voce nella matrice **AcceleratorCapabilities** che si trova nello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="f1530-195">Note, each entry of this array is related to the entry in the **AcceleratorCapabilities** array that is located at the same index.</span></span>

<span data-ttu-id="f1530-196">Questa proprietà viene ereditata da [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-196">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1530-197">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="f1530-197">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-198">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f1530-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-199">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-200">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="f1530-200">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-201">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f1530-201">Short description of the object.</span></span>

<span data-ttu-id="f1530-202">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-202">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1530-203">**ColorTableEntries**</span><span class="sxs-lookup"><span data-stu-id="f1530-203">**ColorTableEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-204">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1530-204">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-205">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-206">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span><span class="sxs-lookup"><span data-stu-id="f1530-206">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-207">Dimensione della tabella dei colori del sistema.</span><span class="sxs-lookup"><span data-stu-id="f1530-207">Size of the system's color table.</span></span> <span data-ttu-id="f1530-208">Il dispositivo deve avere una profondità di colore di non più di 8 bit per pixel; in caso contrario, questa proprietà non è impostata.</span><span class="sxs-lookup"><span data-stu-id="f1530-208">The device must have a color depth of no more than 8 bits per pixel; otherwise, this property is not set.</span></span>

<span data-ttu-id="f1530-209">Esempio: 256</span><span class="sxs-lookup"><span data-stu-id="f1530-209">Example: 256</span></span>

</dd> <dt>

<span data-ttu-id="f1530-210">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="f1530-210">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-211">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1530-211">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-212">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-213">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f1530-213">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-214">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="f1530-214">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="f1530-215">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-215">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="f1530-216"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="f1530-216"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="f1530-217"> (0)</span><span class="sxs-lookup"><span data-stu-id="f1530-217">(0)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-218">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="f1530-218">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="f1530-219"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="f1530-219"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="f1530-220">(1)</span><span class="sxs-lookup"><span data-stu-id="f1530-220">(1)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-221">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="f1530-221">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f1530-222"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f1530-222"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="f1530-223">(2)</span><span class="sxs-lookup"><span data-stu-id="f1530-223">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="f1530-224"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="f1530-224"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="f1530-225">(3)</span><span class="sxs-lookup"><span data-stu-id="f1530-225">(3)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-226">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="f1530-226">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="f1530-227"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="f1530-227"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="f1530-228">(4)</span><span class="sxs-lookup"><span data-stu-id="f1530-228">(4)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-229">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="f1530-229">Device is not working properly.</span></span> <span data-ttu-id="f1530-230">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="f1530-230">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="f1530-231"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="f1530-231"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="f1530-232">(5)</span><span class="sxs-lookup"><span data-stu-id="f1530-232">(5)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-233">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="f1530-233">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="f1530-234"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="f1530-234"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="f1530-235"> (6)</span><span class="sxs-lookup"><span data-stu-id="f1530-235">(6)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-236">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="f1530-236">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="f1530-237"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="f1530-237"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="f1530-238">(7)</span><span class="sxs-lookup"><span data-stu-id="f1530-238">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="f1530-239"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="f1530-239"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="f1530-240">(8)</span><span class="sxs-lookup"><span data-stu-id="f1530-240">(8)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-241">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="f1530-241">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="f1530-242"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="f1530-242"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="f1530-243">(9)</span><span class="sxs-lookup"><span data-stu-id="f1530-243">(9)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-244">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="f1530-244">Device is not working properly.</span></span> <span data-ttu-id="f1530-245">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f1530-245">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="f1530-246"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f1530-246"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="f1530-247">(10)</span><span class="sxs-lookup"><span data-stu-id="f1530-247">(10)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-248">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f1530-248">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="f1530-249"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f1530-249"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="f1530-250">(11)</span><span class="sxs-lookup"><span data-stu-id="f1530-250">(11)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-251">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f1530-251">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="f1530-252"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="f1530-252"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="f1530-253">12</span><span class="sxs-lookup"><span data-stu-id="f1530-253">(12)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-254">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="f1530-254">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="f1530-255"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f1530-255"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="f1530-256">(13)</span><span class="sxs-lookup"><span data-stu-id="f1530-256">(13)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-257">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f1530-257">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="f1530-258"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="f1530-258"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="f1530-259">(14)</span><span class="sxs-lookup"><span data-stu-id="f1530-259">(14)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-260">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="f1530-260">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="f1530-261"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="f1530-261"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="f1530-262">(15)</span><span class="sxs-lookup"><span data-stu-id="f1530-262">(15)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-263">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="f1530-263">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="f1530-264"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f1530-264"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="f1530-265">(16)</span><span class="sxs-lookup"><span data-stu-id="f1530-265">(16)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-266">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f1530-266">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="f1530-267"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="f1530-267"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="f1530-268">(17)</span><span class="sxs-lookup"><span data-stu-id="f1530-268">(17)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-269">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="f1530-269">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f1530-270"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f1530-270"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="f1530-271">(18)</span><span class="sxs-lookup"><span data-stu-id="f1530-271">(18)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-272">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f1530-272">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="f1530-273"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="f1530-273"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="f1530-274">(19)</span><span class="sxs-lookup"><span data-stu-id="f1530-274">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="f1530-275"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="f1530-275"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="f1530-276">(20)</span><span class="sxs-lookup"><span data-stu-id="f1530-276">(20)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-277">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="f1530-277">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="f1530-278"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f1530-278"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="f1530-279">(21)</span><span class="sxs-lookup"><span data-stu-id="f1530-279">(21)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-280">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="f1530-280">System failure.</span></span> <span data-ttu-id="f1530-281">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="f1530-281">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="f1530-282">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f1530-282">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="f1530-283"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="f1530-283"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="f1530-284">(22)</span><span class="sxs-lookup"><span data-stu-id="f1530-284">(22)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-285">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="f1530-285">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="f1530-286"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="f1530-286"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="f1530-287">(23)</span><span class="sxs-lookup"><span data-stu-id="f1530-287">(23)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-288">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="f1530-288">System failure.</span></span> <span data-ttu-id="f1530-289">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="f1530-289">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="f1530-290"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="f1530-290"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="f1530-291">(24)</span><span class="sxs-lookup"><span data-stu-id="f1530-291">(24)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-292">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="f1530-292">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="f1530-293"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f1530-293"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="f1530-294">(25)</span><span class="sxs-lookup"><span data-stu-id="f1530-294">(25)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-295">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f1530-295">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="f1530-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f1530-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="f1530-297">(26)</span><span class="sxs-lookup"><span data-stu-id="f1530-297">(26)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-298">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f1530-298">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="f1530-299"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="f1530-299"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="f1530-300">(27)</span><span class="sxs-lookup"><span data-stu-id="f1530-300">(27)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-301">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="f1530-301">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="f1530-302"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="f1530-302"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="f1530-303">(28)</span><span class="sxs-lookup"><span data-stu-id="f1530-303">(28)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-304">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="f1530-304">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="f1530-305"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="f1530-305"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="f1530-306">(29)</span><span class="sxs-lookup"><span data-stu-id="f1530-306">(29)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-307">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="f1530-307">Device is disabled.</span></span> <span data-ttu-id="f1530-308">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="f1530-308">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="f1530-309"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f1530-309"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="f1530-310">(30)</span><span class="sxs-lookup"><span data-stu-id="f1530-310">(30)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-311">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f1530-311">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f1530-312"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f1530-312"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="f1530-313">31</span><span class="sxs-lookup"><span data-stu-id="f1530-313">(31)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-314">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="f1530-314">Device is not working properly.</span></span> <span data-ttu-id="f1530-315">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="f1530-315">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f1530-316">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="f1530-316">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-317">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f1530-317">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-318">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-319">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f1530-319">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-320">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="f1530-320">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="f1530-321">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-321">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1530-322">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f1530-322">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-323">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f1530-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-324">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-325">Qualificatori: [ **\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="f1530-325">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="f1530-326">Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="f1530-326">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="f1530-327">Se utilizzata con le altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="f1530-327">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="f1530-328">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-328">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1530-329">**CurrentBitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="f1530-329">**CurrentBitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-330">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1530-330">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-331">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-332">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| Video \| 003,12 "), [**unità**](../wmisdk/standard-qualifiers.md) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="f1530-332">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.12"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-333">Numero di bit utilizzati per visualizzare ogni pixel.</span><span class="sxs-lookup"><span data-stu-id="f1530-333">Number of bits used to display each pixel.</span></span>

<span data-ttu-id="f1530-334">Questa proprietà viene ereditata da [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-334">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1530-335">**CurrentHorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="f1530-335">**CurrentHorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-336">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1530-336">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-337">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-338">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| Video \| 003,11 "), [**unità**](../wmisdk/standard-qualifiers.md) (" pixel ")</span><span class="sxs-lookup"><span data-stu-id="f1530-338">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.11"), [**Units**](../wmisdk/standard-qualifiers.md) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-339">Numero corrente di pixel orizzontali.</span><span class="sxs-lookup"><span data-stu-id="f1530-339">Current number of horizontal pixels.</span></span>

<span data-ttu-id="f1530-340">Questa proprietà viene ereditata da [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-340">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1530-341">**CurrentNumberOfColors**</span><span class="sxs-lookup"><span data-stu-id="f1530-341">**CurrentNumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-342">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f1530-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-343">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1530-344">Numero di colori supportati nella risoluzione corrente.</span><span class="sxs-lookup"><span data-stu-id="f1530-344">Number of colors supported at the current resolution.</span></span>

<span data-ttu-id="f1530-345">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-345">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="f1530-346">Questa proprietà viene ereditata da [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-346">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1530-347">**CurrentNumberOfColumns**</span><span class="sxs-lookup"><span data-stu-id="f1530-347">**CurrentNumberOfColumns**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-348">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1530-348">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-349">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-350">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. Video di DMTF \| \| 003,14 ")</span><span class="sxs-lookup"><span data-stu-id="f1530-350">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.14")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-351">Numero di colonne per il controller video in modalità carattere.</span><span class="sxs-lookup"><span data-stu-id="f1530-351">Number of columns for this video controller (if in character mode).</span></span> <span data-ttu-id="f1530-352">In caso contrario, immettere 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="f1530-352">Otherwise, enter 0 (zero).</span></span>

<span data-ttu-id="f1530-353">Questa proprietà viene ereditata da [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-353">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1530-354">**CurrentNumberOfRows**</span><span class="sxs-lookup"><span data-stu-id="f1530-354">**CurrentNumberOfRows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-355">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1530-355">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-356">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-357">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. Video di DMTF \| \| 003,13 ")</span><span class="sxs-lookup"><span data-stu-id="f1530-357">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.13")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-358">Numero di righe per il controller video in modalità carattere.</span><span class="sxs-lookup"><span data-stu-id="f1530-358">Number of rows for this video controller (if in character mode).</span></span> <span data-ttu-id="f1530-359">In caso contrario, immettere 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="f1530-359">Otherwise, enter 0 (zero).</span></span>

<span data-ttu-id="f1530-360">Questa proprietà viene ereditata da [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-360">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1530-361">**CurrentRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="f1530-361">**CurrentRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-362">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1530-362">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-363">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-364">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("CurrentRefreshRate"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HardwareInformation."), [**unità**](../wmisdk/standard-qualifiers.md) ("Hertz")</span><span class="sxs-lookup"><span data-stu-id="f1530-364">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("CurrentRefreshRate"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HardwareInformation."), [**Units**](../wmisdk/standard-qualifiers.md) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-365">Frequenza con cui il controller video aggiorna l'immagine per il monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="f1530-365">Frequency at which the video controller refreshes the image for the monitor.</span></span> <span data-ttu-id="f1530-366">Il valore 0 (zero) indica che è in uso la frequenza predefinita, mentre 0xFFFFFFFF indica che è in uso la velocità ottimale.</span><span class="sxs-lookup"><span data-stu-id="f1530-366">A value of 0 (zero) indicates the default rate is being used, while 0xFFFFFFFF indicates the optimal rate is being used.</span></span>

<span data-ttu-id="f1530-367">Questa proprietà viene ereditata da [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-367">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1530-368">**CurrentScanMode**</span><span class="sxs-lookup"><span data-stu-id="f1530-368">**CurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-369">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1530-369">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-370">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-371">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. Video di DMTF \| \| 003,8 ")</span><span class="sxs-lookup"><span data-stu-id="f1530-371">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.8")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-372">Modalità di analisi corrente.</span><span class="sxs-lookup"><span data-stu-id="f1530-372">Current scan mode.</span></span>

<span data-ttu-id="f1530-373">Questa proprietà viene ereditata da [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-373">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f1530-374"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="f1530-374"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f1530-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="f1530-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>

<span data-ttu-id="f1530-376"><span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>**Interlacciato** (3)</span><span class="sxs-lookup"><span data-stu-id="f1530-376"><span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>**Interlaced** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>

<span data-ttu-id="f1530-377"><span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>**Non interlacciato** (4)</span><span class="sxs-lookup"><span data-stu-id="f1530-377"><span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>**Non Interlaced** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-378">Non interlacciati</span><span class="sxs-lookup"><span data-stu-id="f1530-378">Noninterlaced</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f1530-379">**CurrentVerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="f1530-379">**CurrentVerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-380">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1530-380">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-381">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-382">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| Video \| 003,10 "), [**unità**](../wmisdk/standard-qualifiers.md) (" pixel ")</span><span class="sxs-lookup"><span data-stu-id="f1530-382">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.10"), [**Units**](../wmisdk/standard-qualifiers.md) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-383">Numero corrente di pixel verticali.</span><span class="sxs-lookup"><span data-stu-id="f1530-383">Current number of vertical pixels.</span></span>

<span data-ttu-id="f1530-384">Questa proprietà viene ereditata da [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-384">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1530-385">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="f1530-385">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-386">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f1530-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-387">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-388">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="f1530-388">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-389">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f1530-389">Description of the object.</span></span>

<span data-ttu-id="f1530-390">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-390">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1530-391">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="f1530-391">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-392">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f1530-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-393">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-394">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="f1530-394">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-395">Identificatore (univoco per il computer System) per questo controller video.</span><span class="sxs-lookup"><span data-stu-id="f1530-395">Identifier (unique to the computer system) for this video controller.</span></span>

<span data-ttu-id="f1530-396">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-396">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1530-397">**DeviceSpecificPens**</span><span class="sxs-lookup"><span data-stu-id="f1530-397">**DeviceSpecificPens**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-398">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1530-398">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-399">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-400">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span><span class="sxs-lookup"><span data-stu-id="f1530-400">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-401">Numero corrente di penne specifiche del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f1530-401">Current number of device-specific pens.</span></span> <span data-ttu-id="f1530-402">Il valore 0xffff indica che il dispositivo non supporta le penne.</span><span class="sxs-lookup"><span data-stu-id="f1530-402">A value of 0xffff means that the device does not support pens.</span></span>

<span data-ttu-id="f1530-403">Esempio: 3</span><span class="sxs-lookup"><span data-stu-id="f1530-403">Example: 3</span></span>

</dd> <dt>

<span data-ttu-id="f1530-404">**DitherType**</span><span class="sxs-lookup"><span data-stu-id="f1530-404">**DitherType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-405">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1530-405">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-406">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-406">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-407">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| EnumDisplaySettings")</span><span class="sxs-lookup"><span data-stu-id="f1530-407">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|EnumDisplaySettings")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-408">Tipo di dithering del controller video.</span><span class="sxs-lookup"><span data-stu-id="f1530-408">Dither type of the video controller.</span></span> <span data-ttu-id="f1530-409">La proprietà può essere uno dei valori predefiniti oppure un valore definito dal driver maggiore o uguale a 256.</span><span class="sxs-lookup"><span data-stu-id="f1530-409">The property can be one of the predefined values, or a driver-defined value greater than or equal to 256.</span></span> <span data-ttu-id="f1530-410">Se si sceglie la retinatura a linee, il controller utilizza un metodo di rethering che produce bordi ben definiti tra le scalazioni di nero, bianco e grigio.</span><span class="sxs-lookup"><span data-stu-id="f1530-410">If line art dithering is chosen, the controller uses a dithering method that produces well-defined borders between black, white, and gray scalings.</span></span> <span data-ttu-id="f1530-411">Il rethering dell'arte line non è adatto per le immagini che includono la graduazione continua in intensità e tonalità, ad esempio le fotografie analizzate.</span><span class="sxs-lookup"><span data-stu-id="f1530-411">Line art dithering is not suitable for images that include continuous graduations in intensity and hue such as scanned photographs.</span></span>

<dt>

<span id="No_dithering"></span><span id="no_dithering"></span><span id="NO_DITHERING"></span>

<span data-ttu-id="f1530-412">**Nessuna retinatura** (1)</span><span class="sxs-lookup"><span data-stu-id="f1530-412">**No dithering** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Dithering_with_a_coarse_brush"></span><span id="dithering_with_a_coarse_brush"></span><span id="DITHERING_WITH_A_COARSE_BRUSH"></span>

<span data-ttu-id="f1530-413">**Retinatura con un pennello grossolano** (2)</span><span class="sxs-lookup"><span data-stu-id="f1530-413">**Dithering with a coarse brush** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dithering_with_a_fine_brush"></span><span id="dithering_with_a_fine_brush"></span><span id="DITHERING_WITH_A_FINE_BRUSH"></span>

<span data-ttu-id="f1530-414">**Retinatura con un pennello fine** (3)</span><span class="sxs-lookup"><span data-stu-id="f1530-414">**Dithering with a fine brush** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_art_dithering"></span><span id="line_art_dithering"></span><span id="LINE_ART_DITHERING"></span>

<span data-ttu-id="f1530-415">**Rethering line art** (4)</span><span class="sxs-lookup"><span data-stu-id="f1530-415">**Line art dithering** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_does_gray_scaling"></span><span id="device_does_gray_scaling"></span><span id="DEVICE_DOES_GRAY_SCALING"></span>

<span data-ttu-id="f1530-416">**Il dispositivo esegue la scalabilità grigia** (5)</span><span class="sxs-lookup"><span data-stu-id="f1530-416">**Device does gray scaling** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f1530-417">**DriverDate**</span><span class="sxs-lookup"><span data-stu-id="f1530-417">**DriverDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-418">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f1530-418">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-419">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-420">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ ")</span><span class="sxs-lookup"><span data-stu-id="f1530-420">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-421">Data e ora dell'Ultima modifica del driver video attualmente installato.</span><span class="sxs-lookup"><span data-stu-id="f1530-421">Last modification date and time of the currently installed video driver.</span></span>

</dd> <dt>

<span data-ttu-id="f1530-422">**DriverVersion**</span><span class="sxs-lookup"><span data-stu-id="f1530-422">**DriverVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-423">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f1530-423">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-424">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-425">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funzioni libreria di installazione file Win32API \| GetFileVersionInfo")</span><span class="sxs-lookup"><span data-stu-id="f1530-425">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|File Installation Library Functions\|GetFileVersionInfo")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-426">Numero di versione del driver video.</span><span class="sxs-lookup"><span data-stu-id="f1530-426">Version number of the video driver.</span></span>

</dd> <dt>

<span data-ttu-id="f1530-427">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="f1530-427">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-428">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f1530-428">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-429">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1530-430">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="f1530-430">If **TRUE**, the error reported in **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="f1530-431">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-431">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1530-432">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="f1530-432">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-433">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f1530-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-434">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-434">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1530-435">Stringa in formato libero che fornisce ulteriori informazioni sull'errore registrato nella proprietà **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="f1530-435">Free-form string supplying more information about the error recorded in **LastErrorCode** property, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="f1530-436">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-436">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1530-437">**ICMIntent**</span><span class="sxs-lookup"><span data-stu-id="f1530-437">**ICMIntent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-438">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1530-438">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-439">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-439">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-440">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Printing and Print spooler Structures \| DEVMODE \| dmICMIntent")</span><span class="sxs-lookup"><span data-stu-id="f1530-440">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Printing and Print Spooler Structures\|DevMode\|dmICMIntent")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-441">Valore specifico di uno dei tre possibili metodi di corrispondenza dei colori o Intent che devono essere utilizzati per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="f1530-441">Specific value of one of the three possible color-matching methods or intents that should be used by default.</span></span> <span data-ttu-id="f1530-442">Questa proprietà viene utilizzata principalmente per le applicazioni non ICM.</span><span class="sxs-lookup"><span data-stu-id="f1530-442">This property is used primarily for non-ICM applications.</span></span> <span data-ttu-id="f1530-443">Le applicazioni ICM stabiliscono gli Intent usando le funzioni ICM.</span><span class="sxs-lookup"><span data-stu-id="f1530-443">ICM applications establish intents by using the ICM functions.</span></span> <span data-ttu-id="f1530-444">Questa proprietà può essere un valore predefinito o un valore definito dal driver maggiore o uguale a 256.</span><span class="sxs-lookup"><span data-stu-id="f1530-444">This property can be a predefined value or a driver defined value greater than or equal to 256.</span></span> <span data-ttu-id="f1530-445">La corrispondenza dei colori basata sulla saturazione è la scelta più appropriata per i grafici aziendali quando non si desidera la retinatura.</span><span class="sxs-lookup"><span data-stu-id="f1530-445">Color matching based on saturation is the most appropriate choice for business graphs when dithering is not desired.</span></span> <span data-ttu-id="f1530-446">La corrispondenza dei colori in base al contrasto è la scelta più appropriata per immagini digitalizzate o fotografiche quando si desidera la retinatura.</span><span class="sxs-lookup"><span data-stu-id="f1530-446">Color matching based on contrast is the most appropriate choice for scanned or photographic images when dithering is desired.</span></span> <span data-ttu-id="f1530-447">La corrispondenza dei colori ottimizzata in modo da corrispondere al colore esatto richiesto è più appropriata per l'uso con logo aziendali o altre immagini quando si desidera una corrispondenza esatta dei colori.</span><span class="sxs-lookup"><span data-stu-id="f1530-447">Color matching optimized to match the exact color requested is most appropriate for use with business logos or other images when an exact color match is desired.</span></span>

<dt>

<span id="Saturation"></span><span id="saturation"></span><span id="SATURATION"></span>

<span data-ttu-id="f1530-448">**Saturazione** (1)</span><span class="sxs-lookup"><span data-stu-id="f1530-448">**Saturation** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Contrast"></span><span id="contrast"></span><span id="CONTRAST"></span>

<span data-ttu-id="f1530-449">**Contrasto** (2)</span><span class="sxs-lookup"><span data-stu-id="f1530-449">**Contrast** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Exact_Color"></span><span id="exact_color"></span><span id="EXACT_COLOR"></span>

<span data-ttu-id="f1530-450">**Colore esatto** (3)</span><span class="sxs-lookup"><span data-stu-id="f1530-450">**Exact Color** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f1530-451">**ICMMethod**</span><span class="sxs-lookup"><span data-stu-id="f1530-451">**ICMMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-452">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1530-452">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-453">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-454">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Printing and Print spooler Structures \| DEVMODE \| dmICMMethod")</span><span class="sxs-lookup"><span data-stu-id="f1530-454">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Printing and Print Spooler Structures\|DevMode\|dmICMMethod")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-455">Metodo di gestione di ICM.</span><span class="sxs-lookup"><span data-stu-id="f1530-455">Method of handling ICM.</span></span> <span data-ttu-id="f1530-456">Per le applicazioni non ICM, questa proprietà determina se ICM è abilitato.</span><span class="sxs-lookup"><span data-stu-id="f1530-456">For non-ICM applications, this property determines if ICM is enabled.</span></span> <span data-ttu-id="f1530-457">Per le applicazioni ICM, il sistema esamina questa proprietà per determinare la modalità di gestione del supporto ICM.</span><span class="sxs-lookup"><span data-stu-id="f1530-457">For ICM applications, the system examines this property to determine how to handle ICM support.</span></span> <span data-ttu-id="f1530-458">Questa proprietà può essere un valore predefinito o un valore definito dal driver maggiore o uguale a 256.</span><span class="sxs-lookup"><span data-stu-id="f1530-458">This property can be a predefined value or a driver-defined value greater than or equal to 256.</span></span> <span data-ttu-id="f1530-459">Il valore determina quale sistema gestisce la corrispondenza dei colori dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="f1530-459">The value determines which system handles image color matching.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f1530-460">**Disabilitato** (1)</span><span class="sxs-lookup"><span data-stu-id="f1530-460">**Disabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows"></span><span id="windows"></span><span id="WINDOWS"></span>

<span data-ttu-id="f1530-461">**Windows** (2)</span><span class="sxs-lookup"><span data-stu-id="f1530-461">**Windows** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Driver"></span><span id="device_driver"></span><span id="DEVICE_DRIVER"></span>

<span data-ttu-id="f1530-462">**Driver di dispositivo** (3)</span><span class="sxs-lookup"><span data-stu-id="f1530-462">**Device Driver** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Destination_Device"></span><span id="destination_device"></span><span id="DESTINATION_DEVICE"></span>

<span data-ttu-id="f1530-463">**Dispositivo di destinazione** (4)</span><span class="sxs-lookup"><span data-stu-id="f1530-463">**Destination Device** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f1530-464">**InfFilename**</span><span class="sxs-lookup"><span data-stu-id="f1530-464">**InfFilename**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-465">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f1530-465">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-466">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-466">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-467">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \\ \\ {4D36E968-E325-11CE-BFC1-08002BE10318} \\ \\ 0000")</span><span class="sxs-lookup"><span data-stu-id="f1530-467">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\\\\{4D36E968-E325-11CE-BFC1-08002BE10318}\\\\0000")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-468">Percorso del file con estensione inf della scheda video.</span><span class="sxs-lookup"><span data-stu-id="f1530-468">Path to the video adapter's .inf file.</span></span>

<span data-ttu-id="f1530-469">Esempio: "C: \\ Windows \\ system32 \\ Drivers"</span><span class="sxs-lookup"><span data-stu-id="f1530-469">Example: "C:\\Windows\\SYSTEM32\\DRIVERS"</span></span>

</dd> <dt>

<span data-ttu-id="f1530-470">**InfSection**</span><span class="sxs-lookup"><span data-stu-id="f1530-470">**InfSection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-471">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f1530-471">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-472">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-472">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-473">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \\ \\ {4D36E968-E325-11CE-BFC1-08002BE10318} \\ \\ 0000")</span><span class="sxs-lookup"><span data-stu-id="f1530-473">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\\\\{4D36E968-E325-11CE-BFC1-08002BE10318}\\\\0000")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-474">Sezione del file con estensione inf in cui si trovano le informazioni sul video di Windows.</span><span class="sxs-lookup"><span data-stu-id="f1530-474">Section of the .inf file where the Windows video information resides.</span></span>

</dd> <dt>

<span data-ttu-id="f1530-475">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f1530-475">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-476">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f1530-476">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-477">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-478">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="f1530-478">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-479">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f1530-479">Date and time the object was installed.</span></span> <span data-ttu-id="f1530-480">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="f1530-480">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="f1530-481">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-481">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1530-482">**InstalledDisplayDrivers**</span><span class="sxs-lookup"><span data-stu-id="f1530-482">**InstalledDisplayDrivers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-483">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f1530-483">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-484">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-484">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-485">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ ")</span><span class="sxs-lookup"><span data-stu-id="f1530-485">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-486">Nome del driver del dispositivo di visualizzazione installato.</span><span class="sxs-lookup"><span data-stu-id="f1530-486">Name of the installed display device driver.</span></span>

</dd> <dt>

<span data-ttu-id="f1530-487">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="f1530-487">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-488">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1530-488">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-489">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-489">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1530-490">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="f1530-490">Last error code reported by the logical device.</span></span>

<span data-ttu-id="f1530-491">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1530-492">**MaxMemorySupported**</span><span class="sxs-lookup"><span data-stu-id="f1530-492">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-493">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1530-493">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-494">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-495">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("byte")</span><span class="sxs-lookup"><span data-stu-id="f1530-495">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-496">Quantità massima di memoria supportata in byte.</span><span class="sxs-lookup"><span data-stu-id="f1530-496">Maximum amount of memory supported in bytes.</span></span>

<span data-ttu-id="f1530-497">Questa proprietà viene ereditata da [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-497">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1530-498">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="f1530-498">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-499">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1530-499">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-500">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-500">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-501">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Porta bus DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="f1530-501">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-502">Numero massimo di entità indirizzabili direttamente supportato da questo controller.</span><span class="sxs-lookup"><span data-stu-id="f1530-502">Maximum number of directly addressable entities supportable by this controller.</span></span> <span data-ttu-id="f1530-503">Se il numero è sconosciuto, è necessario usare un valore pari a 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="f1530-503">A value of 0 (zero) should be used if the number is unknown.</span></span>

<span data-ttu-id="f1530-504">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-504">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1530-505">**MaxRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="f1530-505">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-506">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1530-506">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-507">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-507">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-508">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| Video \| 003,5 "), [**unità**](../wmisdk/standard-qualifiers.md) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="f1530-508">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.5"), [**Units**](../wmisdk/standard-qualifiers.md) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-509">Frequenza di aggiornamento massima del controller video in Hertz.</span><span class="sxs-lookup"><span data-stu-id="f1530-509">Maximum refresh rate of the video controller in hertz.</span></span>

<span data-ttu-id="f1530-510">Questa proprietà viene ereditata da [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-510">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1530-511">**MinRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="f1530-511">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-512">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1530-512">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-513">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-514">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| Video \| 003,4 "), [**unità**](../wmisdk/standard-qualifiers.md) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="f1530-514">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.4"), [**Units**](../wmisdk/standard-qualifiers.md) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-515">Frequenza di aggiornamento minima del controller video in Hertz.</span><span class="sxs-lookup"><span data-stu-id="f1530-515">Minimum refresh rate of the video controller in hertz.</span></span>

<span data-ttu-id="f1530-516">Questa proprietà viene ereditata da [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-516">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1530-517">**Monocromatico**</span><span class="sxs-lookup"><span data-stu-id="f1530-517">**Monochrome**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-518">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f1530-518">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-519">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-519">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-520">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="f1530-520">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-521">Se **true**, la scala di grigi viene utilizzata per visualizzare le immagini.</span><span class="sxs-lookup"><span data-stu-id="f1530-521">If **TRUE**, gray scale is used to display images.</span></span>

</dd> <dt>

<span data-ttu-id="f1530-522">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f1530-522">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-523">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f1530-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-524">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-525">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="f1530-525">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-526">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="f1530-526">Label by which the object is known.</span></span> <span data-ttu-id="f1530-527">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="f1530-527">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="f1530-528">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-528">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1530-529">**NumberOfColorPlanes**</span><span class="sxs-lookup"><span data-stu-id="f1530-529">**NumberOfColorPlanes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-530">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1530-530">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-531">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-531">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1530-532">Numero corrente di piani di colore.</span><span class="sxs-lookup"><span data-stu-id="f1530-532">Current number of color planes.</span></span> <span data-ttu-id="f1530-533">Se questo valore non è applicabile per la configurazione video corrente, immettere 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="f1530-533">If this value is not applicable for the current video configuration, enter 0 (zero).</span></span>

<span data-ttu-id="f1530-534">Questa proprietà viene ereditata da [**CIM \_ PCVideoController**](cim-pcvideocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-534">This property is inherited from [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1530-535">**NumberOfVideoPages**</span><span class="sxs-lookup"><span data-stu-id="f1530-535">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-536">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1530-536">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-537">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1530-538">Numero di pagine video supportate in base alle risoluzioni correnti e alla memoria disponibile.</span><span class="sxs-lookup"><span data-stu-id="f1530-538">Number of video pages supported given the current resolutions and available memory.</span></span>

<span data-ttu-id="f1530-539">Questa proprietà viene ereditata da [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-539">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1530-540">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="f1530-540">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-541">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f1530-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-542">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-542">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-543">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f1530-543">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-544">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="f1530-544">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="f1530-545">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="f1530-545">Example: "\*PNP030b"</span></span>

<span data-ttu-id="f1530-546">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-546">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1530-547">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="f1530-547">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-548">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1530-548">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f1530-549">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-549">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1530-550">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="f1530-550">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="f1530-551">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-551">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f1530-552"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="f1530-552"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="f1530-553"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="f1530-553"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f1530-554"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="f1530-554"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f1530-555"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="f1530-555"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-556">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="f1530-556">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="f1530-557"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="f1530-557"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-558">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="f1530-558">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="f1530-559"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="f1530-559"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-560">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="f1530-560">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="f1530-561">Questo metodo è disponibile nella classe [**\_ LogicalDevice CIM**](cim-logicaldevice.md) padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="f1530-561">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="f1530-562">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-562">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="f1530-563"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="f1530-563"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-564">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="f1530-564">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="f1530-565"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="f1530-565"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-566">Tempo Power-On supportato</span><span class="sxs-lookup"><span data-stu-id="f1530-566">Timed Power-On Supported</span></span>

<span data-ttu-id="f1530-567">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="f1530-567">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f1530-568">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="f1530-568">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-569">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f1530-569">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-570">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-570">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1530-571">Se **true**, il dispositivo può essere gestito dal risparmio di energia (può essere impostato in modalità di sospensione e così via).</span><span class="sxs-lookup"><span data-stu-id="f1530-571">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="f1530-572">La proprietà non indica che le funzionalità di risparmio energia sono attualmente abilitate, solo che il dispositivo logico è in grado di gestire il risparmio di energia.</span><span class="sxs-lookup"><span data-stu-id="f1530-572">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="f1530-573">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-573">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1530-574">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="f1530-574">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-575">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1530-575">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-576">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-576">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-577">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Porta bus DMTF \| 001,2 "," MIF. \|Dischi DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="f1530-577">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-578">Protocollo usato dal controller per accedere ai dispositivi "controllati".</span><span class="sxs-lookup"><span data-stu-id="f1530-578">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="f1530-579">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-579">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f1530-580"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="f1530-580"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f1530-581"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="f1530-581"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="f1530-582"><span id="EISA"></span><span id="eisa"></span>**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="f1530-582"><span id="EISA"></span><span id="eisa"></span>**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="f1530-583"><span id="ISA"></span><span id="isa"></span>**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="f1530-583"><span id="ISA"></span><span id="isa"></span>**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="f1530-584"><span id="PCI"></span><span id="pci"></span>**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="f1530-584"><span id="PCI"></span><span id="pci"></span>**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="f1530-585"><span id="ATA_ATAPI"></span><span id="ata_atapi"></span>**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="f1530-585"><span id="ATA_ATAPI"></span><span id="ata_atapi"></span>**ATA/ATAPI** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f1530-586">ATA o ATAPI</span><span class="sxs-lookup"><span data-stu-id="f1530-586">ATA or ATAPI</span></span>

</dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="f1530-587"><span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>**Dischetto flessibile** (7)</span><span class="sxs-lookup"><span data-stu-id="f1530-587"><span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="f1530-588"><span id="1496"></span>**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="f1530-588"><span id="1496"></span>**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="f1530-589"><span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>**Interfaccia parallela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="f1530-589"><span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="f1530-590"><span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>**Protocollo di Fibre Channel SCSI** (10)</span><span class="sxs-lookup"><span data-stu-id="f1530-590"><span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="f1530-591"><span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>**Protocollo bus seriale SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="f1530-591"><span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="f1530-592"><span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>**Protocollo bus seriale SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="f1530-592"><span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="f1530-593"><span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>**Architettura di archiviazione seriale SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="f1530-593"><span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="f1530-594"><span id="VESA"></span><span id="vesa"></span>**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="f1530-594"><span id="VESA"></span><span id="vesa"></span>**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="f1530-595"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="f1530-595"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="f1530-596"><span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>**Bus seriale universale** (16)</span><span class="sxs-lookup"><span data-stu-id="f1530-596"><span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="f1530-597"><span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>**Protocollo parallelo** (17)</span><span class="sxs-lookup"><span data-stu-id="f1530-597"><span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="f1530-598"><span id="ESCON"></span><span id="escon"></span>**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="f1530-598"><span id="ESCON"></span><span id="escon"></span>**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="f1530-599"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostica** (19)</span><span class="sxs-lookup"><span data-stu-id="f1530-599"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="f1530-600"><span id="I2C"></span><span id="i2c"></span>**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="f1530-600"><span id="I2C"></span><span id="i2c"></span>**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="f1530-601"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Potenza** (21)</span><span class="sxs-lookup"><span data-stu-id="f1530-601"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="f1530-602"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="f1530-602"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="f1530-603"><span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="f1530-603"><span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="f1530-604"><span id="VME"></span><span id="vme"></span>**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="f1530-604"><span id="VME"></span><span id="vme"></span>**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="f1530-605"><span id="IPI"></span><span id="ipi"></span>**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="f1530-605"><span id="IPI"></span><span id="ipi"></span>**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="f1530-606"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="f1530-606"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="f1530-607"><span id="RS232"></span><span id="rs232"></span>**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="f1530-607"><span id="RS232"></span><span id="rs232"></span>**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="f1530-608"><span id="ieee_802.3_10base5"></span>**IEEE 802,3 10Base5** (28)</span><span class="sxs-lookup"><span data-stu-id="f1530-608"><span id="ieee_802.3_10base5"></span>**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="f1530-609"><span id="ieee_802.3_10base2"></span>**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="f1530-609"><span id="ieee_802.3_10base2"></span>**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="f1530-610"><span id="ieee_802.3_1base5"></span>**IEEE 802,3 1Base5** (30)</span><span class="sxs-lookup"><span data-stu-id="f1530-610"><span id="ieee_802.3_1base5"></span>**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="f1530-611"><span id="ieee_802.3_10broad36"></span>**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="f1530-611"><span id="ieee_802.3_10broad36"></span>**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="f1530-612"><span id="ieee_802.3_100basevg"></span>**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="f1530-612"><span id="ieee_802.3_100basevg"></span>**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="f1530-613"><span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>**Token-ring IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="f1530-613"><span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="f1530-614"><span id="ansi_x3t9.5_fddi"></span>**ANSI X3T 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="f1530-614"><span id="ansi_x3t9.5_fddi"></span>**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="f1530-615"><span id="MCA"></span><span id="mca"></span>**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="f1530-615"><span id="MCA"></span><span id="mca"></span>**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="f1530-616"><span id="ESDI"></span><span id="esdi"></span>**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="f1530-616"><span id="ESDI"></span><span id="esdi"></span>**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="f1530-617"><span id="IDE"></span><span id="ide"></span>**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="f1530-617"><span id="IDE"></span><span id="ide"></span>**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="f1530-618"><span id="CMD"></span><span id="cmd"></span>**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="f1530-618"><span id="CMD"></span><span id="cmd"></span>**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="f1530-619"><span id="ST506"></span><span id="st506"></span>**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="f1530-619"><span id="ST506"></span><span id="st506"></span>**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="f1530-620"><span id="DSSI"></span><span id="dssi"></span>**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="f1530-620"><span id="DSSI"></span><span id="dssi"></span>**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="f1530-621"><span id="QIC2"></span><span id="qic2"></span>**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="f1530-621"><span id="QIC2"></span><span id="qic2"></span>**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="f1530-622"><span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>**ATA/IDE avanzato** (42)</span><span class="sxs-lookup"><span data-stu-id="f1530-622"><span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="f1530-623"><span id="AGP"></span><span id="agp"></span>**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="f1530-623"><span id="AGP"></span><span id="agp"></span>**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="f1530-624"><span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>**TWIRP (infrarossi bidirezionali)** (44)</span><span class="sxs-lookup"><span data-stu-id="f1530-624"><span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="f1530-625"><span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>**FIR (infrarossi veloci)** (45)</span><span class="sxs-lookup"><span data-stu-id="f1530-625"><span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="f1530-626"><span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>**Sir (Serial Infrared)** (46)</span><span class="sxs-lookup"><span data-stu-id="f1530-626"><span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="f1530-627"><span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="f1530-627"><span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f1530-628">**ReservedSystemPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="f1530-628">**ReservedSystemPaletteEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-629">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1530-629">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-630">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-630">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-631">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span><span class="sxs-lookup"><span data-stu-id="f1530-631">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-632">Numero di voci riservate nella tavolozza di sistema.</span><span class="sxs-lookup"><span data-stu-id="f1530-632">Number of reserved entries in the system palette.</span></span> <span data-ttu-id="f1530-633">Il sistema operativo può riservare le voci per supportare i colori standard per le barre delle attività e altri elementi visualizzati sul desktop.</span><span class="sxs-lookup"><span data-stu-id="f1530-633">The operating system may reserve entries to support standard colors for task bars and other desktop display items.</span></span> <span data-ttu-id="f1530-634">Questo indice è valido solo se il driver di dispositivo imposta il bit della **\_ tavolozza RC** nell'indice RASTERCAPS ed è disponibile solo se il driver è compatibile con Windows a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="f1530-634">This index is valid only if the device driver sets the **RC\_PALETTE** bit in the RASTERCAPS index, and is available only if the driver is compatible with 16-bit Windows.</span></span> <span data-ttu-id="f1530-635">Se il sistema non utilizza una tavolozza, **ReservedSystemPaletteEntries** non è impostato.</span><span class="sxs-lookup"><span data-stu-id="f1530-635">If the system is not using a palette, **ReservedSystemPaletteEntries** is not set.</span></span>

<span data-ttu-id="f1530-636">Esempio: 20</span><span class="sxs-lookup"><span data-stu-id="f1530-636">Example: 20</span></span>

</dd> <dt>

<span data-ttu-id="f1530-637">**SpecificationVersion**</span><span class="sxs-lookup"><span data-stu-id="f1530-637">**SpecificationVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-638">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1530-638">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-639">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-639">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-640">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Printing and Print spooler Structures \| DEVMODE \| dmSpecVersion")</span><span class="sxs-lookup"><span data-stu-id="f1530-640">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Printing and Print Spooler Structures\|DevMode\|dmSpecVersion")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-641">Numero di versione della specifica dei dati di inizializzazione (su cui si basa la struttura).</span><span class="sxs-lookup"><span data-stu-id="f1530-641">Version number of the initialization data specification (upon which the structure is based).</span></span>

</dd> <dt>

<span data-ttu-id="f1530-642">**Status**</span><span class="sxs-lookup"><span data-stu-id="f1530-642">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-643">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f1530-643">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-644">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-644">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-645">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="f1530-645">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-646">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f1530-646">Current status of the object.</span></span> <span data-ttu-id="f1530-647">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="f1530-647">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="f1530-648">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="f1530-648">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="f1530-649">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="f1530-649">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f1530-650">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="f1530-650">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f1530-651">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="f1530-651">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f1530-652">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-652">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f1530-653">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="f1530-653">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f1530-654">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="f1530-654">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f1530-655">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="f1530-655">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f1530-656">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="f1530-656">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f1530-657">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="f1530-657">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f1530-658">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="f1530-658">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f1530-659">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="f1530-659">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f1530-660">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="f1530-660">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f1530-661">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="f1530-661">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f1530-662">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="f1530-662">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f1530-663">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="f1530-663">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f1530-664">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="f1530-664">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f1530-665">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="f1530-665">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f1530-666">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="f1530-666">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-667">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1530-667">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-668">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-668">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-669">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="f1530-669">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-670">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="f1530-670">State of the logical device.</span></span> <span data-ttu-id="f1530-671">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="f1530-671">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="f1530-672">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-672">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f1530-673">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="f1530-673">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f1530-674">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="f1530-674">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f1530-675">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="f1530-675">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f1530-676">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="f1530-676">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f1530-677">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="f1530-677">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f1530-678">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f1530-678">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-679">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f1530-679">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-680">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-680">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-681">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="f1530-681">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="f1530-682">Valore della proprietà **CreationClassName** del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="f1530-682">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="f1530-683">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-683">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1530-684">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="f1530-684">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-685">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f1530-685">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-686">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-686">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-687">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="f1530-687">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="f1530-688">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="f1530-688">Name of the scoping system.</span></span>

<span data-ttu-id="f1530-689">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-689">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1530-690">**SystemPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="f1530-690">**SystemPaletteEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-691">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1530-691">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-692">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-692">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-693">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span><span class="sxs-lookup"><span data-stu-id="f1530-693">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-694">Numero corrente di voci di indice dei colori nella tavolozza di sistema.</span><span class="sxs-lookup"><span data-stu-id="f1530-694">Current number of color index entries in the system palette.</span></span> <span data-ttu-id="f1530-695">Questo indice è valido solo se il driver di dispositivo imposta il bit della **\_ tavolozza RC** nell'indice RASTERCAPS ed è disponibile solo se il driver è compatibile con Windows a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="f1530-695">This index is valid only if the device driver sets the **RC\_PALETTE** bit in the RASTERCAPS index, and is available only if the driver is compatible with 16-bit Windows.</span></span> <span data-ttu-id="f1530-696">Se il sistema non utilizza una tavolozza, **SystemPaletteEntries** non è impostato.</span><span class="sxs-lookup"><span data-stu-id="f1530-696">If the system is not using a palette, **SystemPaletteEntries** is not set.</span></span>

<span data-ttu-id="f1530-697">Esempio: 20</span><span class="sxs-lookup"><span data-stu-id="f1530-697">Example: 20</span></span>

</dd> <dt>

<span data-ttu-id="f1530-698">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="f1530-698">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-699">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f1530-699">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-700">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-700">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1530-701">Data e ora dell'ultima reimpostazione del controller.</span><span class="sxs-lookup"><span data-stu-id="f1530-701">Date and time this controller was last reset.</span></span> <span data-ttu-id="f1530-702">Questo potrebbe significare che il controller è stato spento o reinizializzato.</span><span class="sxs-lookup"><span data-stu-id="f1530-702">This could mean the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="f1530-703">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-703">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1530-704">**VideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="f1530-704">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-705">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1530-705">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-706">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-706">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-707">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. Video di DMTF \| \| 003,2 ")</span><span class="sxs-lookup"><span data-stu-id="f1530-707">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.2")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-708">Tipo di architettura video.</span><span class="sxs-lookup"><span data-stu-id="f1530-708">Type of video architecture.</span></span>

<span data-ttu-id="f1530-709">Questa proprietà viene ereditata da [**CIM \_ PCVideoController**](cim-pcvideocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-709">This property is inherited from [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f1530-710">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="f1530-710">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f1530-711">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="f1530-711">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="CGA"></span><span id="cga"></span>

<span data-ttu-id="f1530-712">**CGA** (3)</span><span class="sxs-lookup"><span data-stu-id="f1530-712">**CGA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="EGA"></span><span id="ega"></span>

<span data-ttu-id="f1530-713">**EGA** (4)</span><span class="sxs-lookup"><span data-stu-id="f1530-713">**EGA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VGA"></span><span id="vga"></span>

<span data-ttu-id="f1530-714">**VGA** (5)</span><span class="sxs-lookup"><span data-stu-id="f1530-714">**VGA** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SVGA"></span><span id="svga"></span>

<span data-ttu-id="f1530-715">**SVGA** (6)</span><span class="sxs-lookup"><span data-stu-id="f1530-715">**SVGA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="MDA"></span><span id="mda"></span>

<span data-ttu-id="f1530-716">**MDA** (7)</span><span class="sxs-lookup"><span data-stu-id="f1530-716">**MDA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="HGC"></span><span id="hgc"></span>

<span data-ttu-id="f1530-717">**HGC** (8)</span><span class="sxs-lookup"><span data-stu-id="f1530-717">**HGC** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="MCGA"></span><span id="mcga"></span>

<span data-ttu-id="f1530-718">**MCGA** (9)</span><span class="sxs-lookup"><span data-stu-id="f1530-718">**MCGA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="8514A"></span><span id="8514a"></span>

<span data-ttu-id="f1530-719">**8514a** (10)</span><span class="sxs-lookup"><span data-stu-id="f1530-719">**8514A** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="XGA"></span><span id="xga"></span>

<span data-ttu-id="f1530-720">**XGA** (11)</span><span class="sxs-lookup"><span data-stu-id="f1530-720">**XGA** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>

<span data-ttu-id="f1530-721">**Buffer frame lineare** (12)</span><span class="sxs-lookup"><span data-stu-id="f1530-721">**Linear Frame Buffer** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="f1530-722">**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="f1530-722">**PC-98** (160)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f1530-723">**VideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="f1530-723">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-724">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1530-724">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-725">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-725">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-726">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. Video di DMTF \| \| 003,6 ")</span><span class="sxs-lookup"><span data-stu-id="f1530-726">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.6")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-727">Tipo di memoria video.</span><span class="sxs-lookup"><span data-stu-id="f1530-727">Type of video memory.</span></span>

<span data-ttu-id="f1530-728">Questa proprietà viene ereditata da [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-728">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f1530-729">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="f1530-729">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f1530-730">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="f1530-730">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="f1530-731">**VRAM** (3)</span><span class="sxs-lookup"><span data-stu-id="f1530-731">**VRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="f1530-732">**DRAM** (4)</span><span class="sxs-lookup"><span data-stu-id="f1530-732">**DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="f1530-733">**SRAM** (5)</span><span class="sxs-lookup"><span data-stu-id="f1530-733">**SRAM** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WRAM"></span><span id="wram"></span>

<span data-ttu-id="f1530-734">**WRAM** (6)</span><span class="sxs-lookup"><span data-stu-id="f1530-734">**WRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO_RAM"></span><span id="edo_ram"></span>

<span data-ttu-id="f1530-735">**RAM EDO** (7)</span><span class="sxs-lookup"><span data-stu-id="f1530-735">**EDO RAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst_Synchronous_DRAM"></span><span id="burst_synchronous_dram"></span><span id="BURST_SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="f1530-736">**DRAM sincrona a impulsi** (8)</span><span class="sxs-lookup"><span data-stu-id="f1530-736">**Burst Synchronous DRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipelined_Burst_SRAM"></span><span id="pipelined_burst_sram"></span><span id="PIPELINED_BURST_SRAM"></span>

<span data-ttu-id="f1530-737">**SRAM di impulso in pipeline** (9)</span><span class="sxs-lookup"><span data-stu-id="f1530-737">**Pipelined Burst SRAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="f1530-738">**CDRAM** (10)</span><span class="sxs-lookup"><span data-stu-id="f1530-738">**CDRAM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="f1530-739">**3DRAM** (11)</span><span class="sxs-lookup"><span data-stu-id="f1530-739">**3DRAM** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="f1530-740">**SDRAM** (12)</span><span class="sxs-lookup"><span data-stu-id="f1530-740">**SDRAM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="f1530-741">**SGRAM** (13)</span><span class="sxs-lookup"><span data-stu-id="f1530-741">**SGRAM** (13)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f1530-742">**VideoMode**</span><span class="sxs-lookup"><span data-stu-id="f1530-742">**VideoMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-743">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1530-743">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-744">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-744">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-745">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. Video di DMTF \| \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="f1530-745">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-746">Modalità video corrente.</span><span class="sxs-lookup"><span data-stu-id="f1530-746">Current video mode.</span></span>

<span data-ttu-id="f1530-747">Questa proprietà viene ereditata da [**CIM \_ PCVideoController**](cim-pcvideocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-747">This property is inherited from [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1530-748">**VideoModeDescription**</span><span class="sxs-lookup"><span data-stu-id="f1530-748">**VideoModeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-749">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f1530-749">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-750">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-750">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1530-751">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span><span class="sxs-lookup"><span data-stu-id="f1530-751">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span></span>
</dt> </dl>

<span data-ttu-id="f1530-752">Impostazioni correnti per la risoluzione, il colore e la modalità di analisi del controller video.</span><span class="sxs-lookup"><span data-stu-id="f1530-752">Current resolution, color, and scan mode settings of the video controller.</span></span>

<span data-ttu-id="f1530-753">Esempio: "1024 x 768 x 256 colori"</span><span class="sxs-lookup"><span data-stu-id="f1530-753">Example: "1024 x 768 x 256 colors"</span></span>

</dd> <dt>

<span data-ttu-id="f1530-754">**VideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="f1530-754">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1530-755">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f1530-755">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1530-756">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1530-756">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1530-757">Stringa in formato libero che descrive il processore video.</span><span class="sxs-lookup"><span data-stu-id="f1530-757">Free-form string describing the video processor.</span></span>

<span data-ttu-id="f1530-758">Questa proprietà viene ereditata da [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-758">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1530-759">Commenti</span><span class="sxs-lookup"><span data-stu-id="f1530-759">Remarks</span></span>

<span data-ttu-id="f1530-760">La classe **Win32 \_ VideoController** è derivata da [**CIM \_ PCVideoController**](cim-pcvideocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="f1530-760">The **Win32\_VideoController** class is derived from [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span>

<span data-ttu-id="f1530-761">Per ulteriori informazioni sull'utilizzo di questa classe, ad esempio il recupero di informazioni da più monitoraggi, vedere [utilizzare PowerShell per individuare informazioni](https://blogs.technet.com/b/heyscriptingguy/archive/2013/10/03/use-powershell-to-discover-multi-monitor-information.aspx)su più monitor.</span><span class="sxs-lookup"><span data-stu-id="f1530-761">For more information about using this class, such as retrieving information from multiple monitors, see [Use PowerShell to Discover Multi-Monitor Information](https://blogs.technet.com/b/heyscriptingguy/archive/2013/10/03/use-powershell-to-discover-multi-monitor-information.aspx).</span></span>

## <a name="examples"></a><span data-ttu-id="f1530-762">Esempio</span><span class="sxs-lookup"><span data-stu-id="f1530-762">Examples</span></span>

<span data-ttu-id="f1530-763">Nell'esempio [elenco di proprietà del controller video](https://Gallery.TechNet.Microsoft.Com/6c1a585c-742f-4f51-bb57-23838e8f011f) sono elencate le proprietà del controller video.</span><span class="sxs-lookup"><span data-stu-id="f1530-763">The [List Video Controller Properties](https://Gallery.TechNet.Microsoft.Com/6c1a585c-742f-4f51-bb57-23838e8f011f) VBScript sample lists the video controller properties.</span></span>

<span data-ttu-id="f1530-764">Nell'esempio di PowerShell seguente sono elencate le proprietà del controller video.</span><span class="sxs-lookup"><span data-stu-id="f1530-764">The following PowerShell example lists the video controller properties.</span></span>


```VB
$strComputer = "." 
 
$colItems = get-wmiobject -class "Win32_VideoController" -namespace "root\CIMV2" ` 
-computername $strComputer 
 
foreach ($objItem in $colItems) { 
      write-host "Accelerator Capabilities: " $objItem.AcceleratorCapabilities 
      write-host "Adapter Compatibility: " $objItem.AdapterCompatibility 
      write-host "Adapter DAC Type: " $objItem.AdapterDACType 
      write-host "Adapter RAM: " $objItem.AdapterRAM 
      write-host "Availability: " $objItem.Availability 
      write-host "Capability Descriptions: " $objItem.CapabilityDescriptions 
      write-host "Caption: " $objItem.Caption 
      write-host "Color Table Entries: " $objItem.ColorTableEntries 
      write-host "Configuration Manager Error Code: " $objItem.ConfigManagerErrorCode 
      write-host "Configuration Manager User Configuration: " $objItem.ConfigManagerUserConfig 
      write-host "Creation Class Name: " $objItem.CreationClassName 
      write-host "Current Bits Per Pixel: " $objItem.CurrentBitsPerPixel 
      write-host "Current Horizontal Resolution: " $objItem.CurrentHorizontalResolution 
      write-host "Current Number Of Colors: " $objItem.CurrentNumberOfColors 
      write-host "Current Number Of Columns: " $objItem.CurrentNumberOfColumns 
      write-host "Current Number Of Rows: " $objItem.CurrentNumberOfRows 
      write-host "Current Refresh Rate: " $objItem.CurrentRefreshRate 
      write-host "Current Scan Mode: " $objItem.CurrentScanMode 
      write-host "Current Vertical Resolution: " $objItem.CurrentVerticalResolution 
      write-host "Description: " $objItem.Description 
      write-host "Device ID: " $objItem.DeviceID 
      write-host "Device Specific Pens: " $objItem.DeviceSpecificPens 
      write-host "Dither Type: " $objItem.DitherType 
      write-host "Driver Date: " $objItem.DriverDate 
      write-host "Driver Version: " $objItem.DriverVersion 
      write-host "Error Cleared: " $objItem.ErrorCleared 
      write-host "Error Description: " $objItem.ErrorDescription 
      write-host "ICM Intent: " $objItem.ICMIntent 
      write-host "ICM Method: " $objItem.ICMMethod 
      write-host "Inf File Name: " $objItem.InfFilename 
      write-host "Inf Section: " $objItem.InfSection 
      write-host "Installation Date: " $objItem.InstallDate 
      write-host "Installed Display Drivers: " $objItem.InstalledDisplayDrivers 
      write-host "Last Error Code: " $objItem.LastErrorCode 
      write-host "Maximum Memory Supported: " $objItem.MaxMemorySupported 
      write-host "Maximum Number Controlled: " $objItem.MaxNumberControlled 
      write-host "Maximum Refresh Rate: " $objItem.MaxRefreshRate 
      write-host "Minimum Refresh Rate: " $objItem.MinRefreshRate 
      write-host "Monochrome: " $objItem.Monochrome 
      write-host "Name: " $objItem.Name 
      write-host "Number Of Color Planes: " $objItem.NumberOfColorPlanes 
      write-host "Number Of Video Pages: " $objItem.NumberOfVideoPages 
      write-host "PNP Device ID: " $objItem.PNPDeviceID 
      write-host "Power Management Capabilities: " $objItem.PowerManagementCapabilities 
      write-host "Power Management Supported: " $objItem.PowerManagementSupported 
      write-host "Protocol Supported: " $objItem.ProtocolSupported 
      write-host "Reserved System Palette Entries: " $objItem.ReservedSystemPaletteEntries 
      write-host "Specification Version: " $objItem.SpecificationVersion 
      write-host "Status: " $objItem.Status 
      write-host "Status Information: " $objItem.StatusInfo 
      write-host "System Creation Class Name: " $objItem.SystemCreationClassName 
      write-host "System Name: " $objItem.SystemName 
      write-host "System Palette Entries: " $objItem.SystemPaletteEntries 
      write-host "Time Of Last Reset: " $objItem.TimeOfLastReset 
      write-host "Video Architecture: " $objItem.VideoArchitecture 
      write-host "Video Memory Type: " $objItem.VideoMemoryType 
      write-host "Video Mode: " $objItem.VideoMode 
      write-host "Video Mode Description: " $objItem.VideoModeDescription 
      write-host "Video Processor: " $objItem.VideoProcessor 
      write-host 
} 
```



## <a name="requirements"></a><span data-ttu-id="f1530-765">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1530-765">Requirements</span></span>



| <span data-ttu-id="f1530-766">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1530-766">Requirement</span></span> | <span data-ttu-id="f1530-767">Valore</span><span class="sxs-lookup"><span data-stu-id="f1530-767">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1530-768">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1530-768">Minimum supported client</span></span><br/> | <span data-ttu-id="f1530-769">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f1530-769">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f1530-770">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1530-770">Minimum supported server</span></span><br/> | <span data-ttu-id="f1530-771">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f1530-771">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f1530-772">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f1530-772">Namespace</span></span><br/>                | <span data-ttu-id="f1530-773">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="f1530-773">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f1530-774">MOF</span><span class="sxs-lookup"><span data-stu-id="f1530-774">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1530-775"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f1530-775"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1530-776">DLL</span><span class="sxs-lookup"><span data-stu-id="f1530-776">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1530-777"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1530-777"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1530-778">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1530-778">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1530-779">**\_PCVIDEOCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="f1530-779">**CIM\_PCVideoController**</span></span>](cim-pcvideocontroller.md)
</dt> <dt>

[<span data-ttu-id="f1530-780">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="f1530-780">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 

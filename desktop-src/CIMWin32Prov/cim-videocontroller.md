---
description: La \_ classe CIM VideoController rappresenta le funzionalità e la gestione del controller video.
ms.assetid: 7cf6bf2a-62a5-46fa-8c8f-976604360461
ms.tgt_platform: multiple
title: Classe CIM_VideoController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoController
- CIM_VideoController.AcceleratorCapabilities
- CIM_VideoController.Availability
- CIM_VideoController.CapabilityDescriptions
- CIM_VideoController.Caption
- CIM_VideoController.ConfigManagerErrorCode
- CIM_VideoController.ConfigManagerUserConfig
- CIM_VideoController.CreationClassName
- CIM_VideoController.CurrentBitsPerPixel
- CIM_VideoController.CurrentHorizontalResolution
- CIM_VideoController.CurrentNumberOfColors
- CIM_VideoController.CurrentNumberOfColumns
- CIM_VideoController.CurrentNumberOfRows
- CIM_VideoController.CurrentRefreshRate
- CIM_VideoController.CurrentScanMode
- CIM_VideoController.CurrentVerticalResolution
- CIM_VideoController.Description
- CIM_VideoController.DeviceID
- CIM_VideoController.ErrorCleared
- CIM_VideoController.ErrorDescription
- CIM_VideoController.InstallDate
- CIM_VideoController.LastErrorCode
- CIM_VideoController.MaxMemorySupported
- CIM_VideoController.MaxNumberControlled
- CIM_VideoController.MaxRefreshRate
- CIM_VideoController.MinRefreshRate
- CIM_VideoController.Name
- CIM_VideoController.NumberOfVideoPages
- CIM_VideoController.PNPDeviceID
- CIM_VideoController.PowerManagementCapabilities
- CIM_VideoController.PowerManagementSupported
- CIM_VideoController.ProtocolSupported
- CIM_VideoController.Status
- CIM_VideoController.StatusInfo
- CIM_VideoController.SystemCreationClassName
- CIM_VideoController.SystemName
- CIM_VideoController.TimeOfLastReset
- CIM_VideoController.VideoMemoryType
- CIM_VideoController.VideoProcessor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6475c99e7a6f2ee1bef56bf2c266c788efc0b805
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878173"
---
# <a name="cim_videocontroller-class"></a><span data-ttu-id="9ccee-103">CIM \_ VideoController (classe)</span><span class="sxs-lookup"><span data-stu-id="9ccee-103">CIM\_VideoController class</span></span>

<span data-ttu-id="9ccee-104">La classe **CIM \_ VideoController** rappresenta le funzionalità e la gestione del controller video.</span><span class="sxs-lookup"><span data-stu-id="9ccee-104">The **CIM\_VideoController** class represents the capabilities and management of the video controller.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9ccee-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="9ccee-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9ccee-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9ccee-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9ccee-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="9ccee-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="9ccee-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="9ccee-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ccee-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9ccee-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCE5-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_VideoController : CIM_Controller
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
  uint16   VideoMemoryType;
  string   VideoProcessor;
};
```

## <a name="members"></a><span data-ttu-id="9ccee-110">Members</span><span class="sxs-lookup"><span data-stu-id="9ccee-110">Members</span></span>

<span data-ttu-id="9ccee-111">La classe **CIM \_ VideoController** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9ccee-111">The **CIM\_VideoController** class has these types of members:</span></span>

-   [<span data-ttu-id="9ccee-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="9ccee-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="9ccee-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9ccee-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9ccee-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="9ccee-114">Methods</span></span>

<span data-ttu-id="9ccee-115">La classe **CIM \_ VideoController** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="9ccee-115">The **CIM\_VideoController** class has these methods.</span></span>



| <span data-ttu-id="9ccee-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="9ccee-116">Method</span></span>                                                                     | <span data-ttu-id="9ccee-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9ccee-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9ccee-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="9ccee-118">**Reset**</span></span>](reset-method-in-class-cim-videocontroller.md)                 | <span data-ttu-id="9ccee-119">Richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="9ccee-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="9ccee-120">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="9ccee-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="9ccee-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="9ccee-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-videocontroller.md) | <span data-ttu-id="9ccee-122">Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="9ccee-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="9ccee-123">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="9ccee-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9ccee-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9ccee-124">Properties</span></span>

<span data-ttu-id="9ccee-125">La classe **CIM \_ VideoController** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9ccee-125">The **CIM\_VideoController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9ccee-126">**AcceleratorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="9ccee-126">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccee-127">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9ccee-127">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ccee-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-129">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VideoController**.**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="9ccee-129">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoController**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="9ccee-130">Grafica e funzionalità 3D del controller video.</span><span class="sxs-lookup"><span data-stu-id="9ccee-130">Graphics and 3-D capabilities of the video controller.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9ccee-131">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="9ccee-131">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9ccee-132">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="9ccee-132">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>

<span data-ttu-id="9ccee-133">**Acceleratore grafico** (2)</span><span class="sxs-lookup"><span data-stu-id="9ccee-133">**Graphics Accelerator** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>

<span data-ttu-id="9ccee-134">**acceleratore 3D** (3)</span><span class="sxs-lookup"><span data-stu-id="9ccee-134">**3D Accelerator** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9ccee-135">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="9ccee-135">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccee-136">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9ccee-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ccee-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-138">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="9ccee-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="9ccee-139">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9ccee-139">Availability and status of the device.</span></span>

<span data-ttu-id="9ccee-140">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ccee-140">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9ccee-141"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="9ccee-141"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9ccee-142"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="9ccee-142"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="9ccee-143"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="9ccee-143"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="9ccee-144"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="9ccee-144"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="9ccee-145"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="9ccee-145"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="9ccee-146"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="9ccee-146"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="9ccee-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="9ccee-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="9ccee-148"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="9ccee-148"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="9ccee-149"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="9ccee-149"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9ccee-150"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="9ccee-150"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="9ccee-151"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="9ccee-151"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="9ccee-152"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="9ccee-152"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="9ccee-153"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="9ccee-153"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-154">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="9ccee-154">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="9ccee-155"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="9ccee-155"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-156">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="9ccee-156">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="9ccee-157"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="9ccee-157"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-158">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="9ccee-158">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="9ccee-159"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="9ccee-159"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="9ccee-160"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="9ccee-160"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-161">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="9ccee-161">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="9ccee-162"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="9ccee-162"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-163">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="9ccee-163">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="9ccee-164"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="9ccee-164"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-165">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="9ccee-165">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="9ccee-166"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="9ccee-166"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-167">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="9ccee-167">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="9ccee-168"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="9ccee-168"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-169">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="9ccee-169">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9ccee-170">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="9ccee-170">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccee-171">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="9ccee-171">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ccee-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-173">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VideoController**.**AcceleratorCapabilities**")</span><span class="sxs-lookup"><span data-stu-id="9ccee-173">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoController**.**AcceleratorCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="9ccee-174">Stringhe in formato libero che forniscono descrizioni dettagliate per le funzionalità di accelerazione video indicate nella matrice **AcceleratorCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="9ccee-174">Free-form strings that provide detailed descriptions for the video accelerator features indicated in the **AcceleratorCapabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="9ccee-175">Ogni voce di questa matrice è correlata alla voce nella matrice **AcceleratorCapabilities** che si trova nello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="9ccee-175">Each entry of this array is related to the entry in the **AcceleratorCapabilities** array that is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="9ccee-176">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="9ccee-176">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccee-177">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9ccee-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ccee-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-179">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="9ccee-179">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="9ccee-180">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9ccee-180">Short textual description of the object.</span></span>

<span data-ttu-id="9ccee-181">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9ccee-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ccee-182">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="9ccee-182">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccee-183">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ccee-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ccee-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-185">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9ccee-185">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9ccee-186">Codice di errore di Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="9ccee-186">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="9ccee-187">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ccee-187">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="9ccee-188"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="9ccee-188"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="9ccee-189"> (0)</span><span class="sxs-lookup"><span data-stu-id="9ccee-189">(0)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-190">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="9ccee-190">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="9ccee-191"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="9ccee-191"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="9ccee-192">(1)</span><span class="sxs-lookup"><span data-stu-id="9ccee-192">(1)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-193">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="9ccee-193">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9ccee-194"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9ccee-194"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="9ccee-195">(2)</span><span class="sxs-lookup"><span data-stu-id="9ccee-195">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="9ccee-196"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="9ccee-196"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="9ccee-197">(3)</span><span class="sxs-lookup"><span data-stu-id="9ccee-197">(3)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-198">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="9ccee-198">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="9ccee-199"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="9ccee-199"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="9ccee-200">(4)</span><span class="sxs-lookup"><span data-stu-id="9ccee-200">(4)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-201">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="9ccee-201">Device is not working properly.</span></span> <span data-ttu-id="9ccee-202">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="9ccee-202">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="9ccee-203"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="9ccee-203"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="9ccee-204">(5)</span><span class="sxs-lookup"><span data-stu-id="9ccee-204">(5)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-205">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="9ccee-205">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="9ccee-206"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="9ccee-206"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="9ccee-207"> (6)</span><span class="sxs-lookup"><span data-stu-id="9ccee-207">(6)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-208">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="9ccee-208">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="9ccee-209"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="9ccee-209"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="9ccee-210">(7)</span><span class="sxs-lookup"><span data-stu-id="9ccee-210">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="9ccee-211"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="9ccee-211"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="9ccee-212">(8)</span><span class="sxs-lookup"><span data-stu-id="9ccee-212">(8)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-213">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="9ccee-213">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="9ccee-214"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="9ccee-214"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="9ccee-215">(9)</span><span class="sxs-lookup"><span data-stu-id="9ccee-215">(9)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-216">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="9ccee-216">Device is not working properly.</span></span> <span data-ttu-id="9ccee-217">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9ccee-217">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="9ccee-218"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9ccee-218"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="9ccee-219">(10)</span><span class="sxs-lookup"><span data-stu-id="9ccee-219">(10)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-220">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9ccee-220">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="9ccee-221"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9ccee-221"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="9ccee-222">(11)</span><span class="sxs-lookup"><span data-stu-id="9ccee-222">(11)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-223">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9ccee-223">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="9ccee-224"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="9ccee-224"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="9ccee-225">12</span><span class="sxs-lookup"><span data-stu-id="9ccee-225">(12)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-226">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="9ccee-226">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="9ccee-227"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9ccee-227"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="9ccee-228">(13)</span><span class="sxs-lookup"><span data-stu-id="9ccee-228">(13)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-229">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9ccee-229">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="9ccee-230"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="9ccee-230"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="9ccee-231">(14)</span><span class="sxs-lookup"><span data-stu-id="9ccee-231">(14)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-232">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="9ccee-232">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="9ccee-233"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="9ccee-233"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="9ccee-234">(15)</span><span class="sxs-lookup"><span data-stu-id="9ccee-234">(15)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-235">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="9ccee-235">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="9ccee-236"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9ccee-236"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="9ccee-237">(16)</span><span class="sxs-lookup"><span data-stu-id="9ccee-237">(16)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-238">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9ccee-238">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="9ccee-239"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="9ccee-239"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="9ccee-240">(17)</span><span class="sxs-lookup"><span data-stu-id="9ccee-240">(17)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-241">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="9ccee-241">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9ccee-242"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9ccee-242"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="9ccee-243">(18)</span><span class="sxs-lookup"><span data-stu-id="9ccee-243">(18)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-244">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9ccee-244">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="9ccee-245"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="9ccee-245"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="9ccee-246">(19)</span><span class="sxs-lookup"><span data-stu-id="9ccee-246">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="9ccee-247"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="9ccee-247"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="9ccee-248">(20)</span><span class="sxs-lookup"><span data-stu-id="9ccee-248">(20)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-249">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="9ccee-249">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="9ccee-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9ccee-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="9ccee-251">(21)</span><span class="sxs-lookup"><span data-stu-id="9ccee-251">(21)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-252">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="9ccee-252">System failure.</span></span> <span data-ttu-id="9ccee-253">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="9ccee-253">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="9ccee-254">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9ccee-254">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="9ccee-255"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="9ccee-255"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="9ccee-256">(22)</span><span class="sxs-lookup"><span data-stu-id="9ccee-256">(22)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-257">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="9ccee-257">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="9ccee-258"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="9ccee-258"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="9ccee-259">(23)</span><span class="sxs-lookup"><span data-stu-id="9ccee-259">(23)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-260">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="9ccee-260">System failure.</span></span> <span data-ttu-id="9ccee-261">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="9ccee-261">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="9ccee-262"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="9ccee-262"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="9ccee-263">(24)</span><span class="sxs-lookup"><span data-stu-id="9ccee-263">(24)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-264">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="9ccee-264">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="9ccee-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9ccee-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="9ccee-266">(25)</span><span class="sxs-lookup"><span data-stu-id="9ccee-266">(25)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-267">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9ccee-267">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="9ccee-268"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9ccee-268"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="9ccee-269">(26)</span><span class="sxs-lookup"><span data-stu-id="9ccee-269">(26)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-270">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9ccee-270">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="9ccee-271"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="9ccee-271"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="9ccee-272">(27)</span><span class="sxs-lookup"><span data-stu-id="9ccee-272">(27)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-273">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="9ccee-273">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="9ccee-274"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="9ccee-274"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="9ccee-275">(28)</span><span class="sxs-lookup"><span data-stu-id="9ccee-275">(28)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-276">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="9ccee-276">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="9ccee-277"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="9ccee-277"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="9ccee-278">(29)</span><span class="sxs-lookup"><span data-stu-id="9ccee-278">(29)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-279">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="9ccee-279">Device is disabled.</span></span> <span data-ttu-id="9ccee-280">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="9ccee-280">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="9ccee-281"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9ccee-281"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="9ccee-282">(30)</span><span class="sxs-lookup"><span data-stu-id="9ccee-282">(30)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-283">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9ccee-283">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9ccee-284"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9ccee-284"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="9ccee-285">31</span><span class="sxs-lookup"><span data-stu-id="9ccee-285">(31)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-286">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="9ccee-286">Device is not working properly.</span></span> <span data-ttu-id="9ccee-287">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="9ccee-287">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9ccee-288">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="9ccee-288">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccee-289">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="9ccee-289">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-290">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ccee-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-291">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9ccee-291">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9ccee-292">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="9ccee-292">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="9ccee-293">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ccee-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ccee-294">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9ccee-294">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccee-295">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9ccee-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-296">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ccee-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-297">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9ccee-297">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9ccee-298">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="9ccee-298">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="9ccee-299">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="9ccee-299">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="9ccee-300">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ccee-300">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ccee-301">**CurrentBitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="9ccee-301">**CurrentBitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccee-302">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ccee-302">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-303">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ccee-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-304">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video \| 003,12 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="9ccee-304">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="9ccee-305">Numero di bit utilizzati per visualizzare ogni pixel.</span><span class="sxs-lookup"><span data-stu-id="9ccee-305">Number of bits used to display each pixel.</span></span>

</dd> <dt>

<span data-ttu-id="9ccee-306">**CurrentHorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="9ccee-306">**CurrentHorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccee-307">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ccee-307">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-308">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ccee-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-309">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video \| 003,11 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" pixel ")</span><span class="sxs-lookup"><span data-stu-id="9ccee-309">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="9ccee-310">Numero corrente di pixel orizzontali.</span><span class="sxs-lookup"><span data-stu-id="9ccee-310">Current number of horizontal pixels.</span></span>

</dd> <dt>

<span data-ttu-id="9ccee-311">**CurrentNumberOfColors**</span><span class="sxs-lookup"><span data-stu-id="9ccee-311">**CurrentNumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccee-312">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9ccee-312">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-313">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ccee-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ccee-314">Numero di colori supportati nella risoluzione corrente.</span><span class="sxs-lookup"><span data-stu-id="9ccee-314">Number of colors supported at the current resolution.</span></span>

<span data-ttu-id="9ccee-315">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9ccee-315">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="9ccee-316">**CurrentNumberOfColumns**</span><span class="sxs-lookup"><span data-stu-id="9ccee-316">**CurrentNumberOfColumns**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccee-317">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ccee-317">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-318">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ccee-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-319">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Video di DMTF \| \| 003,14 ")</span><span class="sxs-lookup"><span data-stu-id="9ccee-319">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.14")</span></span>
</dt> </dl>

<span data-ttu-id="9ccee-320">Se è in modalità carattere, numero di colonne per il controller video; in caso contrario, immettere 0.</span><span class="sxs-lookup"><span data-stu-id="9ccee-320">If in character mode, number of columns for the video controller; otherwise, enter 0.</span></span>

</dd> <dt>

<span data-ttu-id="9ccee-321">**CurrentNumberOfRows**</span><span class="sxs-lookup"><span data-stu-id="9ccee-321">**CurrentNumberOfRows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccee-322">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ccee-322">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-323">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ccee-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-324">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Video di DMTF \| \| 003,13 ")</span><span class="sxs-lookup"><span data-stu-id="9ccee-324">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.13")</span></span>
</dt> </dl>

<span data-ttu-id="9ccee-325">Se è in modalità carattere, numero di righe per il controller video; in caso contrario, immettere 0.</span><span class="sxs-lookup"><span data-stu-id="9ccee-325">If in character mode, number of rows for the video controller; otherwise, enter 0.</span></span>

</dd> <dt>

<span data-ttu-id="9ccee-326">**CurrentRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="9ccee-326">**CurrentRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccee-327">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ccee-327">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-328">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ccee-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-329">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video \| 003,15 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="9ccee-329">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="9ccee-330">Frequenza di aggiornamento corrente, in Hertz.</span><span class="sxs-lookup"><span data-stu-id="9ccee-330">Current refresh rate, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="9ccee-331">**CurrentScanMode**</span><span class="sxs-lookup"><span data-stu-id="9ccee-331">**CurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccee-332">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9ccee-332">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-333">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ccee-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-334">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Video di DMTF \| \| 003,8 ")</span><span class="sxs-lookup"><span data-stu-id="9ccee-334">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.8")</span></span>
</dt> </dl>

<span data-ttu-id="9ccee-335">Modalità di analisi corrente.</span><span class="sxs-lookup"><span data-stu-id="9ccee-335">Current scan mode.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9ccee-336">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="9ccee-336">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9ccee-337">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="9ccee-337">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>

<span data-ttu-id="9ccee-338">**Interlacciato** (3)</span><span class="sxs-lookup"><span data-stu-id="9ccee-338">**Interlaced** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>

<span data-ttu-id="9ccee-339">**Non interlacciato** (4)</span><span class="sxs-lookup"><span data-stu-id="9ccee-339">**Non Interlaced** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9ccee-340">**CurrentVerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="9ccee-340">**CurrentVerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccee-341">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ccee-341">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-342">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ccee-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-343">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video \| 003,10 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" pixel ")</span><span class="sxs-lookup"><span data-stu-id="9ccee-343">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="9ccee-344">Numero corrente di pixel verticali.</span><span class="sxs-lookup"><span data-stu-id="9ccee-344">Current number of vertical pixels.</span></span>

</dd> <dt>

<span data-ttu-id="9ccee-345">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="9ccee-345">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccee-346">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9ccee-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-347">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ccee-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-348">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="9ccee-348">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="9ccee-349">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9ccee-349">Textual description of the object.</span></span>

<span data-ttu-id="9ccee-350">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9ccee-350">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ccee-351">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="9ccee-351">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccee-352">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9ccee-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-353">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ccee-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-354">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9ccee-354">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9ccee-355">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="9ccee-355">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="9ccee-356">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ccee-356">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ccee-357">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="9ccee-357">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccee-358">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="9ccee-358">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-359">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ccee-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ccee-360">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="9ccee-360">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="9ccee-361">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ccee-361">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ccee-362">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="9ccee-362">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccee-363">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9ccee-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-364">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ccee-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ccee-365">Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.</span><span class="sxs-lookup"><span data-stu-id="9ccee-365">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="9ccee-366">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ccee-366">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ccee-367">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9ccee-367">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccee-368">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9ccee-368">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-369">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ccee-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-370">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="9ccee-370">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="9ccee-371">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9ccee-371">Date and time the object was installed.</span></span> <span data-ttu-id="9ccee-372">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="9ccee-372">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="9ccee-373">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9ccee-373">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ccee-374">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="9ccee-374">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccee-375">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ccee-375">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-376">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ccee-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ccee-377">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="9ccee-377">Last error code reported by the logical device.</span></span>

<span data-ttu-id="9ccee-378">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ccee-378">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ccee-379">**MaxMemorySupported**</span><span class="sxs-lookup"><span data-stu-id="9ccee-379">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccee-380">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ccee-380">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-381">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ccee-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-382">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="9ccee-382">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="9ccee-383">Quantità massima di memoria supportata, in byte.</span><span class="sxs-lookup"><span data-stu-id="9ccee-383">Maximum amount of memory supported, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="9ccee-384">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="9ccee-384">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccee-385">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ccee-385">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-386">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ccee-386">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-387">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta bus DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="9ccee-387">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="9ccee-388">Numero massimo di entità indirizzabili direttamente supportate dal controller.</span><span class="sxs-lookup"><span data-stu-id="9ccee-388">Maximum number of directly addressable entities supported by the controller.</span></span> <span data-ttu-id="9ccee-389">Se il numero è sconosciuto o illimitato, è necessario utilizzare il valore 0.</span><span class="sxs-lookup"><span data-stu-id="9ccee-389">A value of 0 should be used if the number is unknown or unlimited.</span></span>

<span data-ttu-id="9ccee-390">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="9ccee-390">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ccee-391">**MaxRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="9ccee-391">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccee-392">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ccee-392">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-393">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ccee-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-394">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video \| 003,5 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="9ccee-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="9ccee-395">Frequenza di aggiornamento massima del controller video, in Hertz.</span><span class="sxs-lookup"><span data-stu-id="9ccee-395">Maximum refresh rate of the video controller, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="9ccee-396">**MinRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="9ccee-396">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccee-397">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ccee-397">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-398">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ccee-398">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-399">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video \| 003,4 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="9ccee-399">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="9ccee-400">Frequenza di aggiornamento minima del controller video, in Hertz.</span><span class="sxs-lookup"><span data-stu-id="9ccee-400">Minimum refresh rate of the video controller, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="9ccee-401">**Nome**</span><span class="sxs-lookup"><span data-stu-id="9ccee-401">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccee-402">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9ccee-402">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-403">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ccee-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-404">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="9ccee-404">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="9ccee-405">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="9ccee-405">Label by which the object is known.</span></span> <span data-ttu-id="9ccee-406">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="9ccee-406">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="9ccee-407">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9ccee-407">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ccee-408">**NumberOfVideoPages**</span><span class="sxs-lookup"><span data-stu-id="9ccee-408">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccee-409">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ccee-409">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-410">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ccee-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ccee-411">Numero di pagine video supportate in base alle risoluzioni correnti e alla memoria disponibile.</span><span class="sxs-lookup"><span data-stu-id="9ccee-411">Number of video pages supported given the current resolutions and available memory.</span></span>

</dd> <dt>

<span data-ttu-id="9ccee-412">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="9ccee-412">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccee-413">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9ccee-413">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-414">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ccee-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-415">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9ccee-415">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9ccee-416">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="9ccee-416">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="9ccee-417">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ccee-417">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="9ccee-418">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="9ccee-418">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="9ccee-419">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="9ccee-419">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccee-420">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9ccee-420">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-421">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ccee-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ccee-422">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="9ccee-422">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="9ccee-423">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="9ccee-423">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9ccee-424"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="9ccee-424"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="9ccee-425"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="9ccee-425"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9ccee-426"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="9ccee-426"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9ccee-427"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="9ccee-427"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-428">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="9ccee-428">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="9ccee-429"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="9ccee-429"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-430">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="9ccee-430">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="9ccee-431"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="9ccee-431"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-432">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="9ccee-432">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="9ccee-433">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="9ccee-433">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="9ccee-434">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="9ccee-434">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="9ccee-435"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="9ccee-435"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-436">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="9ccee-436">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="9ccee-437"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="9ccee-437"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="9ccee-438">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="9ccee-438">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9ccee-439">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="9ccee-439">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccee-440">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="9ccee-440">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-441">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ccee-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ccee-442">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="9ccee-442">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="9ccee-443">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="9ccee-443">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="9ccee-444">Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="9ccee-444">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="9ccee-445">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="9ccee-445">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="9ccee-446">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ccee-446">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ccee-447">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="9ccee-447">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccee-448">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9ccee-448">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-449">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ccee-449">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-450">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta bus DMTF \| 001,2 "," MIF. \|Dischi DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="9ccee-450">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="9ccee-451">Protocollo usato dal controller per accedere ai dispositivi "controllati".</span><span class="sxs-lookup"><span data-stu-id="9ccee-451">Protocol used by the controller to access 'controlled' devices.</span></span>

<span data-ttu-id="9ccee-452">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="9ccee-452">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="9ccee-453">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="9ccee-453">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9ccee-454">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="9ccee-454">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9ccee-455">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="9ccee-455">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="9ccee-456">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="9ccee-456">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="9ccee-457">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="9ccee-457">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="9ccee-458">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="9ccee-458">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="9ccee-459">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="9ccee-459">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="9ccee-460">**Dischetto flessibile** (7)</span><span class="sxs-lookup"><span data-stu-id="9ccee-460">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="9ccee-461">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="9ccee-461">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="9ccee-462">**Interfaccia parallela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="9ccee-462">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="9ccee-463">**Protocollo di Fibre Channel SCSI** (10)</span><span class="sxs-lookup"><span data-stu-id="9ccee-463">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="9ccee-464">**Protocollo bus seriale SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="9ccee-464">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="9ccee-465">**Protocollo bus seriale SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="9ccee-465">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="9ccee-466">**Architettura di archiviazione seriale SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="9ccee-466">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="9ccee-467">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="9ccee-467">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="9ccee-468">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="9ccee-468">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="9ccee-469">**Bus seriale universale** (16)</span><span class="sxs-lookup"><span data-stu-id="9ccee-469">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="9ccee-470">**Protocollo parallelo** (17)</span><span class="sxs-lookup"><span data-stu-id="9ccee-470">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="9ccee-471">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="9ccee-471">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="9ccee-472">**Diagnostica** (19)</span><span class="sxs-lookup"><span data-stu-id="9ccee-472">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="9ccee-473">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="9ccee-473">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="9ccee-474">**Potenza** (21)</span><span class="sxs-lookup"><span data-stu-id="9ccee-474">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="9ccee-475">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="9ccee-475">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="9ccee-476">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="9ccee-476">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="9ccee-477">**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="9ccee-477">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="9ccee-478">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="9ccee-478">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="9ccee-479">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="9ccee-479">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="9ccee-480">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="9ccee-480">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="9ccee-481">**IEEE 802,3 10Base5** (28)</span><span class="sxs-lookup"><span data-stu-id="9ccee-481">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="9ccee-482">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="9ccee-482">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="9ccee-483">**IEEE 802,3 1Base5** (30)</span><span class="sxs-lookup"><span data-stu-id="9ccee-483">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="9ccee-484">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="9ccee-484">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="9ccee-485">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="9ccee-485">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="9ccee-486">**Token-ring IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="9ccee-486">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="9ccee-487">**ANSI X3T 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="9ccee-487">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="9ccee-488">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="9ccee-488">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="9ccee-489">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="9ccee-489">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="9ccee-490">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="9ccee-490">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="9ccee-491">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="9ccee-491">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="9ccee-492">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="9ccee-492">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="9ccee-493">**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="9ccee-493">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="9ccee-494">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="9ccee-494">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="9ccee-495">**ATA/IDE avanzato** (42)</span><span class="sxs-lookup"><span data-stu-id="9ccee-495">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="9ccee-496">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="9ccee-496">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="9ccee-497">**TWIRP (infrarossi bidirezionali)** (44)</span><span class="sxs-lookup"><span data-stu-id="9ccee-497">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="9ccee-498">**FIR (infrarossi veloci)** (45)</span><span class="sxs-lookup"><span data-stu-id="9ccee-498">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="9ccee-499">**Sir (Serial Infrared)** (46)</span><span class="sxs-lookup"><span data-stu-id="9ccee-499">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="9ccee-500">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="9ccee-500">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9ccee-501">**Status**</span><span class="sxs-lookup"><span data-stu-id="9ccee-501">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccee-502">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9ccee-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-503">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ccee-503">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-504">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="9ccee-504">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="9ccee-505">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9ccee-505">Current status of the object.</span></span> <span data-ttu-id="9ccee-506">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9ccee-506">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="9ccee-507">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="9ccee-507">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="9ccee-508">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="9ccee-508">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="9ccee-509">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="9ccee-509">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9ccee-510">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="9ccee-510">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9ccee-511">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="9ccee-511">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="9ccee-512">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="9ccee-512">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="9ccee-513">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="9ccee-513">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="9ccee-514">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="9ccee-514">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9ccee-515">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="9ccee-515">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="9ccee-516">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="9ccee-516">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="9ccee-517">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="9ccee-517">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="9ccee-518">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="9ccee-518">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="9ccee-519">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="9ccee-519">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9ccee-520">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="9ccee-520">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccee-521">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9ccee-521">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-522">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ccee-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-523">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="9ccee-523">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="9ccee-524">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="9ccee-524">State of the logical device.</span></span> <span data-ttu-id="9ccee-525">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="9ccee-525">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="9ccee-526">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ccee-526">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9ccee-527">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="9ccee-527">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9ccee-528">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="9ccee-528">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9ccee-529">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="9ccee-529">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9ccee-530">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="9ccee-530">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="9ccee-531">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="9ccee-531">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9ccee-532">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9ccee-532">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccee-533">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9ccee-533">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-534">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ccee-534">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-535">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9ccee-535">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9ccee-536">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="9ccee-536">Scoping system's creation class name.</span></span>

<span data-ttu-id="9ccee-537">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ccee-537">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ccee-538">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="9ccee-538">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccee-539">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9ccee-539">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-540">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ccee-540">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-541">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9ccee-541">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9ccee-542">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="9ccee-542">Scoping system's name.</span></span>

<span data-ttu-id="9ccee-543">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ccee-543">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ccee-544">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="9ccee-544">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccee-545">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9ccee-545">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-546">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ccee-546">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ccee-547">Data e ora dell'ultima reimpostazione del controller, ovvero il controller è stato spento o reinizializzato.</span><span class="sxs-lookup"><span data-stu-id="9ccee-547">Date and time the controller was last reset, meaning the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="9ccee-548">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="9ccee-548">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ccee-549">**VideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="9ccee-549">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccee-550">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9ccee-550">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-551">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ccee-551">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-552">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Video di DMTF \| \| 003,6 ")</span><span class="sxs-lookup"><span data-stu-id="9ccee-552">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.6")</span></span>
</dt> </dl>

<span data-ttu-id="9ccee-553">Tipo di memoria video.</span><span class="sxs-lookup"><span data-stu-id="9ccee-553">Type of video memory.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9ccee-554">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="9ccee-554">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9ccee-555">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="9ccee-555">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="9ccee-556">**VRAM** (3)</span><span class="sxs-lookup"><span data-stu-id="9ccee-556">**VRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="9ccee-557">**DRAM** (4)</span><span class="sxs-lookup"><span data-stu-id="9ccee-557">**DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="9ccee-558">**SRAM** (5)</span><span class="sxs-lookup"><span data-stu-id="9ccee-558">**SRAM** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WRAM"></span><span id="wram"></span>

<span data-ttu-id="9ccee-559">**WRAM** (6)</span><span class="sxs-lookup"><span data-stu-id="9ccee-559">**WRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO_RAM"></span><span id="edo_ram"></span>

<span data-ttu-id="9ccee-560">**RAM EDO** (7)</span><span class="sxs-lookup"><span data-stu-id="9ccee-560">**EDO RAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst_Synchronous_DRAM"></span><span id="burst_synchronous_dram"></span><span id="BURST_SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="9ccee-561">**DRAM sincrona a impulsi** (8)</span><span class="sxs-lookup"><span data-stu-id="9ccee-561">**Burst Synchronous DRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipelined_Burst_SRAM"></span><span id="pipelined_burst_sram"></span><span id="PIPELINED_BURST_SRAM"></span>

<span data-ttu-id="9ccee-562">**SRAM di impulso in pipeline** (9)</span><span class="sxs-lookup"><span data-stu-id="9ccee-562">**Pipelined Burst SRAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="9ccee-563">**CDRAM** (10)</span><span class="sxs-lookup"><span data-stu-id="9ccee-563">**CDRAM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="9ccee-564">**3DRAM** (11)</span><span class="sxs-lookup"><span data-stu-id="9ccee-564">**3DRAM** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="9ccee-565">**SDRAM** (12)</span><span class="sxs-lookup"><span data-stu-id="9ccee-565">**SDRAM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="9ccee-566">**SGRAM** (13)</span><span class="sxs-lookup"><span data-stu-id="9ccee-566">**SGRAM** (13)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9ccee-567">**VideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="9ccee-567">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccee-568">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9ccee-568">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ccee-569">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ccee-569">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ccee-570">Stringa in formato libero che descrive il processore video o il controller.</span><span class="sxs-lookup"><span data-stu-id="9ccee-570">Free-form string that describes the video processor or controller.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9ccee-571">Commenti</span><span class="sxs-lookup"><span data-stu-id="9ccee-571">Remarks</span></span>

<span data-ttu-id="9ccee-572">La classe **CIM \_ VideoController** è derivata dal [**\_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="9ccee-572">The **CIM\_VideoController** class is derived from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="9ccee-573">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="9ccee-573">WMI does not implement this class.</span></span> <span data-ttu-id="9ccee-574">Per le classi WMI derivate da **CIM \_ VideoController**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9ccee-574">For WMI classes derived from **CIM\_VideoController**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="9ccee-575">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="9ccee-575">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9ccee-576">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="9ccee-576">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ccee-577">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ccee-577">Requirements</span></span>



| <span data-ttu-id="9ccee-578">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ccee-578">Requirement</span></span> | <span data-ttu-id="9ccee-579">Valore</span><span class="sxs-lookup"><span data-stu-id="9ccee-579">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ccee-580">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ccee-580">Minimum supported client</span></span><br/> | <span data-ttu-id="9ccee-581">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9ccee-581">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9ccee-582">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ccee-582">Minimum supported server</span></span><br/> | <span data-ttu-id="9ccee-583">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9ccee-583">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9ccee-584">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9ccee-584">Namespace</span></span><br/>                | <span data-ttu-id="9ccee-585">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="9ccee-585">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9ccee-586">MOF</span><span class="sxs-lookup"><span data-stu-id="9ccee-586">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ccee-587"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9ccee-587"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9ccee-588">DLL</span><span class="sxs-lookup"><span data-stu-id="9ccee-588">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ccee-589"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ccee-589"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ccee-590">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9ccee-590">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ccee-591">**\_Controller CIM**</span><span class="sxs-lookup"><span data-stu-id="9ccee-591">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 


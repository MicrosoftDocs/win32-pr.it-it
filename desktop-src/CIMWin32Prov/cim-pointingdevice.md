---
description: La \_ classe CIM PointingDevice rappresenta un dispositivo che punta alle aree sullo schermo. Qualsiasi dispositivo che manipola un puntatore o punta a aree in una visualizzazione visiva è un membro di questa classe. Ad esempio mouse, stilo, touch pad o tablet.
ms.assetid: b093134a-534a-4680-8fce-d96baff26139
ms.tgt_platform: multiple
title: Classe CIM_PointingDevice (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PointingDevice
- CIM_PointingDevice.Availability
- CIM_PointingDevice.Caption
- CIM_PointingDevice.ConfigManagerErrorCode
- CIM_PointingDevice.ConfigManagerUserConfig
- CIM_PointingDevice.CreationClassName
- CIM_PointingDevice.Description
- CIM_PointingDevice.DeviceID
- CIM_PointingDevice.ErrorCleared
- CIM_PointingDevice.ErrorDescription
- CIM_PointingDevice.Handedness
- CIM_PointingDevice.InstallDate
- CIM_PointingDevice.IsLocked
- CIM_PointingDevice.LastErrorCode
- CIM_PointingDevice.Name
- CIM_PointingDevice.NumberOfButtons
- CIM_PointingDevice.PNPDeviceID
- CIM_PointingDevice.PointingType
- CIM_PointingDevice.PowerManagementCapabilities
- CIM_PointingDevice.PowerManagementSupported
- CIM_PointingDevice.Resolution
- CIM_PointingDevice.Status
- CIM_PointingDevice.StatusInfo
- CIM_PointingDevice.SystemCreationClassName
- CIM_PointingDevice.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3f0a52ac11d927f5cabf171f49fee3a5febaa6a2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225746"
---
# <a name="cim_pointingdevice-class-cimwin32-wmi-providers"></a><span data-ttu-id="2f57e-105">Classe CIM_PointingDevice (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="2f57e-105">CIM_PointingDevice class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="2f57e-106">La classe **CIM \_ PointingDevice** rappresenta un dispositivo che punta alle aree sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="2f57e-106">The **CIM\_PointingDevice** class represents a device that points to regions on the display.</span></span> <span data-ttu-id="2f57e-107">Qualsiasi dispositivo che manipola un puntatore o punta a aree in una visualizzazione visiva è un membro di questa classe.</span><span class="sxs-lookup"><span data-stu-id="2f57e-107">Any device that manipulates a pointer, or points to regions on a visual display, is a member of this class.</span></span> <span data-ttu-id="2f57e-108">Ad esempio mouse, stilo, touch pad o tablet.</span><span class="sxs-lookup"><span data-stu-id="2f57e-108">For example, a mouse, stylus, touch pad, or tablet.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2f57e-109">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="2f57e-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2f57e-110">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2f57e-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2f57e-111">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="2f57e-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="2f57e-112">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="2f57e-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f57e-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2f57e-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C535-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_PointingDevice : CIM_UserDevice
{
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint16   Handedness;
  datetime InstallDate;
  boolean  IsLocked;
  uint32   LastErrorCode;
  string   Name;
  uint8    NumberOfButtons;
  string   PNPDeviceID;
  uint16   PointingType;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   Resolution;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="2f57e-114">Members</span><span class="sxs-lookup"><span data-stu-id="2f57e-114">Members</span></span>

<span data-ttu-id="2f57e-115">La classe **CIM \_ PointingDevice** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2f57e-115">The **CIM\_PointingDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="2f57e-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="2f57e-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="2f57e-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2f57e-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2f57e-118">Metodi</span><span class="sxs-lookup"><span data-stu-id="2f57e-118">Methods</span></span>

<span data-ttu-id="2f57e-119">La classe **CIM \_ PointingDevice** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="2f57e-119">The **CIM\_PointingDevice** class has these methods.</span></span>



| <span data-ttu-id="2f57e-120">Metodo</span><span class="sxs-lookup"><span data-stu-id="2f57e-120">Method</span></span>                                                                    | <span data-ttu-id="2f57e-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f57e-121">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2f57e-122">**Reset**</span><span class="sxs-lookup"><span data-stu-id="2f57e-122">**Reset**</span></span>](reset-method-in-class-cim-pointingdevice.md)                 | <span data-ttu-id="2f57e-123">Richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="2f57e-123">Requests a reset of the logical device.</span></span> <span data-ttu-id="2f57e-124">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="2f57e-124">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="2f57e-125">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="2f57e-125">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-pointingdevice.md) | <span data-ttu-id="2f57e-126">Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="2f57e-126">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="2f57e-127">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="2f57e-127">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2f57e-128">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2f57e-128">Properties</span></span>

<span data-ttu-id="2f57e-129">La classe **CIM \_ PointingDevice** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2f57e-129">The **CIM\_PointingDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2f57e-130">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="2f57e-130">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f57e-131">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2f57e-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2f57e-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-133">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="2f57e-133">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="2f57e-134">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2f57e-134">Availability and status of the device.</span></span>

<span data-ttu-id="2f57e-135">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2f57e-135">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2f57e-136"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="2f57e-136"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2f57e-137"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="2f57e-137"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="2f57e-138"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="2f57e-138"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="2f57e-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="2f57e-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="2f57e-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="2f57e-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2f57e-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="2f57e-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="2f57e-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="2f57e-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="2f57e-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="2f57e-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="2f57e-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="2f57e-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2f57e-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="2f57e-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="2f57e-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="2f57e-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="2f57e-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="2f57e-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="2f57e-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="2f57e-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-149">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="2f57e-149">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="2f57e-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="2f57e-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-151">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="2f57e-151">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="2f57e-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="2f57e-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-153">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="2f57e-153">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="2f57e-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="2f57e-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="2f57e-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="2f57e-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-156">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="2f57e-156">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="2f57e-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="2f57e-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-158">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="2f57e-158">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="2f57e-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="2f57e-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-160">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="2f57e-160">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="2f57e-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="2f57e-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-162">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="2f57e-162">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="2f57e-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="2f57e-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-164">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="2f57e-164">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2f57e-165">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="2f57e-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f57e-166">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2f57e-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2f57e-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-168">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="2f57e-168">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="2f57e-169">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2f57e-169">Short textual description of the object.</span></span>

<span data-ttu-id="2f57e-170">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2f57e-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f57e-171">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="2f57e-171">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f57e-172">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2f57e-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2f57e-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-174">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2f57e-174">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2f57e-175">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="2f57e-175">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="2f57e-176">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2f57e-176">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="2f57e-177"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="2f57e-177"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="2f57e-178"> (0)</span><span class="sxs-lookup"><span data-stu-id="2f57e-178">(0)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-179">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="2f57e-179">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="2f57e-180"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="2f57e-180"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="2f57e-181">(1)</span><span class="sxs-lookup"><span data-stu-id="2f57e-181">(1)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-182">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="2f57e-182">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2f57e-183"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2f57e-183"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="2f57e-184">(2)</span><span class="sxs-lookup"><span data-stu-id="2f57e-184">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="2f57e-185"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="2f57e-185"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="2f57e-186">(3)</span><span class="sxs-lookup"><span data-stu-id="2f57e-186">(3)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-187">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="2f57e-187">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="2f57e-188"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="2f57e-188"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="2f57e-189">(4)</span><span class="sxs-lookup"><span data-stu-id="2f57e-189">(4)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-190">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="2f57e-190">Device is not working properly.</span></span> <span data-ttu-id="2f57e-191">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="2f57e-191">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="2f57e-192"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="2f57e-192"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="2f57e-193">(5)</span><span class="sxs-lookup"><span data-stu-id="2f57e-193">(5)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-194">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="2f57e-194">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="2f57e-195"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="2f57e-195"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="2f57e-196"> (6)</span><span class="sxs-lookup"><span data-stu-id="2f57e-196">(6)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-197">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="2f57e-197">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="2f57e-198"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="2f57e-198"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="2f57e-199">(7)</span><span class="sxs-lookup"><span data-stu-id="2f57e-199">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="2f57e-200"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="2f57e-200"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="2f57e-201">(8)</span><span class="sxs-lookup"><span data-stu-id="2f57e-201">(8)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-202">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="2f57e-202">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="2f57e-203"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="2f57e-203"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="2f57e-204">(9)</span><span class="sxs-lookup"><span data-stu-id="2f57e-204">(9)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-205">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="2f57e-205">Device is not working properly.</span></span> <span data-ttu-id="2f57e-206">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2f57e-206">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="2f57e-207"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2f57e-207"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="2f57e-208">(10)</span><span class="sxs-lookup"><span data-stu-id="2f57e-208">(10)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-209">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2f57e-209">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="2f57e-210"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2f57e-210"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="2f57e-211">(11)</span><span class="sxs-lookup"><span data-stu-id="2f57e-211">(11)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-212">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2f57e-212">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="2f57e-213"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="2f57e-213"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="2f57e-214">12</span><span class="sxs-lookup"><span data-stu-id="2f57e-214">(12)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-215">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="2f57e-215">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="2f57e-216"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2f57e-216"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="2f57e-217">(13)</span><span class="sxs-lookup"><span data-stu-id="2f57e-217">(13)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-218">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2f57e-218">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="2f57e-219"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="2f57e-219"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="2f57e-220">(14)</span><span class="sxs-lookup"><span data-stu-id="2f57e-220">(14)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-221">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="2f57e-221">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="2f57e-222"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="2f57e-222"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="2f57e-223">(15)</span><span class="sxs-lookup"><span data-stu-id="2f57e-223">(15)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-224">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="2f57e-224">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="2f57e-225"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2f57e-225"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="2f57e-226">(16)</span><span class="sxs-lookup"><span data-stu-id="2f57e-226">(16)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-227">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2f57e-227">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="2f57e-228"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="2f57e-228"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="2f57e-229">(17)</span><span class="sxs-lookup"><span data-stu-id="2f57e-229">(17)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-230">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="2f57e-230">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2f57e-231"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2f57e-231"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="2f57e-232">(18)</span><span class="sxs-lookup"><span data-stu-id="2f57e-232">(18)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-233">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2f57e-233">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="2f57e-234"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="2f57e-234"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="2f57e-235">(19)</span><span class="sxs-lookup"><span data-stu-id="2f57e-235">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="2f57e-236"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="2f57e-236"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="2f57e-237">(20)</span><span class="sxs-lookup"><span data-stu-id="2f57e-237">(20)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-238">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="2f57e-238">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="2f57e-239"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2f57e-239"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="2f57e-240">(21)</span><span class="sxs-lookup"><span data-stu-id="2f57e-240">(21)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-241">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="2f57e-241">System failure.</span></span> <span data-ttu-id="2f57e-242">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="2f57e-242">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="2f57e-243">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2f57e-243">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="2f57e-244"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="2f57e-244"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="2f57e-245">(22)</span><span class="sxs-lookup"><span data-stu-id="2f57e-245">(22)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-246">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="2f57e-246">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="2f57e-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="2f57e-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="2f57e-248">(23)</span><span class="sxs-lookup"><span data-stu-id="2f57e-248">(23)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-249">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="2f57e-249">System failure.</span></span> <span data-ttu-id="2f57e-250">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="2f57e-250">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="2f57e-251"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="2f57e-251"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="2f57e-252">(24)</span><span class="sxs-lookup"><span data-stu-id="2f57e-252">(24)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-253">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="2f57e-253">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="2f57e-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2f57e-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="2f57e-255">(25)</span><span class="sxs-lookup"><span data-stu-id="2f57e-255">(25)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-256">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2f57e-256">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="2f57e-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2f57e-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="2f57e-258">(26)</span><span class="sxs-lookup"><span data-stu-id="2f57e-258">(26)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-259">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2f57e-259">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="2f57e-260"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="2f57e-260"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="2f57e-261">(27)</span><span class="sxs-lookup"><span data-stu-id="2f57e-261">(27)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-262">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="2f57e-262">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="2f57e-263"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="2f57e-263"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="2f57e-264">(28)</span><span class="sxs-lookup"><span data-stu-id="2f57e-264">(28)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-265">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="2f57e-265">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="2f57e-266"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="2f57e-266"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="2f57e-267">(29)</span><span class="sxs-lookup"><span data-stu-id="2f57e-267">(29)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-268">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="2f57e-268">Device is disabled.</span></span> <span data-ttu-id="2f57e-269">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="2f57e-269">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="2f57e-270"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2f57e-270"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="2f57e-271">(30)</span><span class="sxs-lookup"><span data-stu-id="2f57e-271">(30)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-272">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2f57e-272">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2f57e-273"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2f57e-273"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="2f57e-274">31</span><span class="sxs-lookup"><span data-stu-id="2f57e-274">(31)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-275">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="2f57e-275">Device is not working properly.</span></span> <span data-ttu-id="2f57e-276">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="2f57e-276">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2f57e-277">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="2f57e-277">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f57e-278">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2f57e-278">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-279">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2f57e-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-280">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2f57e-280">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2f57e-281">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="2f57e-281">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="2f57e-282">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2f57e-282">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f57e-283">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2f57e-283">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f57e-284">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2f57e-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-285">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2f57e-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-286">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2f57e-286">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2f57e-287">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="2f57e-287">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="2f57e-288">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="2f57e-288">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="2f57e-289">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2f57e-289">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f57e-290">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="2f57e-290">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f57e-291">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2f57e-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-292">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2f57e-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-293">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="2f57e-293">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="2f57e-294">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2f57e-294">Textual description of the object.</span></span>

<span data-ttu-id="2f57e-295">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2f57e-295">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f57e-296">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="2f57e-296">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f57e-297">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2f57e-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-298">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2f57e-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-299">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2f57e-299">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2f57e-300">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="2f57e-300">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="2f57e-301">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2f57e-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f57e-302">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="2f57e-302">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f57e-303">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2f57e-303">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-304">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2f57e-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f57e-305">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="2f57e-305">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="2f57e-306">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2f57e-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f57e-307">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="2f57e-307">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f57e-308">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2f57e-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-309">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2f57e-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f57e-310">Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.</span><span class="sxs-lookup"><span data-stu-id="2f57e-310">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="2f57e-311">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2f57e-311">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f57e-312">**Mano**</span><span class="sxs-lookup"><span data-stu-id="2f57e-312">**Handedness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f57e-313">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2f57e-313">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-314">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2f57e-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f57e-315">Configurazione del dispositivo di puntamento per l'operazione a destra o a sinistra.</span><span class="sxs-lookup"><span data-stu-id="2f57e-315">Configuration of the pointing device for right-hand or left-hand operation.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2f57e-316"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="2f57e-316"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2f57e-317"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (1)</span><span class="sxs-lookup"><span data-stu-id="2f57e-317"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>

<span data-ttu-id="2f57e-318"><span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>**Operazione gestita a destra** (2)</span><span class="sxs-lookup"><span data-stu-id="2f57e-318"><span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>**Right Handed Operation** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-319">Operazione a destra</span><span class="sxs-lookup"><span data-stu-id="2f57e-319">Right-hand operation</span></span>

</dd> <dt>

<span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>

<span data-ttu-id="2f57e-320"><span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>**Operazione a sinistra** (3)</span><span class="sxs-lookup"><span data-stu-id="2f57e-320"><span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>**Left Handed Operation** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-321">Operazione a sinistra</span><span class="sxs-lookup"><span data-stu-id="2f57e-321">Left-hand operation</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2f57e-322">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2f57e-322">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f57e-323">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2f57e-323">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-324">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2f57e-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-325">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="2f57e-325">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="2f57e-326">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2f57e-326">Date and time the object was installed.</span></span> <span data-ttu-id="2f57e-327">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="2f57e-327">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="2f57e-328">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2f57e-328">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f57e-329">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="2f57e-329">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f57e-330">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2f57e-330">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-331">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2f57e-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f57e-332">Se **true**, il dispositivo è bloccato impedendo l'input o l'output dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2f57e-332">If **TRUE**, the device is locked, preventing user input or output.</span></span>

<span data-ttu-id="2f57e-333">Questa proprietà viene ereditata da [**CIM \_ UserDevice**](cim-userdevice.md).</span><span class="sxs-lookup"><span data-stu-id="2f57e-333">This property is inherited from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f57e-334">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="2f57e-334">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f57e-335">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2f57e-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-336">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2f57e-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f57e-337">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="2f57e-337">Last error code reported by the logical device.</span></span>

<span data-ttu-id="2f57e-338">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2f57e-338">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f57e-339">**Nome**</span><span class="sxs-lookup"><span data-stu-id="2f57e-339">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f57e-340">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2f57e-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-341">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2f57e-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-342">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="2f57e-342">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="2f57e-343">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="2f57e-343">Label by which the object is known.</span></span> <span data-ttu-id="2f57e-344">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="2f57e-344">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="2f57e-345">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2f57e-345">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f57e-346">**NumberOfButtons**</span><span class="sxs-lookup"><span data-stu-id="2f57e-346">**NumberOfButtons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f57e-347">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="2f57e-347">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-348">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2f57e-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f57e-349">Numero di pulsanti sul dispositivo di puntamento.</span><span class="sxs-lookup"><span data-stu-id="2f57e-349">Number of buttons on the pointing device.</span></span>

<span data-ttu-id="2f57e-350">Esempio: "2"</span><span class="sxs-lookup"><span data-stu-id="2f57e-350">Example: "2"</span></span>

</dd> <dt>

<span data-ttu-id="2f57e-351">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="2f57e-351">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f57e-352">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2f57e-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-353">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2f57e-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-354">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2f57e-354">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2f57e-355">Win32 Plug and Play identificatore dispositivo del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="2f57e-355">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="2f57e-356">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2f57e-356">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="2f57e-357">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="2f57e-357">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="2f57e-358">**PointingType**</span><span class="sxs-lookup"><span data-stu-id="2f57e-358">**PointingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f57e-359">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2f57e-359">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-360">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2f57e-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-361">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF che \| punta al dispositivo \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="2f57e-361">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Pointing Device\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="2f57e-362">Tipo del dispositivo di puntamento.</span><span class="sxs-lookup"><span data-stu-id="2f57e-362">Type of the pointing device.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2f57e-363"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="2f57e-363"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2f57e-364"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="2f57e-364"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>

<span data-ttu-id="2f57e-365"><span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>**Mouse** (3)</span><span class="sxs-lookup"><span data-stu-id="2f57e-365"><span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>**Mouse** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>

<span data-ttu-id="2f57e-366"><span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>**Track Ball** (4)</span><span class="sxs-lookup"><span data-stu-id="2f57e-366"><span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>**Track Ball** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-367">Trackball</span><span class="sxs-lookup"><span data-stu-id="2f57e-367">Trackball</span></span>

</dd> <dt>

<span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>

<span data-ttu-id="2f57e-368"><span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>**Track point** (5)</span><span class="sxs-lookup"><span data-stu-id="2f57e-368"><span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>**Track Point** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>

<span data-ttu-id="2f57e-369"><span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>**Punto di scorrimento** (6)</span><span class="sxs-lookup"><span data-stu-id="2f57e-369"><span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>**Glide Point** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>

<span data-ttu-id="2f57e-370"><span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>**Touch pad** (7)</span><span class="sxs-lookup"><span data-stu-id="2f57e-370"><span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>**Touch Pad** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>

<span data-ttu-id="2f57e-371"><span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>**Touchscreen** (8)</span><span class="sxs-lookup"><span data-stu-id="2f57e-371"><span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>**Touch Screen** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>

<span data-ttu-id="2f57e-372"><span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>**Sensore ottico del mouse** (9)</span><span class="sxs-lookup"><span data-stu-id="2f57e-372"><span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>**Mouse - Optical Sensor** (9)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-373">Sensore ottico del mouse</span><span class="sxs-lookup"><span data-stu-id="2f57e-373">Mouse   optical sensor</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2f57e-374">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="2f57e-374">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f57e-375">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2f57e-375">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-376">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2f57e-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f57e-377">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="2f57e-377">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="2f57e-378">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="2f57e-378">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2f57e-379"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="2f57e-379"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="2f57e-380"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="2f57e-380"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2f57e-381"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="2f57e-381"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2f57e-382"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="2f57e-382"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-383">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="2f57e-383">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="2f57e-384"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="2f57e-384"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-385">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="2f57e-385">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="2f57e-386"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="2f57e-386"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-387">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="2f57e-387">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="2f57e-388">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="2f57e-388">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="2f57e-389">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="2f57e-389">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="2f57e-390"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="2f57e-390"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-391">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="2f57e-391">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="2f57e-392"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="2f57e-392"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="2f57e-393">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="2f57e-393">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2f57e-394">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="2f57e-394">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f57e-395">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2f57e-395">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-396">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2f57e-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f57e-397">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="2f57e-397">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="2f57e-398">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="2f57e-398">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="2f57e-399">Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="2f57e-399">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="2f57e-400">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="2f57e-400">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="2f57e-401">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2f57e-401">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f57e-402">**Risoluzione**</span><span class="sxs-lookup"><span data-stu-id="2f57e-402">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f57e-403">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2f57e-403">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-404">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2f57e-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-405">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("conteggi per pollice")</span><span class="sxs-lookup"><span data-stu-id="2f57e-405">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("counts per inch")</span></span>
</dt> </dl>

<span data-ttu-id="2f57e-406">Risoluzione del rilevamento.</span><span class="sxs-lookup"><span data-stu-id="2f57e-406">Tracking resolution.</span></span>

<span data-ttu-id="2f57e-407">Esempio: "0"</span><span class="sxs-lookup"><span data-stu-id="2f57e-407">Example: "0"</span></span>

</dd> <dt>

<span data-ttu-id="2f57e-408">**Status**</span><span class="sxs-lookup"><span data-stu-id="2f57e-408">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f57e-409">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2f57e-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-410">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2f57e-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-411">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="2f57e-411">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="2f57e-412">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2f57e-412">Current status of the object.</span></span> <span data-ttu-id="2f57e-413">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2f57e-413">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="2f57e-414">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="2f57e-414">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2f57e-415">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="2f57e-415">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="2f57e-416">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="2f57e-416">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2f57e-417">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="2f57e-417">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2f57e-418">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="2f57e-418">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="2f57e-419">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="2f57e-419">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="2f57e-420">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="2f57e-420">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="2f57e-421">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="2f57e-421">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2f57e-422">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="2f57e-422">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="2f57e-423">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="2f57e-423">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="2f57e-424">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="2f57e-424">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="2f57e-425">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="2f57e-425">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="2f57e-426">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="2f57e-426">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2f57e-427">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="2f57e-427">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f57e-428">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2f57e-428">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-429">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2f57e-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-430">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="2f57e-430">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="2f57e-431">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="2f57e-431">State of the logical device.</span></span> <span data-ttu-id="2f57e-432">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="2f57e-432">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="2f57e-433">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2f57e-433">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2f57e-434">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="2f57e-434">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2f57e-435">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="2f57e-435">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2f57e-436">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="2f57e-436">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2f57e-437">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="2f57e-437">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2f57e-438">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="2f57e-438">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2f57e-439">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2f57e-439">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f57e-440">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2f57e-440">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-441">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2f57e-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-442">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2f57e-442">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2f57e-443">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="2f57e-443">Scoping system's creation class name.</span></span>

<span data-ttu-id="2f57e-444">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2f57e-444">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f57e-445">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="2f57e-445">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f57e-446">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2f57e-446">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-447">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2f57e-447">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f57e-448">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2f57e-448">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2f57e-449">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="2f57e-449">Scoping system's name.</span></span>

<span data-ttu-id="2f57e-450">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2f57e-450">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2f57e-451">Commenti</span><span class="sxs-lookup"><span data-stu-id="2f57e-451">Remarks</span></span>

<span data-ttu-id="2f57e-452">La classe **CIM \_ PointingDevice** è derivata da [**CIM \_ UserDevice**](cim-userdevice.md).</span><span class="sxs-lookup"><span data-stu-id="2f57e-452">The **CIM\_PointingDevice** class is derived from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

<span data-ttu-id="2f57e-453">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="2f57e-453">WMI does not implement this class.</span></span> <span data-ttu-id="2f57e-454">Per le classi WMI derivate da **CIM \_ PointingDevice**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="2f57e-454">For WMI classes derived from **CIM\_PointingDevice**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="2f57e-455">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="2f57e-455">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2f57e-456">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="2f57e-456">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f57e-457">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f57e-457">Requirements</span></span>



| <span data-ttu-id="2f57e-458">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f57e-458">Requirement</span></span> | <span data-ttu-id="2f57e-459">Valore</span><span class="sxs-lookup"><span data-stu-id="2f57e-459">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f57e-460">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f57e-460">Minimum supported client</span></span><br/> | <span data-ttu-id="2f57e-461">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2f57e-461">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2f57e-462">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f57e-462">Minimum supported server</span></span><br/> | <span data-ttu-id="2f57e-463">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2f57e-463">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2f57e-464">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2f57e-464">Namespace</span></span><br/>                | <span data-ttu-id="2f57e-465">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="2f57e-465">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2f57e-466">MOF</span><span class="sxs-lookup"><span data-stu-id="2f57e-466">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2f57e-467"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2f57e-467"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2f57e-468">DLL</span><span class="sxs-lookup"><span data-stu-id="2f57e-468">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f57e-469"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f57e-469"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f57e-470">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2f57e-470">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f57e-471">**\_USERDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="2f57e-471">**CIM\_UserDevice**</span></span>](cim-userdevice.md)
</dt> </dl>

 


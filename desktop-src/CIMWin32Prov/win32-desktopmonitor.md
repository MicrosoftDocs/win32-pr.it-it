---
description: Rappresenta il tipo di monitoraggio o dispositivo di visualizzazione collegato al sistema del computer.
ms.assetid: 922be3c1-3c7b-4418-a72f-ab5ada91a7a4
ms.tgt_platform: multiple
title: Classe Win32_DesktopMonitor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DesktopMonitor
- Win32_DesktopMonitor.Reset
- Win32_DesktopMonitor.SetPowerState
- Win32_DesktopMonitor.Availability
- Win32_DesktopMonitor.Bandwidth
- Win32_DesktopMonitor.Caption
- Win32_DesktopMonitor.ConfigManagerErrorCode
- Win32_DesktopMonitor.ConfigManagerUserConfig
- Win32_DesktopMonitor.CreationClassName
- Win32_DesktopMonitor.Description
- Win32_DesktopMonitor.DeviceID
- Win32_DesktopMonitor.DisplayType
- Win32_DesktopMonitor.ErrorCleared
- Win32_DesktopMonitor.ErrorDescription
- Win32_DesktopMonitor.InstallDate
- Win32_DesktopMonitor.IsLocked
- Win32_DesktopMonitor.LastErrorCode
- Win32_DesktopMonitor.MonitorManufacturer
- Win32_DesktopMonitor.MonitorType
- Win32_DesktopMonitor.Name
- Win32_DesktopMonitor.PixelsPerXLogicalInch
- Win32_DesktopMonitor.PixelsPerYLogicalInch
- Win32_DesktopMonitor.PNPDeviceID
- Win32_DesktopMonitor.PowerManagementCapabilities
- Win32_DesktopMonitor.PowerManagementSupported
- Win32_DesktopMonitor.ScreenHeight
- Win32_DesktopMonitor.ScreenWidth
- Win32_DesktopMonitor.Status
- Win32_DesktopMonitor.StatusInfo
- Win32_DesktopMonitor.SystemCreationClassName
- Win32_DesktopMonitor.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ccf986957d73dd93837b0ab7a1e10b50aec5e8f9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524290"
---
# <a name="win32_desktopmonitor-class"></a><span data-ttu-id="b2e8d-103">Win32 \_ DesktopMonitor (classe)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-103">Win32\_DesktopMonitor class</span></span>

<span data-ttu-id="b2e8d-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DesktopMonitor Win32** rappresenta il tipo di monitoraggio o dispositivo di visualizzazione collegato al sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-104">The **Win32\_DesktopMonitor** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the type of monitor or display device attached to the computer system.</span></span>

<span data-ttu-id="b2e8d-105">L'hardware non compatibile con Windows Display Driver Model (WDDM) restituisce valori di proprietà non accurati per le istanze di questa classe.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-105">Hardware that is not compatible with Windows Display Driver Model (WDDM) returns inaccurate property values for instances of this class.</span></span>

<span data-ttu-id="b2e8d-106">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b2e8d-107">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2e8d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b2e8d-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{1008CCF0-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class Win32_DesktopMonitor : CIM_DesktopMonitor
{
  uint16   Availability;
  uint32   Bandwidth;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  uint16   DisplayType;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  boolean  IsLocked;
  uint32   LastErrorCode;
  string   MonitorManufacturer;
  string   MonitorType;
  string   Name;
  uint32   PixelsPerXLogicalInch;
  uint32   PixelsPerYLogicalInch;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   ScreenHeight;
  uint32   ScreenWidth;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="b2e8d-109">Members</span><span class="sxs-lookup"><span data-stu-id="b2e8d-109">Members</span></span>

<span data-ttu-id="b2e8d-110">La classe **Win32 \_ DesktopMonitor** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b2e8d-110">The **Win32\_DesktopMonitor** class has these types of members:</span></span>

-   [<span data-ttu-id="b2e8d-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="b2e8d-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="b2e8d-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b2e8d-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b2e8d-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="b2e8d-113">Methods</span></span>

<span data-ttu-id="b2e8d-114">La classe **Win32 \_ DesktopMonitor** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-114">The **Win32\_DesktopMonitor** class has these methods.</span></span>



| <span data-ttu-id="b2e8d-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="b2e8d-115">Method</span></span>            | <span data-ttu-id="b2e8d-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2e8d-116">Description</span></span>                                                                                                                                                                                                        |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2e8d-117">**Reimpostazione**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-117">**Reset**</span></span>         | <span data-ttu-id="b2e8d-118">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-118">Not implemented.</span></span> <span data-ttu-id="b2e8d-119">Per implementare questo metodo, vedere il metodo [**Reset**](reset-method-in-class-cim-controller.md) in [**CIM \_ DesktopMonitor**](cim-desktopmonitor.md) per la documentazione.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-119">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_DesktopMonitor**](cim-desktopmonitor.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="b2e8d-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-120">**SetPowerState**</span></span> | <span data-ttu-id="b2e8d-121">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-121">Not implemented.</span></span> <span data-ttu-id="b2e8d-122">Per implementare questo metodo, vedere il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) in [**CIM \_ DesktopMonitor**](cim-desktopmonitor.md) per la documentazione.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-122">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_DesktopMonitor**](cim-desktopmonitor.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b2e8d-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b2e8d-123">Properties</span></span>

<span data-ttu-id="b2e8d-124">La classe **Win32 \_ DesktopMonitor** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-124">The **Win32\_DesktopMonitor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b2e8d-125">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-125">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2e8d-126">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2e8d-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-128">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="b2e8d-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="b2e8d-129">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-129">Availability and status of the device.</span></span>

<span data-ttu-id="b2e8d-130">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b2e8d-130">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b2e8d-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b2e8d-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="b2e8d-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-134">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="b2e8d-134">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="b2e8d-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="b2e8d-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b2e8d-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="b2e8d-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="b2e8d-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="b2e8d-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="b2e8d-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="b2e8d-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b2e8d-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="b2e8d-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="b2e8d-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="b2e8d-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-145">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="b2e8d-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-147">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="b2e8d-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-149">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-149">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="b2e8d-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="b2e8d-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-152">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="b2e8d-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-154">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="b2e8d-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-156">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="b2e8d-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-158">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="b2e8d-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-160">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b2e8d-161">**Larghezza di banda**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-161">**Bandwidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2e8d-162">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2e8d-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-164">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span><span class="sxs-lookup"><span data-stu-id="b2e8d-164">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span></span>
</dt> </dl>

<span data-ttu-id="b2e8d-165">Larghezza di banda del monitoraggio in megahertz.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-165">Monitor's bandwidth in megahertz.</span></span> <span data-ttu-id="b2e8d-166">Se è sconosciuto, immettere 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="b2e8d-166">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="b2e8d-167">Questa proprietà viene ereditata da [**CIM \_ DesktopMonitor**](cim-desktopmonitor.md).</span><span class="sxs-lookup"><span data-stu-id="b2e8d-167">This property is inherited from [**CIM\_DesktopMonitor**](cim-desktopmonitor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2e8d-168">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-168">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2e8d-169">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-170">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2e8d-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-171">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b2e8d-171">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b2e8d-172">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-172">Short description of the object.</span></span>

<span data-ttu-id="b2e8d-173">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b2e8d-173">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2e8d-174">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-174">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2e8d-175">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-175">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2e8d-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-177">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b2e8d-177">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b2e8d-178">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-178">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="b2e8d-179">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b2e8d-179">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="b2e8d-180"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-180"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="b2e8d-181"> (0)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-181">(0)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-182">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-182">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="b2e8d-183"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-183"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="b2e8d-184">(1)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-184">(1)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-185">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-185">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b2e8d-186"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-186"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="b2e8d-187">(2)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-187">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="b2e8d-188"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-188"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="b2e8d-189">(3)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-189">(3)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-190">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-190">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b2e8d-191"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-191"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="b2e8d-192">(4)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-192">(4)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-193">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-193">Device is not working properly.</span></span> <span data-ttu-id="b2e8d-194">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-194">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="b2e8d-195"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-195"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="b2e8d-196">(5)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-196">(5)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-197">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-197">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="b2e8d-198"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-198"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="b2e8d-199"> (6)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-199">(6)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-200">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-200">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="b2e8d-201"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-201"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="b2e8d-202">(7)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-202">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="b2e8d-203"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-203"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="b2e8d-204">(8)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-204">(8)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-205">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-205">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="b2e8d-206"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-206"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="b2e8d-207">(9)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-207">(9)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-208">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-208">Device is not working properly.</span></span> <span data-ttu-id="b2e8d-209">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-209">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="b2e8d-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="b2e8d-211">(10)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-211">(10)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-212">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-212">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="b2e8d-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="b2e8d-214">(11)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-214">(11)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-215">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-215">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="b2e8d-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="b2e8d-217">12</span><span class="sxs-lookup"><span data-stu-id="b2e8d-217">(12)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-218">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-218">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="b2e8d-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="b2e8d-220">(13)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-220">(13)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-221">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-221">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="b2e8d-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="b2e8d-223">(14)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-223">(14)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-224">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-224">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="b2e8d-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="b2e8d-226">(15)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-226">(15)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-227">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-227">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="b2e8d-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="b2e8d-229">(16)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-229">(16)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-230">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-230">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="b2e8d-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="b2e8d-232">(17)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-232">(17)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-233">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-233">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b2e8d-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="b2e8d-235">(18)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-235">(18)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-236">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-236">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="b2e8d-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="b2e8d-238">(19)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-238">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b2e8d-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="b2e8d-240">(20)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-240">(20)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-241">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-241">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="b2e8d-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="b2e8d-243">(21)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-243">(21)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-244">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-244">System failure.</span></span> <span data-ttu-id="b2e8d-245">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-245">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="b2e8d-246">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-246">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="b2e8d-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="b2e8d-248">(22)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-248">(22)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-249">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-249">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="b2e8d-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="b2e8d-251">(23)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-251">(23)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-252">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-252">System failure.</span></span> <span data-ttu-id="b2e8d-253">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-253">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="b2e8d-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="b2e8d-255">(24)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-255">(24)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-256">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-256">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b2e8d-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b2e8d-258">(25)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-258">(25)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-259">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-259">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b2e8d-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b2e8d-261">(26)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-261">(26)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-262">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-262">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="b2e8d-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="b2e8d-264">(27)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-264">(27)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-265">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-265">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="b2e8d-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="b2e8d-267">(28)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-267">(28)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-268">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-268">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="b2e8d-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="b2e8d-270">(29)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-270">(29)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-271">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-271">Device is disabled.</span></span> <span data-ttu-id="b2e8d-272">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-272">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="b2e8d-273"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-273"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="b2e8d-274">(30)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-274">(30)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-275">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-275">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b2e8d-276"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-276"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="b2e8d-277">31</span><span class="sxs-lookup"><span data-stu-id="b2e8d-277">(31)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-278">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-278">Device is not working properly.</span></span> <span data-ttu-id="b2e8d-279">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-279">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b2e8d-280">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-280">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2e8d-281">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-281">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-282">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2e8d-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-283">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b2e8d-283">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b2e8d-284">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-284">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="b2e8d-285">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b2e8d-285">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2e8d-286">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-286">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2e8d-287">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-288">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2e8d-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-289">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-289">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b2e8d-290">Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-290">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="b2e8d-291">Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-291">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="b2e8d-292">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b2e8d-292">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2e8d-293">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-293">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2e8d-294">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-295">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2e8d-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-296">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="b2e8d-296">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b2e8d-297">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-297">Description of the object.</span></span>

<span data-ttu-id="b2e8d-298">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b2e8d-298">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2e8d-299">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-299">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2e8d-300">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-301">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2e8d-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-302">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Windows GDI \| HMONITOR")</span><span class="sxs-lookup"><span data-stu-id="b2e8d-302">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Windows GDI\|HMONITOR")</span></span>
</dt> </dl>

<span data-ttu-id="b2e8d-303">Identificatore univoco di un monitor desktop.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-303">Unique identifier of a desktop monitor.</span></span>

<span data-ttu-id="b2e8d-304">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b2e8d-304">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2e8d-305">**DisplayType**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-305">**DisplayType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2e8d-306">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-306">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-307">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2e8d-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2e8d-308">Tipo di monitor desktop o CRT.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-308">Type of desktop monitor or CRT.</span></span>

<span data-ttu-id="b2e8d-309">Questa proprietà viene ereditata da [**CIM \_ DesktopMonitor**](cim-desktopmonitor.md).</span><span class="sxs-lookup"><span data-stu-id="b2e8d-309">This property is inherited from [**CIM\_DesktopMonitor**](cim-desktopmonitor.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b2e8d-310">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-310">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b2e8d-311">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-311">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiscan_Color"></span><span id="multiscan_color"></span><span id="MULTISCAN_COLOR"></span>

<span data-ttu-id="b2e8d-312">**Colore MultiScan** (2)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-312">**Multiscan Color** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiscan_Monochrome"></span><span id="multiscan_monochrome"></span><span id="MULTISCAN_MONOCHROME"></span>

<span data-ttu-id="b2e8d-313">**MultiScan monocromatico** (3)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-313">**Multiscan Monochrome** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Color"></span><span id="fixed_frequency_color"></span><span id="FIXED_FREQUENCY_COLOR"></span>

<span data-ttu-id="b2e8d-314">**Colore a frequenza fissa** (4)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-314">**Fixed Frequency Color** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Monochrome"></span><span id="fixed_frequency_monochrome"></span><span id="FIXED_FREQUENCY_MONOCHROME"></span>

<span data-ttu-id="b2e8d-315">**Frequenza fissa monocromatico** (5)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-315">**Fixed Frequency Monochrome** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b2e8d-316">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-316">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2e8d-317">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-317">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-318">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2e8d-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2e8d-319">Se **true**, l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-319">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="b2e8d-320">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b2e8d-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2e8d-321">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-321">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2e8d-322">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-323">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2e8d-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2e8d-324">Stringa in formato libero che fornisce ulteriori informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-324">Free-form string supplying more information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="b2e8d-325">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b2e8d-325">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2e8d-326">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-326">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2e8d-327">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-327">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-328">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2e8d-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-329">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="b2e8d-329">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b2e8d-330">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-330">Date and time the object was installed.</span></span> <span data-ttu-id="b2e8d-331">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-331">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b2e8d-332">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b2e8d-332">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2e8d-333">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-333">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2e8d-334">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-334">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-335">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2e8d-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2e8d-336">Se **true**, il dispositivo è bloccato impedendo l'input o l'output dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-336">If **TRUE**, the device is locked, preventing user input or output.</span></span>

<span data-ttu-id="b2e8d-337">Questa proprietà viene ereditata da [**CIM \_ UserDevice**](cim-userdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b2e8d-337">This property is inherited from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2e8d-338">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-338">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2e8d-339">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-339">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-340">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2e8d-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2e8d-341">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-341">Last error code reported by the logical device.</span></span>

<span data-ttu-id="b2e8d-342">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b2e8d-342">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2e8d-343">**MonitorManufacturer**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-343">**MonitorManufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2e8d-344">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-345">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2e8d-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-346">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="b2e8d-346">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="b2e8d-347">Nome del produttore del monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-347">Name of the monitor manufacturer.</span></span>

<span data-ttu-id="b2e8d-348">Esempio: "NEC"</span><span class="sxs-lookup"><span data-stu-id="b2e8d-348">Example: "NEC"</span></span>

</dd> <dt>

<span data-ttu-id="b2e8d-349">**Monitoraggio**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-349">**MonitorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2e8d-350">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-351">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2e8d-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-352">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="b2e8d-352">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="b2e8d-353">Tipo di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-353">Type of monitor.</span></span>

<span data-ttu-id="b2e8d-354">Esempio: "NEC 5FGp"</span><span class="sxs-lookup"><span data-stu-id="b2e8d-354">Example: "NEC 5FGp"</span></span>

</dd> <dt>

<span data-ttu-id="b2e8d-355">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-355">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2e8d-356">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-357">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2e8d-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-358">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="b2e8d-358">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b2e8d-359">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-359">Label by which the object is known.</span></span> <span data-ttu-id="b2e8d-360">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-360">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="b2e8d-361">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b2e8d-361">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2e8d-362">**PixelsPerXLogicalInch**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-362">**PixelsPerXLogicalInch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2e8d-363">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-363">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-364">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2e8d-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-365">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixel per pollice logico")</span><span class="sxs-lookup"><span data-stu-id="b2e8d-365">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels per logical inch")</span></span>
</dt> </dl>

<span data-ttu-id="b2e8d-366">Risoluzione lungo l'asse x (direzione orizzontale) del monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-366">Resolution along the x-axis (horizontal direction) of the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="b2e8d-367">**PixelsPerYLogicalInch**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-367">**PixelsPerYLogicalInch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2e8d-368">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-368">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-369">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2e8d-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-370">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixel per pollice logico")</span><span class="sxs-lookup"><span data-stu-id="b2e8d-370">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels per logical inch")</span></span>
</dt> </dl>

<span data-ttu-id="b2e8d-371">Risoluzione lungo l'asse y (direzione verticale) del monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-371">Resolution along the y-axis (vertical direction) of the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="b2e8d-372">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-372">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2e8d-373">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-374">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2e8d-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-375">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b2e8d-375">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b2e8d-376">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-376">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="b2e8d-377">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b2e8d-377">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="b2e8d-378">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="b2e8d-378">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="b2e8d-379">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-379">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2e8d-380">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-380">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-381">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2e8d-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2e8d-382">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-382">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="b2e8d-383">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b2e8d-383">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b2e8d-384"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-384"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="b2e8d-385"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-385"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-386">Le capacità relative al risparmio di energia non sono supportate per questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-386">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b2e8d-387"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-387"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b2e8d-388"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-388"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-389">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-389">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="b2e8d-390"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-390"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-391">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-391">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="b2e8d-392"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-392"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-393">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-393">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="b2e8d-394">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-394">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="b2e8d-395">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="b2e8d-395">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="b2e8d-396"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-396"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-397">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="b2e8d-397">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="b2e8d-398"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-398"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-399">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-399">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b2e8d-400">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-400">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2e8d-401">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-401">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-402">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2e8d-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2e8d-403">Se **true**, il dispositivo può essere gestito dal risparmio di energia (può essere impostato in modalità di sospensione e così via).</span><span class="sxs-lookup"><span data-stu-id="b2e8d-403">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="b2e8d-404">La proprietà non indica che le funzionalità di risparmio energia sono attualmente abilitate, solo che il dispositivo logico è in grado di gestire il risparmio di energia.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-404">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="b2e8d-405">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b2e8d-405">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2e8d-406">**ScreenHeight**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-406">**ScreenHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2e8d-407">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-407">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-408">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2e8d-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2e8d-409">Altezza logica dello schermo nelle coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-409">Logical height of the display in screen coordinates.</span></span>

<span data-ttu-id="b2e8d-410">Questa proprietà viene ereditata da [**CIM \_ DesktopMonitor**](cim-desktopmonitor.md).</span><span class="sxs-lookup"><span data-stu-id="b2e8d-410">This property is inherited from [**CIM\_DesktopMonitor**](cim-desktopmonitor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2e8d-411">**ScreenWidth**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-411">**ScreenWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2e8d-412">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-412">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-413">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2e8d-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2e8d-414">Larghezza logica dello schermo nelle coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-414">Logical width of the display in screen coordinates.</span></span>

<span data-ttu-id="b2e8d-415">Questa proprietà viene ereditata da [**CIM \_ DesktopMonitor**](cim-desktopmonitor.md).</span><span class="sxs-lookup"><span data-stu-id="b2e8d-415">This property is inherited from [**CIM\_DesktopMonitor**](cim-desktopmonitor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2e8d-416">**Status**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-416">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2e8d-417">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-417">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-418">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2e8d-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-419">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="b2e8d-419">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b2e8d-420">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-420">Current status of the object.</span></span> <span data-ttu-id="b2e8d-421">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-421">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="b2e8d-422">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="b2e8d-422">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="b2e8d-423">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="b2e8d-423">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b2e8d-424">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-424">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b2e8d-425">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-425">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b2e8d-426">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b2e8d-426">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b2e8d-427">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="b2e8d-427">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b2e8d-428">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="b2e8d-428">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b2e8d-429">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="b2e8d-429">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b2e8d-430">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="b2e8d-430">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b2e8d-431">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="b2e8d-431">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b2e8d-432">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="b2e8d-432">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b2e8d-433">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="b2e8d-433">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b2e8d-434">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="b2e8d-434">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b2e8d-435">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="b2e8d-435">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b2e8d-436">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-436">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b2e8d-437">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="b2e8d-437">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b2e8d-438">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="b2e8d-438">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b2e8d-439">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="b2e8d-439">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b2e8d-440">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-440">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2e8d-441">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-441">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-442">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2e8d-442">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-443">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="b2e8d-443">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="b2e8d-444">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-444">State of the logical device.</span></span> <span data-ttu-id="b2e8d-445">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="b2e8d-445">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="b2e8d-446">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b2e8d-446">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b2e8d-447">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-447">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b2e8d-448">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-448">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b2e8d-449">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-449">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b2e8d-450">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-450">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b2e8d-451">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-451">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b2e8d-452">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-452">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2e8d-453">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-453">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-454">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2e8d-454">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-455">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-455">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b2e8d-456">Valore della proprietà **CreationClassName** del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-456">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="b2e8d-457">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b2e8d-457">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2e8d-458">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-458">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2e8d-459">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-459">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-460">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2e8d-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-461">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b2e8d-461">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b2e8d-462">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-462">Name of the scoping system.</span></span>

<span data-ttu-id="b2e8d-463">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b2e8d-463">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b2e8d-464">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2e8d-464">Remarks</span></span>

<span data-ttu-id="b2e8d-465">La classe **Win32 \_ DesktopMonitor** è derivata da [**CIM \_ DesktopMonitor**](cim-desktopmonitor.md), che deriva dalla [**\_ visualizzazione CIM**](cim-display.md).</span><span class="sxs-lookup"><span data-stu-id="b2e8d-465">The **Win32\_DesktopMonitor** class is derived from [**CIM\_DesktopMonitor**](cim-desktopmonitor.md), which derives from [**CIM\_Display**](cim-display.md).</span></span> <span data-ttu-id="b2e8d-466">**CIM \_ La visualizzazione** è derivata da [**CIM \_ UserDevice**](cim-userdevice.md), che deriva da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b2e8d-466">**CIM\_Display** is derived from [**CIM\_UserDevice**](cim-userdevice.md), which derives from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b2e8d-467">Esempio</span><span class="sxs-lookup"><span data-stu-id="b2e8d-467">Examples</span></span>

<span data-ttu-id="b2e8d-468">L'esempio di [creazione di un disegno di configurazione computer tramite](https://Gallery.TechNet.Microsoft.Com/84e2c31a-e644-4f79-83cd-e2b1a0ef8557) PowerShell per PowerShell nella raccolta TechNet USA **Win32 \_ DesktopMonitor** per interagire con il modello di automazione di Visio per creare un disegno di Visio.</span><span class="sxs-lookup"><span data-stu-id="b2e8d-468">The [PS Create a Computer Configuration Drawing using Visio](https://Gallery.TechNet.Microsoft.Com/84e2c31a-e644-4f79-83cd-e2b1a0ef8557) PowerShell sample on TechNet Gallery uses **Win32\_DesktopMonitor** to interact with the Visio automation model to create a Visio drawing.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2e8d-469">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2e8d-469">Requirements</span></span>



| <span data-ttu-id="b2e8d-470">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2e8d-470">Requirement</span></span> | <span data-ttu-id="b2e8d-471">Valore</span><span class="sxs-lookup"><span data-stu-id="b2e8d-471">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2e8d-472">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2e8d-472">Minimum supported client</span></span><br/> | <span data-ttu-id="b2e8d-473">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b2e8d-473">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b2e8d-474">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2e8d-474">Minimum supported server</span></span><br/> | <span data-ttu-id="b2e8d-475">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b2e8d-475">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b2e8d-476">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b2e8d-476">Namespace</span></span><br/>                | <span data-ttu-id="b2e8d-477">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="b2e8d-477">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b2e8d-478">MOF</span><span class="sxs-lookup"><span data-stu-id="b2e8d-478">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2e8d-479"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b2e8d-479"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b2e8d-480">DLL</span><span class="sxs-lookup"><span data-stu-id="b2e8d-480">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2e8d-481"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2e8d-481"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2e8d-482">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2e8d-482">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2e8d-483">**\_DESKTOPMONITOR CIM**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-483">**CIM\_DesktopMonitor**</span></span>](cim-desktopmonitor.md)
</dt> <dt>

[<span data-ttu-id="b2e8d-484">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="b2e8d-484">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="b2e8d-485">Attività WMI: gestione desktop</span><span class="sxs-lookup"><span data-stu-id="b2e8d-485">WMI Tasks: Desktop Management</span></span>](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 


---
description: La \_ classe CIM DesktopMonitor rappresenta le funzionalità e la gestione del dispositivo logico monitor desktop (CRT).
ms.assetid: dc65aa38-5255-4a40-8ffc-f05f9af71dc6
ms.tgt_platform: multiple
title: Classe CIM_DesktopMonitor (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DesktopMonitor
- CIM_DesktopMonitor.Caption
- CIM_DesktopMonitor.Description
- CIM_DesktopMonitor.InstallDate
- CIM_DesktopMonitor.Name
- CIM_DesktopMonitor.Status
- CIM_DesktopMonitor.Availability
- CIM_DesktopMonitor.ConfigManagerErrorCode
- CIM_DesktopMonitor.ConfigManagerUserConfig
- CIM_DesktopMonitor.CreationClassName
- CIM_DesktopMonitor.DeviceID
- CIM_DesktopMonitor.PowerManagementCapabilities
- CIM_DesktopMonitor.ErrorCleared
- CIM_DesktopMonitor.ErrorDescription
- CIM_DesktopMonitor.LastErrorCode
- CIM_DesktopMonitor.PNPDeviceID
- CIM_DesktopMonitor.PowerManagementSupported
- CIM_DesktopMonitor.StatusInfo
- CIM_DesktopMonitor.SystemCreationClassName
- CIM_DesktopMonitor.SystemName
- CIM_DesktopMonitor.IsLocked
- CIM_DesktopMonitor.Bandwidth
- CIM_DesktopMonitor.DisplayType
- CIM_DesktopMonitor.ScreenHeight
- CIM_DesktopMonitor.ScreenWidth
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b22d0b681491bbddf0ee357b394da5f1a77aa0e1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225689"
---
# <a name="cim_desktopmonitor-class-cimwin32-wmi-providers"></a><span data-ttu-id="eb55c-103">Classe CIM_DesktopMonitor (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="eb55c-103">CIM_DesktopMonitor class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="eb55c-104">La classe **CIM \_ DesktopMonitor** rappresenta le funzionalità e la gestione del dispositivo logico monitor desktop (CRT).</span><span class="sxs-lookup"><span data-stu-id="eb55c-104">The **CIM\_DesktopMonitor** class represents the capabilities and management of the desktop monitor (CRT) logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eb55c-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="eb55c-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="eb55c-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="eb55c-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="eb55c-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="eb55c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="eb55c-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="eb55c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb55c-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eb55c-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCE8-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_DesktopMonitor : CIM_Display
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint16   Availability;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   DeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   LastErrorCode;
  string   PNPDeviceID;
  boolean  PowerManagementSupported;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  boolean  IsLocked;
  uint32   Bandwidth;
  uint16   DisplayType;
  uint32   ScreenHeight;
  uint32   ScreenWidth;
};
```

## <a name="members"></a><span data-ttu-id="eb55c-110">Members</span><span class="sxs-lookup"><span data-stu-id="eb55c-110">Members</span></span>

<span data-ttu-id="eb55c-111">La classe **CIM \_ DesktopMonitor** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="eb55c-111">The **CIM\_DesktopMonitor** class has these types of members:</span></span>

-   [<span data-ttu-id="eb55c-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="eb55c-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="eb55c-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="eb55c-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="eb55c-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="eb55c-114">Methods</span></span>

<span data-ttu-id="eb55c-115">La classe **CIM \_ DesktopMonitor** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="eb55c-115">The **CIM\_DesktopMonitor** class has these methods.</span></span>



| <span data-ttu-id="eb55c-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="eb55c-116">Method</span></span>                                                                    | <span data-ttu-id="eb55c-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eb55c-117">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eb55c-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="eb55c-118">**Reset**</span></span>](reset-method-in-class-cim-desktopmonitor.md)                 | <span data-ttu-id="eb55c-119">Richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="eb55c-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="eb55c-120">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="eb55c-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="eb55c-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="eb55c-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-desktopmonitor.md) | <span data-ttu-id="eb55c-122">Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="eb55c-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="eb55c-123">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="eb55c-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="eb55c-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="eb55c-124">Properties</span></span>

<span data-ttu-id="eb55c-125">La classe **CIM \_ DesktopMonitor** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="eb55c-125">The **CIM\_DesktopMonitor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eb55c-126">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="eb55c-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb55c-127">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eb55c-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eb55c-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb55c-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb55c-129">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="eb55c-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="eb55c-130">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eb55c-130">Availability and status of the device.</span></span>

<span data-ttu-id="eb55c-131">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="eb55c-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="eb55c-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="eb55c-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="eb55c-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="eb55c-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="eb55c-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="eb55c-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="eb55c-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="eb55c-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="eb55c-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="eb55c-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="eb55c-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="eb55c-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="eb55c-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="eb55c-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="eb55c-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="eb55c-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="eb55c-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="eb55c-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="eb55c-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="eb55c-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="eb55c-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="eb55c-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="eb55c-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="eb55c-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="eb55c-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="eb55c-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="eb55c-145">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="eb55c-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="eb55c-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="eb55c-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="eb55c-147">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="eb55c-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="eb55c-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="eb55c-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="eb55c-149">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="eb55c-149">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="eb55c-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="eb55c-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="eb55c-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="eb55c-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="eb55c-152">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="eb55c-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="eb55c-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="eb55c-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="eb55c-154">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="eb55c-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="eb55c-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="eb55c-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="eb55c-156">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="eb55c-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="eb55c-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="eb55c-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="eb55c-158">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="eb55c-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="eb55c-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="eb55c-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="eb55c-160">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="eb55c-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="eb55c-161">**Larghezza di banda**</span><span class="sxs-lookup"><span data-stu-id="eb55c-161">**Bandwidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb55c-162">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eb55c-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eb55c-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb55c-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb55c-164">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span><span class="sxs-lookup"><span data-stu-id="eb55c-164">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span></span>
</dt> </dl>

<span data-ttu-id="eb55c-165">Larghezza di banda del monitoraggio in MHz.</span><span class="sxs-lookup"><span data-stu-id="eb55c-165">Monitor's bandwidth in MHz.</span></span> <span data-ttu-id="eb55c-166">Se sconosciuto, usare 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="eb55c-166">If unknown, use 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="eb55c-167">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="eb55c-167">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb55c-168">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eb55c-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb55c-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb55c-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb55c-170">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="eb55c-170">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="eb55c-171">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="eb55c-171">A short textual description of the object.</span></span>

<span data-ttu-id="eb55c-172">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="eb55c-172">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb55c-173">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="eb55c-173">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb55c-174">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eb55c-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eb55c-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb55c-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb55c-176">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="eb55c-176">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="eb55c-177">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="eb55c-177">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="eb55c-178">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="eb55c-178">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="eb55c-179">**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="eb55c-179">**This device is working properly.**</span></span> <span data-ttu-id="eb55c-180"> (0)</span><span class="sxs-lookup"><span data-stu-id="eb55c-180">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="eb55c-181">**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="eb55c-181">**This device is not configured correctly.**</span></span> <span data-ttu-id="eb55c-182">(1)</span><span class="sxs-lookup"><span data-stu-id="eb55c-182">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="eb55c-183">**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="eb55c-183">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="eb55c-184">(2)</span><span class="sxs-lookup"><span data-stu-id="eb55c-184">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="eb55c-185">**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="eb55c-185">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="eb55c-186">(3)</span><span class="sxs-lookup"><span data-stu-id="eb55c-186">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="eb55c-187">**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="eb55c-187">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="eb55c-188">(4)</span><span class="sxs-lookup"><span data-stu-id="eb55c-188">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="eb55c-189">**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="eb55c-189">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="eb55c-190">(5)</span><span class="sxs-lookup"><span data-stu-id="eb55c-190">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="eb55c-191">**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="eb55c-191">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="eb55c-192"> (6)</span><span class="sxs-lookup"><span data-stu-id="eb55c-192">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="eb55c-193">**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="eb55c-193">**Cannot filter.**</span></span> <span data-ttu-id="eb55c-194">(7)</span><span class="sxs-lookup"><span data-stu-id="eb55c-194">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="eb55c-195">**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="eb55c-195">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="eb55c-196">(8)</span><span class="sxs-lookup"><span data-stu-id="eb55c-196">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="eb55c-197">**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="eb55c-197">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="eb55c-198">(9)</span><span class="sxs-lookup"><span data-stu-id="eb55c-198">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="eb55c-199">**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="eb55c-199">**This device cannot start.**</span></span> <span data-ttu-id="eb55c-200">(10)</span><span class="sxs-lookup"><span data-stu-id="eb55c-200">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="eb55c-201">**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="eb55c-201">**This device failed.**</span></span> <span data-ttu-id="eb55c-202">(11)</span><span class="sxs-lookup"><span data-stu-id="eb55c-202">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="eb55c-203">**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="eb55c-203">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="eb55c-204">12</span><span class="sxs-lookup"><span data-stu-id="eb55c-204">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="eb55c-205">**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="eb55c-205">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="eb55c-206">(13)</span><span class="sxs-lookup"><span data-stu-id="eb55c-206">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="eb55c-207">**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="eb55c-207">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="eb55c-208">(14)</span><span class="sxs-lookup"><span data-stu-id="eb55c-208">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="eb55c-209">**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="eb55c-209">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="eb55c-210">(15)</span><span class="sxs-lookup"><span data-stu-id="eb55c-210">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="eb55c-211">**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="eb55c-211">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="eb55c-212">(16)</span><span class="sxs-lookup"><span data-stu-id="eb55c-212">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="eb55c-213">**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="eb55c-213">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="eb55c-214">(17)</span><span class="sxs-lookup"><span data-stu-id="eb55c-214">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="eb55c-215">**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="eb55c-215">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="eb55c-216">(18)</span><span class="sxs-lookup"><span data-stu-id="eb55c-216">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="eb55c-217">**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="eb55c-217">**Failure using the VxD loader.**</span></span> <span data-ttu-id="eb55c-218">(19)</span><span class="sxs-lookup"><span data-stu-id="eb55c-218">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="eb55c-219">**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="eb55c-219">**Your registry might be corrupted.**</span></span> <span data-ttu-id="eb55c-220">(20)</span><span class="sxs-lookup"><span data-stu-id="eb55c-220">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="eb55c-221">**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="eb55c-221">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="eb55c-222">(21)</span><span class="sxs-lookup"><span data-stu-id="eb55c-222">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="eb55c-223">**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="eb55c-223">**This device is disabled.**</span></span> <span data-ttu-id="eb55c-224">(22)</span><span class="sxs-lookup"><span data-stu-id="eb55c-224">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="eb55c-225">**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="eb55c-225">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="eb55c-226">(23)</span><span class="sxs-lookup"><span data-stu-id="eb55c-226">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="eb55c-227">**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="eb55c-227">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="eb55c-228">(24)</span><span class="sxs-lookup"><span data-stu-id="eb55c-228">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="eb55c-229">**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="eb55c-229">**Windows is still setting up this device.**</span></span> <span data-ttu-id="eb55c-230">(25)</span><span class="sxs-lookup"><span data-stu-id="eb55c-230">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="eb55c-231">**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="eb55c-231">**Windows is still setting up this device.**</span></span> <span data-ttu-id="eb55c-232">(26)</span><span class="sxs-lookup"><span data-stu-id="eb55c-232">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="eb55c-233">**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="eb55c-233">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="eb55c-234">(27)</span><span class="sxs-lookup"><span data-stu-id="eb55c-234">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="eb55c-235">**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="eb55c-235">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="eb55c-236">(28)</span><span class="sxs-lookup"><span data-stu-id="eb55c-236">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="eb55c-237">**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="eb55c-237">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="eb55c-238">(29)</span><span class="sxs-lookup"><span data-stu-id="eb55c-238">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="eb55c-239">**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="eb55c-239">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="eb55c-240">(30)</span><span class="sxs-lookup"><span data-stu-id="eb55c-240">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="eb55c-241">**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="eb55c-241">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="eb55c-242">31</span><span class="sxs-lookup"><span data-stu-id="eb55c-242">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="eb55c-243">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="eb55c-243">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb55c-244">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="eb55c-244">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eb55c-245">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb55c-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb55c-246">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="eb55c-246">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="eb55c-247">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="eb55c-247">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="eb55c-248">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="eb55c-248">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb55c-249">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="eb55c-249">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb55c-250">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eb55c-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb55c-251">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb55c-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb55c-252">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="eb55c-252">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="eb55c-253">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="eb55c-253">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="eb55c-254">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="eb55c-254">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="eb55c-255">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="eb55c-255">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb55c-256">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="eb55c-256">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb55c-257">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eb55c-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb55c-258">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb55c-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb55c-259">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="eb55c-259">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="eb55c-260">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="eb55c-260">A textual description of the object.</span></span>

<span data-ttu-id="eb55c-261">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="eb55c-261">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb55c-262">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="eb55c-262">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb55c-263">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eb55c-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb55c-264">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb55c-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb55c-265">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="eb55c-265">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="eb55c-266">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="eb55c-266">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="eb55c-267">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="eb55c-267">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb55c-268">**DisplayType**</span><span class="sxs-lookup"><span data-stu-id="eb55c-268">**DisplayType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb55c-269">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eb55c-269">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eb55c-270">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb55c-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb55c-271">Tipo di monitor desktop o CRT.</span><span class="sxs-lookup"><span data-stu-id="eb55c-271">Type of desktop monitor or CRT.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="eb55c-272">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="eb55c-272">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="eb55c-273">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="eb55c-273">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiscan_Color"></span><span id="multiscan_color"></span><span id="MULTISCAN_COLOR"></span>

<span data-ttu-id="eb55c-274">**Colore MultiScan** (2)</span><span class="sxs-lookup"><span data-stu-id="eb55c-274">**Multiscan Color** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiscan_Monochrome"></span><span id="multiscan_monochrome"></span><span id="MULTISCAN_MONOCHROME"></span>

<span data-ttu-id="eb55c-275">**MultiScan monocromatico** (3)</span><span class="sxs-lookup"><span data-stu-id="eb55c-275">**Multiscan Monochrome** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Color"></span><span id="fixed_frequency_color"></span><span id="FIXED_FREQUENCY_COLOR"></span>

<span data-ttu-id="eb55c-276">**Colore a frequenza fissa** (4)</span><span class="sxs-lookup"><span data-stu-id="eb55c-276">**Fixed Frequency Color** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Monochrome"></span><span id="fixed_frequency_monochrome"></span><span id="FIXED_FREQUENCY_MONOCHROME"></span>

<span data-ttu-id="eb55c-277">**Frequenza fissa monocromatico** (5)</span><span class="sxs-lookup"><span data-stu-id="eb55c-277">**Fixed Frequency Monochrome** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="eb55c-278">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="eb55c-278">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb55c-279">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="eb55c-279">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eb55c-280">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb55c-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb55c-281">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="eb55c-281">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="eb55c-282">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="eb55c-282">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb55c-283">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="eb55c-283">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb55c-284">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eb55c-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb55c-285">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb55c-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb55c-286">Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.</span><span class="sxs-lookup"><span data-stu-id="eb55c-286">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="eb55c-287">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="eb55c-287">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb55c-288">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="eb55c-288">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb55c-289">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="eb55c-289">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="eb55c-290">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb55c-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb55c-291">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="eb55c-291">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="eb55c-292">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="eb55c-292">Indicates when the object was installed.</span></span> <span data-ttu-id="eb55c-293">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="eb55c-293">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="eb55c-294">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="eb55c-294">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb55c-295">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="eb55c-295">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb55c-296">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="eb55c-296">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eb55c-297">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb55c-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb55c-298">Se **true**, il dispositivo è bloccato impedendo l'input o l'output dell'utente.</span><span class="sxs-lookup"><span data-stu-id="eb55c-298">If **TRUE**, the device is locked, preventing user input or output.</span></span>

<span data-ttu-id="eb55c-299">Questa proprietà viene ereditata da [**CIM \_ UserDevice**](cim-userdevice.md).</span><span class="sxs-lookup"><span data-stu-id="eb55c-299">This property is inherited from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb55c-300">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="eb55c-300">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb55c-301">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eb55c-301">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eb55c-302">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb55c-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb55c-303">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="eb55c-303">Last error code reported by the logical device.</span></span>

<span data-ttu-id="eb55c-304">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="eb55c-304">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb55c-305">**Nome**</span><span class="sxs-lookup"><span data-stu-id="eb55c-305">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb55c-306">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eb55c-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb55c-307">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb55c-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb55c-308">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="eb55c-308">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="eb55c-309">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="eb55c-309">Label by which the object is known.</span></span> <span data-ttu-id="eb55c-310">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="eb55c-310">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="eb55c-311">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="eb55c-311">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb55c-312">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="eb55c-312">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb55c-313">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eb55c-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb55c-314">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb55c-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb55c-315">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="eb55c-315">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="eb55c-316">Indica l'identificatore del dispositivo Plug and Play Win32 del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="eb55c-316">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="eb55c-317">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="eb55c-317">Example: "\*PNP030b"</span></span>

<span data-ttu-id="eb55c-318">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="eb55c-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb55c-319">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="eb55c-319">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb55c-320">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eb55c-320">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="eb55c-321">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb55c-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb55c-322">Indica le funzionalità specifiche relative al risparmio di energia del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="eb55c-322">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="eb55c-323">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="eb55c-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="eb55c-324"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="eb55c-324"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="eb55c-325">Le capacità relative al risparmio di energia sono sconosciute.</span><span class="sxs-lookup"><span data-stu-id="eb55c-325">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="eb55c-326"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="eb55c-326"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="eb55c-327">Le capacità relative al risparmio di energia non sono supportate per questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eb55c-327">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="eb55c-328"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="eb55c-328"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="eb55c-329">Le capacità correlate all'alimentazione sono state disabilitate.</span><span class="sxs-lookup"><span data-stu-id="eb55c-329">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="eb55c-330"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="eb55c-330"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="eb55c-331">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="eb55c-331">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="eb55c-332"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="eb55c-332"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="eb55c-333">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="eb55c-333">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="eb55c-334"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="eb55c-334"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="eb55c-335">Il metodo **SetPowerState** è supportato.</span><span class="sxs-lookup"><span data-stu-id="eb55c-335">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="eb55c-336">Questo metodo è disponibile nella classe [**\_ LogicalDevice CIM**](cim-logicaldevice.md) padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="eb55c-336">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="eb55c-337">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="eb55c-337">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="eb55c-338"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="eb55c-338"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="eb55c-339">Il metodo **SetPowerState** può essere richiamato con il parametro *PowerState* impostato su 5 ("ciclo di alimentazione").</span><span class="sxs-lookup"><span data-stu-id="eb55c-339">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="eb55c-340"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="eb55c-340"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="eb55c-341">Il metodo **SetPowerState** può essere richiamato con il parametro *PowerState* impostato su 5 ("ciclo di alimentazione") e il parametro *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="eb55c-341">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="eb55c-342">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="eb55c-342">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb55c-343">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="eb55c-343">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eb55c-344">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb55c-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb55c-345">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="eb55c-345">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="eb55c-346">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="eb55c-346">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="eb55c-347">Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="eb55c-347">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="eb55c-348">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="eb55c-348">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="eb55c-349">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="eb55c-349">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb55c-350">**ScreenHeight**</span><span class="sxs-lookup"><span data-stu-id="eb55c-350">**ScreenHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb55c-351">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eb55c-351">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eb55c-352">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb55c-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb55c-353">Altezza logica dello schermo, in coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="eb55c-353">Logical height of the display, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="eb55c-354">**ScreenWidth**</span><span class="sxs-lookup"><span data-stu-id="eb55c-354">**ScreenWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb55c-355">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eb55c-355">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eb55c-356">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb55c-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb55c-357">Larghezza logica dello schermo, in coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="eb55c-357">Logical width of the display, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="eb55c-358">**Status**</span><span class="sxs-lookup"><span data-stu-id="eb55c-358">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb55c-359">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eb55c-359">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb55c-360">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb55c-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb55c-361">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="eb55c-361">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="eb55c-362">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="eb55c-362">String that indicates the current status of the object.</span></span> <span data-ttu-id="eb55c-363">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="eb55c-363">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="eb55c-364">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="eb55c-364">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="eb55c-365">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="eb55c-365">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="eb55c-366">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="eb55c-366">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="eb55c-367">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="eb55c-367">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="eb55c-368">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="eb55c-368">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="eb55c-369">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="eb55c-369">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="eb55c-370">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="eb55c-370">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="eb55c-371">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="eb55c-371">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="eb55c-372">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="eb55c-372">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="eb55c-373">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="eb55c-373">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="eb55c-374">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="eb55c-374">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="eb55c-375">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="eb55c-375">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="eb55c-376">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="eb55c-376">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="eb55c-377">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="eb55c-377">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="eb55c-378">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="eb55c-378">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="eb55c-379">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="eb55c-379">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="eb55c-380">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="eb55c-380">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="eb55c-381">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="eb55c-381">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="eb55c-382">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="eb55c-382">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="eb55c-383">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="eb55c-383">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb55c-384">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eb55c-384">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eb55c-385">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb55c-385">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb55c-386">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="eb55c-386">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="eb55c-387">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="eb55c-387">State of the logical device.</span></span> <span data-ttu-id="eb55c-388">Se questa proprietà non è applicabile al dispositivo logico, è necessario utilizzare il valore 5 ("non applicabile").</span><span class="sxs-lookup"><span data-stu-id="eb55c-388">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="eb55c-389">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="eb55c-389">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="eb55c-390">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="eb55c-390">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="eb55c-391">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="eb55c-391">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="eb55c-392">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="eb55c-392">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="eb55c-393">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="eb55c-393">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="eb55c-394">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="eb55c-394">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="eb55c-395">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="eb55c-395">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb55c-396">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eb55c-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb55c-397">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb55c-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb55c-398">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="eb55c-398">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="eb55c-399">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="eb55c-399">The scoping system's creation class name.</span></span>

<span data-ttu-id="eb55c-400">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="eb55c-400">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb55c-401">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="eb55c-401">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb55c-402">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eb55c-402">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb55c-403">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb55c-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb55c-404">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="eb55c-404">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="eb55c-405">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="eb55c-405">The scoping system's name.</span></span>

<span data-ttu-id="eb55c-406">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="eb55c-406">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb55c-407">Commenti</span><span class="sxs-lookup"><span data-stu-id="eb55c-407">Remarks</span></span>

<span data-ttu-id="eb55c-408">La classe **CIM \_ DesktopMonitor** è derivata dalla [**\_ visualizzazione CIM**](cim-display.md).</span><span class="sxs-lookup"><span data-stu-id="eb55c-408">The **CIM\_DesktopMonitor** class is derived from [**CIM\_Display**](cim-display.md).</span></span>

<span data-ttu-id="eb55c-409">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="eb55c-409">WMI does not implement this class.</span></span> <span data-ttu-id="eb55c-410">Per ulteriori informazioni sulle classi derivate da **CIM \_ DesktopMonitor**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="eb55c-410">For more information about classes derived from **CIM\_DesktopMonitor**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="eb55c-411">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="eb55c-411">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="eb55c-412">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="eb55c-412">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb55c-413">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eb55c-413">Requirements</span></span>



| <span data-ttu-id="eb55c-414">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb55c-414">Requirement</span></span> | <span data-ttu-id="eb55c-415">Valore</span><span class="sxs-lookup"><span data-stu-id="eb55c-415">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb55c-416">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb55c-416">Minimum supported client</span></span><br/> | <span data-ttu-id="eb55c-417">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eb55c-417">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eb55c-418">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb55c-418">Minimum supported server</span></span><br/> | <span data-ttu-id="eb55c-419">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb55c-419">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eb55c-420">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="eb55c-420">Namespace</span></span><br/>                | <span data-ttu-id="eb55c-421">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="eb55c-421">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="eb55c-422">MOF</span><span class="sxs-lookup"><span data-stu-id="eb55c-422">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb55c-423"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eb55c-423"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="eb55c-424">DLL</span><span class="sxs-lookup"><span data-stu-id="eb55c-424">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb55c-425"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb55c-425"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb55c-426">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eb55c-426">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb55c-427">**\_Visualizzazione CIM**</span><span class="sxs-lookup"><span data-stu-id="eb55c-427">**CIM\_Display**</span></span>](cim-display.md)
</dt> </dl>

 


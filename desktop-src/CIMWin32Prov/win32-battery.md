---
description: Rappresenta una batteria connessa al sistema del computer.
ms.assetid: b07ccb1d-008e-4bf1-8299-33706cbcbaee
ms.tgt_platform: multiple
title: Classe Win32_Battery
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Battery
- Win32_Battery.Reset
- Win32_Battery.SetPowerState
- Win32_Battery.Availability
- Win32_Battery.BatteryRechargeTime
- Win32_Battery.BatteryStatus
- Win32_Battery.Caption
- Win32_Battery.Chemistry
- Win32_Battery.ConfigManagerErrorCode
- Win32_Battery.ConfigManagerUserConfig
- Win32_Battery.CreationClassName
- Win32_Battery.Description
- Win32_Battery.DesignCapacity
- Win32_Battery.DesignVoltage
- Win32_Battery.DeviceID
- Win32_Battery.ErrorCleared
- Win32_Battery.ErrorDescription
- Win32_Battery.EstimatedChargeRemaining
- Win32_Battery.EstimatedRunTime
- Win32_Battery.ExpectedBatteryLife
- Win32_Battery.ExpectedLife
- Win32_Battery.FullChargeCapacity
- Win32_Battery.InstallDate
- Win32_Battery.LastErrorCode
- Win32_Battery.MaxRechargeTime
- Win32_Battery.Name
- Win32_Battery.PNPDeviceID
- Win32_Battery.PowerManagementCapabilities
- Win32_Battery.PowerManagementSupported
- Win32_Battery.SmartBatteryVersion
- Win32_Battery.Status
- Win32_Battery.StatusInfo
- Win32_Battery.SystemCreationClassName
- Win32_Battery.SystemName
- Win32_Battery.TimeOnBattery
- Win32_Battery.TimeToFullCharge
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 75477bcf670bcc0cf16c63f130f95d4c38d7b783
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049270"
---
# <a name="win32_battery-class"></a><span data-ttu-id="6145c-103">\_Classe della batteria Win32</span><span class="sxs-lookup"><span data-stu-id="6145c-103">Win32\_Battery class</span></span>

<span data-ttu-id="6145c-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ della batteria Win32** rappresenta una batteria connessa al sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="6145c-104">The **Win32\_Battery** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a battery connected to the computer system.</span></span>

<span data-ttu-id="6145c-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="6145c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6145c-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="6145c-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6145c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6145c-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B9-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Battery : CIM_Battery
{
  uint16   Availability;
  uint32   BatteryRechargeTime;
  uint16   BatteryStatus;
  string   Caption;
  uint16   Chemistry;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  uint32   DesignCapacity;
  uint64   DesignVoltage;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint16   EstimatedChargeRemaining;
  uint32   EstimatedRunTime;
  uint32   ExpectedBatteryLife;
  uint32   ExpectedLife;
  uint32   FullChargeCapacity;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxRechargeTime;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   SmartBatteryVersion;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   TimeOnBattery;
  uint32   TimeToFullCharge;
};
```

## <a name="members"></a><span data-ttu-id="6145c-108">Members</span><span class="sxs-lookup"><span data-stu-id="6145c-108">Members</span></span>

<span data-ttu-id="6145c-109">La classe della **\_ batteria Win32** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6145c-109">The **Win32\_Battery** class has these types of members:</span></span>

-   [<span data-ttu-id="6145c-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="6145c-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="6145c-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6145c-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6145c-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="6145c-112">Methods</span></span>

<span data-ttu-id="6145c-113">La classe della **\_ batteria Win32** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="6145c-113">The **Win32\_Battery** class has these methods.</span></span>



| <span data-ttu-id="6145c-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="6145c-114">Method</span></span>            | <span data-ttu-id="6145c-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6145c-115">Description</span></span>                                                                                                                                                                                          |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6145c-116">**Reimpostazione**</span><span class="sxs-lookup"><span data-stu-id="6145c-116">**Reset**</span></span>         | <span data-ttu-id="6145c-117">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="6145c-117">Not implemented.</span></span> <span data-ttu-id="6145c-118">Per implementare questo metodo, vedere il metodo [**Reset**](reset-method-in-class-cim-controller.md) nella [**\_ batteria CIM**](cim-battery.md) per la documentazione.</span><span class="sxs-lookup"><span data-stu-id="6145c-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_Battery**](cim-battery.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="6145c-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="6145c-119">**SetPowerState**</span></span> | <span data-ttu-id="6145c-120">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="6145c-120">Not implemented.</span></span> <span data-ttu-id="6145c-121">Per implementare questo metodo, vedere il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) nella [**\_ batteria CIM**](cim-battery.md) per la documentazione.</span><span class="sxs-lookup"><span data-stu-id="6145c-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_Battery**](cim-battery.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6145c-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6145c-122">Properties</span></span>

<span data-ttu-id="6145c-123">La classe della **\_ batteria Win32** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6145c-123">The **Win32\_Battery** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6145c-124">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="6145c-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6145c-125">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6145c-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6145c-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6145c-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6145c-127">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="6145c-127">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="6145c-128">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6145c-128">Availability and status of the device.</span></span>

<span data-ttu-id="6145c-129">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6145c-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6145c-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="6145c-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6145c-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="6145c-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="6145c-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="6145c-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-133">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="6145c-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="6145c-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="6145c-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="6145c-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="6145c-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="6145c-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="6145c-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="6145c-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="6145c-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="6145c-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="6145c-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="6145c-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="6145c-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6145c-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="6145c-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="6145c-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="6145c-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="6145c-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="6145c-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="6145c-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="6145c-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-144">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="6145c-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="6145c-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="6145c-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-146">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="6145c-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="6145c-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="6145c-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-148">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="6145c-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="6145c-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="6145c-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="6145c-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="6145c-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-151">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="6145c-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="6145c-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="6145c-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-153">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="6145c-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="6145c-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="6145c-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-155">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="6145c-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="6145c-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="6145c-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-157">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="6145c-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="6145c-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="6145c-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-159">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="6145c-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6145c-160">**BatteryRechargeTime**</span><span class="sxs-lookup"><span data-stu-id="6145c-160">**BatteryRechargeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6145c-161">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6145c-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6145c-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6145c-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6145c-163">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("HKEY \_ Local \_ computer \\ \\ System \\ \\ CurrentControlSet \\ \\ Services \| rechargerate"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("minuti")</span><span class="sxs-lookup"><span data-stu-id="6145c-163">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("HKEY\_LOCAL\_MACHINE\\\\System\\\\CurrentControlSet\\\\Services\|RechargeRate"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="6145c-164">Tempo necessario per l'addebito completo della batteria.</span><span class="sxs-lookup"><span data-stu-id="6145c-164">Time required to fully charge the battery.</span></span> <span data-ttu-id="6145c-165">Questa proprietà non è supportata.</span><span class="sxs-lookup"><span data-stu-id="6145c-165">This property is not supported.</span></span> <span data-ttu-id="6145c-166">**BatteryRechargeTime** non dispone di una proprietà di sostituzione ed è ora considerato obsoleto.</span><span class="sxs-lookup"><span data-stu-id="6145c-166">**BatteryRechargeTime** does not have a replacement property, and is now considered obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="6145c-167">**BatteryStatus**</span><span class="sxs-lookup"><span data-stu-id="6145c-167">**BatteryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6145c-168">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6145c-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6145c-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6145c-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6145c-170">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Portable batteria \| 002,14 ")</span><span class="sxs-lookup"><span data-stu-id="6145c-170">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.14")</span></span>
</dt> </dl>

<span data-ttu-id="6145c-171">Stato della batteria.</span><span class="sxs-lookup"><span data-stu-id="6145c-171">Status of the battery.</span></span> <span data-ttu-id="6145c-172">Il valore 10 (undefined) non è valido nello schema CIM perché in DMI indica che non è installata alcuna batteria.</span><span class="sxs-lookup"><span data-stu-id="6145c-172">The value 10 (Undefined) is not valid in the CIM schema because in DMI it represents that no battery is installed.</span></span> <span data-ttu-id="6145c-173">In questo caso, non è necessario creare un'istanza dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6145c-173">In this case, the object should not be instantiated.</span></span>

<span data-ttu-id="6145c-174">Questa proprietà viene ereditata [**dalla \_ batteria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="6145c-174">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6145c-175"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="6145c-175"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-176">La batteria sta per essere scaricata.</span><span class="sxs-lookup"><span data-stu-id="6145c-176">The battery is discharging.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6145c-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="6145c-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-178">Il sistema ha accesso a AC, quindi la batteria non viene ricaricata.</span><span class="sxs-lookup"><span data-stu-id="6145c-178">The system has access to AC so no battery is being discharged.</span></span> <span data-ttu-id="6145c-179">Tuttavia, la batteria non viene addebitata necessariamente.</span><span class="sxs-lookup"><span data-stu-id="6145c-179">However, the battery is not necessarily charging.</span></span>

</dd> <dt>

<span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>

<span data-ttu-id="6145c-180"><span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>**Costo totale** (3)</span><span class="sxs-lookup"><span data-stu-id="6145c-180"><span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>**Fully Charged** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="6145c-181"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Bassa** (4)</span><span class="sxs-lookup"><span data-stu-id="6145c-181"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="6145c-182"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critico** (5)</span><span class="sxs-lookup"><span data-stu-id="6145c-182"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>

<span data-ttu-id="6145c-183"><span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>**Addebito** (6)</span><span class="sxs-lookup"><span data-stu-id="6145c-183"><span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>**Charging** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>

<span data-ttu-id="6145c-184"><span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>**Addebito e elevato** (7)</span><span class="sxs-lookup"><span data-stu-id="6145c-184"><span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>**Charging and High** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>

<span data-ttu-id="6145c-185"><span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>**Ricarica e bassa** (8)</span><span class="sxs-lookup"><span data-stu-id="6145c-185"><span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>**Charging and Low** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>

<span data-ttu-id="6145c-186"><span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>**Addebito e critico** (9)</span><span class="sxs-lookup"><span data-stu-id="6145c-186"><span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>**Charging and Critical** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="6145c-187"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>Non **definito** (10)</span><span class="sxs-lookup"><span data-stu-id="6145c-187"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>

<span data-ttu-id="6145c-188"><span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>**Parzialmente addebitato** (11)</span><span class="sxs-lookup"><span data-stu-id="6145c-188"><span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>**Partially Charged** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6145c-189">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="6145c-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6145c-190">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6145c-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6145c-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6145c-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6145c-192">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="6145c-192">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="6145c-193">Breve descrizione dell'oggetto stringa a una riga.</span><span class="sxs-lookup"><span data-stu-id="6145c-193">Short description of the object a one-line string.</span></span>

<span data-ttu-id="6145c-194">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6145c-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6145c-195">**Chimica**</span><span class="sxs-lookup"><span data-stu-id="6145c-195">**Chemistry**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6145c-196">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6145c-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6145c-197">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6145c-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6145c-198">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Portable batteria \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="6145c-198">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="6145c-199">Enumerazione che descrive la chimica della batteria.</span><span class="sxs-lookup"><span data-stu-id="6145c-199">Enumeration that describes the battery's chemistry.</span></span>

<span data-ttu-id="6145c-200">Questa proprietà viene ereditata [**dalla \_ batteria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="6145c-200">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6145c-201">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="6145c-201">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6145c-202">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="6145c-202">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Lead_Acid"></span><span id="lead_acid"></span><span id="LEAD_ACID"></span>

<span data-ttu-id="6145c-203">**Acido di piombo** (3)</span><span class="sxs-lookup"><span data-stu-id="6145c-203">**Lead Acid** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Nickel_Cadmium"></span><span id="nickel_cadmium"></span><span id="NICKEL_CADMIUM"></span>

<span data-ttu-id="6145c-204">**Nichel cadmio** (4)</span><span class="sxs-lookup"><span data-stu-id="6145c-204">**Nickel Cadmium** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Nickel_Metal_Hydride"></span><span id="nickel_metal_hydride"></span><span id="NICKEL_METAL_HYDRIDE"></span>

<span data-ttu-id="6145c-205">**Idruro Nickel Metal** (5)</span><span class="sxs-lookup"><span data-stu-id="6145c-205">**Nickel Metal Hydride** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Lithium-ion"></span><span id="lithium-ion"></span><span id="LITHIUM-ION"></span>

<span data-ttu-id="6145c-206">**Lithium-Ion** (6)</span><span class="sxs-lookup"><span data-stu-id="6145c-206">**Lithium-ion** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Zinc_air"></span><span id="zinc_air"></span><span id="ZINC_AIR"></span>

<span data-ttu-id="6145c-207">**Zinco aria** (7)</span><span class="sxs-lookup"><span data-stu-id="6145c-207">**Zinc air** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Lithium_Polymer"></span><span id="lithium_polymer"></span><span id="LITHIUM_POLYMER"></span>

<span data-ttu-id="6145c-208">**Polimero Lithium** (8)</span><span class="sxs-lookup"><span data-stu-id="6145c-208">**Lithium Polymer** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6145c-209">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="6145c-209">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6145c-210">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6145c-210">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6145c-211">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6145c-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6145c-212">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="6145c-212">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6145c-213">Codice di errore di Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="6145c-213">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="6145c-214">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6145c-214">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="6145c-215"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="6145c-215"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="6145c-216"> (0)</span><span class="sxs-lookup"><span data-stu-id="6145c-216">(0)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-217">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="6145c-217">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="6145c-218"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="6145c-218"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="6145c-219">(1)</span><span class="sxs-lookup"><span data-stu-id="6145c-219">(1)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-220">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="6145c-220">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6145c-221"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="6145c-221"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="6145c-222">(2)</span><span class="sxs-lookup"><span data-stu-id="6145c-222">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="6145c-223"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="6145c-223"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="6145c-224">(3)</span><span class="sxs-lookup"><span data-stu-id="6145c-224">(3)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-225">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="6145c-225">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="6145c-226"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="6145c-226"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="6145c-227">(4)</span><span class="sxs-lookup"><span data-stu-id="6145c-227">(4)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-228">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="6145c-228">Device is not working properly.</span></span> <span data-ttu-id="6145c-229">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="6145c-229">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="6145c-230"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="6145c-230"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="6145c-231">(5)</span><span class="sxs-lookup"><span data-stu-id="6145c-231">(5)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-232">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="6145c-232">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="6145c-233"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="6145c-233"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="6145c-234"> (6)</span><span class="sxs-lookup"><span data-stu-id="6145c-234">(6)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-235">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="6145c-235">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="6145c-236"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="6145c-236"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="6145c-237">(7)</span><span class="sxs-lookup"><span data-stu-id="6145c-237">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="6145c-238"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="6145c-238"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="6145c-239">(8)</span><span class="sxs-lookup"><span data-stu-id="6145c-239">(8)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-240">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="6145c-240">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="6145c-241"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="6145c-241"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="6145c-242">(9)</span><span class="sxs-lookup"><span data-stu-id="6145c-242">(9)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-243">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="6145c-243">Device is not working properly.</span></span> <span data-ttu-id="6145c-244">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6145c-244">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="6145c-245"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="6145c-245"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="6145c-246">(10)</span><span class="sxs-lookup"><span data-stu-id="6145c-246">(10)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-247">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6145c-247">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="6145c-248"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="6145c-248"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="6145c-249">(11)</span><span class="sxs-lookup"><span data-stu-id="6145c-249">(11)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-250">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6145c-250">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="6145c-251"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="6145c-251"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="6145c-252">12</span><span class="sxs-lookup"><span data-stu-id="6145c-252">(12)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-253">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="6145c-253">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="6145c-254"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="6145c-254"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="6145c-255">(13)</span><span class="sxs-lookup"><span data-stu-id="6145c-255">(13)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-256">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6145c-256">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="6145c-257"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="6145c-257"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="6145c-258">(14)</span><span class="sxs-lookup"><span data-stu-id="6145c-258">(14)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-259">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="6145c-259">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="6145c-260"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="6145c-260"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="6145c-261">(15)</span><span class="sxs-lookup"><span data-stu-id="6145c-261">(15)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-262">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="6145c-262">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="6145c-263"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="6145c-263"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="6145c-264">(16)</span><span class="sxs-lookup"><span data-stu-id="6145c-264">(16)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-265">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6145c-265">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="6145c-266"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="6145c-266"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="6145c-267">(17)</span><span class="sxs-lookup"><span data-stu-id="6145c-267">(17)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-268">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="6145c-268">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6145c-269"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="6145c-269"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="6145c-270">(18)</span><span class="sxs-lookup"><span data-stu-id="6145c-270">(18)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-271">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6145c-271">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="6145c-272"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="6145c-272"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="6145c-273">(19)</span><span class="sxs-lookup"><span data-stu-id="6145c-273">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="6145c-274"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="6145c-274"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="6145c-275">(20)</span><span class="sxs-lookup"><span data-stu-id="6145c-275">(20)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-276">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="6145c-276">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="6145c-277"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="6145c-277"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="6145c-278">(21)</span><span class="sxs-lookup"><span data-stu-id="6145c-278">(21)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-279">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="6145c-279">System failure.</span></span> <span data-ttu-id="6145c-280">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="6145c-280">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="6145c-281">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6145c-281">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="6145c-282"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="6145c-282"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="6145c-283">(22)</span><span class="sxs-lookup"><span data-stu-id="6145c-283">(22)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-284">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="6145c-284">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="6145c-285"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="6145c-285"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="6145c-286">(23)</span><span class="sxs-lookup"><span data-stu-id="6145c-286">(23)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-287">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="6145c-287">System failure.</span></span> <span data-ttu-id="6145c-288">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="6145c-288">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="6145c-289"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="6145c-289"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="6145c-290">(24)</span><span class="sxs-lookup"><span data-stu-id="6145c-290">(24)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-291">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="6145c-291">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="6145c-292"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="6145c-292"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="6145c-293">(25)</span><span class="sxs-lookup"><span data-stu-id="6145c-293">(25)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-294">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6145c-294">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="6145c-295"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="6145c-295"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="6145c-296">(26)</span><span class="sxs-lookup"><span data-stu-id="6145c-296">(26)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-297">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6145c-297">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="6145c-298"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="6145c-298"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="6145c-299">(27)</span><span class="sxs-lookup"><span data-stu-id="6145c-299">(27)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-300">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="6145c-300">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="6145c-301"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="6145c-301"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="6145c-302">(28)</span><span class="sxs-lookup"><span data-stu-id="6145c-302">(28)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-303">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="6145c-303">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="6145c-304"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="6145c-304"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="6145c-305">(29)</span><span class="sxs-lookup"><span data-stu-id="6145c-305">(29)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-306">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="6145c-306">Device is disabled.</span></span> <span data-ttu-id="6145c-307">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="6145c-307">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="6145c-308"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="6145c-308"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="6145c-309">(30)</span><span class="sxs-lookup"><span data-stu-id="6145c-309">(30)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-310">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6145c-310">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6145c-311"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="6145c-311"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="6145c-312">31</span><span class="sxs-lookup"><span data-stu-id="6145c-312">(31)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-313">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="6145c-313">Device is not working properly.</span></span> <span data-ttu-id="6145c-314">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="6145c-314">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6145c-315">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="6145c-315">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6145c-316">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6145c-316">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6145c-317">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6145c-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6145c-318">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="6145c-318">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6145c-319">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="6145c-319">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="6145c-320">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6145c-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6145c-321">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6145c-321">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6145c-322">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6145c-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6145c-323">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6145c-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6145c-324">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6145c-324">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6145c-325">Nome della prima classe concreta visualizzata nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="6145c-325">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="6145c-326">Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="6145c-326">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="6145c-327">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6145c-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6145c-328">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="6145c-328">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6145c-329">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6145c-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6145c-330">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6145c-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6145c-331">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="6145c-331">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="6145c-332">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6145c-332">Description of the object.</span></span>

<span data-ttu-id="6145c-333">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6145c-333">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6145c-334">**DesignCapacity**</span><span class="sxs-lookup"><span data-stu-id="6145c-334">**DesignCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6145c-335">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6145c-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6145c-336">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6145c-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6145c-337">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Portable batteria \| 002,8 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliwatt-ore ")</span><span class="sxs-lookup"><span data-stu-id="6145c-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="6145c-338">Capacità di progettazione della batteria in milliwatt ore.</span><span class="sxs-lookup"><span data-stu-id="6145c-338">Design capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="6145c-339">Se la proprietà non è supportata, immettere 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="6145c-339">If the property is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="6145c-340">Questa proprietà viene ereditata [**dalla \_ batteria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="6145c-340">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="6145c-341">**DesignVoltage**</span><span class="sxs-lookup"><span data-stu-id="6145c-341">**DesignVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6145c-342">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6145c-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6145c-343">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6145c-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6145c-344">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Portable batteria \| 002,9 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" millivolt ")</span><span class="sxs-lookup"><span data-stu-id="6145c-344">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.9"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="6145c-345">Tensione di progettazione della batteria in millivolt.</span><span class="sxs-lookup"><span data-stu-id="6145c-345">Design voltage of the battery in millivolts.</span></span> <span data-ttu-id="6145c-346">Se l'attributo non è supportato, immettere 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="6145c-346">If the attribute is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="6145c-347">Questa proprietà viene ereditata [**dalla \_ batteria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="6145c-347">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<span data-ttu-id="6145c-348">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="6145c-348">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="6145c-349">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="6145c-349">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6145c-350">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6145c-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6145c-351">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6145c-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6145c-352">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="6145c-352">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="6145c-353">Identifica la batteria.</span><span class="sxs-lookup"><span data-stu-id="6145c-353">Identifies the battery.</span></span>

<span data-ttu-id="6145c-354">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6145c-354">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="6145c-355">Esempio: "batteria interna"</span><span class="sxs-lookup"><span data-stu-id="6145c-355">Example: "Internal Battery"</span></span>

</dd> <dt>

<span data-ttu-id="6145c-356">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="6145c-356">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6145c-357">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6145c-357">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6145c-358">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6145c-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6145c-359">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="6145c-359">If **True**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="6145c-360">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6145c-360">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6145c-361">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="6145c-361">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6145c-362">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6145c-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6145c-363">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6145c-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6145c-364">Stringa in formato libero che fornisce ulteriori informazioni sull'errore registrato nella proprietà **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="6145c-364">Free-form string that supplies more information about the error recorded in **LastErrorCode** property, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="6145c-365">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6145c-365">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6145c-366">**EstimatedChargeRemaining**</span><span class="sxs-lookup"><span data-stu-id="6145c-366">**EstimatedChargeRemaining**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6145c-367">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6145c-367">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6145c-368">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6145c-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6145c-369">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("percentuale")</span><span class="sxs-lookup"><span data-stu-id="6145c-369">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="6145c-370">Stima della percentuale di costo totale rimanente.</span><span class="sxs-lookup"><span data-stu-id="6145c-370">Estimate of the percentage of full charge remaining.</span></span>

<span data-ttu-id="6145c-371">Questa proprietà viene ereditata [**dalla \_ batteria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="6145c-371">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="6145c-372">**EstimatedRunTime**</span><span class="sxs-lookup"><span data-stu-id="6145c-372">**EstimatedRunTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6145c-373">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6145c-373">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6145c-374">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6145c-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6145c-375">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Portable batteria \| 002,15 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" minuti ")</span><span class="sxs-lookup"><span data-stu-id="6145c-375">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="6145c-376">Stima in minuti del tempo di esaurimento della carica della batteria sotto le condizioni di carico attuali se l'alimentazione dell'utilità è disattivata o persa e rimane spenta o se un portatile è disconnesso da una fonte di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="6145c-376">Estimate in minutes of the time to battery charge depletion under the present load conditions if the utility power is off, or lost and remains off, or a laptop is disconnected from a power source.</span></span>

<span data-ttu-id="6145c-377">Questa proprietà viene ereditata [**dalla \_ batteria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="6145c-377">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="6145c-378">**ExpectedBatteryLife**</span><span class="sxs-lookup"><span data-stu-id="6145c-378">**ExpectedBatteryLife**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6145c-379">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6145c-379">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6145c-380">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6145c-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6145c-381">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("HKEY \_ Local \_ computer \\ \\ System \\ \\ CurrentControlSet \\ \\ Services \| BatteryLife"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("minuti")</span><span class="sxs-lookup"><span data-stu-id="6145c-381">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("HKEY\_LOCAL\_MACHINE\\\\System\\\\CurrentControlSet\\\\Services\|BatteryLife"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="6145c-382">Quantità di tempo necessaria per svuotare completamente la batteria dopo che è stata completamente addebitata.</span><span class="sxs-lookup"><span data-stu-id="6145c-382">Amount of time it takes to completely drain the battery after it is fully charged.</span></span> <span data-ttu-id="6145c-383">Questa proprietà non viene più utilizzata ed è considerata obsoleta.</span><span class="sxs-lookup"><span data-stu-id="6145c-383">This property is no longer used and is considered obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="6145c-384">**ExpectedLife**</span><span class="sxs-lookup"><span data-stu-id="6145c-384">**ExpectedLife**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6145c-385">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6145c-385">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6145c-386">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6145c-386">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6145c-387">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("minuti")</span><span class="sxs-lookup"><span data-stu-id="6145c-387">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="6145c-388">Durata prevista della batteria in minuti, presupponendo che la batteria venga addebitata completamente.</span><span class="sxs-lookup"><span data-stu-id="6145c-388">Battery's expected lifetime in minutes, assuming that the battery is fully charged.</span></span> <span data-ttu-id="6145c-389">La proprietà rappresenta la durata totale prevista della batteria, non la durata rimanente corrente, indicata dalla proprietà **EstimatedRunTime** .</span><span class="sxs-lookup"><span data-stu-id="6145c-389">The property represents the total expected life of the battery, not its current remaining life, which is indicated by the **EstimatedRunTime** property.</span></span>

<span data-ttu-id="6145c-390">Questa proprietà viene ereditata [**dalla \_ batteria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="6145c-390">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="6145c-391">**FullChargeCapacity**</span><span class="sxs-lookup"><span data-stu-id="6145c-391">**FullChargeCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6145c-392">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6145c-392">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6145c-393">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6145c-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6145c-394">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Portable batteria \| 002,11 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliwatt-ore ")</span><span class="sxs-lookup"><span data-stu-id="6145c-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="6145c-395">Capacità di addebito completo della batteria in milliwatt ore.</span><span class="sxs-lookup"><span data-stu-id="6145c-395">Full charge capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="6145c-396">Il confronto tra il valore e la proprietà **DesignCapacity** determina quando la batteria richiede la sostituzione.</span><span class="sxs-lookup"><span data-stu-id="6145c-396">Comparison of the value to the **DesignCapacity** property determines when the battery requires replacement.</span></span> <span data-ttu-id="6145c-397">La fine della durata della batteria è in genere quando la proprietà **FullChargeCapacity** è inferiore al 80% della proprietà **DesignCapacity** .</span><span class="sxs-lookup"><span data-stu-id="6145c-397">A battery's end of life is typically when the **FullChargeCapacity** property falls below 80% of the **DesignCapacity** property.</span></span> <span data-ttu-id="6145c-398">Se la proprietà non è supportata, immettere 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="6145c-398">If the property is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="6145c-399">Questa proprietà viene ereditata [**dalla \_ batteria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="6145c-399">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="6145c-400">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6145c-400">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6145c-401">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6145c-401">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6145c-402">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6145c-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6145c-403">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="6145c-403">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="6145c-404">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6145c-404">Date and time the object was installed.</span></span> <span data-ttu-id="6145c-405">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="6145c-405">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="6145c-406">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6145c-406">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6145c-407">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="6145c-407">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6145c-408">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6145c-408">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6145c-409">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6145c-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6145c-410">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="6145c-410">Last error code reported by the logical device.</span></span>

<span data-ttu-id="6145c-411">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6145c-411">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6145c-412">**MaxRechargeTime**</span><span class="sxs-lookup"><span data-stu-id="6145c-412">**MaxRechargeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6145c-413">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6145c-413">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6145c-414">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6145c-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6145c-415">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("minuti")</span><span class="sxs-lookup"><span data-stu-id="6145c-415">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="6145c-416">Tempo massimo, in minuti, per l'addebito completo della batteria.</span><span class="sxs-lookup"><span data-stu-id="6145c-416">Maximum time, in minutes, to fully charge the battery.</span></span> <span data-ttu-id="6145c-417">La proprietà rappresenta il tempo per ricaricare una batteria completamente esaurita, non il tempo di ricarica rimanente corrente, indicato nella proprietà **TimeToFullCharge** .</span><span class="sxs-lookup"><span data-stu-id="6145c-417">The property represents the time to recharge a fully depleted battery, not the current remaining charge time, which is indicated in the **TimeToFullCharge** property.</span></span>

<span data-ttu-id="6145c-418">Questa proprietà viene ereditata [**dalla \_ batteria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="6145c-418">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="6145c-419">**Nome**</span><span class="sxs-lookup"><span data-stu-id="6145c-419">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6145c-420">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6145c-420">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6145c-421">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6145c-421">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6145c-422">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="6145c-422">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="6145c-423">Definisce l'etichetta in base alla quale l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="6145c-423">Defines the label by which the object is known.</span></span> <span data-ttu-id="6145c-424">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="6145c-424">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="6145c-425">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6145c-425">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6145c-426">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="6145c-426">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6145c-427">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6145c-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6145c-428">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6145c-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6145c-429">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="6145c-429">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6145c-430">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="6145c-430">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="6145c-431">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6145c-431">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="6145c-432">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="6145c-432">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="6145c-433">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="6145c-433">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6145c-434">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6145c-434">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6145c-435">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6145c-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6145c-436">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="6145c-436">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="6145c-437">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="6145c-437">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6145c-438"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="6145c-438"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="6145c-439"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="6145c-439"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6145c-440"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="6145c-440"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="6145c-441"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="6145c-441"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-442">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="6145c-442">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="6145c-443"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="6145c-443"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-444">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="6145c-444">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="6145c-445"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="6145c-445"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-446">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="6145c-446">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="6145c-447">Questo metodo è disponibile nella classe [**\_ LogicalDevice CIM**](cim-logicaldevice.md) padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="6145c-447">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="6145c-448">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="6145c-448">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="6145c-449"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="6145c-449"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-450">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="6145c-450">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="6145c-451"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="6145c-451"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="6145c-452">Tempo Power-On supportato</span><span class="sxs-lookup"><span data-stu-id="6145c-452">Timed Power-On Supported</span></span>

<span data-ttu-id="6145c-453">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="6145c-453">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6145c-454">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="6145c-454">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6145c-455">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6145c-455">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6145c-456">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6145c-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6145c-457">Se **true**, il dispositivo può essere gestito dal risparmio di energia (può essere impostato in modalità di sospensione e così via).</span><span class="sxs-lookup"><span data-stu-id="6145c-457">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="6145c-458">La proprietà non indica che le funzionalità di risparmio energia sono attualmente abilitate, solo che il dispositivo logico è in grado di gestire il risparmio di energia.</span><span class="sxs-lookup"><span data-stu-id="6145c-458">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="6145c-459">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6145c-459">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6145c-460">**SmartBatteryVersion**</span><span class="sxs-lookup"><span data-stu-id="6145c-460">**SmartBatteryVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6145c-461">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6145c-461">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6145c-462">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6145c-462">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6145c-463">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Portable batteria \| 002,10 ")</span><span class="sxs-lookup"><span data-stu-id="6145c-463">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.10")</span></span>
</dt> </dl>

<span data-ttu-id="6145c-464">Numero di versione della specifica dati supportato dalla batteria.</span><span class="sxs-lookup"><span data-stu-id="6145c-464">Data Specification version number supported by the battery.</span></span> <span data-ttu-id="6145c-465">Se la batteria non supporta questa funzione, il valore deve essere lasciato vuoto.</span><span class="sxs-lookup"><span data-stu-id="6145c-465">If the battery does not support this function, the value should be left blank.</span></span>

<span data-ttu-id="6145c-466">Questa proprietà viene ereditata [**dalla \_ batteria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="6145c-466">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="6145c-467">**Status**</span><span class="sxs-lookup"><span data-stu-id="6145c-467">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6145c-468">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6145c-468">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6145c-469">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6145c-469">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6145c-470">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="6145c-470">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="6145c-471">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6145c-471">Current status of the object.</span></span> <span data-ttu-id="6145c-472">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="6145c-472">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="6145c-473">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="6145c-473">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="6145c-474">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="6145c-474">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="6145c-475">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="6145c-475">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="6145c-476">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="6145c-476">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="6145c-477">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6145c-477">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="6145c-478">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="6145c-478">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6145c-479">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="6145c-479">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6145c-480">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="6145c-480">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6145c-481">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="6145c-481">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6145c-482">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="6145c-482">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="6145c-483">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="6145c-483">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6145c-484">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="6145c-484">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="6145c-485">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="6145c-485">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6145c-486">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="6145c-486">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="6145c-487">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="6145c-487">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="6145c-488">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="6145c-488">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6145c-489">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="6145c-489">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="6145c-490">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="6145c-490">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6145c-491">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="6145c-491">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6145c-492">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6145c-492">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6145c-493">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6145c-493">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6145c-494">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="6145c-494">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="6145c-495">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="6145c-495">State of the logical device.</span></span> <span data-ttu-id="6145c-496">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="6145c-496">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="6145c-497">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6145c-497">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6145c-498">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="6145c-498">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6145c-499">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="6145c-499">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="6145c-500">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="6145c-500">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6145c-501">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="6145c-501">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="6145c-502">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="6145c-502">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6145c-503">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6145c-503">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6145c-504">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6145c-504">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6145c-505">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6145c-505">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6145c-506">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6145c-506">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6145c-507">Valore della proprietà **CreationClassName** del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="6145c-507">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="6145c-508">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6145c-508">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6145c-509">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="6145c-509">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6145c-510">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6145c-510">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6145c-511">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6145c-511">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6145c-512">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6145c-512">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6145c-513">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="6145c-513">Name of the scoping system.</span></span>

<span data-ttu-id="6145c-514">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6145c-514">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6145c-515">**TimeOnBattery**</span><span class="sxs-lookup"><span data-stu-id="6145c-515">**TimeOnBattery**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6145c-516">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6145c-516">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6145c-517">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6145c-517">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6145c-518">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("secondi")</span><span class="sxs-lookup"><span data-stu-id="6145c-518">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="6145c-519">Tempo trascorso in secondi dall'ultima volta in cui l'UPS del sistema informatico passa alla potenza della batteria oppure il tempo trascorso dall'ultimo riavvio del sistema o dell'UPS, a seconda del numero minore.</span><span class="sxs-lookup"><span data-stu-id="6145c-519">Elapsed time in seconds since the computer system's UPS last switched to battery power, or the time since the system or UPS was last restarted, whichever is less.</span></span> <span data-ttu-id="6145c-520">Se la batteria è "on line", viene restituito 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="6145c-520">If the battery is "on line", 0 (zero) is returned.</span></span>

<span data-ttu-id="6145c-521">Questa proprietà viene ereditata [**dalla \_ batteria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="6145c-521">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="6145c-522">**TimeToFullCharge**</span><span class="sxs-lookup"><span data-stu-id="6145c-522">**TimeToFullCharge**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6145c-523">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6145c-523">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6145c-524">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6145c-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6145c-525">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Portable batteria \| 002,16 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" minuti ")</span><span class="sxs-lookup"><span data-stu-id="6145c-525">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.16"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="6145c-526">Tempo rimanente per l'addebito completo della batteria in pochi minuti alla tariffa e all'utilizzo correnti.</span><span class="sxs-lookup"><span data-stu-id="6145c-526">Remaining time to charge the battery fully in minutes at the current charging rate and usage.</span></span>

<span data-ttu-id="6145c-527">Questa proprietà viene ereditata [**dalla \_ batteria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="6145c-527">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6145c-528">Commenti</span><span class="sxs-lookup"><span data-stu-id="6145c-528">Remarks</span></span>

<span data-ttu-id="6145c-529">La classe della **\_ batteria Win32** è derivata [**dalla \_ batteria CIM**](cim-battery.md) che deriva da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6145c-529">The **Win32\_Battery** class is derived from [**CIM\_Battery**](cim-battery.md) which derives from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="6145c-530">Windows Server 2008 contiene i driver UPS (APC) nel sistema operativo, che consente di gestire il gruppo di continuità come alimentatore della batteria.</span><span class="sxs-lookup"><span data-stu-id="6145c-530">Windows Server 2008 contains the (APC) UPS drivers in the OS, which allows you to treat the UPS as a battery supply.</span></span> <span data-ttu-id="6145c-531">In questo modo è possibile monitorare lo stato degli UPS usando uno script e intraprendere le azioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="6145c-531">This allows you to monitor the UPS status using a script and take actions when necessary.</span></span>

## <a name="examples"></a><span data-ttu-id="6145c-532">Esempio</span><span class="sxs-lookup"><span data-stu-id="6145c-532">Examples</span></span>

<span data-ttu-id="6145c-533">Nell'esempio di codice di [Toggle-Wireless.ps1](https://Gallery.TechNet.Microsoft.Com/Toggle-Wirelessps1-2d244a8f) PowerShell viene eseguita una query sulla **\_ batteria Win32** per determinare se disabilitare o meno il wireless per risparmiare energia.</span><span class="sxs-lookup"><span data-stu-id="6145c-533">The [Toggle-Wireless.ps1](https://Gallery.TechNet.Microsoft.Com/Toggle-Wirelessps1-2d244a8f) PowerShell code sample queries **Win32\_Battery** to determine whether or not to toggle the wireless in order to save power.</span></span>

<span data-ttu-id="6145c-534">L'esempio [List UPS Information](https://Gallery.TechNet.Microsoft.Com/7196121e-97de-4290-9939-26d0ce266270) perl elenca le informazioni sulle fonti di continuità elettrica collegate a un computer.</span><span class="sxs-lookup"><span data-stu-id="6145c-534">The [List UPS Information](https://Gallery.TechNet.Microsoft.Com/7196121e-97de-4290-9939-26d0ce266270) Perl sample Lists information about the uninterruptible power sources attached to a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="6145c-535">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6145c-535">Requirements</span></span>



| <span data-ttu-id="6145c-536">Requisito</span><span class="sxs-lookup"><span data-stu-id="6145c-536">Requirement</span></span> | <span data-ttu-id="6145c-537">Valore</span><span class="sxs-lookup"><span data-stu-id="6145c-537">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6145c-538">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6145c-538">Minimum supported client</span></span><br/> | <span data-ttu-id="6145c-539">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6145c-539">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6145c-540">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6145c-540">Minimum supported server</span></span><br/> | <span data-ttu-id="6145c-541">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6145c-541">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6145c-542">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6145c-542">Namespace</span></span><br/>                | <span data-ttu-id="6145c-543">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="6145c-543">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6145c-544">MOF</span><span class="sxs-lookup"><span data-stu-id="6145c-544">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6145c-545"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6145c-545"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6145c-546">DLL</span><span class="sxs-lookup"><span data-stu-id="6145c-546">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6145c-547"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6145c-547"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6145c-548">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6145c-548">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6145c-549">**\_Batteria CIM**</span><span class="sxs-lookup"><span data-stu-id="6145c-549">**CIM\_Battery**</span></span>](cim-battery.md)
</dt> <dt>

[<span data-ttu-id="6145c-550">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="6145c-550">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 


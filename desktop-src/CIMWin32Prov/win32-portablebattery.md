---
description: La \_ classe WMI PortableBattery Win32 contiene le proprietà correlate a una batteria portatile, ad esempio una batteria del computer notebook.
ms.assetid: ca7d061f-8fc6-4a1e-aa75-2465ce5e2735
ms.tgt_platform: multiple
title: Classe Win32_PortableBattery
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PortableBattery
- Win32_PortableBattery.Reset
- Win32_PortableBattery.SetPowerState
- Win32_PortableBattery.Availability
- Win32_PortableBattery.BatteryStatus
- Win32_PortableBattery.CapacityMultiplier
- Win32_PortableBattery.Caption
- Win32_PortableBattery.Chemistry
- Win32_PortableBattery.ConfigManagerErrorCode
- Win32_PortableBattery.ConfigManagerUserConfig
- Win32_PortableBattery.CreationClassName
- Win32_PortableBattery.Description
- Win32_PortableBattery.DesignCapacity
- Win32_PortableBattery.DesignVoltage
- Win32_PortableBattery.DeviceID
- Win32_PortableBattery.ErrorCleared
- Win32_PortableBattery.ErrorDescription
- Win32_PortableBattery.EstimatedChargeRemaining
- Win32_PortableBattery.EstimatedRunTime
- Win32_PortableBattery.ExpectedBatteryLife
- Win32_PortableBattery.ExpectedLife
- Win32_PortableBattery.FullChargeCapacity
- Win32_PortableBattery.InstallDate
- Win32_PortableBattery.LastErrorCode
- Win32_PortableBattery.Location
- Win32_PortableBattery.ManufactureDate
- Win32_PortableBattery.Manufacturer
- Win32_PortableBattery.MaxBatteryError
- Win32_PortableBattery.MaxRechargeTime
- Win32_PortableBattery.Name
- Win32_PortableBattery.PNPDeviceID
- Win32_PortableBattery.PowerManagementCapabilities
- Win32_PortableBattery.PowerManagementSupported
- Win32_PortableBattery.SmartBatteryVersion
- Win32_PortableBattery.Status
- Win32_PortableBattery.StatusInfo
- Win32_PortableBattery.SystemCreationClassName
- Win32_PortableBattery.SystemName
- Win32_PortableBattery.TimeOnBattery
- Win32_PortableBattery.TimeToFullCharge
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9db875e7e4d1736cf45945b53f2f20fec0490a47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747911"
---
# <a name="win32_portablebattery-class"></a><span data-ttu-id="43f2c-103">Win32 \_ PortableBattery (classe)</span><span class="sxs-lookup"><span data-stu-id="43f2c-103">Win32\_PortableBattery class</span></span>

<span data-ttu-id="43f2c-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PortableBattery Win32** contiene le proprietà correlate a una batteria portatile, ad esempio una batteria del computer notebook.</span><span class="sxs-lookup"><span data-stu-id="43f2c-104">The **Win32\_PortableBattery** [WMI class](../wmisdk/retrieving-a-class.md) contains the properties related to a portable battery, such as a notebook computer battery.</span></span>

<span data-ttu-id="43f2c-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="43f2c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="43f2c-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="43f2c-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="43f2c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="43f2c-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B9E-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_PortableBattery : CIM_Battery
{
  uint16   Availability;
  uint16   BatteryStatus;
  uint16   CapacityMultiplier;
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
  string   Location;
  string   ManufactureDate;
  string   Manufacturer;
  uint16   MaxBatteryError;
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

## <a name="members"></a><span data-ttu-id="43f2c-108">Members</span><span class="sxs-lookup"><span data-stu-id="43f2c-108">Members</span></span>

<span data-ttu-id="43f2c-109">La classe **Win32 \_ PortableBattery** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="43f2c-109">The **Win32\_PortableBattery** class has these types of members:</span></span>

-   [<span data-ttu-id="43f2c-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="43f2c-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="43f2c-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="43f2c-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="43f2c-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="43f2c-112">Methods</span></span>

<span data-ttu-id="43f2c-113">La classe **Win32 \_ PortableBattery** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="43f2c-113">The **Win32\_PortableBattery** class has these methods.</span></span>



| <span data-ttu-id="43f2c-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="43f2c-114">Method</span></span>            | <span data-ttu-id="43f2c-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43f2c-115">Description</span></span>                                                                                                                                                                        |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43f2c-116">**Reimpostazione**</span><span class="sxs-lookup"><span data-stu-id="43f2c-116">**Reset**</span></span>         | <span data-ttu-id="43f2c-117">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="43f2c-117">Not implemented.</span></span> <span data-ttu-id="43f2c-118">Per implementare questo metodo, vedere il metodo [**Reset**](reset-method-in-class-cim-controller.md) nella [**\_ batteria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="43f2c-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_Battery**](cim-battery.md).</span></span><br/>                 |
| <span data-ttu-id="43f2c-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="43f2c-119">**SetPowerState**</span></span> | <span data-ttu-id="43f2c-120">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="43f2c-120">Not implemented.</span></span> <span data-ttu-id="43f2c-121">Per implementare questo metodo, vedere il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) nella [**\_ batteria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="43f2c-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_Battery**](cim-battery.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="43f2c-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="43f2c-122">Properties</span></span>

<span data-ttu-id="43f2c-123">La classe **Win32 \_ PortableBattery** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="43f2c-123">The **Win32\_PortableBattery** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="43f2c-124">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="43f2c-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f2c-125">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="43f2c-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43f2c-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-127">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="43f2c-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="43f2c-128">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="43f2c-128">Availability and status of the device.</span></span>

<span data-ttu-id="43f2c-129">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="43f2c-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="43f2c-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="43f2c-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="43f2c-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="43f2c-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="43f2c-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="43f2c-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-133">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="43f2c-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="43f2c-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="43f2c-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="43f2c-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="43f2c-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="43f2c-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="43f2c-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="43f2c-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="43f2c-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="43f2c-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="43f2c-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="43f2c-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="43f2c-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="43f2c-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="43f2c-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="43f2c-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="43f2c-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="43f2c-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="43f2c-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="43f2c-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="43f2c-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-144">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="43f2c-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="43f2c-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="43f2c-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-146">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="43f2c-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="43f2c-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="43f2c-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-148">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="43f2c-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="43f2c-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="43f2c-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="43f2c-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="43f2c-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-151">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="43f2c-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="43f2c-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="43f2c-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-153">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="43f2c-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="43f2c-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="43f2c-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-155">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="43f2c-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="43f2c-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="43f2c-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-157">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="43f2c-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="43f2c-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="43f2c-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-159">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="43f2c-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="43f2c-160">**BatteryStatus**</span><span class="sxs-lookup"><span data-stu-id="43f2c-160">**BatteryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f2c-161">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="43f2c-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43f2c-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-163">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| Portable batteria \| 002,14 ")</span><span class="sxs-lookup"><span data-stu-id="43f2c-163">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.14")</span></span>
</dt> </dl>

<span data-ttu-id="43f2c-164">Descrizione dello stato di carica della batteria.</span><span class="sxs-lookup"><span data-stu-id="43f2c-164">Description of the battery's charge status.</span></span> <span data-ttu-id="43f2c-165">Il valore 10 (undefined) non è valido nello schema Common Information Model (CIM) perché in Desktop Management Interface (DMI) indica che non è installata alcuna batteria.</span><span class="sxs-lookup"><span data-stu-id="43f2c-165">The value 10 (Undefined) is not valid in the Common Information Model (CIM) schema because in Desktop Management Interface (DMI) it indicates that no battery is installed.</span></span> <span data-ttu-id="43f2c-166">In questo caso, non è necessario creare un'istanza di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="43f2c-166">In this case, this object should not be instantiated.</span></span>

<span data-ttu-id="43f2c-167">Questa proprietà viene ereditata [**dalla \_ batteria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="43f2c-167">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="43f2c-168">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="43f2c-168">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="43f2c-169">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="43f2c-169">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>

<span data-ttu-id="43f2c-170">**Costo totale** (3)</span><span class="sxs-lookup"><span data-stu-id="43f2c-170">**Fully Charged** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="43f2c-171">**Bassa** (4)</span><span class="sxs-lookup"><span data-stu-id="43f2c-171">**Low** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="43f2c-172">**Critico** (5)</span><span class="sxs-lookup"><span data-stu-id="43f2c-172">**Critical** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>

<span data-ttu-id="43f2c-173">**Addebito** (6)</span><span class="sxs-lookup"><span data-stu-id="43f2c-173">**Charging** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>

<span data-ttu-id="43f2c-174">**Addebito e elevato** (7)</span><span class="sxs-lookup"><span data-stu-id="43f2c-174">**Charging and High** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>

<span data-ttu-id="43f2c-175">**Ricarica e bassa** (8)</span><span class="sxs-lookup"><span data-stu-id="43f2c-175">**Charging and Low** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>

<span data-ttu-id="43f2c-176">**Addebito e critico** (9)</span><span class="sxs-lookup"><span data-stu-id="43f2c-176">**Charging and Critical** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="43f2c-177">Non **definito** (10)</span><span class="sxs-lookup"><span data-stu-id="43f2c-177">**Undefined** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>

<span data-ttu-id="43f2c-178">**Parzialmente addebitato** (11)</span><span class="sxs-lookup"><span data-stu-id="43f2c-178">**Partially Charged** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="43f2c-179">**CapacityMultiplier**</span><span class="sxs-lookup"><span data-stu-id="43f2c-179">**CapacityMultiplier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f2c-180">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="43f2c-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-181">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43f2c-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-182">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 22 \| Design Capacity moltiplicatore")</span><span class="sxs-lookup"><span data-stu-id="43f2c-182">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 22\|Design Capacity Multiplier")</span></span>
</dt> </dl>

<span data-ttu-id="43f2c-183">Fattore di moltiplicazione del valore di **DesignCapacity** per garantire che il valore di milliwatt hour non venga sottoposto a overflow per le implementazioni di SBDS (Smart Battery Data Specification).</span><span class="sxs-lookup"><span data-stu-id="43f2c-183">Multiplication factor of the **DesignCapacity** value to ensure that the milliwatt hour value does not overflow for Smart Battery Data Specification (SBDS) implementations.</span></span>

</dd> <dt>

<span data-ttu-id="43f2c-184">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="43f2c-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f2c-185">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="43f2c-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-186">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43f2c-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-187">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="43f2c-187">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="43f2c-188">Breve descrizione dell'oggetto, ovvero una stringa a una riga.</span><span class="sxs-lookup"><span data-stu-id="43f2c-188">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="43f2c-189">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="43f2c-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="43f2c-190">**Chimica**</span><span class="sxs-lookup"><span data-stu-id="43f2c-190">**Chemistry**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f2c-191">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="43f2c-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-192">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43f2c-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-193">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| Portable batteria \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="43f2c-193">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="43f2c-194">Chimica della batteria.</span><span class="sxs-lookup"><span data-stu-id="43f2c-194">Chemistry of the battery.</span></span>

<span data-ttu-id="43f2c-195">Questa proprietà viene ereditata [**dalla \_ batteria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="43f2c-195">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="43f2c-196">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="43f2c-196">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="43f2c-197">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="43f2c-197">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Lead_Acid"></span><span id="lead_acid"></span><span id="LEAD_ACID"></span>

<span data-ttu-id="43f2c-198">**Acido di piombo** (3)</span><span class="sxs-lookup"><span data-stu-id="43f2c-198">**Lead Acid** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Nickel_Cadmium"></span><span id="nickel_cadmium"></span><span id="NICKEL_CADMIUM"></span>

<span data-ttu-id="43f2c-199">**Nichel cadmio** (4)</span><span class="sxs-lookup"><span data-stu-id="43f2c-199">**Nickel Cadmium** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Nickel_Metal_Hydride"></span><span id="nickel_metal_hydride"></span><span id="NICKEL_METAL_HYDRIDE"></span>

<span data-ttu-id="43f2c-200">**Idruro Nickel Metal** (5)</span><span class="sxs-lookup"><span data-stu-id="43f2c-200">**Nickel Metal Hydride** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Lithium-ion"></span><span id="lithium-ion"></span><span id="LITHIUM-ION"></span>

<span data-ttu-id="43f2c-201">**Lithium-Ion** (6)</span><span class="sxs-lookup"><span data-stu-id="43f2c-201">**Lithium-ion** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Zinc_air"></span><span id="zinc_air"></span><span id="ZINC_AIR"></span>

<span data-ttu-id="43f2c-202">**Zinco aria** (7)</span><span class="sxs-lookup"><span data-stu-id="43f2c-202">**Zinc air** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Lithium_Polymer"></span><span id="lithium_polymer"></span><span id="LITHIUM_POLYMER"></span>

<span data-ttu-id="43f2c-203">**Polimero Lithium** (8)</span><span class="sxs-lookup"><span data-stu-id="43f2c-203">**Lithium Polymer** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="43f2c-204">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="43f2c-204">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f2c-205">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43f2c-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-206">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43f2c-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-207">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="43f2c-207">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="43f2c-208">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="43f2c-208">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="43f2c-209">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="43f2c-209">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="43f2c-210"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="43f2c-210"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="43f2c-211"> (0)</span><span class="sxs-lookup"><span data-stu-id="43f2c-211">(0)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-212">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="43f2c-212">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="43f2c-213"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="43f2c-213"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="43f2c-214">(1)</span><span class="sxs-lookup"><span data-stu-id="43f2c-214">(1)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-215">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="43f2c-215">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="43f2c-216"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="43f2c-216"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="43f2c-217">(2)</span><span class="sxs-lookup"><span data-stu-id="43f2c-217">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="43f2c-218"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="43f2c-218"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="43f2c-219">(3)</span><span class="sxs-lookup"><span data-stu-id="43f2c-219">(3)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-220">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="43f2c-220">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="43f2c-221"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="43f2c-221"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="43f2c-222">(4)</span><span class="sxs-lookup"><span data-stu-id="43f2c-222">(4)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-223">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="43f2c-223">Device is not working properly.</span></span> <span data-ttu-id="43f2c-224">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="43f2c-224">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="43f2c-225"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="43f2c-225"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="43f2c-226">(5)</span><span class="sxs-lookup"><span data-stu-id="43f2c-226">(5)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-227">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="43f2c-227">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="43f2c-228"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="43f2c-228"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="43f2c-229"> (6)</span><span class="sxs-lookup"><span data-stu-id="43f2c-229">(6)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-230">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="43f2c-230">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="43f2c-231"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="43f2c-231"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="43f2c-232">(7)</span><span class="sxs-lookup"><span data-stu-id="43f2c-232">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="43f2c-233"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="43f2c-233"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="43f2c-234">(8)</span><span class="sxs-lookup"><span data-stu-id="43f2c-234">(8)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-235">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="43f2c-235">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="43f2c-236"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="43f2c-236"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="43f2c-237">(9)</span><span class="sxs-lookup"><span data-stu-id="43f2c-237">(9)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-238">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="43f2c-238">Device is not working properly.</span></span> <span data-ttu-id="43f2c-239">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="43f2c-239">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="43f2c-240"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="43f2c-240"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="43f2c-241">(10)</span><span class="sxs-lookup"><span data-stu-id="43f2c-241">(10)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-242">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="43f2c-242">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="43f2c-243"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="43f2c-243"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="43f2c-244">(11)</span><span class="sxs-lookup"><span data-stu-id="43f2c-244">(11)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-245">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="43f2c-245">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="43f2c-246"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="43f2c-246"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="43f2c-247">12</span><span class="sxs-lookup"><span data-stu-id="43f2c-247">(12)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-248">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="43f2c-248">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="43f2c-249"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="43f2c-249"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="43f2c-250">(13)</span><span class="sxs-lookup"><span data-stu-id="43f2c-250">(13)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-251">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="43f2c-251">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="43f2c-252"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="43f2c-252"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="43f2c-253">(14)</span><span class="sxs-lookup"><span data-stu-id="43f2c-253">(14)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-254">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="43f2c-254">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="43f2c-255"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="43f2c-255"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="43f2c-256">(15)</span><span class="sxs-lookup"><span data-stu-id="43f2c-256">(15)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-257">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="43f2c-257">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="43f2c-258"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="43f2c-258"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="43f2c-259">(16)</span><span class="sxs-lookup"><span data-stu-id="43f2c-259">(16)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-260">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="43f2c-260">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="43f2c-261"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="43f2c-261"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="43f2c-262">(17)</span><span class="sxs-lookup"><span data-stu-id="43f2c-262">(17)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-263">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="43f2c-263">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="43f2c-264"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="43f2c-264"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="43f2c-265">(18)</span><span class="sxs-lookup"><span data-stu-id="43f2c-265">(18)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-266">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="43f2c-266">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="43f2c-267"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="43f2c-267"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="43f2c-268">(19)</span><span class="sxs-lookup"><span data-stu-id="43f2c-268">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="43f2c-269"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="43f2c-269"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="43f2c-270">(20)</span><span class="sxs-lookup"><span data-stu-id="43f2c-270">(20)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-271">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="43f2c-271">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="43f2c-272"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="43f2c-272"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="43f2c-273">(21)</span><span class="sxs-lookup"><span data-stu-id="43f2c-273">(21)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-274">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="43f2c-274">System failure.</span></span> <span data-ttu-id="43f2c-275">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="43f2c-275">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="43f2c-276">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="43f2c-276">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="43f2c-277"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="43f2c-277"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="43f2c-278">(22)</span><span class="sxs-lookup"><span data-stu-id="43f2c-278">(22)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-279">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="43f2c-279">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="43f2c-280"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="43f2c-280"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="43f2c-281">(23)</span><span class="sxs-lookup"><span data-stu-id="43f2c-281">(23)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-282">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="43f2c-282">System failure.</span></span> <span data-ttu-id="43f2c-283">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="43f2c-283">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="43f2c-284"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="43f2c-284"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="43f2c-285">(24)</span><span class="sxs-lookup"><span data-stu-id="43f2c-285">(24)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-286">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="43f2c-286">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="43f2c-287"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="43f2c-287"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="43f2c-288">(25)</span><span class="sxs-lookup"><span data-stu-id="43f2c-288">(25)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-289">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="43f2c-289">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="43f2c-290"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="43f2c-290"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="43f2c-291">(26)</span><span class="sxs-lookup"><span data-stu-id="43f2c-291">(26)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-292">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="43f2c-292">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="43f2c-293"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="43f2c-293"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="43f2c-294">(27)</span><span class="sxs-lookup"><span data-stu-id="43f2c-294">(27)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-295">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="43f2c-295">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="43f2c-296"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="43f2c-296"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="43f2c-297">(28)</span><span class="sxs-lookup"><span data-stu-id="43f2c-297">(28)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-298">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="43f2c-298">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="43f2c-299"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="43f2c-299"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="43f2c-300">(29)</span><span class="sxs-lookup"><span data-stu-id="43f2c-300">(29)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-301">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="43f2c-301">Device is disabled.</span></span> <span data-ttu-id="43f2c-302">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="43f2c-302">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="43f2c-303"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="43f2c-303"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="43f2c-304">(30)</span><span class="sxs-lookup"><span data-stu-id="43f2c-304">(30)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-305">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="43f2c-305">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="43f2c-306"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="43f2c-306"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="43f2c-307">31</span><span class="sxs-lookup"><span data-stu-id="43f2c-307">(31)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-308">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="43f2c-308">Device is not working properly.</span></span> <span data-ttu-id="43f2c-309">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="43f2c-309">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="43f2c-310">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="43f2c-310">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f2c-311">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="43f2c-311">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-312">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43f2c-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-313">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="43f2c-313">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="43f2c-314">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="43f2c-314">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="43f2c-315">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="43f2c-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="43f2c-316">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="43f2c-316">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f2c-317">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="43f2c-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-318">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43f2c-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-319">Qualificatori: [ **\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="43f2c-319">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="43f2c-320">Nome della prima classe concreta visualizzata nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="43f2c-320">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="43f2c-321">Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="43f2c-321">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="43f2c-322">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="43f2c-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="43f2c-323">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="43f2c-323">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f2c-324">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="43f2c-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-325">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43f2c-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-326">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="43f2c-326">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="43f2c-327">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="43f2c-327">Description of the object.</span></span>

<span data-ttu-id="43f2c-328">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="43f2c-328">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="43f2c-329">**DesignCapacity**</span><span class="sxs-lookup"><span data-stu-id="43f2c-329">**DesignCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f2c-330">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43f2c-330">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-331">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43f2c-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-332">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| Portable batteria \| 002,8 "), [**unità**](../wmisdk/standard-qualifiers.md) (" milliwatt-ore ")</span><span class="sxs-lookup"><span data-stu-id="43f2c-332">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.8"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="43f2c-333">Capacità di progettazione della batteria in milliwatt ore.</span><span class="sxs-lookup"><span data-stu-id="43f2c-333">Design capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="43f2c-334">Se questa proprietà non è supportata, immettere 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="43f2c-334">If this property is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="43f2c-335">Questa proprietà viene ereditata [**dalla \_ batteria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="43f2c-335">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="43f2c-336">**DesignVoltage**</span><span class="sxs-lookup"><span data-stu-id="43f2c-336">**DesignVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f2c-337">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="43f2c-337">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-338">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43f2c-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-339">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| Portable batteria \| 002,9 "), [**unità**](../wmisdk/standard-qualifiers.md) (" millivolt ")</span><span class="sxs-lookup"><span data-stu-id="43f2c-339">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.9"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="43f2c-340">Tensione di progettazione della batteria in millivolt.</span><span class="sxs-lookup"><span data-stu-id="43f2c-340">Design voltage of the battery in millivolts.</span></span> <span data-ttu-id="43f2c-341">Se questo attributo non è supportato, immettere 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="43f2c-341">If this attribute is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="43f2c-342">Questa proprietà viene ereditata [**dalla \_ batteria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="43f2c-342">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<span data-ttu-id="43f2c-343">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="43f2c-343">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="43f2c-344">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="43f2c-344">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f2c-345">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="43f2c-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-346">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43f2c-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-347">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="43f2c-347">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="43f2c-348">Identificatore della batteria.</span><span class="sxs-lookup"><span data-stu-id="43f2c-348">Battery identifier.</span></span>

<span data-ttu-id="43f2c-349">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="43f2c-349">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="43f2c-350">Esempio: "batteria interna"</span><span class="sxs-lookup"><span data-stu-id="43f2c-350">Example: "Internal Battery"</span></span>

</dd> <dt>

<span data-ttu-id="43f2c-351">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="43f2c-351">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f2c-352">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="43f2c-352">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-353">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43f2c-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43f2c-354">Se **true**, l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="43f2c-354">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="43f2c-355">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="43f2c-355">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="43f2c-356">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="43f2c-356">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f2c-357">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="43f2c-357">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-358">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43f2c-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43f2c-359">Altre informazioni sull'errore registrato in **LastErrorCode** ed eventuali azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="43f2c-359">More information about the error recorded in **LastErrorCode**, and any corrective actions that may be taken.</span></span>

<span data-ttu-id="43f2c-360">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="43f2c-360">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="43f2c-361">**EstimatedChargeRemaining**</span><span class="sxs-lookup"><span data-stu-id="43f2c-361">**EstimatedChargeRemaining**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f2c-362">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="43f2c-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-363">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43f2c-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-364">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("percentuale")</span><span class="sxs-lookup"><span data-stu-id="43f2c-364">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="43f2c-365">Stima della percentuale di costo totale rimanente.</span><span class="sxs-lookup"><span data-stu-id="43f2c-365">Estimate of the percentage of full charge remaining.</span></span>

<span data-ttu-id="43f2c-366">Questa proprietà viene ereditata [**dalla \_ batteria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="43f2c-366">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="43f2c-367">**EstimatedRunTime**</span><span class="sxs-lookup"><span data-stu-id="43f2c-367">**EstimatedRunTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f2c-368">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43f2c-368">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-369">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43f2c-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-370">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| Portable batteria \| 002,15 "), [**unità**](../wmisdk/standard-qualifiers.md) (" minuti ")</span><span class="sxs-lookup"><span data-stu-id="43f2c-370">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.15"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="43f2c-371">Stima in minuti del tempo di esaurimento della carica della batteria sotto le condizioni di carico attuali se l'alimentazione dell'utilità è disattivata o persa e rimane spenta o se un portatile è disconnesso da una fonte di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="43f2c-371">Estimate in minutes of the time to battery charge depletion under the present load conditions if the utility power is off, or lost and remains off, or a laptop is disconnected from a power source.</span></span>

<span data-ttu-id="43f2c-372">Questa proprietà viene ereditata [**dalla \_ batteria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="43f2c-372">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="43f2c-373">**ExpectedBatteryLife**</span><span class="sxs-lookup"><span data-stu-id="43f2c-373">**ExpectedBatteryLife**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f2c-374">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43f2c-374">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-375">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43f2c-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43f2c-376">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="43f2c-376">Not supported.</span></span>

<span data-ttu-id="43f2c-377">Questa proprietà viene ereditata [**dalla \_ batteria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="43f2c-377">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="43f2c-378">**ExpectedLife**</span><span class="sxs-lookup"><span data-stu-id="43f2c-378">**ExpectedLife**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f2c-379">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43f2c-379">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-380">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43f2c-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-381">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("minuti")</span><span class="sxs-lookup"><span data-stu-id="43f2c-381">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="43f2c-382">Durata prevista della batteria in minuti, presupponendo che la batteria venga addebitata completamente.</span><span class="sxs-lookup"><span data-stu-id="43f2c-382">Battery's expected lifetime in minutes, assuming that the battery is fully charged.</span></span> <span data-ttu-id="43f2c-383">Questa proprietà rappresenta la durata totale prevista della batteria, non la durata rimanente corrente, indicata dalla proprietà **EstimatedRunTime** .</span><span class="sxs-lookup"><span data-stu-id="43f2c-383">This property represents the total expected life of the battery, not its current remaining life, which is indicated by the **EstimatedRunTime** property.</span></span>

<span data-ttu-id="43f2c-384">Questa proprietà viene ereditata [**dalla \_ batteria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="43f2c-384">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="43f2c-385">**FullChargeCapacity**</span><span class="sxs-lookup"><span data-stu-id="43f2c-385">**FullChargeCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f2c-386">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43f2c-386">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-387">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43f2c-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-388">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| Portable batteria \| 002,11 "), [**unità**](../wmisdk/standard-qualifiers.md) (" milliwatt-ore ")</span><span class="sxs-lookup"><span data-stu-id="43f2c-388">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.11"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="43f2c-389">Capacità di addebito completo della batteria in milliwatt ore.</span><span class="sxs-lookup"><span data-stu-id="43f2c-389">Full charge capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="43f2c-390">Il confronto di questo valore con la proprietà **DesignCapacity** determina quando la batteria richiede la sostituzione.</span><span class="sxs-lookup"><span data-stu-id="43f2c-390">Comparison of this value to the **DesignCapacity** property determines when the battery requires replacement.</span></span> <span data-ttu-id="43f2c-391">La fine della durata della batteria è in genere quando la proprietà **FullChargeCapacity** è inferiore al 80% della proprietà **DesignCapacity** .</span><span class="sxs-lookup"><span data-stu-id="43f2c-391">A battery's end of life is typically when the **FullChargeCapacity** property falls below 80% of the **DesignCapacity** property.</span></span> <span data-ttu-id="43f2c-392">Se questa proprietà non è supportata, immettere 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="43f2c-392">If this property is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="43f2c-393">Questa proprietà viene ereditata [**dalla \_ batteria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="43f2c-393">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="43f2c-394">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="43f2c-394">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f2c-395">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="43f2c-395">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-396">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43f2c-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-397">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="43f2c-397">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="43f2c-398">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="43f2c-398">Date and time the object was installed.</span></span> <span data-ttu-id="43f2c-399">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="43f2c-399">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="43f2c-400">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="43f2c-400">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="43f2c-401">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="43f2c-401">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f2c-402">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43f2c-402">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-403">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43f2c-403">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43f2c-404">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="43f2c-404">Last error code reported by the logical device.</span></span>

<span data-ttu-id="43f2c-405">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="43f2c-405">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="43f2c-406">**Posizione**</span><span class="sxs-lookup"><span data-stu-id="43f2c-406">**Location**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f2c-407">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="43f2c-407">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-408">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43f2c-408">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-409">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 22 \| location")</span><span class="sxs-lookup"><span data-stu-id="43f2c-409">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 22\|Location")</span></span>
</dt> </dl>

<span data-ttu-id="43f2c-410">Posizione fisica della batteria.</span><span class="sxs-lookup"><span data-stu-id="43f2c-410">Physical location of the battery.</span></span> <span data-ttu-id="43f2c-411">Questa proprietà viene compilata dal produttore del computer.</span><span class="sxs-lookup"><span data-stu-id="43f2c-411">This property is filled by the computer manufacturer.</span></span>

<span data-ttu-id="43f2c-412">Esempio: "nella parte posteriore, a sinistra"</span><span class="sxs-lookup"><span data-stu-id="43f2c-412">Example: "In the back, on the left"</span></span>

</dd> <dt>

<span data-ttu-id="43f2c-413">**Prodotto**</span><span class="sxs-lookup"><span data-stu-id="43f2c-413">**ManufactureDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f2c-414">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="43f2c-414">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-415">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43f2c-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-416">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 22 \| Manufacture Date")</span><span class="sxs-lookup"><span data-stu-id="43f2c-416">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 22\|Manufacture Date")</span></span>
</dt> </dl>

<span data-ttu-id="43f2c-417">Data di produzione della batteria.</span><span class="sxs-lookup"><span data-stu-id="43f2c-417">Date when the battery was manufactured.</span></span>

</dd> <dt>

<span data-ttu-id="43f2c-418">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="43f2c-418">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f2c-419">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="43f2c-419">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-420">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43f2c-420">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-421">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 22 \| Manufacturer")</span><span class="sxs-lookup"><span data-stu-id="43f2c-421">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 22\|Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="43f2c-422">Produttore della batteria.</span><span class="sxs-lookup"><span data-stu-id="43f2c-422">Manufacturer of the battery.</span></span>

</dd> <dt>

<span data-ttu-id="43f2c-423">**MaxBatteryError**</span><span class="sxs-lookup"><span data-stu-id="43f2c-423">**MaxBatteryError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f2c-424">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="43f2c-424">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-425">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43f2c-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-426">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| tipo 22 \| errore massimo nei dati della batteria"), [**unità**](../wmisdk/standard-qualifiers.md) ("percentuale")</span><span class="sxs-lookup"><span data-stu-id="43f2c-426">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 22\|Maximum Error in Battery Data"), [**Units**](../wmisdk/standard-qualifiers.md) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="43f2c-427">Differenza tra la quantità più elevata di energia rimanente nella batteria e la quantità corrente indicata dalla batteria.</span><span class="sxs-lookup"><span data-stu-id="43f2c-427">Difference between the highest estimated amount of energy left in the battery and the current amount reported by the battery.</span></span>

</dd> <dt>

<span data-ttu-id="43f2c-428">**MaxRechargeTime**</span><span class="sxs-lookup"><span data-stu-id="43f2c-428">**MaxRechargeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f2c-429">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43f2c-429">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-430">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43f2c-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-431">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("minuti")</span><span class="sxs-lookup"><span data-stu-id="43f2c-431">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="43f2c-432">Tempo massimo, in minuti, per l'addebito completo della batteria.</span><span class="sxs-lookup"><span data-stu-id="43f2c-432">Maximum time, in minutes, to fully charge the battery.</span></span> <span data-ttu-id="43f2c-433">Questa proprietà rappresenta il tempo per ricaricare una batteria completamente esaurita, non il tempo di ricarica rimanente corrente, indicato nella proprietà **TimeToFullCharge** .</span><span class="sxs-lookup"><span data-stu-id="43f2c-433">This property represents the time to recharge a fully depleted battery, not the current remaining charge time, which is indicated in the **TimeToFullCharge** property.</span></span>

<span data-ttu-id="43f2c-434">Questa proprietà viene ereditata [**dalla \_ batteria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="43f2c-434">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="43f2c-435">**Nome**</span><span class="sxs-lookup"><span data-stu-id="43f2c-435">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f2c-436">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="43f2c-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-437">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43f2c-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-438">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="43f2c-438">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="43f2c-439">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="43f2c-439">Label by which the object is known.</span></span> <span data-ttu-id="43f2c-440">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="43f2c-440">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="43f2c-441">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="43f2c-441">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="43f2c-442">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="43f2c-442">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f2c-443">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="43f2c-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-444">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43f2c-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-445">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="43f2c-445">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="43f2c-446">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="43f2c-446">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="43f2c-447">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="43f2c-447">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="43f2c-448">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="43f2c-448">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="43f2c-449">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="43f2c-449">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f2c-450">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="43f2c-450">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-451">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43f2c-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43f2c-452">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="43f2c-452">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="43f2c-453">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="43f2c-453">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="43f2c-454"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="43f2c-454"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="43f2c-455"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="43f2c-455"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="43f2c-456"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="43f2c-456"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="43f2c-457"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="43f2c-457"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-458">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="43f2c-458">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="43f2c-459"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="43f2c-459"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-460">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="43f2c-460">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="43f2c-461"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="43f2c-461"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-462">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="43f2c-462">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="43f2c-463">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="43f2c-463">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="43f2c-464">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="43f2c-464">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="43f2c-465"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="43f2c-465"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-466">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="43f2c-466">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="43f2c-467"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="43f2c-467"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="43f2c-468">Tempo Power-On supportato</span><span class="sxs-lookup"><span data-stu-id="43f2c-468">Timed Power-On Supported</span></span>

<span data-ttu-id="43f2c-469">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="43f2c-469">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="43f2c-470">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="43f2c-470">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f2c-471">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="43f2c-471">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-472">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43f2c-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43f2c-473">Se **true**, il dispositivo può essere gestito dal risparmio di energia (può essere impostato in modalità di sospensione e così via).</span><span class="sxs-lookup"><span data-stu-id="43f2c-473">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="43f2c-474">La proprietà non indica che le funzionalità di risparmio energia sono attualmente abilitate, solo che il dispositivo logico è in grado di gestire il risparmio di energia.</span><span class="sxs-lookup"><span data-stu-id="43f2c-474">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="43f2c-475">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="43f2c-475">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="43f2c-476">**SmartBatteryVersion**</span><span class="sxs-lookup"><span data-stu-id="43f2c-476">**SmartBatteryVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f2c-477">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="43f2c-477">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-478">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43f2c-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-479">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| Portable batteria \| 002,10 ")</span><span class="sxs-lookup"><span data-stu-id="43f2c-479">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.10")</span></span>
</dt> </dl>

<span data-ttu-id="43f2c-480">Numero di versione della specifica dei dati della batteria intelligente supportato da questa batteria.</span><span class="sxs-lookup"><span data-stu-id="43f2c-480">Smart Battery Data Specification version number supported by this battery.</span></span> <span data-ttu-id="43f2c-481">Se la batteria non supporta questa funzione, il valore deve essere lasciato vuoto.</span><span class="sxs-lookup"><span data-stu-id="43f2c-481">If the battery does not support this function, the value should be left blank.</span></span>

<span data-ttu-id="43f2c-482">Questa proprietà viene ereditata [**dalla \_ batteria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="43f2c-482">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="43f2c-483">**Status**</span><span class="sxs-lookup"><span data-stu-id="43f2c-483">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f2c-484">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="43f2c-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-485">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43f2c-485">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-486">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="43f2c-486">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="43f2c-487">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="43f2c-487">Current status of the object.</span></span> <span data-ttu-id="43f2c-488">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="43f2c-488">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="43f2c-489">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="43f2c-489">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="43f2c-490">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="43f2c-490">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="43f2c-491">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="43f2c-491">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="43f2c-492">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="43f2c-492">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="43f2c-493">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="43f2c-493">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="43f2c-494">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="43f2c-494">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="43f2c-495">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="43f2c-495">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="43f2c-496">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="43f2c-496">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="43f2c-497">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="43f2c-497">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="43f2c-498">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="43f2c-498">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="43f2c-499">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="43f2c-499">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="43f2c-500">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="43f2c-500">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="43f2c-501">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="43f2c-501">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="43f2c-502">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="43f2c-502">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="43f2c-503">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="43f2c-503">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="43f2c-504">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="43f2c-504">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="43f2c-505">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="43f2c-505">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="43f2c-506">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="43f2c-506">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="43f2c-507">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="43f2c-507">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f2c-508">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="43f2c-508">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-509">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43f2c-509">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-510">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="43f2c-510">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="43f2c-511">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="43f2c-511">State of the logical device.</span></span> <span data-ttu-id="43f2c-512">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="43f2c-512">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="43f2c-513">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="43f2c-513">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="43f2c-514">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="43f2c-514">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="43f2c-515">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="43f2c-515">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="43f2c-516">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="43f2c-516">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="43f2c-517">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="43f2c-517">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="43f2c-518">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="43f2c-518">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="43f2c-519">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="43f2c-519">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f2c-520">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="43f2c-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-521">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43f2c-521">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-522">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="43f2c-522">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="43f2c-523">Valore della proprietà **CreationClassName** del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="43f2c-523">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="43f2c-524">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="43f2c-524">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="43f2c-525">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="43f2c-525">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f2c-526">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="43f2c-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-527">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43f2c-527">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-528">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="43f2c-528">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="43f2c-529">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="43f2c-529">Name of the scoping system.</span></span>

<span data-ttu-id="43f2c-530">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="43f2c-530">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="43f2c-531">**TimeOnBattery**</span><span class="sxs-lookup"><span data-stu-id="43f2c-531">**TimeOnBattery**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f2c-532">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43f2c-532">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-533">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43f2c-533">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-534">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("secondi")</span><span class="sxs-lookup"><span data-stu-id="43f2c-534">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="43f2c-535">Tempo trascorso in secondi dall'ultima volta in cui l'UPS del sistema informatico passa alla potenza della batteria oppure il tempo trascorso dall'ultimo riavvio del sistema o dell'UPS, a seconda del numero minore.</span><span class="sxs-lookup"><span data-stu-id="43f2c-535">Elapsed time in seconds since the computer system's UPS last switched to battery power, or the time since the system or UPS was last restarted, whichever is less.</span></span> <span data-ttu-id="43f2c-536">Se la batteria è online, viene restituito 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="43f2c-536">If the battery is online, 0 (zero) is returned.</span></span>

<span data-ttu-id="43f2c-537">Questa proprietà viene ereditata [**dalla \_ batteria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="43f2c-537">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="43f2c-538">**TimeToFullCharge**</span><span class="sxs-lookup"><span data-stu-id="43f2c-538">**TimeToFullCharge**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f2c-539">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43f2c-539">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-540">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43f2c-540">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f2c-541">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| Portable batteria \| 002,16 "), [**unità**](../wmisdk/standard-qualifiers.md) (" minuti ")</span><span class="sxs-lookup"><span data-stu-id="43f2c-541">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.16"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="43f2c-542">Tempo rimanente in minuti per l'addebito completo della batteria alla tariffa e all'utilizzo correnti.</span><span class="sxs-lookup"><span data-stu-id="43f2c-542">Remaining time in minutes to charge the battery fully at the current charge rate and usage.</span></span>

<span data-ttu-id="43f2c-543">Questa proprietà viene ereditata [**dalla \_ batteria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="43f2c-543">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="43f2c-544">Commenti</span><span class="sxs-lookup"><span data-stu-id="43f2c-544">Remarks</span></span>

<span data-ttu-id="43f2c-545">La classe **Win32 \_ PortableBattery** è derivata dalla [**\_ batteria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="43f2c-545">The **Win32\_PortableBattery** class is derived from [**CIM\_Battery**](cim-battery.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="43f2c-546">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43f2c-546">Requirements</span></span>



| <span data-ttu-id="43f2c-547">Requisito</span><span class="sxs-lookup"><span data-stu-id="43f2c-547">Requirement</span></span> | <span data-ttu-id="43f2c-548">Valore</span><span class="sxs-lookup"><span data-stu-id="43f2c-548">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43f2c-549">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43f2c-549">Minimum supported client</span></span><br/> | <span data-ttu-id="43f2c-550">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="43f2c-550">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="43f2c-551">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43f2c-551">Minimum supported server</span></span><br/> | <span data-ttu-id="43f2c-552">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="43f2c-552">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="43f2c-553">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="43f2c-553">Namespace</span></span><br/>                | <span data-ttu-id="43f2c-554">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="43f2c-554">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="43f2c-555">MOF</span><span class="sxs-lookup"><span data-stu-id="43f2c-555">MOF</span></span><br/>                      | <dl> <span data-ttu-id="43f2c-556"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="43f2c-556"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="43f2c-557">DLL</span><span class="sxs-lookup"><span data-stu-id="43f2c-557">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43f2c-558"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43f2c-558"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43f2c-559">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="43f2c-559">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43f2c-560">**\_Batteria CIM**</span><span class="sxs-lookup"><span data-stu-id="43f2c-560">**CIM\_Battery**</span></span>](cim-battery.md)
</dt> <dt>

[<span data-ttu-id="43f2c-561">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="43f2c-561">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 

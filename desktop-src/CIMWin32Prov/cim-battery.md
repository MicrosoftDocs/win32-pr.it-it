---
description: La \_ classe CIM batteria rappresenta le funzionalità e la gestione del dispositivo logico della batteria. Questa classe si applica alle batterie nei sistemi portatili e altre batterie interne ed esterne.
ms.assetid: af127b7a-021b-4cd8-af1b-176aff760858
ms.tgt_platform: multiple
title: Classe CIM_Battery
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Battery
- CIM_Battery.Caption
- CIM_Battery.Description
- CIM_Battery.InstallDate
- CIM_Battery.Name
- CIM_Battery.Status
- CIM_Battery.Availability
- CIM_Battery.ConfigManagerErrorCode
- CIM_Battery.ConfigManagerUserConfig
- CIM_Battery.CreationClassName
- CIM_Battery.DeviceID
- CIM_Battery.PowerManagementCapabilities
- CIM_Battery.ErrorCleared
- CIM_Battery.ErrorDescription
- CIM_Battery.LastErrorCode
- CIM_Battery.PNPDeviceID
- CIM_Battery.PowerManagementSupported
- CIM_Battery.StatusInfo
- CIM_Battery.SystemCreationClassName
- CIM_Battery.SystemName
- CIM_Battery.BatteryStatus
- CIM_Battery.Chemistry
- CIM_Battery.DesignCapacity
- CIM_Battery.DesignVoltage
- CIM_Battery.EstimatedChargeRemaining
- CIM_Battery.EstimatedRunTime
- CIM_Battery.ExpectedLife
- CIM_Battery.FullChargeCapacity
- CIM_Battery.MaxRechargeTime
- CIM_Battery.SmartBatteryVersion
- CIM_Battery.TimeOnBattery
- CIM_Battery.TimeToFullCharge
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3719b2700c69cfa58921bed1242aa8a6de158466
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305039"
---
# <a name="cim_battery-class"></a><span data-ttu-id="5efcb-104">\_Classe CIM Battery</span><span class="sxs-lookup"><span data-stu-id="5efcb-104">CIM\_Battery class</span></span>

<span data-ttu-id="5efcb-105">La classe **CIM \_ batteria** rappresenta le funzionalità e la gestione del dispositivo logico della batteria.</span><span class="sxs-lookup"><span data-stu-id="5efcb-105">The **CIM\_Battery** class represents the capabilities and management of the battery logical device.</span></span> <span data-ttu-id="5efcb-106">Questa classe si applica alle batterie nei sistemi portatili e altre batterie interne ed esterne.</span><span class="sxs-lookup"><span data-stu-id="5efcb-106">This class applies to batteries in laptop systems and other internal and external batteries.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5efcb-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="5efcb-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5efcb-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5efcb-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5efcb-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5efcb-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5efcb-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="5efcb-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5efcb-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5efcb-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C548-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Battery : CIM_LogicalDevice
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
  uint16   BatteryStatus;
  uint16   Chemistry;
  uint32   DesignCapacity;
  uint64   DesignVoltage;
  uint16   EstimatedChargeRemaining;
  uint32   EstimatedRunTime;
  uint32   ExpectedLife;
  uint32   FullChargeCapacity;
  uint32   MaxRechargeTime;
  string   SmartBatteryVersion;
  uint32   TimeOnBattery;
  uint32   TimeToFullCharge;
};
```

## <a name="members"></a><span data-ttu-id="5efcb-112">Members</span><span class="sxs-lookup"><span data-stu-id="5efcb-112">Members</span></span>

<span data-ttu-id="5efcb-113">La classe **CIM \_ Battery** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5efcb-113">The **CIM\_Battery** class has these types of members:</span></span>

-   [<span data-ttu-id="5efcb-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="5efcb-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="5efcb-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5efcb-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5efcb-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="5efcb-116">Methods</span></span>

<span data-ttu-id="5efcb-117">La classe **CIM \_ Battery** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="5efcb-117">The **CIM\_Battery** class has these methods.</span></span>



| <span data-ttu-id="5efcb-118">Metodo</span><span class="sxs-lookup"><span data-stu-id="5efcb-118">Method</span></span>                                                             | <span data-ttu-id="5efcb-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5efcb-119">Description</span></span>                                                                                                                                |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5efcb-120">**Reset**</span><span class="sxs-lookup"><span data-stu-id="5efcb-120">**Reset**</span></span>](reset-method-in-class-cim-battery.md)                 | <span data-ttu-id="5efcb-121">Richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="5efcb-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="5efcb-122">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="5efcb-122">Not implemented by WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="5efcb-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="5efcb-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-battery.md) | <span data-ttu-id="5efcb-124">Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando il dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="5efcb-124">Defines the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="5efcb-125">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="5efcb-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5efcb-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5efcb-126">Properties</span></span>

<span data-ttu-id="5efcb-127">La classe **CIM \_ Battery** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5efcb-127">The **CIM\_Battery** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5efcb-128">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="5efcb-128">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efcb-129">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5efcb-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5efcb-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-131">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="5efcb-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="5efcb-132">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5efcb-132">Availability and status of the device.</span></span>

<span data-ttu-id="5efcb-133">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5efcb-133">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5efcb-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="5efcb-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5efcb-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="5efcb-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="5efcb-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="5efcb-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="5efcb-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="5efcb-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="5efcb-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="5efcb-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="5efcb-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="5efcb-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="5efcb-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="5efcb-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="5efcb-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="5efcb-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="5efcb-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="5efcb-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5efcb-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="5efcb-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="5efcb-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="5efcb-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="5efcb-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="5efcb-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="5efcb-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="5efcb-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="5efcb-147">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="5efcb-147">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="5efcb-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="5efcb-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="5efcb-149">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="5efcb-149">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="5efcb-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="5efcb-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="5efcb-151">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="5efcb-151">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="5efcb-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="5efcb-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="5efcb-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="5efcb-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="5efcb-154">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="5efcb-154">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="5efcb-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="5efcb-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="5efcb-156">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="5efcb-156">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="5efcb-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="5efcb-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="5efcb-158">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="5efcb-158">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="5efcb-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="5efcb-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="5efcb-160">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="5efcb-160">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="5efcb-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="5efcb-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="5efcb-162">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="5efcb-162">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5efcb-163">**BatteryStatus**</span><span class="sxs-lookup"><span data-stu-id="5efcb-163">**BatteryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efcb-164">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5efcb-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5efcb-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-166">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Portable batteria \| 002,14 ")</span><span class="sxs-lookup"><span data-stu-id="5efcb-166">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.14")</span></span>
</dt> </dl>

<span data-ttu-id="5efcb-167">Descrizione dello stato di carica della batteria.</span><span class="sxs-lookup"><span data-stu-id="5efcb-167">Description of the battery's charge status.</span></span> <span data-ttu-id="5efcb-168">Il valore 10 non è valido nello schema CIM, che non rappresenta la batteria installata in Desktop Management Interface (DMI).</span><span class="sxs-lookup"><span data-stu-id="5efcb-168">The value 10 is not valid in the CIM schema, which represents no battery being installed in Desktop Management Interface (DMI).</span></span> <span data-ttu-id="5efcb-169">In questo caso, non è necessario creare un'istanza dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5efcb-169">In this case, the object should not be instantiated.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5efcb-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="5efcb-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5efcb-171">Altro.</span><span class="sxs-lookup"><span data-stu-id="5efcb-171">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5efcb-172"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="5efcb-172"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5efcb-173">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="5efcb-173">Unknown.</span></span>

</dd> <dt>

<span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>

<span data-ttu-id="5efcb-174"><span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>**Costo totale** (3)</span><span class="sxs-lookup"><span data-stu-id="5efcb-174"><span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>**Fully Charged** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5efcb-175">Completamente addebitato.</span><span class="sxs-lookup"><span data-stu-id="5efcb-175">Fully charged.</span></span>

</dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="5efcb-176"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Bassa** (4)</span><span class="sxs-lookup"><span data-stu-id="5efcb-176"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (4)</span></span>


</dt> <dd>

<span data-ttu-id="5efcb-177">Bassa.</span><span class="sxs-lookup"><span data-stu-id="5efcb-177">Low.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="5efcb-178"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critico** (5)</span><span class="sxs-lookup"><span data-stu-id="5efcb-178"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (5)</span></span>


</dt> <dd>

<span data-ttu-id="5efcb-179">Critica.</span><span class="sxs-lookup"><span data-stu-id="5efcb-179">Critical.</span></span>

</dd> <dt>

<span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>

<span data-ttu-id="5efcb-180"><span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>**Addebito** (6)</span><span class="sxs-lookup"><span data-stu-id="5efcb-180"><span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>**Charging** (6)</span></span>


</dt> <dd>

<span data-ttu-id="5efcb-181">Addebito.</span><span class="sxs-lookup"><span data-stu-id="5efcb-181">Charging.</span></span>

</dd> <dt>

<span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>

<span data-ttu-id="5efcb-182"><span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>**Addebito e elevato** (7)</span><span class="sxs-lookup"><span data-stu-id="5efcb-182"><span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>**Charging and High** (7)</span></span>


</dt> <dd>

<span data-ttu-id="5efcb-183">Addebito e alto.</span><span class="sxs-lookup"><span data-stu-id="5efcb-183">Charging and high.</span></span>

</dd> <dt>

<span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>

<span data-ttu-id="5efcb-184"><span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>**Ricarica e bassa** (8)</span><span class="sxs-lookup"><span data-stu-id="5efcb-184"><span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>**Charging and Low** (8)</span></span>


</dt> <dd>

<span data-ttu-id="5efcb-185">Ricarica e bassa.</span><span class="sxs-lookup"><span data-stu-id="5efcb-185">Charging and low.</span></span>

</dd> <dt>

<span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>

<span data-ttu-id="5efcb-186"><span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>**Addebito e critico** (9)</span><span class="sxs-lookup"><span data-stu-id="5efcb-186"><span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>**Charging and Critical** (9)</span></span>


</dt> <dd>

<span data-ttu-id="5efcb-187">Addebito e critico.</span><span class="sxs-lookup"><span data-stu-id="5efcb-187">Charging and critical.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="5efcb-188"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>Non **definito** (10)</span><span class="sxs-lookup"><span data-stu-id="5efcb-188"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (10)</span></span>


</dt> <dd>

<span data-ttu-id="5efcb-189">Non definito.</span><span class="sxs-lookup"><span data-stu-id="5efcb-189">Undefined.</span></span>

</dd> <dt>

<span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>

<span data-ttu-id="5efcb-190"><span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>**Parzialmente addebitato** (11)</span><span class="sxs-lookup"><span data-stu-id="5efcb-190"><span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>**Partially Charged** (11)</span></span>


</dt> <dd>

<span data-ttu-id="5efcb-191">Addebitato parzialmente.</span><span class="sxs-lookup"><span data-stu-id="5efcb-191">Partially charged.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5efcb-192">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="5efcb-192">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efcb-193">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5efcb-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-194">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5efcb-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-195">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="5efcb-195">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="5efcb-196">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5efcb-196">A short textual description of the object.</span></span>

<span data-ttu-id="5efcb-197">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5efcb-197">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5efcb-198">**Chimica**</span><span class="sxs-lookup"><span data-stu-id="5efcb-198">**Chemistry**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efcb-199">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5efcb-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-200">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5efcb-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-201">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Portable batteria \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="5efcb-201">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="5efcb-202">Enumerazione che descrive la chimica della batteria.</span><span class="sxs-lookup"><span data-stu-id="5efcb-202">Enumeration that describes the battery's chemistry.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5efcb-203"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="5efcb-203"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5efcb-204">Altro.</span><span class="sxs-lookup"><span data-stu-id="5efcb-204">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5efcb-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="5efcb-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5efcb-206">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="5efcb-206">Unknown.</span></span>

</dd> <dt>

<span id="Lead_Acid"></span><span id="lead_acid"></span><span id="LEAD_ACID"></span>

<span data-ttu-id="5efcb-207"><span id="Lead_Acid"></span><span id="lead_acid"></span><span id="LEAD_ACID"></span>**Acido di piombo** (3)</span><span class="sxs-lookup"><span data-stu-id="5efcb-207"><span id="Lead_Acid"></span><span id="lead_acid"></span><span id="LEAD_ACID"></span>**Lead Acid** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5efcb-208">Acido principale.</span><span class="sxs-lookup"><span data-stu-id="5efcb-208">Lead acid.</span></span>

</dd> <dt>

<span id="Nickel_Cadmium"></span><span id="nickel_cadmium"></span><span id="NICKEL_CADMIUM"></span>

<span data-ttu-id="5efcb-209"><span id="Nickel_Cadmium"></span><span id="nickel_cadmium"></span><span id="NICKEL_CADMIUM"></span>**Nichel cadmio** (4)</span><span class="sxs-lookup"><span data-stu-id="5efcb-209"><span id="Nickel_Cadmium"></span><span id="nickel_cadmium"></span><span id="NICKEL_CADMIUM"></span>**Nickel Cadmium** (4)</span></span>


</dt> <dd>

<span data-ttu-id="5efcb-210">Nichel cadmio.</span><span class="sxs-lookup"><span data-stu-id="5efcb-210">Nickel cadmium.</span></span>

</dd> <dt>

<span id="Nickel_Metal_Hydride"></span><span id="nickel_metal_hydride"></span><span id="NICKEL_METAL_HYDRIDE"></span>

<span data-ttu-id="5efcb-211"><span id="Nickel_Metal_Hydride"></span><span id="nickel_metal_hydride"></span><span id="NICKEL_METAL_HYDRIDE"></span>**Idruro Nickel Metal** (5)</span><span class="sxs-lookup"><span data-stu-id="5efcb-211"><span id="Nickel_Metal_Hydride"></span><span id="nickel_metal_hydride"></span><span id="NICKEL_METAL_HYDRIDE"></span>**Nickel Metal Hydride** (5)</span></span>


</dt> <dd>

<span data-ttu-id="5efcb-212">Idruro Nickel metal.</span><span class="sxs-lookup"><span data-stu-id="5efcb-212">Nickel metal hydride.</span></span>

</dd> <dt>

<span id="Lithium-ion"></span><span id="lithium-ion"></span><span id="LITHIUM-ION"></span>

<span data-ttu-id="5efcb-213"><span id="Lithium-ion"></span><span id="lithium-ion"></span><span id="LITHIUM-ION"></span>**Lithium-Ion** (6)</span><span class="sxs-lookup"><span data-stu-id="5efcb-213"><span id="Lithium-ion"></span><span id="lithium-ion"></span><span id="LITHIUM-ION"></span>**Lithium-ion** (6)</span></span>


</dt> <dd>

<span data-ttu-id="5efcb-214">Ioni di litio.</span><span class="sxs-lookup"><span data-stu-id="5efcb-214">Lithium ion.</span></span>

</dd> <dt>

<span id="Zinc_air"></span><span id="zinc_air"></span><span id="ZINC_AIR"></span>

<span data-ttu-id="5efcb-215"><span id="Zinc_air"></span><span id="zinc_air"></span><span id="ZINC_AIR"></span>**Zinco aria** (7)</span><span class="sxs-lookup"><span data-stu-id="5efcb-215"><span id="Zinc_air"></span><span id="zinc_air"></span><span id="ZINC_AIR"></span>**Zinc air** (7)</span></span>


</dt> <dd>

<span data-ttu-id="5efcb-216">Aria zincata.</span><span class="sxs-lookup"><span data-stu-id="5efcb-216">Zinc air.</span></span>

</dd> <dt>

<span id="Lithium_Polymer"></span><span id="lithium_polymer"></span><span id="LITHIUM_POLYMER"></span>

<span data-ttu-id="5efcb-217"><span id="Lithium_Polymer"></span><span id="lithium_polymer"></span><span id="LITHIUM_POLYMER"></span>**Polimero Lithium** (8)</span><span class="sxs-lookup"><span data-stu-id="5efcb-217"><span id="Lithium_Polymer"></span><span id="lithium_polymer"></span><span id="LITHIUM_POLYMER"></span>**Lithium Polymer** (8)</span></span>


</dt> <dd>

<span data-ttu-id="5efcb-218">Polimero Lithium.</span><span class="sxs-lookup"><span data-stu-id="5efcb-218">Lithium polymer.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5efcb-219">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="5efcb-219">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efcb-220">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5efcb-220">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-221">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5efcb-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-222">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5efcb-222">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5efcb-223">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="5efcb-223">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="5efcb-224">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5efcb-224">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="5efcb-225">**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="5efcb-225">**This device is working properly.**</span></span> <span data-ttu-id="5efcb-226"> (0)</span><span class="sxs-lookup"><span data-stu-id="5efcb-226">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="5efcb-227">**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="5efcb-227">**This device is not configured correctly.**</span></span> <span data-ttu-id="5efcb-228">(1)</span><span class="sxs-lookup"><span data-stu-id="5efcb-228">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5efcb-229">**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5efcb-229">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="5efcb-230">(2)</span><span class="sxs-lookup"><span data-stu-id="5efcb-230">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="5efcb-231">**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="5efcb-231">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="5efcb-232">(3)</span><span class="sxs-lookup"><span data-stu-id="5efcb-232">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="5efcb-233">**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="5efcb-233">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="5efcb-234">(4)</span><span class="sxs-lookup"><span data-stu-id="5efcb-234">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="5efcb-235">**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="5efcb-235">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="5efcb-236">(5)</span><span class="sxs-lookup"><span data-stu-id="5efcb-236">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="5efcb-237">**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="5efcb-237">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="5efcb-238"> (6)</span><span class="sxs-lookup"><span data-stu-id="5efcb-238">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="5efcb-239">**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="5efcb-239">**Cannot filter.**</span></span> <span data-ttu-id="5efcb-240">(7)</span><span class="sxs-lookup"><span data-stu-id="5efcb-240">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="5efcb-241">**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="5efcb-241">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="5efcb-242">(8)</span><span class="sxs-lookup"><span data-stu-id="5efcb-242">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="5efcb-243">**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="5efcb-243">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="5efcb-244">(9)</span><span class="sxs-lookup"><span data-stu-id="5efcb-244">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="5efcb-245">**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5efcb-245">**This device cannot start.**</span></span> <span data-ttu-id="5efcb-246">(10)</span><span class="sxs-lookup"><span data-stu-id="5efcb-246">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="5efcb-247">**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5efcb-247">**This device failed.**</span></span> <span data-ttu-id="5efcb-248">(11)</span><span class="sxs-lookup"><span data-stu-id="5efcb-248">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="5efcb-249">**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="5efcb-249">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="5efcb-250">12</span><span class="sxs-lookup"><span data-stu-id="5efcb-250">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="5efcb-251">**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5efcb-251">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="5efcb-252">(13)</span><span class="sxs-lookup"><span data-stu-id="5efcb-252">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="5efcb-253">**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="5efcb-253">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="5efcb-254">(14)</span><span class="sxs-lookup"><span data-stu-id="5efcb-254">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="5efcb-255">**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="5efcb-255">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="5efcb-256">(15)</span><span class="sxs-lookup"><span data-stu-id="5efcb-256">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="5efcb-257">**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5efcb-257">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="5efcb-258">(16)</span><span class="sxs-lookup"><span data-stu-id="5efcb-258">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="5efcb-259">**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="5efcb-259">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="5efcb-260">(17)</span><span class="sxs-lookup"><span data-stu-id="5efcb-260">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5efcb-261">**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5efcb-261">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="5efcb-262">(18)</span><span class="sxs-lookup"><span data-stu-id="5efcb-262">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="5efcb-263">**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="5efcb-263">**Failure using the VxD loader.**</span></span> <span data-ttu-id="5efcb-264">(19)</span><span class="sxs-lookup"><span data-stu-id="5efcb-264">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="5efcb-265">**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="5efcb-265">**Your registry might be corrupted.**</span></span> <span data-ttu-id="5efcb-266">(20)</span><span class="sxs-lookup"><span data-stu-id="5efcb-266">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="5efcb-267">**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5efcb-267">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="5efcb-268">(21)</span><span class="sxs-lookup"><span data-stu-id="5efcb-268">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="5efcb-269">**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="5efcb-269">**This device is disabled.**</span></span> <span data-ttu-id="5efcb-270">(22)</span><span class="sxs-lookup"><span data-stu-id="5efcb-270">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="5efcb-271">**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="5efcb-271">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="5efcb-272">(23)</span><span class="sxs-lookup"><span data-stu-id="5efcb-272">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="5efcb-273">**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="5efcb-273">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="5efcb-274">(24)</span><span class="sxs-lookup"><span data-stu-id="5efcb-274">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="5efcb-275">**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5efcb-275">**Windows is still setting up this device.**</span></span> <span data-ttu-id="5efcb-276">(25)</span><span class="sxs-lookup"><span data-stu-id="5efcb-276">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="5efcb-277">**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5efcb-277">**Windows is still setting up this device.**</span></span> <span data-ttu-id="5efcb-278">(26)</span><span class="sxs-lookup"><span data-stu-id="5efcb-278">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="5efcb-279">**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="5efcb-279">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="5efcb-280">(27)</span><span class="sxs-lookup"><span data-stu-id="5efcb-280">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="5efcb-281">**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="5efcb-281">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="5efcb-282">(28)</span><span class="sxs-lookup"><span data-stu-id="5efcb-282">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="5efcb-283">**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="5efcb-283">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="5efcb-284">(29)</span><span class="sxs-lookup"><span data-stu-id="5efcb-284">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="5efcb-285">**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5efcb-285">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="5efcb-286">(30)</span><span class="sxs-lookup"><span data-stu-id="5efcb-286">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5efcb-287">**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5efcb-287">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="5efcb-288">31</span><span class="sxs-lookup"><span data-stu-id="5efcb-288">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5efcb-289">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="5efcb-289">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efcb-290">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5efcb-290">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-291">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5efcb-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-292">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5efcb-292">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5efcb-293">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="5efcb-293">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="5efcb-294">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5efcb-294">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5efcb-295">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5efcb-295">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efcb-296">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5efcb-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-297">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5efcb-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-298">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5efcb-298">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5efcb-299">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="5efcb-299">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="5efcb-300">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="5efcb-300">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="5efcb-301">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5efcb-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5efcb-302">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="5efcb-302">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efcb-303">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5efcb-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-304">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5efcb-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-305">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="5efcb-305">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="5efcb-306">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5efcb-306">A textual description of the object.</span></span>

<span data-ttu-id="5efcb-307">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5efcb-307">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5efcb-308">**DesignCapacity**</span><span class="sxs-lookup"><span data-stu-id="5efcb-308">**DesignCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efcb-309">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5efcb-309">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-310">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5efcb-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-311">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Portable batteria \| 002,8 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliwatt-ore ")</span><span class="sxs-lookup"><span data-stu-id="5efcb-311">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="5efcb-312">Capacità progettata della batteria in milliwatt ore.</span><span class="sxs-lookup"><span data-stu-id="5efcb-312">Designed capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="5efcb-313">Se questa proprietà non è supportata, immettere 0.</span><span class="sxs-lookup"><span data-stu-id="5efcb-313">If this property is not supported, enter 0.</span></span>

</dd> <dt>

<span data-ttu-id="5efcb-314">**DesignVoltage**</span><span class="sxs-lookup"><span data-stu-id="5efcb-314">**DesignVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efcb-315">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5efcb-315">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-316">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5efcb-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-317">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Portable batteria \| 002,9 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" millivolt ")</span><span class="sxs-lookup"><span data-stu-id="5efcb-317">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.9"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="5efcb-318">Tensione progettata della batteria in millivolt.</span><span class="sxs-lookup"><span data-stu-id="5efcb-318">Designed voltage of the battery in millivolts.</span></span> <span data-ttu-id="5efcb-319">Se questo attributo non è supportato, immettere 0.</span><span class="sxs-lookup"><span data-stu-id="5efcb-319">If this attribute is not supported, enter 0.</span></span>

<span data-ttu-id="5efcb-320">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="5efcb-320">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="5efcb-321">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="5efcb-321">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efcb-322">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5efcb-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-323">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5efcb-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-324">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5efcb-324">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5efcb-325">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="5efcb-325">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="5efcb-326">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5efcb-326">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5efcb-327">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="5efcb-327">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efcb-328">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5efcb-328">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-329">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5efcb-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5efcb-330">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="5efcb-330">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="5efcb-331">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5efcb-331">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5efcb-332">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="5efcb-332">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efcb-333">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5efcb-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-334">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5efcb-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5efcb-335">Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.</span><span class="sxs-lookup"><span data-stu-id="5efcb-335">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="5efcb-336">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5efcb-336">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5efcb-337">**EstimatedChargeRemaining**</span><span class="sxs-lookup"><span data-stu-id="5efcb-337">**EstimatedChargeRemaining**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efcb-338">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5efcb-338">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-339">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5efcb-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-340">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("percentuale")</span><span class="sxs-lookup"><span data-stu-id="5efcb-340">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="5efcb-341">Percentuale stimata del costo totale rimanente.</span><span class="sxs-lookup"><span data-stu-id="5efcb-341">Estimated percentage of the remaining full charge.</span></span>

</dd> <dt>

<span data-ttu-id="5efcb-342">**EstimatedRunTime**</span><span class="sxs-lookup"><span data-stu-id="5efcb-342">**EstimatedRunTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efcb-343">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5efcb-343">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-344">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5efcb-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-345">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Portable batteria \| 002,15 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" minuti ")</span><span class="sxs-lookup"><span data-stu-id="5efcb-345">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="5efcb-346">Tempo stimato, in minuti, fino a quando non viene esaurito il costo della batteria sotto le condizioni di carico attuali se l'alimentazione dell'utilità è disattivata, viene persa e rimane spenta o se un portatile è disconnesso da una fonte di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="5efcb-346">Estimated time, in minutes, until the battery charge is depleted under the present load conditions if the utility power is off, is lost and remains off, or if a laptop is disconnected from a power source.</span></span>

</dd> <dt>

<span data-ttu-id="5efcb-347">**ExpectedLife**</span><span class="sxs-lookup"><span data-stu-id="5efcb-347">**ExpectedLife**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efcb-348">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5efcb-348">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-349">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5efcb-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-350">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("minuti")</span><span class="sxs-lookup"><span data-stu-id="5efcb-350">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="5efcb-351">Durata prevista della batteria, in minuti, presupponendo che la batteria venga addebitata completamente.</span><span class="sxs-lookup"><span data-stu-id="5efcb-351">Battery's expected lifetime, in minutes, assuming that the battery is fully charged.</span></span> <span data-ttu-id="5efcb-352">Questa proprietà rappresenta la durata totale prevista della batteria, non la durata rimanente corrente, indicata dalla proprietà **EstimatedRunTime** .</span><span class="sxs-lookup"><span data-stu-id="5efcb-352">This property represents the total expected life of the battery, not its current remaining life, which is indicated by the **EstimatedRunTime** property.</span></span>

</dd> <dt>

<span data-ttu-id="5efcb-353">**FullChargeCapacity**</span><span class="sxs-lookup"><span data-stu-id="5efcb-353">**FullChargeCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efcb-354">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5efcb-354">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-355">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5efcb-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-356">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Portable batteria \| 002,11 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliwatt-ore ")</span><span class="sxs-lookup"><span data-stu-id="5efcb-356">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="5efcb-357">La capacità di addebito completo della batteria in milliwatt ore.</span><span class="sxs-lookup"><span data-stu-id="5efcb-357">The full charge capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="5efcb-358">Confrontare questo valore con la proprietà **DesignCapacity** per determinare quando la batteria deve essere sostituita.</span><span class="sxs-lookup"><span data-stu-id="5efcb-358">Compare this value to the **DesignCapacity** property to determine when the battery requires replacement.</span></span> <span data-ttu-id="5efcb-359">La durata della batteria è in genere quando la proprietà **FullChargeCapacity** è inferiore al 80% della proprietà **DesignCapacity** .</span><span class="sxs-lookup"><span data-stu-id="5efcb-359">A battery's end-life is typically when the **FullChargeCapacity** property falls below 80 percent of the **DesignCapacity** property.</span></span> <span data-ttu-id="5efcb-360">Se questa proprietà non è supportata, immettere 0.</span><span class="sxs-lookup"><span data-stu-id="5efcb-360">If this property is not supported, enter 0.</span></span>

</dd> <dt>

<span data-ttu-id="5efcb-361">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5efcb-361">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efcb-362">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5efcb-362">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-363">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5efcb-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-364">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="5efcb-364">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="5efcb-365">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="5efcb-365">Indicates when the object was installed.</span></span> <span data-ttu-id="5efcb-366">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="5efcb-366">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="5efcb-367">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5efcb-367">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5efcb-368">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="5efcb-368">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efcb-369">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5efcb-369">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-370">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5efcb-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5efcb-371">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="5efcb-371">Last error code reported by the logical device.</span></span>

<span data-ttu-id="5efcb-372">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5efcb-372">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5efcb-373">**MaxRechargeTime**</span><span class="sxs-lookup"><span data-stu-id="5efcb-373">**MaxRechargeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efcb-374">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5efcb-374">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-375">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5efcb-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-376">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("minuti")</span><span class="sxs-lookup"><span data-stu-id="5efcb-376">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="5efcb-377">Tempo massimo, in minuti, per l'addebito completo della batteria.</span><span class="sxs-lookup"><span data-stu-id="5efcb-377">Maximum time, in minutes, to fully charge the battery.</span></span> <span data-ttu-id="5efcb-378">Questa proprietà rappresenta il tempo per ricaricare una batteria completamente esaurita, non il tempo di ricarica rimanente corrente, indicato nella proprietà **TimeToFullCharge** .</span><span class="sxs-lookup"><span data-stu-id="5efcb-378">This property represents the time to recharge a fully depleted battery, not the current remaining charging time, which is indicated in the **TimeToFullCharge** property.</span></span>

</dd> <dt>

<span data-ttu-id="5efcb-379">**Nome**</span><span class="sxs-lookup"><span data-stu-id="5efcb-379">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efcb-380">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5efcb-380">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-381">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5efcb-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-382">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="5efcb-382">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="5efcb-383">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="5efcb-383">Label by which the object is known.</span></span> <span data-ttu-id="5efcb-384">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="5efcb-384">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="5efcb-385">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5efcb-385">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5efcb-386">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="5efcb-386">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efcb-387">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5efcb-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-388">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5efcb-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-389">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5efcb-389">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5efcb-390">Indica l'identificatore del dispositivo Plug and Play Win32 del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="5efcb-390">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="5efcb-391">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="5efcb-391">Example: "\*PNP030b"</span></span>

<span data-ttu-id="5efcb-392">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5efcb-392">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5efcb-393">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="5efcb-393">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efcb-394">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5efcb-394">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-395">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5efcb-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5efcb-396">Indica le funzionalità specifiche relative al risparmio di energia del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="5efcb-396">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="5efcb-397">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5efcb-397">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5efcb-398"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="5efcb-398"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="5efcb-399">Le capacità relative al risparmio di energia sono sconosciute.</span><span class="sxs-lookup"><span data-stu-id="5efcb-399">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="5efcb-400"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="5efcb-400"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5efcb-401">Le capacità relative al risparmio di energia non sono supportate per questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5efcb-401">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5efcb-402"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="5efcb-402"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5efcb-403">Le capacità correlate all'alimentazione sono state disabilitate.</span><span class="sxs-lookup"><span data-stu-id="5efcb-403">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="5efcb-404"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="5efcb-404"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5efcb-405">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="5efcb-405">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="5efcb-406"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="5efcb-406"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="5efcb-407">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="5efcb-407">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="5efcb-408"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="5efcb-408"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="5efcb-409">Il metodo **SetPowerState** è supportato.</span><span class="sxs-lookup"><span data-stu-id="5efcb-409">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="5efcb-410">Questo metodo è disponibile nella classe [**\_ LogicalDevice CIM**](cim-logicaldevice.md) padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="5efcb-410">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="5efcb-411">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="5efcb-411">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="5efcb-412"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="5efcb-412"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="5efcb-413">Il metodo **SetPowerState** può essere richiamato con il parametro *PowerState* impostato su 5 ("ciclo di alimentazione").</span><span class="sxs-lookup"><span data-stu-id="5efcb-413">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="5efcb-414"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="5efcb-414"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="5efcb-415">Il metodo **SetPowerState** può essere richiamato con il parametro *PowerState* impostato su 5 ("ciclo di alimentazione") e il parametro *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="5efcb-415">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5efcb-416">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="5efcb-416">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efcb-417">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5efcb-417">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-418">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5efcb-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5efcb-419">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="5efcb-419">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="5efcb-420">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="5efcb-420">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="5efcb-421">Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="5efcb-421">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="5efcb-422">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="5efcb-422">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="5efcb-423">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5efcb-423">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5efcb-424">**SmartBatteryVersion**</span><span class="sxs-lookup"><span data-stu-id="5efcb-424">**SmartBatteryVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efcb-425">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5efcb-425">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-426">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5efcb-426">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-427">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Portable batteria \| 002,10 ")</span><span class="sxs-lookup"><span data-stu-id="5efcb-427">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.10")</span></span>
</dt> </dl>

<span data-ttu-id="5efcb-428">Smart Battery data-specifica il numero di versione supportato da questa batteria.</span><span class="sxs-lookup"><span data-stu-id="5efcb-428">Smart battery data-specification version number that is supported by this battery.</span></span> <span data-ttu-id="5efcb-429">Se la batteria non supporta questa funzione, il valore deve essere lasciato vuoto.</span><span class="sxs-lookup"><span data-stu-id="5efcb-429">If the battery does not support this function, the value should be left empty.</span></span>

</dd> <dt>

<span data-ttu-id="5efcb-430">**Status**</span><span class="sxs-lookup"><span data-stu-id="5efcb-430">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efcb-431">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5efcb-431">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-432">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5efcb-432">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-433">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="5efcb-433">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="5efcb-434">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5efcb-434">String that indicates the current status of the object.</span></span> <span data-ttu-id="5efcb-435">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="5efcb-435">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="5efcb-436">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="5efcb-436">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="5efcb-437">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="5efcb-437">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="5efcb-438">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="5efcb-438">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5efcb-439">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="5efcb-439">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5efcb-440">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="5efcb-440">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5efcb-441">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5efcb-441">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5efcb-442">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="5efcb-442">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5efcb-443">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="5efcb-443">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="5efcb-444">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="5efcb-444">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5efcb-445">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="5efcb-445">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5efcb-446">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="5efcb-446">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="5efcb-447">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="5efcb-447">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="5efcb-448">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="5efcb-448">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="5efcb-449">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="5efcb-449">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="5efcb-450">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="5efcb-450">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="5efcb-451">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="5efcb-451">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="5efcb-452">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="5efcb-452">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5efcb-453">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="5efcb-453">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="5efcb-454">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="5efcb-454">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5efcb-455">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="5efcb-455">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efcb-456">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5efcb-456">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-457">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5efcb-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-458">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="5efcb-458">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="5efcb-459">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="5efcb-459">State of the logical device.</span></span> <span data-ttu-id="5efcb-460">Se questa proprietà non è applicabile al dispositivo logico, è necessario utilizzare il valore 5 ("non applicabile").</span><span class="sxs-lookup"><span data-stu-id="5efcb-460">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="5efcb-461">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5efcb-461">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5efcb-462">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="5efcb-462">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5efcb-463">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="5efcb-463">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="5efcb-464">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="5efcb-464">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5efcb-465">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="5efcb-465">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="5efcb-466">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="5efcb-466">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5efcb-467">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5efcb-467">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efcb-468">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5efcb-468">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-469">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5efcb-469">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-470">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5efcb-470">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5efcb-471">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="5efcb-471">The scoping system's creation class name.</span></span>

<span data-ttu-id="5efcb-472">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5efcb-472">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5efcb-473">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="5efcb-473">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efcb-474">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5efcb-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-475">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5efcb-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-476">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5efcb-476">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5efcb-477">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="5efcb-477">The scoping system's name.</span></span>

<span data-ttu-id="5efcb-478">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5efcb-478">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5efcb-479">**TimeOnBattery**</span><span class="sxs-lookup"><span data-stu-id="5efcb-479">**TimeOnBattery**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efcb-480">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5efcb-480">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-481">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5efcb-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-482">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("secondi")</span><span class="sxs-lookup"><span data-stu-id="5efcb-482">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="5efcb-483">Tempo trascorso, in secondi, dal momento in cui l'UPS del sistema informatico ha comportato l'ultima alimentazione a batteria o la quantità di tempo trascorsa dall'ultimo riavvio del sistema o dell'UPS, a seconda del valore minore.</span><span class="sxs-lookup"><span data-stu-id="5efcb-483">Elapsed time, in seconds, since the computer system's UPS last switched to battery power, or the amount of time since the system or UPS was last restarted, whichever is less.</span></span> <span data-ttu-id="5efcb-484">Se la batteria è "online", viene restituito il valore 0.</span><span class="sxs-lookup"><span data-stu-id="5efcb-484">A value of 0 is returned if the battery is "online."</span></span>

</dd> <dt>

<span data-ttu-id="5efcb-485">**TimeToFullCharge**</span><span class="sxs-lookup"><span data-stu-id="5efcb-485">**TimeToFullCharge**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efcb-486">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5efcb-486">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-487">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5efcb-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5efcb-488">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Portable batteria \| 002,16 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" minuti ")</span><span class="sxs-lookup"><span data-stu-id="5efcb-488">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.16"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="5efcb-489">Tempo rimanente, espresso in minuti, per addebitare la batteria in modo completo al tasso di ricarica corrente e usare.</span><span class="sxs-lookup"><span data-stu-id="5efcb-489">Remaining time, in minutes, to charge the battery fully at the current charging rate and use.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5efcb-490">Commenti</span><span class="sxs-lookup"><span data-stu-id="5efcb-490">Remarks</span></span>

<span data-ttu-id="5efcb-491">La classe **CIM \_ Battery** è derivata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5efcb-491">The **CIM\_Battery** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="5efcb-492">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="5efcb-492">WMI does not implement this class.</span></span> <span data-ttu-id="5efcb-493">Per ulteriori informazioni sulle classi derivate dalla **\_ batteria CIM**, vedere la pagina relativa alle [classi Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="5efcb-493">For more information about classes derived from **CIM\_Battery**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="5efcb-494">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="5efcb-494">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5efcb-495">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="5efcb-495">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5efcb-496">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5efcb-496">Requirements</span></span>



| <span data-ttu-id="5efcb-497">Requisito</span><span class="sxs-lookup"><span data-stu-id="5efcb-497">Requirement</span></span> | <span data-ttu-id="5efcb-498">Valore</span><span class="sxs-lookup"><span data-stu-id="5efcb-498">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5efcb-499">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5efcb-499">Minimum supported client</span></span><br/> | <span data-ttu-id="5efcb-500">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5efcb-500">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5efcb-501">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5efcb-501">Minimum supported server</span></span><br/> | <span data-ttu-id="5efcb-502">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5efcb-502">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5efcb-503">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5efcb-503">Namespace</span></span><br/>                | <span data-ttu-id="5efcb-504">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="5efcb-504">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5efcb-505">MOF</span><span class="sxs-lookup"><span data-stu-id="5efcb-505">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5efcb-506"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5efcb-506"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5efcb-507">DLL</span><span class="sxs-lookup"><span data-stu-id="5efcb-507">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5efcb-508"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5efcb-508"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5efcb-509">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5efcb-509">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5efcb-510">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="5efcb-510">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 


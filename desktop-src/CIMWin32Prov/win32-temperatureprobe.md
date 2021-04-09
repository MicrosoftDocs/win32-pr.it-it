---
description: Win32 \_ TemperatureProbe&\# 32; La classe WMI rappresenta le proprietà di un sensore di temperatura (termometro elettronico).
ms.assetid: 63ba1ae2-6abc-4d86-a7f6-f02536ebd8ac
ms.tgt_platform: multiple
title: Classe Win32_TemperatureProbe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_TemperatureProbe
- Win32_TemperatureProbe.Reset
- Win32_TemperatureProbe.SetPowerState
- Win32_TemperatureProbe.Accuracy
- Win32_TemperatureProbe.Availability
- Win32_TemperatureProbe.Caption
- Win32_TemperatureProbe.ConfigManagerErrorCode
- Win32_TemperatureProbe.ConfigManagerUserConfig
- Win32_TemperatureProbe.CreationClassName
- Win32_TemperatureProbe.CurrentReading
- Win32_TemperatureProbe.Description
- Win32_TemperatureProbe.DeviceID
- Win32_TemperatureProbe.ErrorCleared
- Win32_TemperatureProbe.ErrorDescription
- Win32_TemperatureProbe.InstallDate
- Win32_TemperatureProbe.IsLinear
- Win32_TemperatureProbe.LastErrorCode
- Win32_TemperatureProbe.LowerThresholdCritical
- Win32_TemperatureProbe.LowerThresholdFatal
- Win32_TemperatureProbe.LowerThresholdNonCritical
- Win32_TemperatureProbe.MaxReadable
- Win32_TemperatureProbe.MinReadable
- Win32_TemperatureProbe.Name
- Win32_TemperatureProbe.NominalReading
- Win32_TemperatureProbe.NormalMax
- Win32_TemperatureProbe.NormalMin
- Win32_TemperatureProbe.PNPDeviceID
- Win32_TemperatureProbe.PowerManagementCapabilities
- Win32_TemperatureProbe.PowerManagementSupported
- Win32_TemperatureProbe.Resolution
- Win32_TemperatureProbe.Status
- Win32_TemperatureProbe.StatusInfo
- Win32_TemperatureProbe.SystemCreationClassName
- Win32_TemperatureProbe.SystemName
- Win32_TemperatureProbe.Tolerance
- Win32_TemperatureProbe.UpperThresholdCritical
- Win32_TemperatureProbe.UpperThresholdFatal
- Win32_TemperatureProbe.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b6de4ed6334747e8313098075bc916a1975f520c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877798"
---
# <a name="win32_temperatureprobe-class"></a><span data-ttu-id="c2d8a-103">Win32 \_ TemperatureProbe (classe)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-103">Win32\_TemperatureProbe class</span></span>

<span data-ttu-id="c2d8a-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ TemperatureProbe Win32** rappresenta le proprietà di un sensore di temperatura (termometro elettronico).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-104">The **Win32\_TemperatureProbe** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a temperature sensor (electronic thermometer).</span></span>

<span data-ttu-id="c2d8a-105">La maggior parte delle informazioni fornite dalla classe WMI **Win32 \_ TemperatureProbe** deriva da SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-105">Most of the information that the **Win32\_TemperatureProbe** WMI class provides comes from SMBIOS.</span></span> <span data-ttu-id="c2d8a-106">Le letture in tempo reale per la proprietà **CurrentReading** non possono essere estratte dalle tabelle SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-106">Real-time readings for the **CurrentReading** property cannot be extracted from SMBIOS tables.</span></span> <span data-ttu-id="c2d8a-107">Per questo motivo, le implementazioni correnti di WMI non popolano la proprietà **CurrentReading** .</span><span class="sxs-lookup"><span data-stu-id="c2d8a-107">For this reason, current implementations of WMI do not populate the **CurrentReading** property.</span></span> <span data-ttu-id="c2d8a-108">La presenza della proprietà **CurrentReading** è riservata per un utilizzo futuro.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-108">The **CurrentReading** property's presence is reserved for future use.</span></span>

<span data-ttu-id="c2d8a-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="c2d8a-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2d8a-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c2d8a-111">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{464FFABB-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class Win32_TemperatureProbe : CIM_TemperatureSensor
{
  sint32   Accuracy;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  sint32   CurrentReading;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  boolean  IsLinear;
  uint32   LastErrorCode;
  sint32   LowerThresholdCritical;
  sint32   LowerThresholdFatal;
  sint32   LowerThresholdNonCritical;
  sint32   MaxReadable;
  sint32   MinReadable;
  string   Name;
  sint32   NominalReading;
  sint32   NormalMax;
  sint32   NormalMin;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   Resolution;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  sint32   Tolerance;
  sint32   UpperThresholdCritical;
  sint32   UpperThresholdFatal;
  sint32   UpperThresholdNonCritical;
};
```

## <a name="members"></a><span data-ttu-id="c2d8a-112">Members</span><span class="sxs-lookup"><span data-stu-id="c2d8a-112">Members</span></span>

<span data-ttu-id="c2d8a-113">La classe **Win32 \_ TemperatureProbe** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c2d8a-113">The **Win32\_TemperatureProbe** class has these types of members:</span></span>

-   [<span data-ttu-id="c2d8a-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="c2d8a-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="c2d8a-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c2d8a-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c2d8a-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="c2d8a-116">Methods</span></span>

<span data-ttu-id="c2d8a-117">La classe **Win32 \_ TemperatureProbe** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-117">The **Win32\_TemperatureProbe** class has these methods.</span></span>



| <span data-ttu-id="c2d8a-118">Metodo</span><span class="sxs-lookup"><span data-stu-id="c2d8a-118">Method</span></span>            | <span data-ttu-id="c2d8a-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2d8a-119">Description</span></span>                                                                                                                                                                                                                     |
|:------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2d8a-120">**Reimpostazione**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-120">**Reset**</span></span>         | <span data-ttu-id="c2d8a-121">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-121">Not implemented.</span></span> <span data-ttu-id="c2d8a-122">Per implementare questo metodo, vedere il metodo [**Reset**](reset-method-in-class-cim-temperaturesensor.md) in [**CIM \_ sensore**](cim-temperaturesensor.md) per la documentazione.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-122">To implement this method, see the [**Reset**](reset-method-in-class-cim-temperaturesensor.md) method in [**CIM\_TemperatureSensor**](cim-temperaturesensor.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="c2d8a-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-123">**SetPowerState**</span></span> | <span data-ttu-id="c2d8a-124">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-124">Not implemented.</span></span> <span data-ttu-id="c2d8a-125">Per implementare questo metodo, vedere il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-temperaturesensor.md) in [**CIM \_ sensore**](cim-temperaturesensor.md) per la documentazione.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-125">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-temperaturesensor.md) method in [**CIM\_TemperatureSensor**](cim-temperaturesensor.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c2d8a-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c2d8a-126">Properties</span></span>

<span data-ttu-id="c2d8a-127">La classe **Win32 \_ TemperatureProbe** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-127">The **Win32\_TemperatureProbe** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c2d8a-128">**Accuratezza**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-128">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d8a-129">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2d8a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-131">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Probe temperatura DMTF \| 001,19 ")</span><span class="sxs-lookup"><span data-stu-id="c2d8a-131">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.19")</span></span>
</dt> </dl>

<span data-ttu-id="c2d8a-132">Accuratezza del sensore per la proprietà misurata.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-132">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="c2d8a-133">Il valore viene registrato come più o meno centesimi di percentuale.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-133">Its value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="c2d8a-134">L'accuratezza, la risoluzione e la tolleranza vengono utilizzate per calcolare il valore effettivo della proprietà fisica misurata.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-134">Accuracy, resolution, and tolerance are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="c2d8a-135">L'accuratezza può variare e varia a seconda che il dispositivo sia lineare o meno sull'intervallo dinamico.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-135">Accuracy may vary and depends on whether or not the device is linear over its dynamic range.</span></span>

<span data-ttu-id="c2d8a-136">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-136">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2d8a-137">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-137">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d8a-138">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2d8a-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-140">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="c2d8a-140">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="c2d8a-141">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-141">Availability and status of the device.</span></span>

<span data-ttu-id="c2d8a-142">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-142">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c2d8a-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c2d8a-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="c2d8a-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="c2d8a-146"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-146"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="c2d8a-147"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-147"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c2d8a-148"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-148"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="c2d8a-149"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="c2d8a-149"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="c2d8a-150"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="c2d8a-150"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-151">Offline</span><span class="sxs-lookup"><span data-stu-id="c2d8a-151">Offline</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="c2d8a-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c2d8a-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="c2d8a-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="c2d8a-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="c2d8a-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-157">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-157">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="c2d8a-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-159">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-159">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="c2d8a-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-161">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-161">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="c2d8a-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="c2d8a-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-164">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-164">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="c2d8a-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-166">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-166">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="c2d8a-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-168">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-168">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="c2d8a-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-170">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-170">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="c2d8a-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-172">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-172">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c2d8a-173">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-173">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d8a-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2d8a-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-176">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c2d8a-176">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c2d8a-177">Breve descrizione di un oggetto, ovvero una stringa a una riga.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-177">Short description of an object—a one-line string.</span></span>

<span data-ttu-id="c2d8a-178">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2d8a-179">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-179">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d8a-180">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-180">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-181">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2d8a-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-182">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c2d8a-182">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c2d8a-183">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-183">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="c2d8a-184">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-184">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="c2d8a-185"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-185"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="c2d8a-186"> (0)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-186">(0)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-187">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-187">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="c2d8a-188"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-188"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="c2d8a-189">(1)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-189">(1)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-190">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-190">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c2d8a-191"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-191"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="c2d8a-192">(2)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-192">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="c2d8a-193"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-193"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="c2d8a-194">(3)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-194">(3)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-195">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-195">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c2d8a-196"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-196"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="c2d8a-197">(4)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-197">(4)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-198">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-198">Device is not working properly.</span></span> <span data-ttu-id="c2d8a-199">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-199">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="c2d8a-200"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-200"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="c2d8a-201">(5)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-201">(5)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-202">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-202">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="c2d8a-203"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-203"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="c2d8a-204"> (6)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-204">(6)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-205">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-205">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="c2d8a-206"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-206"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="c2d8a-207">(7)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-207">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="c2d8a-208"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-208"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="c2d8a-209">(8)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-209">(8)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-210">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-210">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="c2d8a-211"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-211"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="c2d8a-212">(9)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-212">(9)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-213">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-213">Device is not working properly.</span></span> <span data-ttu-id="c2d8a-214">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-214">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="c2d8a-215"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-215"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="c2d8a-216">(10)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-216">(10)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-217">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-217">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="c2d8a-218"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-218"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="c2d8a-219">(11)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-219">(11)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-220">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-220">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="c2d8a-221"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-221"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="c2d8a-222">12</span><span class="sxs-lookup"><span data-stu-id="c2d8a-222">(12)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-223">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-223">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="c2d8a-224"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-224"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="c2d8a-225">(13)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-225">(13)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-226">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-226">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="c2d8a-227"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-227"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="c2d8a-228">(14)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-228">(14)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-229">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-229">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="c2d8a-230"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-230"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="c2d8a-231">(15)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-231">(15)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-232">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-232">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="c2d8a-233"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-233"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="c2d8a-234">(16)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-234">(16)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-235">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-235">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="c2d8a-236"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-236"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="c2d8a-237">(17)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-237">(17)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-238">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-238">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c2d8a-239"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-239"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="c2d8a-240">(18)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-240">(18)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-241">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-241">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="c2d8a-242"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-242"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="c2d8a-243">(19)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-243">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c2d8a-244"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-244"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="c2d8a-245">(20)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-245">(20)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-246">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-246">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="c2d8a-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="c2d8a-248">(21)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-248">(21)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-249">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-249">System failure.</span></span> <span data-ttu-id="c2d8a-250">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-250">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="c2d8a-251">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-251">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="c2d8a-252"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-252"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="c2d8a-253">(22)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-253">(22)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-254">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-254">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="c2d8a-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="c2d8a-256">(23)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-256">(23)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-257">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-257">System failure.</span></span> <span data-ttu-id="c2d8a-258">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-258">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="c2d8a-259"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-259"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="c2d8a-260">(24)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-260">(24)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-261">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-261">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c2d8a-262"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-262"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="c2d8a-263">(25)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-263">(25)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-264">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-264">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c2d8a-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="c2d8a-266">(26)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-266">(26)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-267">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-267">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="c2d8a-268"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-268"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="c2d8a-269">(27)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-269">(27)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-270">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-270">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="c2d8a-271"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-271"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="c2d8a-272">(28)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-272">(28)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-273">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-273">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="c2d8a-274"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-274"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="c2d8a-275">(29)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-275">(29)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-276">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-276">Device is disabled.</span></span> <span data-ttu-id="c2d8a-277">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-277">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="c2d8a-278"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-278"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="c2d8a-279">(30)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-279">(30)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-280">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-280">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c2d8a-281"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-281"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="c2d8a-282">31</span><span class="sxs-lookup"><span data-stu-id="c2d8a-282">(31)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-283">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-283">Device is not working properly.</span></span> <span data-ttu-id="c2d8a-284">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-284">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c2d8a-285">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-285">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d8a-286">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-286">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-287">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2d8a-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-288">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c2d8a-288">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c2d8a-289">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-289">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="c2d8a-290">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-290">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2d8a-291">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-291">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d8a-292">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-293">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2d8a-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-294">Qualificatori: [ **\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-294">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="c2d8a-295">Nome della prima classe concreta visualizzata nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-295">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="c2d8a-296">Se utilizzata con le altre proprietà chiave di una classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-296">When used with the other key properties of a class, this property allows all instances of the class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="c2d8a-297">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-297">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2d8a-298">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-298">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d8a-299">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-299">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-300">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2d8a-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-301">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Probe temperatura DMTF \| 001,5 "), [**unità**](../wmisdk/standard-qualifiers.md) (" decimi di gradi centigradi ")</span><span class="sxs-lookup"><span data-stu-id="c2d8a-301">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.5"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="c2d8a-302">Valore corrente indicato dal sensore.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-302">Current value indicated by the sensor.</span></span>

<span data-ttu-id="c2d8a-303">Le implementazioni correnti di WMI non popolano la proprietà **CurrentReading** .</span><span class="sxs-lookup"><span data-stu-id="c2d8a-303">Current implementations of WMI do not populate the **CurrentReading** property.</span></span> <span data-ttu-id="c2d8a-304">La presenza della proprietà **CurrentReading** è riservata per un utilizzo futuro.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-304">The **CurrentReading** property's presence is reserved for future use.</span></span>

<span data-ttu-id="c2d8a-305">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-305">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2d8a-306">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-306">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d8a-307">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-308">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2d8a-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-309">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="c2d8a-309">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c2d8a-310">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-310">Description of the object.</span></span>

<span data-ttu-id="c2d8a-311">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-311">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2d8a-312">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-312">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d8a-313">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-314">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2d8a-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-315">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="c2d8a-315">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="c2d8a-316">Identificatore univoco del probe corrente.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-316">Unique identifier of the current probe.</span></span>

<span data-ttu-id="c2d8a-317">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-317">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2d8a-318">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-318">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d8a-319">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-319">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-320">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2d8a-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2d8a-321">Se **true**, l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-321">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="c2d8a-322">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2d8a-323">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-323">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d8a-324">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-325">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2d8a-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2d8a-326">Altre informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che è possibile eseguire.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-326">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that you can take.</span></span>

<span data-ttu-id="c2d8a-327">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2d8a-328">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-328">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d8a-329">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-329">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-330">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2d8a-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-331">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="c2d8a-331">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c2d8a-332">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-332">Date and time the object is installed.</span></span> <span data-ttu-id="c2d8a-333">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-333">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="c2d8a-334">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-334">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2d8a-335">**Lineari**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-335">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d8a-336">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-336">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-337">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2d8a-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2d8a-338">Se **true**, il sensore è lineare sull'intervallo dinamico.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-338">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

<span data-ttu-id="c2d8a-339">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-339">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2d8a-340">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-340">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d8a-341">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-341">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-342">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2d8a-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2d8a-343">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-343">Last error code reported by the logical device.</span></span>

<span data-ttu-id="c2d8a-344">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-344">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2d8a-345">**LowerThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-345">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d8a-346">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-346">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-347">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2d8a-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-348">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Probe temperatura DMTF \| 001,13 "), [**unità**](../wmisdk/standard-qualifiers.md) (" decimi di gradi centigradi ")</span><span class="sxs-lookup"><span data-stu-id="c2d8a-348">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.13"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="c2d8a-349">Valore soglia sensore per specificare gli intervalli (valori minimo e massimo) che identificano le condizioni operative del sensore, che possono essere condizioni normali, non critiche, critiche o irreversibili.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-349">Sensor threshold value to specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="c2d8a-350">Se **CurrentReading** è compreso tra **LowerThresholdCritical** e **LowerThresholdFatal**, lo stato corrente è critico.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-350">If **CurrentReading** is between **LowerThresholdCritical** and **LowerThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="c2d8a-351">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-351">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2d8a-352">**LowerThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-352">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d8a-353">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-353">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-354">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2d8a-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-355">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Probe temperatura DMTF \| 001,15 "), [**unità**](../wmisdk/standard-qualifiers.md) (" decimi di gradi centigradi ")</span><span class="sxs-lookup"><span data-stu-id="c2d8a-355">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.15"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="c2d8a-356">Valore soglia sensore per specificare gli intervalli (valori minimo e massimo) che identificano le condizioni operative del sensore, che possono essere condizioni normali, non critiche, critiche o irreversibili.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-356">Sensor threshold value to specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="c2d8a-357">Se **CurrentReading** è inferiore a **LowerThresholdFatal**, lo stato corrente è irreversibile.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-357">If **CurrentReading** is below **LowerThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="c2d8a-358">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-358">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2d8a-359">**LowerThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-359">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d8a-360">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-360">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-361">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2d8a-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-362">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Probe temperatura DMTF \| 001,11 "), [**unità**](../wmisdk/standard-qualifiers.md) (" decimi di gradi centigradi ")</span><span class="sxs-lookup"><span data-stu-id="c2d8a-362">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.11"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="c2d8a-363">Valore soglia sensore per specificare gli intervalli (valori minimo e massimo) che identificano le condizioni operative del sensore, che possono essere condizioni normali, non critiche, critiche o irreversibili.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-363">Sensor threshold value to specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="c2d8a-364">Se **CurrentReading** è compreso tra **LowerThresholdNonCritical** e **UpperThresholdNonCritical**, il sensore segnala un valore normale.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-364">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="c2d8a-365">Se **CurrentReading** è compreso tra **LowerThresholdNonCritical** e **LowerThresholdCritical**, lo stato corrente è non critico.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-365">If **CurrentReading** is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="c2d8a-366">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-366">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2d8a-367">**MaxReadable**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-367">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d8a-368">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-368">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-369">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2d8a-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-370">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Probe temperatura DMTF \| 001,9 "), [**unità**](../wmisdk/standard-qualifiers.md) (" decimi di gradi centigradi ")</span><span class="sxs-lookup"><span data-stu-id="c2d8a-370">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.9"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="c2d8a-371">Valore più grande della proprietà misurata che può essere letta dal sensore numerico.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-371">Largest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="c2d8a-372">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-372">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2d8a-373">**MinReadable**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-373">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d8a-374">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-374">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-375">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2d8a-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-376">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Probe temperatura DMTF \| 001,10 "), [**unità**](../wmisdk/standard-qualifiers.md) (" decimi di gradi centigradi ")</span><span class="sxs-lookup"><span data-stu-id="c2d8a-376">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.10"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="c2d8a-377">Valore più piccolo della proprietà misurata che può essere letta dal sensore numerico.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-377">Smallest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="c2d8a-378">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-378">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2d8a-379">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-379">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d8a-380">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-380">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-381">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2d8a-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-382">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="c2d8a-382">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="c2d8a-383">Etichetta per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-383">Label for the object.</span></span> <span data-ttu-id="c2d8a-384">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-384">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="c2d8a-385">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-385">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2d8a-386">**NominalReading**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-386">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d8a-387">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-387">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-388">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2d8a-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-389">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Probe temperatura DMTF \| 001,6 "), [**unità**](../wmisdk/standard-qualifiers.md) (" decimi di gradi centigradi ")</span><span class="sxs-lookup"><span data-stu-id="c2d8a-389">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.6"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="c2d8a-390">Valore normale o previsto per il sensore numerico.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-390">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="c2d8a-391">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-391">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2d8a-392">**NormalMax**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-392">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d8a-393">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-393">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-394">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2d8a-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-395">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Probe temperatura DMTF \| 001,7 "), [**unità**](../wmisdk/standard-qualifiers.md) (" decimi di gradi centigradi ")</span><span class="sxs-lookup"><span data-stu-id="c2d8a-395">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.7"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="c2d8a-396">Valore normale o previsto per il sensore numerico.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-396">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="c2d8a-397">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-397">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2d8a-398">**NormalMin**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-398">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d8a-399">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-399">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-400">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2d8a-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-401">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Probe temperatura DMTF \| 001,8 "), [**unità**](../wmisdk/standard-qualifiers.md) (" decimi di gradi centigradi ")</span><span class="sxs-lookup"><span data-stu-id="c2d8a-401">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.8"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="c2d8a-402">Linee guida per l'utente sull'intervallo minimo normale per il sensore numerico.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-402">Guidance for the user as to the normal minimum range for the numeric sensor.</span></span>

<span data-ttu-id="c2d8a-403">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-403">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2d8a-404">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-404">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d8a-405">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-406">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2d8a-406">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-407">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c2d8a-407">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c2d8a-408">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-408">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="c2d8a-409">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="c2d8a-409">Example: "\*PNP030b"</span></span>

<span data-ttu-id="c2d8a-410">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-410">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2d8a-411">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-411">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d8a-412">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-412">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-413">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2d8a-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2d8a-414">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-414">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="c2d8a-415">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-415">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c2d8a-416"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-416"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="c2d8a-417"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-417"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c2d8a-418"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-418"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c2d8a-419"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-419"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-420">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-420">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="c2d8a-421"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-421"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-422">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-422">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="c2d8a-423"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-423"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-424">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-424">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="c2d8a-425">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-425">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="c2d8a-426">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-426">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="c2d8a-427"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-427"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-428">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-428">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="c2d8a-429"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-429"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c2d8a-430">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-430">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c2d8a-431">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-431">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d8a-432">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-432">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-433">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2d8a-433">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2d8a-434">Se **true**, il dispositivo può essere gestito dal risparmio di energia (può essere impostato in modalità di sospensione e così via).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-434">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="c2d8a-435">La proprietà non indica che le funzionalità di risparmio energia sono attualmente abilitate, solo che il dispositivo logico è in grado di gestire il risparmio di energia.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-435">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="c2d8a-436">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-436">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2d8a-437">**Risoluzione**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-437">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d8a-438">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-438">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-439">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2d8a-439">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-440">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Probe temperatura DMTF \| 001,17 "), [**unità**](../wmisdk/standard-qualifiers.md) (" centesimi di gradi centigradi ")</span><span class="sxs-lookup"><span data-stu-id="c2d8a-440">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.17"), [**Units**](../wmisdk/standard-qualifiers.md) ("hundredths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="c2d8a-441">Capacità del sensore di risolvere le differenze nella proprietà misurata.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-441">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="c2d8a-442">Questo valore può variare a seconda che il dispositivo sia lineare sull'intervallo dinamico.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-442">This value may vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="c2d8a-443">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-443">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2d8a-444">**Status**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-444">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d8a-445">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-446">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2d8a-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-447">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="c2d8a-447">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c2d8a-448">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-448">Current status of the object.</span></span> <span data-ttu-id="c2d8a-449">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-449">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="c2d8a-450">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-450">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="c2d8a-451">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="c2d8a-451">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c2d8a-452">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-452">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c2d8a-453">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-453">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c2d8a-454">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-454">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c2d8a-455">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="c2d8a-455">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c2d8a-456">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="c2d8a-456">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c2d8a-457">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="c2d8a-457">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c2d8a-458">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="c2d8a-458">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c2d8a-459">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="c2d8a-459">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c2d8a-460">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="c2d8a-460">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c2d8a-461">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="c2d8a-461">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c2d8a-462">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="c2d8a-462">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c2d8a-463">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="c2d8a-463">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c2d8a-464">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-464">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c2d8a-465">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="c2d8a-465">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c2d8a-466">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="c2d8a-466">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c2d8a-467">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="c2d8a-467">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c2d8a-468">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-468">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d8a-469">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-469">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-470">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2d8a-470">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-471">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="c2d8a-471">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="c2d8a-472">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-472">State of the logical device.</span></span> <span data-ttu-id="c2d8a-473">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-473">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="c2d8a-474">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-474">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c2d8a-475">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-475">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c2d8a-476">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-476">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c2d8a-477">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-477">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c2d8a-478">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-478">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c2d8a-479">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-479">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c2d8a-480">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-480">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d8a-481">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-482">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2d8a-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-483">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-483">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="c2d8a-484">Valore per la proprietà **CreationClassName** del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-484">Value for the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="c2d8a-485">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-485">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2d8a-486">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-486">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d8a-487">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-488">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2d8a-488">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-489">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="c2d8a-489">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="c2d8a-490">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-490">Name of the scoping system.</span></span>

<span data-ttu-id="c2d8a-491">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2d8a-492">**Tolleranza**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-492">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d8a-493">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-493">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-494">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2d8a-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-495">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Probe temperatura DMTF \| 001,18 "), [**unità**](../wmisdk/standard-qualifiers.md) (" decimi di gradi centigradi ")</span><span class="sxs-lookup"><span data-stu-id="c2d8a-495">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.18"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="c2d8a-496">Tolleranza del sensore per la proprietà misurata.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-496">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="c2d8a-497">La tolleranza, insieme a risoluzione e accuratezza, viene utilizzata per calcolare il valore effettivo della proprietà fisica misurata.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-497">Tolerance, along with resolution and accuracy, is used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="c2d8a-498">La tolleranza può variare a seconda che il dispositivo sia lineare sull'intervallo dinamico.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-498">Tolerance may vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="c2d8a-499">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-499">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2d8a-500">**UpperThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-500">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d8a-501">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-501">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-502">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2d8a-502">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-503">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Probe temperatura DMTF \| 001,14 "), [**unità**](../wmisdk/standard-qualifiers.md) (" decimi di gradi centigradi ")</span><span class="sxs-lookup"><span data-stu-id="c2d8a-503">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.14"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="c2d8a-504">I valori di soglia del sensore specificano gli intervalli (valori minimo e massimo) che identificano le condizioni operative del sensore, che possono essere condizioni normali, non critiche, critiche o irreversibili.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-504">Sensor's threshold values specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="c2d8a-505">Se **CurrentReading** è compreso tra **UpperThresholdCritical** e **UpperThresholdFatal**, lo stato corrente è critico.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-505">If **CurrentReading** is between **UpperThresholdCritical** and **UpperThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="c2d8a-506">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-506">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2d8a-507">**UpperThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-507">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d8a-508">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-508">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-509">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2d8a-509">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-510">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Probe temperatura DMTF \| 001,16 "), [**unità**](../wmisdk/standard-qualifiers.md) (" decimi di gradi centigradi ")</span><span class="sxs-lookup"><span data-stu-id="c2d8a-510">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.16"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="c2d8a-511">I valori di soglia del sensore specificano gli intervalli (valori minimo e massimo) che identificano le condizioni operative del sensore, che possono essere condizioni normali, non critiche, critiche o irreversibili.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-511">Sensor's threshold values specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="c2d8a-512">Se **CurrentReading** è maggiore di **UpperThresholdFatal**, lo stato corrente è irreversibile.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-512">If **CurrentReading** is above **UpperThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="c2d8a-513">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-513">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2d8a-514">**UpperThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-514">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d8a-515">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-515">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-516">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2d8a-516">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d8a-517">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Probe temperatura DMTF \| 001,12 "), [**unità**](../wmisdk/standard-qualifiers.md) (" decimi di gradi centigradi ")</span><span class="sxs-lookup"><span data-stu-id="c2d8a-517">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.12"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="c2d8a-518">I valori di soglia del sensore specificano gli intervalli (valori minimo e massimo) che identificano le condizioni operative del sensore, che possono essere condizioni normali, non critiche, critiche o irreversibili.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-518">Sensor's threshold values specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="c2d8a-519">Se **CurrentReading** è compreso tra **LowerThresholdNonCritical** e **UpperThresholdNonCritical**, il sensore segnala un valore normale.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-519">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="c2d8a-520">Se **CurrentReading** è compreso tra **UpperThresholdNonCritical** e **UpperThresholdCritical**, lo stato corrente è non critico.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-520">If **CurrentReading** is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="c2d8a-521">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-521">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c2d8a-522">Commenti</span><span class="sxs-lookup"><span data-stu-id="c2d8a-522">Remarks</span></span>

<span data-ttu-id="c2d8a-523">La classe **Win32 \_ TemperatureProbe** è derivata da [**CIM \_ sensore**](cim-temperaturesensor.md).</span><span class="sxs-lookup"><span data-stu-id="c2d8a-523">The **Win32\_TemperatureProbe** class is derived from [**CIM\_TemperatureSensor**](cim-temperaturesensor.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c2d8a-524">Esempio</span><span class="sxs-lookup"><span data-stu-id="c2d8a-524">Examples</span></span>

<span data-ttu-id="c2d8a-525">Nell'esempio seguente vengono restituiti i dati di probe di temperatura per il computer locale.</span><span class="sxs-lookup"><span data-stu-id="c2d8a-525">The following example returns temperature probe data for the local computer.</span></span>


```VB
strComputer = "."
Set colTempProbe = GetObject("Winmgmts:"_
    & "{impersonationLevel=impersonate}!\\"_ 
    & strComputer & "\root\cimv2")._
    InstancesOf("Win32_TemperatureProbe")
Num = 0
For Each obj In colTempProbe      
    WScript.Echo   obj.Name & VBNewLine _
        & obj.DeviceID & VBNewLine _
        & obj.Status & VBNewLine _
        & obj.Resolution & VBNewLine _
        & obj.Tolerance & VBNewLine _
        & obj.Accuracy 
    Num = Num +1
Next
If Num = 0 Then
    WScript.Echo "No temperature probe data"
End If
```



## <a name="requirements"></a><span data-ttu-id="c2d8a-526">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c2d8a-526">Requirements</span></span>



| <span data-ttu-id="c2d8a-527">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2d8a-527">Requirement</span></span> | <span data-ttu-id="c2d8a-528">Valore</span><span class="sxs-lookup"><span data-stu-id="c2d8a-528">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2d8a-529">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2d8a-529">Minimum supported client</span></span><br/> | <span data-ttu-id="c2d8a-530">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c2d8a-530">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c2d8a-531">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2d8a-531">Minimum supported server</span></span><br/> | <span data-ttu-id="c2d8a-532">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c2d8a-532">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c2d8a-533">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c2d8a-533">Namespace</span></span><br/>                | <span data-ttu-id="c2d8a-534">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="c2d8a-534">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c2d8a-535">MOF</span><span class="sxs-lookup"><span data-stu-id="c2d8a-535">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c2d8a-536"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c2d8a-536"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c2d8a-537">DLL</span><span class="sxs-lookup"><span data-stu-id="c2d8a-537">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2d8a-538"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2d8a-538"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2d8a-539">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c2d8a-539">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2d8a-540">**\_Sensore CIM**</span><span class="sxs-lookup"><span data-stu-id="c2d8a-540">**CIM\_TemperatureSensor**</span></span>](cim-temperaturesensor.md)
</dt> <dt>

[<span data-ttu-id="c2d8a-541">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="c2d8a-541">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 

---
description: La \_ classe WMI VoltageProbe Win32 rappresenta le proprietà di un sensore di tensione (voltmetro elettronico).
ms.assetid: ca27c1df-fb38-412d-b77c-d9ccf7941c66
ms.tgt_platform: multiple
title: Classe Win32_VoltageProbe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VoltageProbe
- Win32_VoltageProbe.Reset
- Win32_VoltageProbe.SetPowerState
- Win32_VoltageProbe.Accuracy
- Win32_VoltageProbe.Availability
- Win32_VoltageProbe.Caption
- Win32_VoltageProbe.ConfigManagerErrorCode
- Win32_VoltageProbe.ConfigManagerUserConfig
- Win32_VoltageProbe.CreationClassName
- Win32_VoltageProbe.CurrentReading
- Win32_VoltageProbe.Description
- Win32_VoltageProbe.DeviceID
- Win32_VoltageProbe.ErrorCleared
- Win32_VoltageProbe.ErrorDescription
- Win32_VoltageProbe.InstallDate
- Win32_VoltageProbe.IsLinear
- Win32_VoltageProbe.LastErrorCode
- Win32_VoltageProbe.LowerThresholdCritical
- Win32_VoltageProbe.LowerThresholdFatal
- Win32_VoltageProbe.LowerThresholdNonCritical
- Win32_VoltageProbe.MaxReadable
- Win32_VoltageProbe.MinReadable
- Win32_VoltageProbe.Name
- Win32_VoltageProbe.NominalReading
- Win32_VoltageProbe.NormalMax
- Win32_VoltageProbe.NormalMin
- Win32_VoltageProbe.PNPDeviceID
- Win32_VoltageProbe.PowerManagementCapabilities
- Win32_VoltageProbe.PowerManagementSupported
- Win32_VoltageProbe.Resolution
- Win32_VoltageProbe.Status
- Win32_VoltageProbe.StatusInfo
- Win32_VoltageProbe.SystemCreationClassName
- Win32_VoltageProbe.SystemName
- Win32_VoltageProbe.Tolerance
- Win32_VoltageProbe.UpperThresholdCritical
- Win32_VoltageProbe.UpperThresholdFatal
- Win32_VoltageProbe.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: acb5fe56706ed55098443ad9667eb980a1fe6d23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225541"
---
# <a name="win32_voltageprobe-class"></a><span data-ttu-id="0e739-103">Win32 \_ VoltageProbe (classe)</span><span class="sxs-lookup"><span data-stu-id="0e739-103">Win32\_VoltageProbe class</span></span>

<span data-ttu-id="0e739-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ VoltageProbe Win32** rappresenta le proprietà di un sensore di tensione (voltmetro elettronico).</span><span class="sxs-lookup"><span data-stu-id="0e739-104">The **Win32\_VoltageProbe** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a voltage sensor (electronic voltmeter).</span></span>

<span data-ttu-id="0e739-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="0e739-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="0e739-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="0e739-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e739-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0e739-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{464FFAB8-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class Win32_VoltageProbe : CIM_VoltageSensor
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

## <a name="members"></a><span data-ttu-id="0e739-108">Members</span><span class="sxs-lookup"><span data-stu-id="0e739-108">Members</span></span>

<span data-ttu-id="0e739-109">La classe **Win32 \_ VoltageProbe** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0e739-109">The **Win32\_VoltageProbe** class has these types of members:</span></span>

-   [<span data-ttu-id="0e739-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="0e739-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="0e739-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0e739-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0e739-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="0e739-112">Methods</span></span>

<span data-ttu-id="0e739-113">La classe **Win32 \_ VoltageProbe** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="0e739-113">The **Win32\_VoltageProbe** class has these methods.</span></span>



| <span data-ttu-id="0e739-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="0e739-114">Method</span></span>            | <span data-ttu-id="0e739-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0e739-115">Description</span></span>                                                                                                                                                                                    |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e739-116">**Reimpostazione**</span><span class="sxs-lookup"><span data-stu-id="0e739-116">**Reset**</span></span>         | <span data-ttu-id="0e739-117">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="0e739-117">Not implemented.</span></span> <span data-ttu-id="0e739-118">Per implementare questo metodo, vedere il metodo [**Reset**](reset-method-in-class-cim-controller.md) in [**CIM \_ sensore**](cim-voltagesensor.md).</span><span class="sxs-lookup"><span data-stu-id="0e739-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_VoltageSensor**](cim-voltagesensor.md).</span></span><br/>                 |
| <span data-ttu-id="0e739-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="0e739-119">**SetPowerState**</span></span> | <span data-ttu-id="0e739-120">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="0e739-120">Not implemented.</span></span> <span data-ttu-id="0e739-121">Per implementare questo metodo, vedere il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) in [**CIM \_ sensore**](cim-voltagesensor.md).</span><span class="sxs-lookup"><span data-stu-id="0e739-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_VoltageSensor**](cim-voltagesensor.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0e739-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0e739-122">Properties</span></span>

<span data-ttu-id="0e739-123">La classe **Win32 \_ VoltageProbe** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0e739-123">The **Win32\_VoltageProbe** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0e739-124">**Accuratezza**</span><span class="sxs-lookup"><span data-stu-id="0e739-124">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e739-125">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0e739-125">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e739-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e739-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e739-127">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Probe di tensione DMTF \| 001,19 ")</span><span class="sxs-lookup"><span data-stu-id="0e739-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.19")</span></span>
</dt> </dl>

<span data-ttu-id="0e739-128">Accuratezza del sensore per la proprietà misurata.</span><span class="sxs-lookup"><span data-stu-id="0e739-128">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="0e739-129">Il valore di accuratezza viene registrato come più o meno centesimi di percentuale.</span><span class="sxs-lookup"><span data-stu-id="0e739-129">The accuracy value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="0e739-130">L'accuratezza, insieme a risoluzione e tolleranza, viene utilizzata per calcolare il valore effettivo della proprietà fisica misurata.</span><span class="sxs-lookup"><span data-stu-id="0e739-130">Accuracy, along with resolution and tolerance, is used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="0e739-131">L'accuratezza può variare e varia a seconda che il dispositivo sia lineare o meno nell'intervallo dinamico.</span><span class="sxs-lookup"><span data-stu-id="0e739-131">The accuracy may vary and depends on whether or not the device is linear in its dynamic range.</span></span>

<span data-ttu-id="0e739-132">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="0e739-132">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e739-133">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="0e739-133">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e739-134">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e739-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e739-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e739-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e739-136">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="0e739-136">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="0e739-137">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0e739-137">Availability and status of the device.</span></span>

<span data-ttu-id="0e739-138">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0e739-138">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0e739-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="0e739-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0e739-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="0e739-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="0e739-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="0e739-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="0e739-142"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="0e739-142"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="0e739-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="0e739-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0e739-144"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="0e739-144"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="0e739-145"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="0e739-145"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="0e739-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="0e739-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="0e739-147"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="0e739-147"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0e739-148"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="0e739-148"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="0e739-149"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="0e739-149"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="0e739-150"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="0e739-150"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="0e739-151"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="0e739-151"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-152">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="0e739-152">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="0e739-153"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="0e739-153"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-154">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="0e739-154">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="0e739-155"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="0e739-155"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-156">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="0e739-156">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="0e739-157"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="0e739-157"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="0e739-158"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="0e739-158"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-159">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="0e739-159">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="0e739-160"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="0e739-160"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-161">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="0e739-161">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="0e739-162"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="0e739-162"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-163">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="0e739-163">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="0e739-164"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="0e739-164"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-165">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="0e739-165">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="0e739-166"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="0e739-166"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-167">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="0e739-167">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e739-168">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="0e739-168">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e739-169">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e739-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e739-170">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e739-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e739-171">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="0e739-171">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="0e739-172">Breve descrizione dell'oggetto, ovvero una stringa a una riga.</span><span class="sxs-lookup"><span data-stu-id="0e739-172">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="0e739-173">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e739-173">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e739-174">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="0e739-174">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e739-175">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0e739-175">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e739-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e739-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e739-177">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0e739-177">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0e739-178">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="0e739-178">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="0e739-179">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0e739-179">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="0e739-180"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="0e739-180"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="0e739-181"> (0)</span><span class="sxs-lookup"><span data-stu-id="0e739-181">(0)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-182">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="0e739-182">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="0e739-183"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="0e739-183"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="0e739-184">(1)</span><span class="sxs-lookup"><span data-stu-id="0e739-184">(1)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-185">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="0e739-185">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0e739-186"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0e739-186"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="0e739-187">(2)</span><span class="sxs-lookup"><span data-stu-id="0e739-187">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="0e739-188"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="0e739-188"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="0e739-189">(3)</span><span class="sxs-lookup"><span data-stu-id="0e739-189">(3)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-190">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="0e739-190">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="0e739-191"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="0e739-191"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="0e739-192">(4)</span><span class="sxs-lookup"><span data-stu-id="0e739-192">(4)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-193">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="0e739-193">Device is not working properly.</span></span> <span data-ttu-id="0e739-194">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="0e739-194">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="0e739-195"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="0e739-195"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="0e739-196">(5)</span><span class="sxs-lookup"><span data-stu-id="0e739-196">(5)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-197">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="0e739-197">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="0e739-198"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="0e739-198"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="0e739-199"> (6)</span><span class="sxs-lookup"><span data-stu-id="0e739-199">(6)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-200">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="0e739-200">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="0e739-201"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="0e739-201"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="0e739-202">(7)</span><span class="sxs-lookup"><span data-stu-id="0e739-202">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="0e739-203"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="0e739-203"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="0e739-204">(8)</span><span class="sxs-lookup"><span data-stu-id="0e739-204">(8)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-205">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="0e739-205">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="0e739-206"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="0e739-206"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="0e739-207">(9)</span><span class="sxs-lookup"><span data-stu-id="0e739-207">(9)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-208">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="0e739-208">Device is not working properly.</span></span> <span data-ttu-id="0e739-209">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0e739-209">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="0e739-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0e739-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="0e739-211">(10)</span><span class="sxs-lookup"><span data-stu-id="0e739-211">(10)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-212">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0e739-212">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="0e739-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0e739-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="0e739-214">(11)</span><span class="sxs-lookup"><span data-stu-id="0e739-214">(11)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-215">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0e739-215">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="0e739-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="0e739-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="0e739-217">12</span><span class="sxs-lookup"><span data-stu-id="0e739-217">(12)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-218">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="0e739-218">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="0e739-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0e739-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="0e739-220">(13)</span><span class="sxs-lookup"><span data-stu-id="0e739-220">(13)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-221">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0e739-221">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="0e739-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="0e739-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="0e739-223">(14)</span><span class="sxs-lookup"><span data-stu-id="0e739-223">(14)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-224">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="0e739-224">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="0e739-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="0e739-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="0e739-226">(15)</span><span class="sxs-lookup"><span data-stu-id="0e739-226">(15)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-227">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="0e739-227">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="0e739-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0e739-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="0e739-229">(16)</span><span class="sxs-lookup"><span data-stu-id="0e739-229">(16)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-230">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0e739-230">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="0e739-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="0e739-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="0e739-232">(17)</span><span class="sxs-lookup"><span data-stu-id="0e739-232">(17)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-233">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="0e739-233">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0e739-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0e739-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="0e739-235">(18)</span><span class="sxs-lookup"><span data-stu-id="0e739-235">(18)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-236">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0e739-236">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="0e739-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="0e739-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="0e739-238">(19)</span><span class="sxs-lookup"><span data-stu-id="0e739-238">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="0e739-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="0e739-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="0e739-240">(20)</span><span class="sxs-lookup"><span data-stu-id="0e739-240">(20)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-241">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="0e739-241">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="0e739-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0e739-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="0e739-243">(21)</span><span class="sxs-lookup"><span data-stu-id="0e739-243">(21)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-244">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="0e739-244">System failure.</span></span> <span data-ttu-id="0e739-245">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="0e739-245">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="0e739-246">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0e739-246">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="0e739-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="0e739-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="0e739-248">(22)</span><span class="sxs-lookup"><span data-stu-id="0e739-248">(22)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-249">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="0e739-249">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="0e739-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="0e739-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="0e739-251">(23)</span><span class="sxs-lookup"><span data-stu-id="0e739-251">(23)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-252">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="0e739-252">System failure.</span></span> <span data-ttu-id="0e739-253">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="0e739-253">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="0e739-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="0e739-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="0e739-255">(24)</span><span class="sxs-lookup"><span data-stu-id="0e739-255">(24)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-256">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="0e739-256">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="0e739-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0e739-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="0e739-258">(25)</span><span class="sxs-lookup"><span data-stu-id="0e739-258">(25)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-259">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0e739-259">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="0e739-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0e739-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="0e739-261">(26)</span><span class="sxs-lookup"><span data-stu-id="0e739-261">(26)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-262">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0e739-262">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="0e739-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="0e739-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="0e739-264">(27)</span><span class="sxs-lookup"><span data-stu-id="0e739-264">(27)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-265">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="0e739-265">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="0e739-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="0e739-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="0e739-267">(28)</span><span class="sxs-lookup"><span data-stu-id="0e739-267">(28)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-268">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="0e739-268">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="0e739-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="0e739-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="0e739-270">(29)</span><span class="sxs-lookup"><span data-stu-id="0e739-270">(29)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-271">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="0e739-271">Device is disabled.</span></span> <span data-ttu-id="0e739-272">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="0e739-272">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="0e739-273"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0e739-273"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="0e739-274">(30)</span><span class="sxs-lookup"><span data-stu-id="0e739-274">(30)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-275">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0e739-275">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0e739-276"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0e739-276"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="0e739-277">31</span><span class="sxs-lookup"><span data-stu-id="0e739-277">(31)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-278">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="0e739-278">Device is not working properly.</span></span> <span data-ttu-id="0e739-279">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="0e739-279">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e739-280">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="0e739-280">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e739-281">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="0e739-281">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0e739-282">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e739-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e739-283">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0e739-283">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0e739-284">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="0e739-284">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="0e739-285">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0e739-285">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e739-286">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0e739-286">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e739-287">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e739-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e739-288">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e739-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e739-289">Qualificatori: [ **\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="0e739-289">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="0e739-290">Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="0e739-290">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="0e739-291">Se utilizzata con le altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="0e739-291">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="0e739-292">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0e739-292">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e739-293">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="0e739-293">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e739-294">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0e739-294">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e739-295">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e739-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e739-296">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Probe di tensione DMTF \| 001,5 "), [**unità**](../wmisdk/standard-qualifiers.md) (" millivolt ")</span><span class="sxs-lookup"><span data-stu-id="0e739-296">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.5"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="0e739-297">Valore corrente indicato dal sensore.</span><span class="sxs-lookup"><span data-stu-id="0e739-297">Current value indicated by the sensor.</span></span>

<span data-ttu-id="0e739-298">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="0e739-298">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e739-299">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="0e739-299">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e739-300">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e739-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e739-301">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e739-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e739-302">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="0e739-302">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="0e739-303">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0e739-303">Description of the object.</span></span>

<span data-ttu-id="0e739-304">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e739-304">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e739-305">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="0e739-305">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e739-306">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e739-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e739-307">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e739-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e739-308">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="0e739-308">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="0e739-309">Identificatore univoco del probe di tensione.</span><span class="sxs-lookup"><span data-stu-id="0e739-309">Unique identifier of the voltage probe.</span></span>

<span data-ttu-id="0e739-310">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0e739-310">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e739-311">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="0e739-311">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e739-312">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="0e739-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0e739-313">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e739-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e739-314">Se **true**, l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="0e739-314">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="0e739-315">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0e739-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e739-316">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="0e739-316">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e739-317">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e739-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e739-318">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e739-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e739-319">Altre informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="0e739-319">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="0e739-320">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0e739-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e739-321">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0e739-321">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e739-322">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0e739-322">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0e739-323">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e739-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e739-324">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="0e739-324">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="0e739-325">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0e739-325">Date and time the object is installed.</span></span> <span data-ttu-id="0e739-326">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="0e739-326">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="0e739-327">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e739-327">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e739-328">**Lineari**</span><span class="sxs-lookup"><span data-stu-id="0e739-328">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e739-329">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="0e739-329">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0e739-330">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e739-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e739-331">Se **true**, il sensore è lineare sull'intervallo dinamico.</span><span class="sxs-lookup"><span data-stu-id="0e739-331">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

<span data-ttu-id="0e739-332">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="0e739-332">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e739-333">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="0e739-333">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e739-334">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0e739-334">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e739-335">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e739-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e739-336">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="0e739-336">Last error code reported by the logical device.</span></span>

<span data-ttu-id="0e739-337">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0e739-337">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e739-338">**LowerThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="0e739-338">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e739-339">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0e739-339">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e739-340">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e739-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e739-341">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Probe di tensione DMTF \| 001,13 "), [**unità**](../wmisdk/standard-qualifiers.md) (" millivolt ")</span><span class="sxs-lookup"><span data-stu-id="0e739-341">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.13"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="0e739-342">I valori di soglia del sensore specificano gli intervalli (valori minimo e massimo) per determinare se il sensore funziona in condizioni normali, non critiche, critiche o irreversibili.</span><span class="sxs-lookup"><span data-stu-id="0e739-342">Sensor threshold values specify the ranges (minimum and maximum values) to determine if the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="0e739-343">Se **CurrentReading** è compreso tra **LowerThresholdCritical** e **LowerThresholdFatal**, lo stato corrente è critico.</span><span class="sxs-lookup"><span data-stu-id="0e739-343">If **CurrentReading** is between **LowerThresholdCritical** and **LowerThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="0e739-344">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="0e739-344">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e739-345">**LowerThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="0e739-345">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e739-346">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0e739-346">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e739-347">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e739-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e739-348">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Probe di tensione DMTF \| 001,15 "), [**unità**](../wmisdk/standard-qualifiers.md) (" millivolt ")</span><span class="sxs-lookup"><span data-stu-id="0e739-348">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.15"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="0e739-349">I valori di soglia del sensore specificano gli intervalli (valori minimo e massimo) per determinare se il sensore funziona in condizioni normali, non critiche, critiche o irreversibili.</span><span class="sxs-lookup"><span data-stu-id="0e739-349">Sensor threshold values specify the ranges (minimum and maximum values) to determine if the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="0e739-350">Se **CurrentReading** è inferiore a **LowerThresholdFatal**, lo stato corrente è irreversibile.</span><span class="sxs-lookup"><span data-stu-id="0e739-350">If **CurrentReading** is below **LowerThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="0e739-351">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="0e739-351">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e739-352">**LowerThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="0e739-352">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e739-353">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0e739-353">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e739-354">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e739-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e739-355">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Probe di tensione DMTF \| 001,11 "), [**unità**](../wmisdk/standard-qualifiers.md) (" millivolt ")</span><span class="sxs-lookup"><span data-stu-id="0e739-355">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.11"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="0e739-356">I valori di soglia del sensore specificano gli intervalli (valori minimo e massimo) per determinare se il sensore funziona in condizioni normali, non critiche, critiche o irreversibili.</span><span class="sxs-lookup"><span data-stu-id="0e739-356">Sensor threshold values specify the ranges (minimum and maximum values) to determine if the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="0e739-357">Se **CurrentReading** è compreso tra **LowerThresholdNonCritical** e **UpperThresholdNonCritical**, il sensore segnala un valore normale.</span><span class="sxs-lookup"><span data-stu-id="0e739-357">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="0e739-358">Se **CurrentReading** è compreso tra **LowerThresholdNonCritical** e **LowerThresholdCritical**, lo stato corrente è non critico.</span><span class="sxs-lookup"><span data-stu-id="0e739-358">If **CurrentReading** is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="0e739-359">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="0e739-359">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e739-360">**MaxReadable**</span><span class="sxs-lookup"><span data-stu-id="0e739-360">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e739-361">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0e739-361">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e739-362">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e739-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e739-363">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Probe di tensione DMTF \| 001,9 "), [**unità**](../wmisdk/standard-qualifiers.md) (" millivolt ")</span><span class="sxs-lookup"><span data-stu-id="0e739-363">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.9"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="0e739-364">Valore più grande della proprietà misurata che il sensore numerico può leggere.</span><span class="sxs-lookup"><span data-stu-id="0e739-364">Largest value of the measured property that the numeric sensor can read.</span></span>

<span data-ttu-id="0e739-365">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="0e739-365">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e739-366">**MinReadable**</span><span class="sxs-lookup"><span data-stu-id="0e739-366">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e739-367">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0e739-367">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e739-368">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e739-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e739-369">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Probe di tensione DMTF \| 001,10 "), [**unità**](../wmisdk/standard-qualifiers.md) (" millivolt ")</span><span class="sxs-lookup"><span data-stu-id="0e739-369">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.10"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="0e739-370">Valore più piccolo della proprietà misurata che il sensore numerico può leggere.</span><span class="sxs-lookup"><span data-stu-id="0e739-370">Smallest value of the measured property that the numeric sensor can read.</span></span>

<span data-ttu-id="0e739-371">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="0e739-371">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e739-372">**Nome**</span><span class="sxs-lookup"><span data-stu-id="0e739-372">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e739-373">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e739-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e739-374">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e739-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e739-375">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="0e739-375">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="0e739-376">Etichetta per un oggetto.</span><span class="sxs-lookup"><span data-stu-id="0e739-376">Label for an object.</span></span> <span data-ttu-id="0e739-377">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="0e739-377">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="0e739-378">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e739-378">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e739-379">**NominalReading**</span><span class="sxs-lookup"><span data-stu-id="0e739-379">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e739-380">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0e739-380">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e739-381">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e739-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e739-382">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Probe di tensione DMTF \| 001,6 "), [**unità**](../wmisdk/standard-qualifiers.md) (" millivolt ")</span><span class="sxs-lookup"><span data-stu-id="0e739-382">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.6"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="0e739-383">Valore normale o previsto per il sensore numerico.</span><span class="sxs-lookup"><span data-stu-id="0e739-383">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="0e739-384">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="0e739-384">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e739-385">**NormalMax**</span><span class="sxs-lookup"><span data-stu-id="0e739-385">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e739-386">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0e739-386">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e739-387">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e739-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e739-388">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Probe di tensione DMTF \| 001,7 "), [**unità**](../wmisdk/standard-qualifiers.md) (" millivolt ")</span><span class="sxs-lookup"><span data-stu-id="0e739-388">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.7"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="0e739-389">Valore normale o previsto per il sensore numerico.</span><span class="sxs-lookup"><span data-stu-id="0e739-389">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="0e739-390">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="0e739-390">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e739-391">**NormalMin**</span><span class="sxs-lookup"><span data-stu-id="0e739-391">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e739-392">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0e739-392">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e739-393">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e739-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e739-394">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Probe di tensione DMTF \| 001,8 "), [**unità**](../wmisdk/standard-qualifiers.md) (" millivolt ")</span><span class="sxs-lookup"><span data-stu-id="0e739-394">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.8"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="0e739-395">Indicazioni per l'utente per indicare l'intervallo minimo normale per il sensore numerico.</span><span class="sxs-lookup"><span data-stu-id="0e739-395">Guidance for the user to indicate the normal minimum range for the numeric sensor.</span></span>

<span data-ttu-id="0e739-396">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="0e739-396">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e739-397">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="0e739-397">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e739-398">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e739-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e739-399">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e739-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e739-400">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0e739-400">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0e739-401">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="0e739-401">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="0e739-402">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0e739-402">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="0e739-403">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="0e739-403">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="0e739-404">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="0e739-404">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e739-405">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e739-405">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0e739-406">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e739-406">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e739-407">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="0e739-407">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="0e739-408">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="0e739-408">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0e739-409"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="0e739-409"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="0e739-410"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="0e739-410"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0e739-411"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="0e739-411"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0e739-412"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="0e739-412"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-413">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="0e739-413">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="0e739-414"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="0e739-414"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-415">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="0e739-415">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="0e739-416"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="0e739-416"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-417">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="0e739-417">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="0e739-418">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="0e739-418">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="0e739-419">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="0e739-419">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="0e739-420"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="0e739-420"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-421">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="0e739-421">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="0e739-422"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="0e739-422"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="0e739-423">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="0e739-423">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e739-424">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="0e739-424">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e739-425">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="0e739-425">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0e739-426">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e739-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e739-427">Se **true**, il dispositivo può essere gestito dal risparmio energia, il che significa che può essere messo in modalità di sospensione e così via.</span><span class="sxs-lookup"><span data-stu-id="0e739-427">If **TRUE**, the device can be power-managed, which means that it can be put into suspend mode, and so on.</span></span> <span data-ttu-id="0e739-428">La proprietà non indica che le funzionalità di risparmio energia sono attualmente abilitate, ma indica che il dispositivo logico è in grado di gestire il risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="0e739-428">The property does not indicate that power management features are currently enabled, but it does indicate that the logical device is capable of power management.</span></span>

<span data-ttu-id="0e739-429">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0e739-429">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e739-430">**Risoluzione**</span><span class="sxs-lookup"><span data-stu-id="0e739-430">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e739-431">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0e739-431">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e739-432">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e739-432">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e739-433">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Probe di tensione DMTF \| 001,17 "), [**unità**](../wmisdk/standard-qualifiers.md) (" decimi di millivolt ")</span><span class="sxs-lookup"><span data-stu-id="0e739-433">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.17"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="0e739-434">Capacità del sensore di risolvere le differenze nella proprietà misurata.</span><span class="sxs-lookup"><span data-stu-id="0e739-434">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="0e739-435">Questo valore può variare e varia a seconda che il dispositivo sia lineare nell'intervallo dinamico.</span><span class="sxs-lookup"><span data-stu-id="0e739-435">This value may vary and depends on whether the device is linear in its dynamic range.</span></span>

<span data-ttu-id="0e739-436">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="0e739-436">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e739-437">**Status**</span><span class="sxs-lookup"><span data-stu-id="0e739-437">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e739-438">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e739-438">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e739-439">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e739-439">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e739-440">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="0e739-440">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="0e739-441">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0e739-441">Current status of the object.</span></span> <span data-ttu-id="0e739-442">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="0e739-442">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="0e739-443">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="0e739-443">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="0e739-444">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="0e739-444">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0e739-445">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="0e739-445">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0e739-446">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="0e739-446">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0e739-447">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e739-447">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0e739-448">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="0e739-448">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0e739-449">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="0e739-449">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0e739-450">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="0e739-450">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0e739-451">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="0e739-451">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0e739-452">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="0e739-452">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="0e739-453">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="0e739-453">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0e739-454">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="0e739-454">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0e739-455">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="0e739-455">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="0e739-456">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="0e739-456">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0e739-457">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="0e739-457">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="0e739-458">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="0e739-458">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0e739-459">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="0e739-459">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="0e739-460">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="0e739-460">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0e739-461">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="0e739-461">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e739-462">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e739-462">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e739-463">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e739-463">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e739-464">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="0e739-464">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="0e739-465">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="0e739-465">State of the logical device.</span></span> <span data-ttu-id="0e739-466">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="0e739-466">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="0e739-467">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0e739-467">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0e739-468">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="0e739-468">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0e739-469">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="0e739-469">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0e739-470">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="0e739-470">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0e739-471">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="0e739-471">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0e739-472">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="0e739-472">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0e739-473">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0e739-473">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e739-474">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e739-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e739-475">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e739-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e739-476">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="0e739-476">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="0e739-477">Valore per la proprietà **CreationClassName** del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="0e739-477">Value for the **CreationClassName** property of the scoping computer.</span></span>

<span data-ttu-id="0e739-478">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0e739-478">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e739-479">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="0e739-479">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e739-480">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e739-480">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e739-481">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e739-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e739-482">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="0e739-482">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="0e739-483">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="0e739-483">Name of the scoping system.</span></span>

<span data-ttu-id="0e739-484">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0e739-484">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e739-485">**Tolleranza**</span><span class="sxs-lookup"><span data-stu-id="0e739-485">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e739-486">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0e739-486">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e739-487">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e739-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e739-488">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Probe di tensione DMTF \| 001,18 "), [**unità**](../wmisdk/standard-qualifiers.md) (" millivolt ")</span><span class="sxs-lookup"><span data-stu-id="0e739-488">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.18"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="0e739-489">Tolleranza del sensore per la proprietà misurata.</span><span class="sxs-lookup"><span data-stu-id="0e739-489">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="0e739-490">La tolleranza, insieme a risoluzione e accuratezza, viene utilizzata per calcolare il valore effettivo della proprietà fisica misurata.</span><span class="sxs-lookup"><span data-stu-id="0e739-490">Tolerance, along with resolution and accuracy, is used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="0e739-491">La tolleranza può variare e varia a seconda che il dispositivo sia lineare nell'intervallo dinamico.</span><span class="sxs-lookup"><span data-stu-id="0e739-491">Tolerance may vary, and depends on whether the device is linear in its dynamic range.</span></span>

<span data-ttu-id="0e739-492">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="0e739-492">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e739-493">**UpperThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="0e739-493">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e739-494">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0e739-494">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e739-495">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e739-495">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e739-496">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Probe di tensione DMTF \| 001,14 "), [**unità**](../wmisdk/standard-qualifiers.md) (" millivolt ")</span><span class="sxs-lookup"><span data-stu-id="0e739-496">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.14"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="0e739-497">I valori di soglia del sensore specificano gli intervalli (valori minimo e massimo) per determinare se il sensore funziona in condizioni normali, non critiche, critiche o irreversibili.</span><span class="sxs-lookup"><span data-stu-id="0e739-497">Sensor threshold values specify the ranges (minimum and maximum values) to determine whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="0e739-498">Se **CurrentReading** è compreso tra **UpperThresholdCritical** e **UpperThresholdFatal**, lo stato corrente è critico.</span><span class="sxs-lookup"><span data-stu-id="0e739-498">If **CurrentReading** is between **UpperThresholdCritical** and **UpperThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="0e739-499">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="0e739-499">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e739-500">**UpperThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="0e739-500">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e739-501">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0e739-501">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e739-502">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e739-502">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e739-503">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Probe di tensione DMTF \| 001,16 "), [**unità**](../wmisdk/standard-qualifiers.md) (" millivolt ")</span><span class="sxs-lookup"><span data-stu-id="0e739-503">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.16"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="0e739-504">I valori di soglia del sensore specificano gli intervalli (valori minimo e massimo) per determinare se il sensore funziona in condizioni normali, non critiche, critiche o irreversibili.</span><span class="sxs-lookup"><span data-stu-id="0e739-504">Sensor threshold values specify the ranges (minimum and maximum values) to determine whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="0e739-505">Se **CurrentReading** è maggiore di **UpperThresholdFatal**, lo stato corrente è irreversibile.</span><span class="sxs-lookup"><span data-stu-id="0e739-505">If **CurrentReading** is above **UpperThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="0e739-506">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="0e739-506">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e739-507">**UpperThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="0e739-507">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e739-508">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0e739-508">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e739-509">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e739-509">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e739-510">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Probe di tensione DMTF \| 001,12 "), [**unità**](../wmisdk/standard-qualifiers.md) (" millivolt ")</span><span class="sxs-lookup"><span data-stu-id="0e739-510">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.12"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="0e739-511">I valori di soglia del sensore specificano gli intervalli (valori minimo e massimo) per determinare se il sensore funziona in condizioni normali, non critiche, critiche o irreversibili.</span><span class="sxs-lookup"><span data-stu-id="0e739-511">Sensor threshold values specify the ranges (minimum and maximum values) to determine whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="0e739-512">Se **CurrentReading** è compreso tra **LowerThresholdNonCritical** e **UpperThresholdNonCritical**, il sensore segnala un valore normale.</span><span class="sxs-lookup"><span data-stu-id="0e739-512">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="0e739-513">Se **CurrentReading** è compreso tra **UpperThresholdNonCritical** e **UpperThresholdCritical**, lo stato corrente è non critico.</span><span class="sxs-lookup"><span data-stu-id="0e739-513">If **CurrentReading** is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="0e739-514">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="0e739-514">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0e739-515">Commenti</span><span class="sxs-lookup"><span data-stu-id="0e739-515">Remarks</span></span>

<span data-ttu-id="0e739-516">La classe **Win32 \_ VoltageProbe** è derivata da [**CIM \_ sensore**](cim-voltagesensor.md).</span><span class="sxs-lookup"><span data-stu-id="0e739-516">The **Win32\_VoltageProbe** class is derived from [**CIM\_VoltageSensor**](cim-voltagesensor.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0e739-517">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e739-517">Requirements</span></span>



| <span data-ttu-id="0e739-518">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e739-518">Requirement</span></span> | <span data-ttu-id="0e739-519">Valore</span><span class="sxs-lookup"><span data-stu-id="0e739-519">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e739-520">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e739-520">Minimum supported client</span></span><br/> | <span data-ttu-id="0e739-521">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e739-521">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0e739-522">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e739-522">Minimum supported server</span></span><br/> | <span data-ttu-id="0e739-523">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0e739-523">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0e739-524">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0e739-524">Namespace</span></span><br/>                | <span data-ttu-id="0e739-525">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="0e739-525">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0e739-526">MOF</span><span class="sxs-lookup"><span data-stu-id="0e739-526">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e739-527"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0e739-527"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e739-528">DLL</span><span class="sxs-lookup"><span data-stu-id="0e739-528">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e739-529"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e739-529"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e739-530">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0e739-530">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e739-531">**\_Sensore CIM**</span><span class="sxs-lookup"><span data-stu-id="0e739-531">**CIM\_VoltageSensor**</span></span>](cim-voltagesensor.md)
</dt> <dt>

[<span data-ttu-id="0e739-532">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="0e739-532">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 

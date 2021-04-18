---
description: La \_ classe CIM sensore esiste per compatibilità con le versioni precedenti delle definizioni dello schema CIM. Con aggiunte alle \_ classi CIM Sensor e CIM \_ NumericSensor nella versione 2,2, non è più necessario.
ms.assetid: a578c7a2-27d5-4bd8-86d7-3962d5091f14
ms.tgt_platform: multiple
title: Classe CIM_VoltageSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VoltageSensor
- CIM_VoltageSensor.Accuracy
- CIM_VoltageSensor.Availability
- CIM_VoltageSensor.Caption
- CIM_VoltageSensor.ConfigManagerErrorCode
- CIM_VoltageSensor.ConfigManagerUserConfig
- CIM_VoltageSensor.CreationClassName
- CIM_VoltageSensor.CurrentReading
- CIM_VoltageSensor.Description
- CIM_VoltageSensor.DeviceID
- CIM_VoltageSensor.ErrorCleared
- CIM_VoltageSensor.ErrorDescription
- CIM_VoltageSensor.InstallDate
- CIM_VoltageSensor.IsLinear
- CIM_VoltageSensor.LastErrorCode
- CIM_VoltageSensor.LowerThresholdCritical
- CIM_VoltageSensor.LowerThresholdFatal
- CIM_VoltageSensor.LowerThresholdNonCritical
- CIM_VoltageSensor.MaxReadable
- CIM_VoltageSensor.MinReadable
- CIM_VoltageSensor.Name
- CIM_VoltageSensor.NominalReading
- CIM_VoltageSensor.NormalMax
- CIM_VoltageSensor.NormalMin
- CIM_VoltageSensor.PNPDeviceID
- CIM_VoltageSensor.PowerManagementCapabilities
- CIM_VoltageSensor.PowerManagementSupported
- CIM_VoltageSensor.Resolution
- CIM_VoltageSensor.Status
- CIM_VoltageSensor.StatusInfo
- CIM_VoltageSensor.SystemCreationClassName
- CIM_VoltageSensor.SystemName
- CIM_VoltageSensor.Tolerance
- CIM_VoltageSensor.UpperThresholdCritical
- CIM_VoltageSensor.UpperThresholdFatal
- CIM_VoltageSensor.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5bd0f3d79415254d0af50429c8f1776d2eb451cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304531"
---
# <a name="cim_voltagesensor-class"></a><span data-ttu-id="ddeaa-104">CIM \_ sensore (classe)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-104">CIM\_VoltageSensor class</span></span>

<span data-ttu-id="ddeaa-105">La classe **CIM \_ sensore** esiste per compatibilità con le versioni precedenti delle definizioni dello schema CIM.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-105">The **CIM\_VoltageSensor** class exists for backward compatibility to earlier CIM schema definitions.</span></span> <span data-ttu-id="ddeaa-106">Con aggiunte alle classi CIM [**\_ Sensor**](cim-sensor.md) e [**cim \_ NumericSensor**](cim-numericsensor.md) nella versione 2,2, non è più necessario.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-106">With additions to the [**CIM\_Sensor**](cim-sensor.md) and [**CIM\_NumericSensor**](cim-numericsensor.md) classes in version 2.2, it is no longer necessary.</span></span> <span data-ttu-id="ddeaa-107">Un sensore di tensione può essere definito impostando la proprietà **SensorType** , ereditata dal [**\_ sensore CIM**](cim-sensor.md), su 3 ("Voltage").</span><span class="sxs-lookup"><span data-stu-id="ddeaa-107">A voltage sensor can be defined by setting the **SensorType** property, inherited from [**CIM\_Sensor**](cim-sensor.md), to 3 ("Voltage").</span></span> <span data-ttu-id="ddeaa-108">Altre proprietà di questa classe sono hardcoded per i valori costanti che corrispondono alle definizioni nella gerarchia del sensore.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-108">Other properties of this class are hard-coded to constant values that correspond to definitions in the sensor hierarchy.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ddeaa-109">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ddeaa-110">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ddeaa-111">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="ddeaa-112">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddeaa-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ddeaa-113">Syntax</span></span>

``` syntax
[UUID("{A998F9B4-E3D4-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_VoltageSensor : CIM_NumericSensor
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

## <a name="members"></a><span data-ttu-id="ddeaa-114">Members</span><span class="sxs-lookup"><span data-stu-id="ddeaa-114">Members</span></span>

<span data-ttu-id="ddeaa-115">La classe **CIM \_ sensore** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ddeaa-115">The **CIM\_VoltageSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="ddeaa-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="ddeaa-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="ddeaa-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ddeaa-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ddeaa-118">Metodi</span><span class="sxs-lookup"><span data-stu-id="ddeaa-118">Methods</span></span>

<span data-ttu-id="ddeaa-119">La classe **CIM \_ sensore** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-119">The **CIM\_VoltageSensor** class has these methods.</span></span>



| <span data-ttu-id="ddeaa-120">Metodo</span><span class="sxs-lookup"><span data-stu-id="ddeaa-120">Method</span></span>                                                                   | <span data-ttu-id="ddeaa-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ddeaa-121">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ddeaa-122">**Reset**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-122">**Reset**</span></span>](reset-method-in-class-cim-voltagesensor.md)                 | <span data-ttu-id="ddeaa-123">Richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-123">Requests a reset of the logical device.</span></span> <span data-ttu-id="ddeaa-124">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-124">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="ddeaa-125">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-125">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-voltagesensor.md) | <span data-ttu-id="ddeaa-126">Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-126">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="ddeaa-127">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-127">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ddeaa-128">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ddeaa-128">Properties</span></span>

<span data-ttu-id="ddeaa-129">La classe **CIM \_ sensore** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-129">The **CIM\_VoltageSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ddeaa-130">**Accuratezza**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-130">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddeaa-131">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddeaa-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-133">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("accuratezza"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Probe di tensione DMTF \| 001,19 ")</span><span class="sxs-lookup"><span data-stu-id="ddeaa-133">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Accuracy"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.19")</span></span>
</dt> </dl>

<span data-ttu-id="ddeaa-134">Accuratezza del sensore per la proprietà misurata.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-134">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="ddeaa-135">Il valore viene registrato come più o meno centesimi di percentuale.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-135">Its value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="ddeaa-136">Questa proprietà e le proprietà di **risoluzione** e **tolleranza** vengono utilizzate per calcolare il valore effettivo della proprietà fisica misurata.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-136">This property, and the **Resolution** and **Tolerance** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="ddeaa-137">L'accuratezza può variare a seconda che il dispositivo sia lineare sull'intervallo dinamico.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-137">Accuracy can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="ddeaa-138">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-138">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddeaa-139">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-139">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddeaa-140">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddeaa-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-142">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="ddeaa-142">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="ddeaa-143">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-143">Availability and status of the device.</span></span>

<span data-ttu-id="ddeaa-144">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-144">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ddeaa-145"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-145"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ddeaa-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="ddeaa-147"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-147"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-148">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="ddeaa-148">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="ddeaa-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="ddeaa-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="ddeaa-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="ddeaa-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="ddeaa-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="ddeaa-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="ddeaa-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="ddeaa-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ddeaa-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="ddeaa-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="ddeaa-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="ddeaa-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-159">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-159">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="ddeaa-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-161">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-161">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="ddeaa-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-163">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-163">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="ddeaa-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="ddeaa-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-166">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-166">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="ddeaa-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-168">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-168">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="ddeaa-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-170">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-170">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="ddeaa-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-172">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-172">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="ddeaa-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-174">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-174">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ddeaa-175">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-175">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddeaa-176">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-177">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddeaa-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-178">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="ddeaa-178">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="ddeaa-179">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-179">Short textual description of the object.</span></span>

<span data-ttu-id="ddeaa-180">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-180">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddeaa-181">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-181">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddeaa-182">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddeaa-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-184">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="ddeaa-184">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ddeaa-185">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-185">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="ddeaa-186">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-186">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="ddeaa-187"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-187"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="ddeaa-188"> (0)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-188">(0)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-189">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-189">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="ddeaa-190"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-190"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="ddeaa-191">(1)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-191">(1)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-192">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-192">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="ddeaa-193"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-193"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="ddeaa-194">(2)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-194">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="ddeaa-195"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-195"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="ddeaa-196">(3)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-196">(3)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-197">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-197">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="ddeaa-198"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-198"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="ddeaa-199">(4)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-199">(4)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-200">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-200">Device is not working properly.</span></span> <span data-ttu-id="ddeaa-201">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-201">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="ddeaa-202"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-202"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="ddeaa-203">(5)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-203">(5)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-204">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-204">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="ddeaa-205"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-205"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="ddeaa-206"> (6)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-206">(6)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-207">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-207">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="ddeaa-208"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-208"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="ddeaa-209">(7)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-209">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="ddeaa-210"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-210"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="ddeaa-211">(8)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-211">(8)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-212">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-212">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="ddeaa-213"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-213"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="ddeaa-214">(9)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-214">(9)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-215">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-215">Device is not working properly.</span></span> <span data-ttu-id="ddeaa-216">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-216">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="ddeaa-217"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-217"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="ddeaa-218">(10)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-218">(10)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-219">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-219">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="ddeaa-220"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-220"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="ddeaa-221">(11)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-221">(11)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-222">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-222">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="ddeaa-223"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-223"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="ddeaa-224">12</span><span class="sxs-lookup"><span data-stu-id="ddeaa-224">(12)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-225">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-225">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="ddeaa-226"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-226"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="ddeaa-227">(13)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-227">(13)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-228">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-228">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="ddeaa-229"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-229"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="ddeaa-230">(14)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-230">(14)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-231">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-231">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="ddeaa-232"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-232"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="ddeaa-233">(15)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-233">(15)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-234">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-234">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="ddeaa-235"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-235"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="ddeaa-236">(16)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-236">(16)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-237">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-237">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="ddeaa-238"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-238"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="ddeaa-239">(17)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-239">(17)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-240">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-240">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="ddeaa-241"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-241"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="ddeaa-242">(18)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-242">(18)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-243">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-243">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="ddeaa-244"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-244"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="ddeaa-245">(19)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-245">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="ddeaa-246"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-246"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="ddeaa-247">(20)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-247">(20)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-248">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-248">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="ddeaa-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="ddeaa-250">(21)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-250">(21)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-251">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-251">System failure.</span></span> <span data-ttu-id="ddeaa-252">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-252">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="ddeaa-253">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-253">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="ddeaa-254"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-254"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="ddeaa-255">(22)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-255">(22)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-256">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-256">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="ddeaa-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="ddeaa-258">(23)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-258">(23)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-259">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-259">System failure.</span></span> <span data-ttu-id="ddeaa-260">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-260">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="ddeaa-261"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-261"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="ddeaa-262">(24)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-262">(24)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-263">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-263">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="ddeaa-264"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-264"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="ddeaa-265">(25)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-265">(25)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-266">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-266">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="ddeaa-267"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-267"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="ddeaa-268">(26)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-268">(26)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-269">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-269">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="ddeaa-270"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-270"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="ddeaa-271">(27)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-271">(27)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-272">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-272">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="ddeaa-273"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-273"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="ddeaa-274">(28)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-274">(28)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-275">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-275">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="ddeaa-276"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-276"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="ddeaa-277">(29)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-277">(29)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-278">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-278">Device is disabled.</span></span> <span data-ttu-id="ddeaa-279">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-279">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="ddeaa-280"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-280"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="ddeaa-281">(30)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-281">(30)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-282">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-282">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="ddeaa-283"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-283"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="ddeaa-284">31</span><span class="sxs-lookup"><span data-stu-id="ddeaa-284">(31)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-285">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-285">Device is not working properly.</span></span> <span data-ttu-id="ddeaa-286">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-286">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ddeaa-287">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-287">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddeaa-288">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-288">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-289">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddeaa-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-290">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="ddeaa-290">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ddeaa-291">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-291">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="ddeaa-292">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-292">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddeaa-293">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-293">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddeaa-294">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-295">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddeaa-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-296">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-296">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ddeaa-297">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-297">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="ddeaa-298">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-298">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="ddeaa-299">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddeaa-300">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-300">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddeaa-301">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-301">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-302">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddeaa-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-303">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CurrentReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Probe di tensione DMTF \| 001,5 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" millivolt ")</span><span class="sxs-lookup"><span data-stu-id="ddeaa-303">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CurrentReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="ddeaa-304">Valore corrente indicato dal sensore.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-304">Current value indicated by the sensor.</span></span>

<span data-ttu-id="ddeaa-305">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-305">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddeaa-306">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-306">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddeaa-307">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-308">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddeaa-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-309">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="ddeaa-309">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="ddeaa-310">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-310">Textual description of the object.</span></span>

<span data-ttu-id="ddeaa-311">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-311">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddeaa-312">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-312">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddeaa-313">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-314">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddeaa-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-315">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-315">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ddeaa-316">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-316">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="ddeaa-317">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-317">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddeaa-318">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-318">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddeaa-319">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-319">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-320">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddeaa-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddeaa-321">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-321">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="ddeaa-322">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddeaa-323">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-323">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddeaa-324">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-325">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddeaa-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddeaa-326">Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-326">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="ddeaa-327">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddeaa-328">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-328">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddeaa-329">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-329">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-330">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddeaa-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-331">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="ddeaa-331">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="ddeaa-332">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-332">Date and time the object was installed.</span></span> <span data-ttu-id="ddeaa-333">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-333">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="ddeaa-334">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-334">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddeaa-335">**Lineari**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-335">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddeaa-336">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-336">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-337">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddeaa-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddeaa-338">Se **true**, il sensore è lineare sull'intervallo dinamico.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-338">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

<span data-ttu-id="ddeaa-339">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-339">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddeaa-340">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-340">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddeaa-341">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-341">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-342">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddeaa-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddeaa-343">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-343">Last error code reported by the logical device.</span></span>

<span data-ttu-id="ddeaa-344">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-344">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddeaa-345">**LowerThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-345">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddeaa-346">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-346">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-347">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddeaa-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-348">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Probe di tensione DMTF \| 001,13 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" millivolt ")</span><span class="sxs-lookup"><span data-stu-id="ddeaa-348">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.13"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="ddeaa-349">Valore di soglia che specifica gli intervalli (valori minimo e massimo) per determinare se il sensore funziona in condizioni normali, non critiche, critiche o irreversibili.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-349">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="ddeaa-350">Se la proprietà **CurrentReading** è compresa tra **LowerThresholdCritical** e **LowerThresholdFatal**, lo stato corrente è critical.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-350">If the **CurrentReading** property is between **LowerThresholdCritical** and **LowerThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="ddeaa-351">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-351">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddeaa-352">**LowerThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-352">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddeaa-353">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-353">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-354">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddeaa-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-355">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Probe di tensione DMTF \| 001,15 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" millivolt ")</span><span class="sxs-lookup"><span data-stu-id="ddeaa-355">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="ddeaa-356">Valore di soglia che specifica gli intervalli (valori minimo e massimo) per determinare se il sensore funziona in condizioni normali, non critiche, critiche o irreversibili.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-356">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="ddeaa-357">Se la proprietà **CurrentReading** è inferiore a **LowerThresholdFatal**, lo stato corrente è irreversibile.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-357">If the **CurrentReading** property is below **LowerThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="ddeaa-358">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-358">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddeaa-359">**LowerThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-359">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddeaa-360">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-360">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-361">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddeaa-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-362">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Probe di tensione DMTF \| 001,11 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" millivolt ")</span><span class="sxs-lookup"><span data-stu-id="ddeaa-362">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="ddeaa-363">Valore di soglia che specifica gli intervalli (valori minimo e massimo) per determinare se il sensore funziona in condizioni normali, non critiche, critiche o irreversibili.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-363">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="ddeaa-364">Se la proprietà **CurrentReading** è compresa tra **LowerThresholdNonCritical** e **UpperThresholdNonCritical**, il sensore segnala un valore normale.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-364">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="ddeaa-365">Se la proprietà **CurrentReading** è compresa tra **LowerThresholdNonCritical** e **LowerThresholdCritical**, lo stato corrente è non critico.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-365">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, then the current state is noncritical.</span></span>

<span data-ttu-id="ddeaa-366">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-366">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddeaa-367">**MaxReadable**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-367">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddeaa-368">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-368">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-369">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddeaa-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-370">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Probe di tensione DMTF \| 001,9 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" millivolt ")</span><span class="sxs-lookup"><span data-stu-id="ddeaa-370">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.9"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="ddeaa-371">Valore più grande della proprietà misurata che può essere letta dal sensore numerico.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-371">Largest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="ddeaa-372">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-372">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddeaa-373">**MinReadable**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-373">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddeaa-374">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-374">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-375">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddeaa-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-376">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MinReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Probe di tensione DMTF \| 001,10 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" millivolt ")</span><span class="sxs-lookup"><span data-stu-id="ddeaa-376">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MinReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="ddeaa-377">Valore più piccolo della proprietà misurata che può essere letta dal sensore numerico.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-377">Smallest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="ddeaa-378">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-378">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddeaa-379">**Nome**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-379">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddeaa-380">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-380">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-381">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddeaa-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-382">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="ddeaa-382">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="ddeaa-383">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-383">Label by which the object is known.</span></span> <span data-ttu-id="ddeaa-384">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-384">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="ddeaa-385">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-385">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddeaa-386">**NominalReading**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-386">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddeaa-387">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-387">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-388">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddeaa-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-389">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NominalReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Probe di tensione DMTF \| 001,6 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" millivolt ")</span><span class="sxs-lookup"><span data-stu-id="ddeaa-389">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NominalReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="ddeaa-390">Previsto o valore normale per il sensore numerico.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-390">Expected or normal value for the numeric sensor.</span></span>

<span data-ttu-id="ddeaa-391">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-391">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddeaa-392">**NormalMax**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-392">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddeaa-393">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-393">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-394">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddeaa-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-395">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMax"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Probe di tensione DMTF \| 001,7 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" millivolt ")</span><span class="sxs-lookup"><span data-stu-id="ddeaa-395">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMax"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="ddeaa-396">Intervallo massimo normale per il sensore numerico.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-396">Normal maximum range for the numeric sensor.</span></span>

<span data-ttu-id="ddeaa-397">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-397">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddeaa-398">**NormalMin**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-398">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddeaa-399">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-399">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-400">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddeaa-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-401">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMin"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Probe di tensione DMTF \| 001,8 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" millivolt ")</span><span class="sxs-lookup"><span data-stu-id="ddeaa-401">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMin"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="ddeaa-402">Intervallo minimo normale per il sensore numerico.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-402">Normal minimum range for the numeric sensor.</span></span>

<span data-ttu-id="ddeaa-403">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-403">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddeaa-404">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-404">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddeaa-405">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-406">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddeaa-406">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-407">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="ddeaa-407">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ddeaa-408">Win32 Plug and Play identificatore dispositivo del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-408">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="ddeaa-409">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-409">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="ddeaa-410">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="ddeaa-410">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="ddeaa-411">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-411">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddeaa-412">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-412">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-413">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddeaa-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddeaa-414">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-414">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="ddeaa-415">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-415">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ddeaa-416"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-416"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="ddeaa-417"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-417"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ddeaa-418"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-418"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="ddeaa-419"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-419"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-420">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-420">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="ddeaa-421"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-421"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-422">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-422">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="ddeaa-423"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-423"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-424">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-424">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="ddeaa-425">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-425">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="ddeaa-426">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-426">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="ddeaa-427"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-427"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-428">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-428">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="ddeaa-429"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-429"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="ddeaa-430">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-430">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ddeaa-431">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-431">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddeaa-432">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-432">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-433">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddeaa-433">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddeaa-434">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-434">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="ddeaa-435">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="ddeaa-435">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="ddeaa-436">Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-436">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="ddeaa-437">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="ddeaa-437">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="ddeaa-438">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddeaa-439">**Risoluzione**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-439">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddeaa-440">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-440">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-441">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddeaa-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-442">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Risoluzione"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Probe di tensione DMTF \| 001,17 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" decimi di millivolt ")</span><span class="sxs-lookup"><span data-stu-id="ddeaa-442">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Resolution"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.17"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="ddeaa-443">Capacità del sensore di risolvere le differenze nella proprietà misurata.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-443">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="ddeaa-444">Questa proprietà e le proprietà di **accuratezza** e **tolleranza** vengono utilizzate per calcolare il valore effettivo della proprietà fisica misurata.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-444">This property, and the **Accuracy** and **Tolerance** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="ddeaa-445">Questo valore può variare a seconda che il dispositivo sia lineare sull'intervallo dinamico.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-445">This value can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="ddeaa-446">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-446">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddeaa-447">**Status**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-447">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddeaa-448">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-449">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddeaa-449">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-450">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="ddeaa-450">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="ddeaa-451">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-451">Current status of the object.</span></span>

<span data-ttu-id="ddeaa-452">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-452">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="ddeaa-453">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="ddeaa-453">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ddeaa-454">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="ddeaa-454">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="ddeaa-455">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="ddeaa-455">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ddeaa-456">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="ddeaa-456">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ddeaa-457">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="ddeaa-457">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="ddeaa-458">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="ddeaa-458">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ddeaa-459">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="ddeaa-459">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="ddeaa-460">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="ddeaa-460">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="ddeaa-461">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="ddeaa-461">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="ddeaa-462">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-462">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="ddeaa-463">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="ddeaa-463">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="ddeaa-464">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="ddeaa-464">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="ddeaa-465">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="ddeaa-465">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ddeaa-466">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-466">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddeaa-467">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-467">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-468">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddeaa-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-469">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="ddeaa-469">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="ddeaa-470">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-470">State of the logical device.</span></span> <span data-ttu-id="ddeaa-471">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-471">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="ddeaa-472">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-472">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ddeaa-473">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-473">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ddeaa-474">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-474">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="ddeaa-475">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-475">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ddeaa-476">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-476">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="ddeaa-477">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-477">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ddeaa-478">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-478">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddeaa-479">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-479">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-480">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddeaa-480">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-481">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-481">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ddeaa-482">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-482">Scoping system's creation class name.</span></span>

<span data-ttu-id="ddeaa-483">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-483">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddeaa-484">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-484">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddeaa-485">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-485">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-486">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddeaa-486">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-487">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ddeaa-487">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ddeaa-488">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-488">Scoping system's name.</span></span>

<span data-ttu-id="ddeaa-489">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-489">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddeaa-490">**Tolleranza**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-490">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddeaa-491">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-491">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-492">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddeaa-492">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-493">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tolerance"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Probe di tensione DMTF \| 001,18 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" millivolt ")</span><span class="sxs-lookup"><span data-stu-id="ddeaa-493">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tolerance"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.18"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="ddeaa-494">Tolleranza del sensore per la proprietà misurata.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-494">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="ddeaa-495">Questa proprietà e le proprietà di **risoluzione** e **accuratezza** vengono utilizzate per calcolare il valore effettivo della proprietà fisica misurata.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-495">This property, and the **Resolution** and **Accuracy** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="ddeaa-496">La tolleranza può variare a seconda che il dispositivo sia lineare sull'intervallo dinamico.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-496">Tolerance can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="ddeaa-497">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-497">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddeaa-498">**UpperThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-498">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddeaa-499">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-499">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-500">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddeaa-500">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-501">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Probe di tensione DMTF \| 001,14 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" millivolt ")</span><span class="sxs-lookup"><span data-stu-id="ddeaa-501">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.14"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="ddeaa-502">Valore di soglia che specifica gli intervalli (valori minimo e massimo) per determinare se il sensore funziona in condizioni normali, non critiche, critiche o irreversibili.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-502">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="ddeaa-503">Se la proprietà **CurrentReading** è compresa tra **UpperThresholdCritical** e **UpperThresholdFatal**, lo stato corrente è critical.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-503">If the **CurrentReading** property is between **UpperThresholdCritical** and **UpperThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="ddeaa-504">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-504">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddeaa-505">**UpperThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-505">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddeaa-506">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-506">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-507">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddeaa-507">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-508">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Probe di tensione DMTF \| 001,16 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" millivolt ")</span><span class="sxs-lookup"><span data-stu-id="ddeaa-508">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.16"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="ddeaa-509">Valore di soglia che specifica gli intervalli (valori minimo e massimo) per determinare se il sensore funziona in condizioni normali, non critiche, critiche o irreversibili.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-509">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="ddeaa-510">Se la proprietà **CurrentReading** è sopra **UpperThresholdFatal**, lo stato corrente è irreversibile.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-510">If the **CurrentReading** property is above **UpperThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="ddeaa-511">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-511">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddeaa-512">**UpperThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-512">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddeaa-513">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-513">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-514">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddeaa-514">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddeaa-515">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Probe di tensione DMTF \| 001,12 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" millivolt ")</span><span class="sxs-lookup"><span data-stu-id="ddeaa-515">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="ddeaa-516">Valore di soglia che specifica gli intervalli (valori minimo e massimo) per determinare se il sensore funziona in condizioni normali, non critiche, critiche o irreversibili.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-516">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="ddeaa-517">Se la proprietà **CurrentReading** è compresa tra **LowerThresholdNonCritical** e **UpperThresholdNonCritical**, il sensore segnala un valore normale.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-517">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="ddeaa-518">Se la proprietà **CurrentReading** è compresa tra **UpperThresholdNonCritical** e **UpperThresholdCritical**, lo stato corrente è non critico.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-518">If the **CurrentReading** property is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, then the current state is noncritical.</span></span>

<span data-ttu-id="ddeaa-519">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-519">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ddeaa-520">Commenti</span><span class="sxs-lookup"><span data-stu-id="ddeaa-520">Remarks</span></span>

<span data-ttu-id="ddeaa-521">La classe **CIM \_ sensore** è derivata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-521">The **CIM\_VoltageSensor** class is derived from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

<span data-ttu-id="ddeaa-522">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-522">WMI does not implement this class.</span></span> <span data-ttu-id="ddeaa-523">Per le classi WMI derivate da **CIM \_ sensore**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ddeaa-523">For WMI classes derived from **CIM\_VoltageSensor**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="ddeaa-524">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-524">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ddeaa-525">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-525">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddeaa-526">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ddeaa-526">Requirements</span></span>



| <span data-ttu-id="ddeaa-527">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddeaa-527">Requirement</span></span> | <span data-ttu-id="ddeaa-528">Valore</span><span class="sxs-lookup"><span data-stu-id="ddeaa-528">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ddeaa-529">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ddeaa-529">Minimum supported client</span></span><br/> | <span data-ttu-id="ddeaa-530">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ddeaa-530">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ddeaa-531">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ddeaa-531">Minimum supported server</span></span><br/> | <span data-ttu-id="ddeaa-532">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ddeaa-532">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ddeaa-533">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ddeaa-533">Namespace</span></span><br/>                | <span data-ttu-id="ddeaa-534">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="ddeaa-534">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ddeaa-535">MOF</span><span class="sxs-lookup"><span data-stu-id="ddeaa-535">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ddeaa-536"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ddeaa-536"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ddeaa-537">DLL</span><span class="sxs-lookup"><span data-stu-id="ddeaa-537">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ddeaa-538"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ddeaa-538"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddeaa-539">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ddeaa-539">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddeaa-540">**\_NUMERICSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-540">**CIM\_NumericSensor**</span></span>](cim-numericsensor.md)
</dt> </dl>

 


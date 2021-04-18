---
description: La \_ classe CIM contagiri esiste per la compatibilità con le versioni precedenti delle definizioni dello schema CIM.
ms.assetid: 30b7c23e-05c6-4fd6-80bc-3f729855ab45
ms.tgt_platform: multiple
title: Classe CIM_Tachometer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Tachometer
- CIM_Tachometer.Accuracy
- CIM_Tachometer.Availability
- CIM_Tachometer.Caption
- CIM_Tachometer.ConfigManagerErrorCode
- CIM_Tachometer.ConfigManagerUserConfig
- CIM_Tachometer.CreationClassName
- CIM_Tachometer.CurrentReading
- CIM_Tachometer.Description
- CIM_Tachometer.DeviceID
- CIM_Tachometer.ErrorCleared
- CIM_Tachometer.ErrorDescription
- CIM_Tachometer.InstallDate
- CIM_Tachometer.IsLinear
- CIM_Tachometer.LastErrorCode
- CIM_Tachometer.LowerThresholdCritical
- CIM_Tachometer.LowerThresholdFatal
- CIM_Tachometer.LowerThresholdNonCritical
- CIM_Tachometer.MaxReadable
- CIM_Tachometer.MinReadable
- CIM_Tachometer.Name
- CIM_Tachometer.NominalReading
- CIM_Tachometer.NormalMax
- CIM_Tachometer.NormalMin
- CIM_Tachometer.PNPDeviceID
- CIM_Tachometer.PowerManagementCapabilities
- CIM_Tachometer.PowerManagementSupported
- CIM_Tachometer.Resolution
- CIM_Tachometer.Status
- CIM_Tachometer.StatusInfo
- CIM_Tachometer.SystemCreationClassName
- CIM_Tachometer.SystemName
- CIM_Tachometer.Tolerance
- CIM_Tachometer.UpperThresholdCritical
- CIM_Tachometer.UpperThresholdFatal
- CIM_Tachometer.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5f761d7ef18ef7e27a46d6b5e8a5a00442752561
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305300"
---
# <a name="cim_tachometer-class"></a><span data-ttu-id="b1430-103">\_Classe CIM contagiri</span><span class="sxs-lookup"><span data-stu-id="b1430-103">CIM\_Tachometer class</span></span>

<span data-ttu-id="b1430-104">La classe **CIM \_ contagiri** esiste per la compatibilità con le versioni precedenti delle definizioni dello schema CIM.</span><span class="sxs-lookup"><span data-stu-id="b1430-104">The **CIM\_Tachometer** class exists for backward compatibility with earlier CIM schema definitions.</span></span> <span data-ttu-id="b1430-105">Con aggiunte alle classi CIM [**\_ Sensor**](cim-sensor.md) e [**cim \_ NumericSensor**](cim-numericsensor.md) nella versione 2,2, non è più necessario.</span><span class="sxs-lookup"><span data-stu-id="b1430-105">With additions to the [**CIM\_Sensor**](cim-sensor.md) and [**CIM\_NumericSensor**](cim-numericsensor.md) classes in version 2.2, it is no longer necessary.</span></span> <span data-ttu-id="b1430-106">È possibile definire un contagiri impostando la proprietà **SensorType** , ereditata **dal \_ sensore CIM**, su 5 ("contagiri").</span><span class="sxs-lookup"><span data-stu-id="b1430-106">A tachometer can be defined by setting the **SensorType** property, inherited from **CIM\_Sensor**, to 5 ("Tachometer").</span></span> <span data-ttu-id="b1430-107">Altre proprietà di questa classe sono hardcoded per i valori costanti che corrispondono alle definizioni nella gerarchia del sensore.</span><span class="sxs-lookup"><span data-stu-id="b1430-107">Other properties of this class are hard-coded to constant values that correspond to definitions in the sensor hierarchy.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b1430-108">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="b1430-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b1430-109">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b1430-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b1430-110">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b1430-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="b1430-111">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="b1430-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1430-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b1430-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{237D964F-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_Tachometer : CIM_NumericSensor
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

## <a name="members"></a><span data-ttu-id="b1430-113">Members</span><span class="sxs-lookup"><span data-stu-id="b1430-113">Members</span></span>

<span data-ttu-id="b1430-114">La classe **CIM \_ contagiri** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b1430-114">The **CIM\_Tachometer** class has these types of members:</span></span>

-   [<span data-ttu-id="b1430-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="b1430-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="b1430-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b1430-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b1430-117">Metodi</span><span class="sxs-lookup"><span data-stu-id="b1430-117">Methods</span></span>

<span data-ttu-id="b1430-118">La classe **CIM \_ contagiri** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="b1430-118">The **CIM\_Tachometer** class has these methods.</span></span>



| <span data-ttu-id="b1430-119">Metodo</span><span class="sxs-lookup"><span data-stu-id="b1430-119">Method</span></span>                                                                | <span data-ttu-id="b1430-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1430-120">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b1430-121">**Reset**</span><span class="sxs-lookup"><span data-stu-id="b1430-121">**Reset**</span></span>](reset-method-in-class-cim-tachometer.md)                 | <span data-ttu-id="b1430-122">Richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="b1430-122">Requests a reset of the logical device.</span></span> <span data-ttu-id="b1430-123">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="b1430-123">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="b1430-124">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="b1430-124">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-tachometer.md) | <span data-ttu-id="b1430-125">Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="b1430-125">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="b1430-126">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="b1430-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b1430-127">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b1430-127">Properties</span></span>

<span data-ttu-id="b1430-128">La classe **CIM \_ contagiri** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b1430-128">The **CIM\_Tachometer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b1430-129">**Accuratezza**</span><span class="sxs-lookup"><span data-stu-id="b1430-129">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1430-130">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b1430-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1430-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1430-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1430-132">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("centesimi di percentuale")</span><span class="sxs-lookup"><span data-stu-id="b1430-132">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hundredths of percent")</span></span>
</dt> </dl>

<span data-ttu-id="b1430-133">Accuratezza del sensore per la proprietà misurata.</span><span class="sxs-lookup"><span data-stu-id="b1430-133">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="b1430-134">Il valore viene registrato come più o meno centesimi di percentuale.</span><span class="sxs-lookup"><span data-stu-id="b1430-134">Its value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="b1430-135">Questa proprietà e le proprietà di **risoluzione** e **tolleranza** vengono utilizzate per calcolare il valore effettivo della proprietà fisica misurata.</span><span class="sxs-lookup"><span data-stu-id="b1430-135">This property, and the **Resolution** and **Tolerance** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="b1430-136">L'accuratezza può variare a seconda che il dispositivo sia lineare sull'intervallo dinamico.</span><span class="sxs-lookup"><span data-stu-id="b1430-136">Accuracy can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="b1430-137">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="b1430-137">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1430-138">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="b1430-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1430-139">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b1430-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b1430-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1430-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1430-141">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="b1430-141">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="b1430-142">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b1430-142">Availability and status of the device.</span></span>

<span data-ttu-id="b1430-143">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1430-143">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b1430-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="b1430-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b1430-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="b1430-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="b1430-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="b1430-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-147">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="b1430-147">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="b1430-148"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="b1430-148"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="b1430-149"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="b1430-149"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b1430-150"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="b1430-150"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="b1430-151"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="b1430-151"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="b1430-152"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="b1430-152"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="b1430-153"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="b1430-153"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b1430-154"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="b1430-154"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="b1430-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="b1430-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="b1430-156"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="b1430-156"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="b1430-157"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="b1430-157"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-158">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="b1430-158">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="b1430-159"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="b1430-159"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-160">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="b1430-160">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="b1430-161"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="b1430-161"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-162">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="b1430-162">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="b1430-163"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="b1430-163"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="b1430-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="b1430-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-165">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="b1430-165">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="b1430-166"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="b1430-166"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-167">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="b1430-167">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="b1430-168"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="b1430-168"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-169">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="b1430-169">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="b1430-170"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="b1430-170"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-171">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="b1430-171">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="b1430-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="b1430-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-173">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="b1430-173">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b1430-174">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="b1430-174">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1430-175">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b1430-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1430-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1430-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1430-177">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b1430-177">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b1430-178">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b1430-178">Short textual description of the object.</span></span>

<span data-ttu-id="b1430-179">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1430-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1430-180">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b1430-180">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1430-181">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b1430-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1430-182">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1430-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1430-183">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b1430-183">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b1430-184">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="b1430-184">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="b1430-185">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1430-185">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="b1430-186"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="b1430-186"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="b1430-187"> (0)</span><span class="sxs-lookup"><span data-stu-id="b1430-187">(0)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-188">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="b1430-188">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="b1430-189"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="b1430-189"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="b1430-190">(1)</span><span class="sxs-lookup"><span data-stu-id="b1430-190">(1)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-191">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="b1430-191">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b1430-192"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b1430-192"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="b1430-193">(2)</span><span class="sxs-lookup"><span data-stu-id="b1430-193">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="b1430-194"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="b1430-194"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="b1430-195">(3)</span><span class="sxs-lookup"><span data-stu-id="b1430-195">(3)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-196">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="b1430-196">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b1430-197"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="b1430-197"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="b1430-198">(4)</span><span class="sxs-lookup"><span data-stu-id="b1430-198">(4)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-199">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="b1430-199">Device is not working properly.</span></span> <span data-ttu-id="b1430-200">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="b1430-200">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="b1430-201"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="b1430-201"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="b1430-202">(5)</span><span class="sxs-lookup"><span data-stu-id="b1430-202">(5)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-203">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="b1430-203">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="b1430-204"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="b1430-204"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="b1430-205"> (6)</span><span class="sxs-lookup"><span data-stu-id="b1430-205">(6)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-206">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="b1430-206">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="b1430-207"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="b1430-207"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="b1430-208">(7)</span><span class="sxs-lookup"><span data-stu-id="b1430-208">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="b1430-209"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="b1430-209"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="b1430-210">(8)</span><span class="sxs-lookup"><span data-stu-id="b1430-210">(8)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-211">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="b1430-211">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="b1430-212"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="b1430-212"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="b1430-213">(9)</span><span class="sxs-lookup"><span data-stu-id="b1430-213">(9)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-214">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="b1430-214">Device is not working properly.</span></span> <span data-ttu-id="b1430-215">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b1430-215">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="b1430-216"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b1430-216"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="b1430-217">(10)</span><span class="sxs-lookup"><span data-stu-id="b1430-217">(10)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-218">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b1430-218">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="b1430-219"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b1430-219"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="b1430-220">(11)</span><span class="sxs-lookup"><span data-stu-id="b1430-220">(11)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-221">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b1430-221">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="b1430-222"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="b1430-222"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="b1430-223">12</span><span class="sxs-lookup"><span data-stu-id="b1430-223">(12)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-224">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="b1430-224">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="b1430-225"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b1430-225"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="b1430-226">(13)</span><span class="sxs-lookup"><span data-stu-id="b1430-226">(13)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-227">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b1430-227">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="b1430-228"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="b1430-228"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="b1430-229">(14)</span><span class="sxs-lookup"><span data-stu-id="b1430-229">(14)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-230">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="b1430-230">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="b1430-231"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="b1430-231"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="b1430-232">(15)</span><span class="sxs-lookup"><span data-stu-id="b1430-232">(15)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-233">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="b1430-233">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="b1430-234"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b1430-234"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="b1430-235">(16)</span><span class="sxs-lookup"><span data-stu-id="b1430-235">(16)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-236">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b1430-236">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="b1430-237"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="b1430-237"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="b1430-238">(17)</span><span class="sxs-lookup"><span data-stu-id="b1430-238">(17)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-239">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="b1430-239">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b1430-240"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b1430-240"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="b1430-241">(18)</span><span class="sxs-lookup"><span data-stu-id="b1430-241">(18)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-242">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b1430-242">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="b1430-243"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="b1430-243"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="b1430-244">(19)</span><span class="sxs-lookup"><span data-stu-id="b1430-244">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b1430-245"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="b1430-245"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="b1430-246">(20)</span><span class="sxs-lookup"><span data-stu-id="b1430-246">(20)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-247">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="b1430-247">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="b1430-248"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b1430-248"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="b1430-249">(21)</span><span class="sxs-lookup"><span data-stu-id="b1430-249">(21)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-250">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="b1430-250">System failure.</span></span> <span data-ttu-id="b1430-251">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="b1430-251">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="b1430-252">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b1430-252">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="b1430-253"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="b1430-253"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="b1430-254">(22)</span><span class="sxs-lookup"><span data-stu-id="b1430-254">(22)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-255">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="b1430-255">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="b1430-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="b1430-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="b1430-257">(23)</span><span class="sxs-lookup"><span data-stu-id="b1430-257">(23)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-258">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="b1430-258">System failure.</span></span> <span data-ttu-id="b1430-259">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="b1430-259">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="b1430-260"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="b1430-260"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="b1430-261">(24)</span><span class="sxs-lookup"><span data-stu-id="b1430-261">(24)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-262">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="b1430-262">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b1430-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b1430-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b1430-264">(25)</span><span class="sxs-lookup"><span data-stu-id="b1430-264">(25)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-265">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b1430-265">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b1430-266"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b1430-266"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b1430-267">(26)</span><span class="sxs-lookup"><span data-stu-id="b1430-267">(26)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-268">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b1430-268">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="b1430-269"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="b1430-269"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="b1430-270">(27)</span><span class="sxs-lookup"><span data-stu-id="b1430-270">(27)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-271">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="b1430-271">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="b1430-272"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="b1430-272"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="b1430-273">(28)</span><span class="sxs-lookup"><span data-stu-id="b1430-273">(28)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-274">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="b1430-274">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="b1430-275"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="b1430-275"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="b1430-276">(29)</span><span class="sxs-lookup"><span data-stu-id="b1430-276">(29)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-277">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="b1430-277">Device is disabled.</span></span> <span data-ttu-id="b1430-278">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="b1430-278">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="b1430-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b1430-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="b1430-280">(30)</span><span class="sxs-lookup"><span data-stu-id="b1430-280">(30)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-281">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b1430-281">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b1430-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b1430-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="b1430-283">31</span><span class="sxs-lookup"><span data-stu-id="b1430-283">(31)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-284">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="b1430-284">Device is not working properly.</span></span> <span data-ttu-id="b1430-285">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="b1430-285">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b1430-286">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="b1430-286">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1430-287">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b1430-287">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b1430-288">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1430-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1430-289">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b1430-289">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b1430-290">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="b1430-290">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="b1430-291">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1430-291">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1430-292">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b1430-292">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1430-293">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b1430-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1430-294">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1430-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1430-295">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b1430-295">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b1430-296">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="b1430-296">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="b1430-297">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="b1430-297">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="b1430-298">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1430-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1430-299">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="b1430-299">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1430-300">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b1430-300">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1430-301">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1430-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1430-302">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CurrentReading"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("rivoluzioni al minuto")</span><span class="sxs-lookup"><span data-stu-id="b1430-302">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CurrentReading"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="b1430-303">Valore corrente indicato dal sensore.</span><span class="sxs-lookup"><span data-stu-id="b1430-303">Current value indicated by the sensor.</span></span>

<span data-ttu-id="b1430-304">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="b1430-304">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1430-305">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="b1430-305">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1430-306">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b1430-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1430-307">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1430-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1430-308">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="b1430-308">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b1430-309">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b1430-309">Textual description of the object.</span></span>

<span data-ttu-id="b1430-310">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1430-310">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1430-311">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="b1430-311">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1430-312">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b1430-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1430-313">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1430-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1430-314">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b1430-314">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b1430-315">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="b1430-315">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="b1430-316">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1430-316">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1430-317">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="b1430-317">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1430-318">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b1430-318">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b1430-319">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1430-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1430-320">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="b1430-320">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="b1430-321">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1430-321">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1430-322">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="b1430-322">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1430-323">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b1430-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1430-324">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1430-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1430-325">Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.</span><span class="sxs-lookup"><span data-stu-id="b1430-325">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="b1430-326">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1430-326">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1430-327">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b1430-327">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1430-328">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b1430-328">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b1430-329">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1430-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1430-330">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="b1430-330">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b1430-331">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b1430-331">Date and time the object was installed.</span></span> <span data-ttu-id="b1430-332">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="b1430-332">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b1430-333">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1430-333">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1430-334">**Lineari**</span><span class="sxs-lookup"><span data-stu-id="b1430-334">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1430-335">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b1430-335">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b1430-336">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1430-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1430-337">Se **true**, il sensore è lineare sull'intervallo dinamico.</span><span class="sxs-lookup"><span data-stu-id="b1430-337">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

<span data-ttu-id="b1430-338">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="b1430-338">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1430-339">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b1430-339">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1430-340">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b1430-340">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1430-341">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1430-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1430-342">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="b1430-342">Last error code reported by the logical device.</span></span>

<span data-ttu-id="b1430-343">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1430-343">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1430-344">**LowerThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="b1430-344">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1430-345">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b1430-345">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1430-346">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1430-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1430-347">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdCritical"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("rivoluzioni al minuto")</span><span class="sxs-lookup"><span data-stu-id="b1430-347">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdCritical"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="b1430-348">Valore di soglia che specifica gli intervalli (valori minimo e massimo) per determinare se il sensore funziona in condizioni normali, non critiche, critiche o irreversibili.</span><span class="sxs-lookup"><span data-stu-id="b1430-348">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="b1430-349">Se la proprietà **CurrentReading** è compresa tra **LowerThresholdCritical** e **LowerThresholdFatal**, lo stato corrente è critical.</span><span class="sxs-lookup"><span data-stu-id="b1430-349">If the **CurrentReading** property is between **LowerThresholdCritical** and **LowerThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="b1430-350">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="b1430-350">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1430-351">**LowerThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="b1430-351">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1430-352">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b1430-352">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1430-353">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1430-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1430-354">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdFatal"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("rivoluzioni al minuto")</span><span class="sxs-lookup"><span data-stu-id="b1430-354">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdFatal"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="b1430-355">Valore di soglia che specifica gli intervalli (valori minimo e massimo) per determinare se il sensore funziona in condizioni normali, non critiche, critiche o irreversibili.</span><span class="sxs-lookup"><span data-stu-id="b1430-355">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="b1430-356">Se la proprietà **CurrentReading** è inferiore a **LowerThresholdFatal**, lo stato corrente è irreversibile.</span><span class="sxs-lookup"><span data-stu-id="b1430-356">If the **CurrentReading** property is below **LowerThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="b1430-357">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="b1430-357">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1430-358">**LowerThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="b1430-358">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1430-359">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b1430-359">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1430-360">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1430-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1430-361">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdNonCritical"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("rivoluzioni al minuto")</span><span class="sxs-lookup"><span data-stu-id="b1430-361">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdNonCritical"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="b1430-362">Valore di soglia che specifica gli intervalli (valori minimo e massimo) per determinare se il sensore funziona in condizioni normali, non critiche, critiche o irreversibili.</span><span class="sxs-lookup"><span data-stu-id="b1430-362">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="b1430-363">Se la proprietà **CurrentReading** è compresa tra **LowerThresholdNonCritical** e **UpperThresholdNonCritical**, il sensore segnala un valore normale.</span><span class="sxs-lookup"><span data-stu-id="b1430-363">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="b1430-364">Se la proprietà **CurrentReading** è compresa tra **LowerThresholdNonCritical** e **LowerThresholdCritical**, lo stato corrente è non critico.</span><span class="sxs-lookup"><span data-stu-id="b1430-364">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, then the current state is non-critical.</span></span>

<span data-ttu-id="b1430-365">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="b1430-365">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1430-366">**MaxReadable**</span><span class="sxs-lookup"><span data-stu-id="b1430-366">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1430-367">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b1430-367">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1430-368">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1430-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1430-369">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxReadable"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("rivoluzioni al minuto")</span><span class="sxs-lookup"><span data-stu-id="b1430-369">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxReadable"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="b1430-370">Valore più grande della proprietà misurata che può essere letta dal sensore numerico.</span><span class="sxs-lookup"><span data-stu-id="b1430-370">Largest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="b1430-371">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="b1430-371">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1430-372">**MinReadable**</span><span class="sxs-lookup"><span data-stu-id="b1430-372">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1430-373">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b1430-373">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1430-374">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1430-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1430-375">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MinReadable"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("rivoluzioni al minuto")</span><span class="sxs-lookup"><span data-stu-id="b1430-375">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MinReadable"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="b1430-376">Valore più piccolo della proprietà misurata che può essere letta dal sensore numerico.</span><span class="sxs-lookup"><span data-stu-id="b1430-376">Smallest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="b1430-377">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="b1430-377">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1430-378">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b1430-378">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1430-379">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b1430-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1430-380">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1430-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1430-381">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="b1430-381">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b1430-382">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="b1430-382">Label by which the object is known.</span></span> <span data-ttu-id="b1430-383">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="b1430-383">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="b1430-384">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1430-384">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1430-385">**NominalReading**</span><span class="sxs-lookup"><span data-stu-id="b1430-385">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1430-386">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b1430-386">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1430-387">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1430-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1430-388">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NominalReading"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("rivoluzioni al minuto")</span><span class="sxs-lookup"><span data-stu-id="b1430-388">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NominalReading"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="b1430-389">Previsto o valore normale per il sensore numerico.</span><span class="sxs-lookup"><span data-stu-id="b1430-389">Expected or normal value for the numeric sensor.</span></span>

<span data-ttu-id="b1430-390">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="b1430-390">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1430-391">**NormalMax**</span><span class="sxs-lookup"><span data-stu-id="b1430-391">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1430-392">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b1430-392">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1430-393">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1430-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1430-394">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMax"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("rivoluzioni al minuto")</span><span class="sxs-lookup"><span data-stu-id="b1430-394">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMax"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="b1430-395">Intervallo massimo normale per il sensore numerico.</span><span class="sxs-lookup"><span data-stu-id="b1430-395">Normal maximum range for the numeric sensor.</span></span>

<span data-ttu-id="b1430-396">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="b1430-396">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1430-397">**NormalMin**</span><span class="sxs-lookup"><span data-stu-id="b1430-397">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1430-398">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b1430-398">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1430-399">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1430-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1430-400">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMin"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("rivoluzioni al minuto")</span><span class="sxs-lookup"><span data-stu-id="b1430-400">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMin"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="b1430-401">Intervallo minimo normale per il sensore numerico.</span><span class="sxs-lookup"><span data-stu-id="b1430-401">Normal minimum range for the numeric sensor.</span></span>

<span data-ttu-id="b1430-402">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="b1430-402">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1430-403">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="b1430-403">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1430-404">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b1430-404">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1430-405">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1430-405">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1430-406">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b1430-406">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b1430-407">Win32 Plug and Play identificatore dispositivo del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="b1430-407">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="b1430-408">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1430-408">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="b1430-409">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="b1430-409">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="b1430-410">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="b1430-410">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1430-411">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b1430-411">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b1430-412">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1430-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1430-413">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="b1430-413">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="b1430-414">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="b1430-414">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b1430-415"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="b1430-415"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="b1430-416"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="b1430-416"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b1430-417"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="b1430-417"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b1430-418"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="b1430-418"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-419">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="b1430-419">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="b1430-420"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="b1430-420"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-421">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="b1430-421">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="b1430-422"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="b1430-422"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-423">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="b1430-423">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="b1430-424">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="b1430-424">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="b1430-425">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="b1430-425">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="b1430-426"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="b1430-426"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-427">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="b1430-427">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="b1430-428"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="b1430-428"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b1430-429">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="b1430-429">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b1430-430">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="b1430-430">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1430-431">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b1430-431">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b1430-432">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1430-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1430-433">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="b1430-433">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="b1430-434">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="b1430-434">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="b1430-435">Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="b1430-435">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="b1430-436">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="b1430-436">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="b1430-437">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1430-437">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1430-438">**Risoluzione**</span><span class="sxs-lookup"><span data-stu-id="b1430-438">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1430-439">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b1430-439">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1430-440">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1430-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1430-441">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Risoluzione"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("decimi di rivoluzioni al minuto")</span><span class="sxs-lookup"><span data-stu-id="b1430-441">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Resolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="b1430-442">Capacità del sensore di risolvere le differenze nella proprietà misurata.</span><span class="sxs-lookup"><span data-stu-id="b1430-442">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="b1430-443">Questo valore può variare a seconda che il dispositivo sia lineare sull'intervallo dinamico.</span><span class="sxs-lookup"><span data-stu-id="b1430-443">This value can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="b1430-444">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="b1430-444">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1430-445">**Status**</span><span class="sxs-lookup"><span data-stu-id="b1430-445">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1430-446">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b1430-446">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1430-447">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1430-447">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1430-448">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="b1430-448">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b1430-449">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b1430-449">Current status of the object.</span></span> <span data-ttu-id="b1430-450">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1430-450">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b1430-451">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="b1430-451">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b1430-452">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="b1430-452">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b1430-453">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="b1430-453">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b1430-454">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="b1430-454">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b1430-455">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="b1430-455">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b1430-456">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="b1430-456">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b1430-457">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="b1430-457">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b1430-458">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="b1430-458">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b1430-459">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="b1430-459">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b1430-460">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="b1430-460">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b1430-461">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="b1430-461">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b1430-462">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="b1430-462">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b1430-463">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="b1430-463">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b1430-464">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="b1430-464">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1430-465">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b1430-465">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b1430-466">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1430-466">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1430-467">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="b1430-467">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="b1430-468">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="b1430-468">State of the logical device.</span></span> <span data-ttu-id="b1430-469">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="b1430-469">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="b1430-470">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1430-470">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b1430-471">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="b1430-471">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b1430-472">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="b1430-472">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b1430-473">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="b1430-473">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b1430-474">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="b1430-474">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b1430-475">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="b1430-475">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b1430-476">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b1430-476">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1430-477">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b1430-477">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1430-478">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1430-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1430-479">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b1430-479">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b1430-480">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="b1430-480">Scoping system's creation class name.</span></span>

<span data-ttu-id="b1430-481">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1430-481">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1430-482">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b1430-482">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1430-483">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b1430-483">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1430-484">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1430-484">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1430-485">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b1430-485">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b1430-486">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="b1430-486">Scoping system's name.</span></span>

<span data-ttu-id="b1430-487">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1430-487">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1430-488">**Tolleranza**</span><span class="sxs-lookup"><span data-stu-id="b1430-488">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1430-489">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b1430-489">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1430-490">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1430-490">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1430-491">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tolerance"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("rivoluzioni al minuto")</span><span class="sxs-lookup"><span data-stu-id="b1430-491">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tolerance"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="b1430-492">Tolleranza del sensore per la proprietà misurata.</span><span class="sxs-lookup"><span data-stu-id="b1430-492">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="b1430-493">Questa proprietà e le proprietà di **risoluzione** e **accuratezza** vengono utilizzate per calcolare il valore effettivo della proprietà fisica misurata.</span><span class="sxs-lookup"><span data-stu-id="b1430-493">This property, and the **Resolution** and **Accuracy** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="b1430-494">La tolleranza può variare a seconda che il dispositivo sia lineare sull'intervallo dinamico.</span><span class="sxs-lookup"><span data-stu-id="b1430-494">Tolerance can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="b1430-495">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="b1430-495">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1430-496">**UpperThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="b1430-496">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1430-497">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b1430-497">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1430-498">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1430-498">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1430-499">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdCritical"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("rivoluzioni al minuto")</span><span class="sxs-lookup"><span data-stu-id="b1430-499">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdCritical"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="b1430-500">Valore di soglia che specifica gli intervalli (valori minimo e massimo) per determinare se il sensore funziona in condizioni normali, non critiche, critiche o irreversibili.</span><span class="sxs-lookup"><span data-stu-id="b1430-500">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="b1430-501">Se la proprietà **CurrentReading** è compresa tra **UpperThresholdCritical** e **UpperThresholdFatal**, lo stato corrente è critical.</span><span class="sxs-lookup"><span data-stu-id="b1430-501">If the **CurrentReading** property is between **UpperThresholdCritical** and **UpperThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="b1430-502">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="b1430-502">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1430-503">**UpperThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="b1430-503">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1430-504">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b1430-504">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1430-505">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1430-505">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1430-506">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdFatal"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("rivoluzioni al minuto")</span><span class="sxs-lookup"><span data-stu-id="b1430-506">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdFatal"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="b1430-507">Valore di soglia che specifica gli intervalli (valori minimo e massimo) per determinare se il sensore funziona in condizioni normali, non critiche, critiche o irreversibili.</span><span class="sxs-lookup"><span data-stu-id="b1430-507">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="b1430-508">Se la proprietà **CurrentReading** è sopra **UpperThresholdFatal**, lo stato corrente è irreversibile.</span><span class="sxs-lookup"><span data-stu-id="b1430-508">If the **CurrentReading** property is above **UpperThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="b1430-509">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="b1430-509">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1430-510">**UpperThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="b1430-510">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1430-511">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b1430-511">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1430-512">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1430-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1430-513">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdNonCritical"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("rivoluzioni al minuto")</span><span class="sxs-lookup"><span data-stu-id="b1430-513">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdNonCritical"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="b1430-514">Valore di soglia che specifica gli intervalli (valori minimo e massimo) per determinare se il sensore funziona in condizioni normali, non critiche, critiche o irreversibili.</span><span class="sxs-lookup"><span data-stu-id="b1430-514">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="b1430-515">Se la proprietà **CurrentReading** è compresa tra **LowerThresholdNonCritical** e **UpperThresholdNonCritical**, il sensore segnala un valore normale.</span><span class="sxs-lookup"><span data-stu-id="b1430-515">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="b1430-516">Se la proprietà **CurrentReading** è compresa tra **UpperThresholdNonCritical** e **UpperThresholdCritical**, lo stato corrente è non critico.</span><span class="sxs-lookup"><span data-stu-id="b1430-516">If the **CurrentReading** property is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, then the current state is non-critical.</span></span>

<span data-ttu-id="b1430-517">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="b1430-517">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b1430-518">Commenti</span><span class="sxs-lookup"><span data-stu-id="b1430-518">Remarks</span></span>

<span data-ttu-id="b1430-519">La classe **CIM \_ contagiri** è derivata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="b1430-519">The **CIM\_Tachometer** class is derived from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

<span data-ttu-id="b1430-520">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="b1430-520">WMI does not implement this class.</span></span>

<span data-ttu-id="b1430-521">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="b1430-521">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b1430-522">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="b1430-522">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1430-523">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1430-523">Requirements</span></span>



| <span data-ttu-id="b1430-524">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1430-524">Requirement</span></span> | <span data-ttu-id="b1430-525">Valore</span><span class="sxs-lookup"><span data-stu-id="b1430-525">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1430-526">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1430-526">Minimum supported client</span></span><br/> | <span data-ttu-id="b1430-527">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b1430-527">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b1430-528">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1430-528">Minimum supported server</span></span><br/> | <span data-ttu-id="b1430-529">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b1430-529">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b1430-530">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b1430-530">Namespace</span></span><br/>                | <span data-ttu-id="b1430-531">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="b1430-531">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b1430-532">MOF</span><span class="sxs-lookup"><span data-stu-id="b1430-532">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b1430-533"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b1430-533"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b1430-534">DLL</span><span class="sxs-lookup"><span data-stu-id="b1430-534">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1430-535"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1430-535"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1430-536">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1430-536">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1430-537">**\_NUMERICSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="b1430-537">**CIM\_NumericSensor**</span></span>](cim-numericsensor.md)
</dt> </dl>

 


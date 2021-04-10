---
description: La \_ classe WMI CurrentProbe Win32 rappresenta le proprietà di un sensore di monitoraggio corrente (amperometro).
ms.assetid: 2e1da856-b787-404b-ac4b-080c4950bad8
ms.tgt_platform: multiple
title: Classe Win32_CurrentProbe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CurrentProbe
- Win32_CurrentProbe.Reset
- Win32_CurrentProbe.SetPowerState
- Win32_CurrentProbe.Accuracy
- Win32_CurrentProbe.Availability
- Win32_CurrentProbe.Caption
- Win32_CurrentProbe.ConfigManagerErrorCode
- Win32_CurrentProbe.ConfigManagerUserConfig
- Win32_CurrentProbe.CreationClassName
- Win32_CurrentProbe.CurrentReading
- Win32_CurrentProbe.Description
- Win32_CurrentProbe.DeviceID
- Win32_CurrentProbe.ErrorCleared
- Win32_CurrentProbe.ErrorDescription
- Win32_CurrentProbe.InstallDate
- Win32_CurrentProbe.IsLinear
- Win32_CurrentProbe.LastErrorCode
- Win32_CurrentProbe.LowerThresholdCritical
- Win32_CurrentProbe.LowerThresholdFatal
- Win32_CurrentProbe.LowerThresholdNonCritical
- Win32_CurrentProbe.MaxReadable
- Win32_CurrentProbe.MinReadable
- Win32_CurrentProbe.Name
- Win32_CurrentProbe.NominalReading
- Win32_CurrentProbe.NormalMax
- Win32_CurrentProbe.NormalMin
- Win32_CurrentProbe.PNPDeviceID
- Win32_CurrentProbe.PowerManagementCapabilities
- Win32_CurrentProbe.PowerManagementSupported
- Win32_CurrentProbe.Resolution
- Win32_CurrentProbe.Status
- Win32_CurrentProbe.StatusInfo
- Win32_CurrentProbe.SystemCreationClassName
- Win32_CurrentProbe.SystemName
- Win32_CurrentProbe.Tolerance
- Win32_CurrentProbe.UpperThresholdCritical
- Win32_CurrentProbe.UpperThresholdFatal
- Win32_CurrentProbe.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: be834e56eb3d958a8cd6ee653dc9a248c14ae3bc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878365"
---
# <a name="win32_currentprobe-class"></a><span data-ttu-id="d01c0-103">Win32 \_ CurrentProbe (classe)</span><span class="sxs-lookup"><span data-stu-id="d01c0-103">Win32\_CurrentProbe class</span></span>

<span data-ttu-id="d01c0-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ CurrentProbe Win32** rappresenta le proprietà di un sensore di monitoraggio corrente (amperometro).</span><span class="sxs-lookup"><span data-stu-id="d01c0-104">The **Win32\_CurrentProbe** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a current monitoring sensor (ammeter).</span></span>

<span data-ttu-id="d01c0-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="d01c0-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d01c0-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="d01c0-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d01c0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d01c0-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{464FFABA-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class Win32_CurrentProbe : CIM_CurrentSensor
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

## <a name="members"></a><span data-ttu-id="d01c0-108">Members</span><span class="sxs-lookup"><span data-stu-id="d01c0-108">Members</span></span>

<span data-ttu-id="d01c0-109">La classe **Win32 \_ CurrentProbe** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d01c0-109">The **Win32\_CurrentProbe** class has these types of members:</span></span>

-   [<span data-ttu-id="d01c0-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="d01c0-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="d01c0-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d01c0-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d01c0-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="d01c0-112">Methods</span></span>

<span data-ttu-id="d01c0-113">La classe **Win32 \_ CurrentProbe** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="d01c0-113">The **Win32\_CurrentProbe** class has these methods.</span></span>



| <span data-ttu-id="d01c0-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="d01c0-114">Method</span></span>            | <span data-ttu-id="d01c0-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d01c0-115">Description</span></span>                                                                                                                                                                                                      |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d01c0-116">**Reimpostazione**</span><span class="sxs-lookup"><span data-stu-id="d01c0-116">**Reset**</span></span>         | <span data-ttu-id="d01c0-117">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="d01c0-117">Not implemented.</span></span> <span data-ttu-id="d01c0-118">Per implementare questo metodo, vedere il metodo [**Reset**](reset-method-in-class-cim-controller.md) in [**CIM \_ CurrentSensor**](cim-currentsensor.md) per la documentazione.</span><span class="sxs-lookup"><span data-stu-id="d01c0-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_CurrentSensor**](cim-currentsensor.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="d01c0-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="d01c0-119">**SetPowerState**</span></span> | <span data-ttu-id="d01c0-120">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="d01c0-120">Not implemented.</span></span> <span data-ttu-id="d01c0-121">Per implementare questo metodo, vedere il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) in [**CIM \_ CurrentSensor**](cim-currentsensor.md) per la documentazione.</span><span class="sxs-lookup"><span data-stu-id="d01c0-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_CurrentSensor**](cim-currentsensor.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d01c0-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d01c0-122">Properties</span></span>

<span data-ttu-id="d01c0-123">La classe **Win32 \_ CurrentProbe** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d01c0-123">The **Win32\_CurrentProbe** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d01c0-124">**Accuratezza**</span><span class="sxs-lookup"><span data-stu-id="d01c0-124">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d01c0-125">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d01c0-125">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d01c0-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-127">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Probe corrente elettrica DMTF \| 001,19 ")</span><span class="sxs-lookup"><span data-stu-id="d01c0-127">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.19")</span></span>
</dt> </dl>

<span data-ttu-id="d01c0-128">Accuratezza del sensore per la proprietà misurata.</span><span class="sxs-lookup"><span data-stu-id="d01c0-128">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="d01c0-129">Il valore viene registrato come più o meno centesimi di percentuale.</span><span class="sxs-lookup"><span data-stu-id="d01c0-129">The value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="d01c0-130">L'accuratezza, insieme a risoluzione e tolleranza, viene utilizzata per calcolare il valore effettivo della proprietà fisica misurata.</span><span class="sxs-lookup"><span data-stu-id="d01c0-130">Accuracy, along with resolution and tolerance, is used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="d01c0-131">L'accuratezza può variare e varia a seconda che il dispositivo sia lineare o meno sull'intervallo dinamico.</span><span class="sxs-lookup"><span data-stu-id="d01c0-131">Accuracy may vary and depends on whether or not the device is linear over its dynamic range.</span></span>

<span data-ttu-id="d01c0-132">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d01c0-132">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d01c0-133">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="d01c0-133">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d01c0-134">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d01c0-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d01c0-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-136">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="d01c0-136">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="d01c0-137">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d01c0-137">Availability and status of the device.</span></span>

<span data-ttu-id="d01c0-138">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d01c0-138">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d01c0-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="d01c0-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d01c0-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="d01c0-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="d01c0-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="d01c0-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-142">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="d01c0-142">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="d01c0-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="d01c0-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="d01c0-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="d01c0-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d01c0-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="d01c0-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="d01c0-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="d01c0-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="d01c0-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="d01c0-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="d01c0-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="d01c0-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d01c0-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="d01c0-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="d01c0-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="d01c0-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="d01c0-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="d01c0-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="d01c0-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="d01c0-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-153">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="d01c0-153">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="d01c0-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="d01c0-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-155">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="d01c0-155">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="d01c0-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="d01c0-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-157">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="d01c0-157">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="d01c0-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="d01c0-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="d01c0-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="d01c0-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-160">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="d01c0-160">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="d01c0-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="d01c0-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-162">(sospeso)</span><span class="sxs-lookup"><span data-stu-id="d01c0-162">Paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="d01c0-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="d01c0-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-164">Non pronto.</span><span class="sxs-lookup"><span data-stu-id="d01c0-164">Not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="d01c0-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="d01c0-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-166">Non configurata.</span><span class="sxs-lookup"><span data-stu-id="d01c0-166">Not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="d01c0-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="d01c0-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-168">Il sensore corrente non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="d01c0-168">Current sensor is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d01c0-169">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="d01c0-169">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d01c0-170">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d01c0-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d01c0-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-172">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="d01c0-172">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d01c0-173">Breve descrizione dell'oggetto stringa a una riga.</span><span class="sxs-lookup"><span data-stu-id="d01c0-173">Short description of the object a one-line string.</span></span>

<span data-ttu-id="d01c0-174">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d01c0-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d01c0-175">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d01c0-175">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d01c0-176">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d01c0-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-177">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d01c0-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-178">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d01c0-178">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d01c0-179">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d01c0-179">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="d01c0-180">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d01c0-180">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="d01c0-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="d01c0-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="d01c0-182"> (0)</span><span class="sxs-lookup"><span data-stu-id="d01c0-182">(0)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-183">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="d01c0-183">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="d01c0-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="d01c0-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="d01c0-185">(1)</span><span class="sxs-lookup"><span data-stu-id="d01c0-185">(1)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-186">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="d01c0-186">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d01c0-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d01c0-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="d01c0-188">(2)</span><span class="sxs-lookup"><span data-stu-id="d01c0-188">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="d01c0-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="d01c0-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="d01c0-190">(3)</span><span class="sxs-lookup"><span data-stu-id="d01c0-190">(3)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-191">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="d01c0-191">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="d01c0-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="d01c0-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="d01c0-193">(4)</span><span class="sxs-lookup"><span data-stu-id="d01c0-193">(4)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-194">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="d01c0-194">Device is not working properly.</span></span> <span data-ttu-id="d01c0-195">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="d01c0-195">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="d01c0-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="d01c0-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="d01c0-197">(5)</span><span class="sxs-lookup"><span data-stu-id="d01c0-197">(5)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-198">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="d01c0-198">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="d01c0-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="d01c0-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="d01c0-200"> (6)</span><span class="sxs-lookup"><span data-stu-id="d01c0-200">(6)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-201">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="d01c0-201">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="d01c0-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="d01c0-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="d01c0-203">(7)</span><span class="sxs-lookup"><span data-stu-id="d01c0-203">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="d01c0-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="d01c0-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="d01c0-205">(8)</span><span class="sxs-lookup"><span data-stu-id="d01c0-205">(8)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-206">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="d01c0-206">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="d01c0-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="d01c0-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="d01c0-208">(9)</span><span class="sxs-lookup"><span data-stu-id="d01c0-208">(9)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-209">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="d01c0-209">Device is not working properly.</span></span> <span data-ttu-id="d01c0-210">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d01c0-210">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="d01c0-211"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d01c0-211"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="d01c0-212">(10)</span><span class="sxs-lookup"><span data-stu-id="d01c0-212">(10)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-213">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d01c0-213">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="d01c0-214"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d01c0-214"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="d01c0-215">(11)</span><span class="sxs-lookup"><span data-stu-id="d01c0-215">(11)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-216">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d01c0-216">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="d01c0-217"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="d01c0-217"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="d01c0-218">12</span><span class="sxs-lookup"><span data-stu-id="d01c0-218">(12)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-219">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="d01c0-219">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="d01c0-220"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d01c0-220"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="d01c0-221">(13)</span><span class="sxs-lookup"><span data-stu-id="d01c0-221">(13)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-222">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d01c0-222">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="d01c0-223"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="d01c0-223"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="d01c0-224">(14)</span><span class="sxs-lookup"><span data-stu-id="d01c0-224">(14)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-225">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="d01c0-225">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="d01c0-226"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="d01c0-226"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="d01c0-227">(15)</span><span class="sxs-lookup"><span data-stu-id="d01c0-227">(15)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-228">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="d01c0-228">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="d01c0-229"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d01c0-229"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="d01c0-230">(16)</span><span class="sxs-lookup"><span data-stu-id="d01c0-230">(16)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-231">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d01c0-231">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="d01c0-232"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="d01c0-232"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="d01c0-233">(17)</span><span class="sxs-lookup"><span data-stu-id="d01c0-233">(17)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-234">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="d01c0-234">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d01c0-235"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d01c0-235"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="d01c0-236">(18)</span><span class="sxs-lookup"><span data-stu-id="d01c0-236">(18)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-237">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d01c0-237">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="d01c0-238"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="d01c0-238"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="d01c0-239">(19)</span><span class="sxs-lookup"><span data-stu-id="d01c0-239">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="d01c0-240"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="d01c0-240"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="d01c0-241">(20)</span><span class="sxs-lookup"><span data-stu-id="d01c0-241">(20)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-242">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="d01c0-242">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="d01c0-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d01c0-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="d01c0-244">(21)</span><span class="sxs-lookup"><span data-stu-id="d01c0-244">(21)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-245">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="d01c0-245">System failure.</span></span> <span data-ttu-id="d01c0-246">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="d01c0-246">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="d01c0-247">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d01c0-247">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="d01c0-248"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="d01c0-248"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="d01c0-249">(22)</span><span class="sxs-lookup"><span data-stu-id="d01c0-249">(22)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-250">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="d01c0-250">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="d01c0-251"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="d01c0-251"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="d01c0-252">(23)</span><span class="sxs-lookup"><span data-stu-id="d01c0-252">(23)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-253">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="d01c0-253">System failure.</span></span> <span data-ttu-id="d01c0-254">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="d01c0-254">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="d01c0-255"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="d01c0-255"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="d01c0-256">(24)</span><span class="sxs-lookup"><span data-stu-id="d01c0-256">(24)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-257">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="d01c0-257">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="d01c0-258"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d01c0-258"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="d01c0-259">(25)</span><span class="sxs-lookup"><span data-stu-id="d01c0-259">(25)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-260">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d01c0-260">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="d01c0-261"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d01c0-261"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="d01c0-262">(26)</span><span class="sxs-lookup"><span data-stu-id="d01c0-262">(26)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-263">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d01c0-263">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="d01c0-264"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="d01c0-264"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="d01c0-265">(27)</span><span class="sxs-lookup"><span data-stu-id="d01c0-265">(27)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-266">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="d01c0-266">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="d01c0-267"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="d01c0-267"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="d01c0-268">(28)</span><span class="sxs-lookup"><span data-stu-id="d01c0-268">(28)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-269">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="d01c0-269">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="d01c0-270"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="d01c0-270"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="d01c0-271">(29)</span><span class="sxs-lookup"><span data-stu-id="d01c0-271">(29)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-272">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="d01c0-272">Device is disabled.</span></span> <span data-ttu-id="d01c0-273">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="d01c0-273">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="d01c0-274"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d01c0-274"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="d01c0-275">(30)</span><span class="sxs-lookup"><span data-stu-id="d01c0-275">(30)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-276">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d01c0-276">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d01c0-277"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d01c0-277"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="d01c0-278">31</span><span class="sxs-lookup"><span data-stu-id="d01c0-278">(31)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-279">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="d01c0-279">Device is not working properly.</span></span> <span data-ttu-id="d01c0-280">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="d01c0-280">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d01c0-281">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="d01c0-281">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d01c0-282">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d01c0-282">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-283">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d01c0-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-284">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d01c0-284">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d01c0-285">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="d01c0-285">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="d01c0-286">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d01c0-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d01c0-287">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d01c0-287">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d01c0-288">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d01c0-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-289">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d01c0-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-290">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d01c0-290">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d01c0-291">Nome della prima classe concreta visualizzata nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="d01c0-291">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="d01c0-292">Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="d01c0-292">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="d01c0-293">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d01c0-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d01c0-294">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="d01c0-294">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d01c0-295">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d01c0-295">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-296">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d01c0-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-297">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Probe corrente elettrica DMTF \| 001,5 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliampere ")</span><span class="sxs-lookup"><span data-stu-id="d01c0-297">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="d01c0-298">Valore corrente indicato dal sensore.</span><span class="sxs-lookup"><span data-stu-id="d01c0-298">Current value indicated by the sensor.</span></span>

<span data-ttu-id="d01c0-299">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d01c0-299">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d01c0-300">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="d01c0-300">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d01c0-301">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d01c0-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-302">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d01c0-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-303">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="d01c0-303">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d01c0-304">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d01c0-304">Description of the object.</span></span>

<span data-ttu-id="d01c0-305">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d01c0-305">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d01c0-306">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="d01c0-306">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d01c0-307">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d01c0-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-308">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d01c0-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-309">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="d01c0-309">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="d01c0-310">Identificatore univoco del probe corrente.</span><span class="sxs-lookup"><span data-stu-id="d01c0-310">Unique identifier of the current probe.</span></span>

<span data-ttu-id="d01c0-311">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d01c0-311">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d01c0-312">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="d01c0-312">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d01c0-313">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d01c0-313">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-314">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d01c0-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d01c0-315">Se **true**, l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="d01c0-315">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="d01c0-316">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d01c0-316">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d01c0-317">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="d01c0-317">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d01c0-318">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d01c0-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-319">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d01c0-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d01c0-320">Altre informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="d01c0-320">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="d01c0-321">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d01c0-321">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d01c0-322">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d01c0-322">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d01c0-323">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d01c0-323">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-324">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d01c0-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-325">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="d01c0-325">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d01c0-326">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d01c0-326">Date and time the object was installed.</span></span> <span data-ttu-id="d01c0-327">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="d01c0-327">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="d01c0-328">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d01c0-328">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d01c0-329">**Lineari**</span><span class="sxs-lookup"><span data-stu-id="d01c0-329">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d01c0-330">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d01c0-330">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-331">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d01c0-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d01c0-332">Se **true**, il sensore è lineare sull'intervallo dinamico.</span><span class="sxs-lookup"><span data-stu-id="d01c0-332">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

<span data-ttu-id="d01c0-333">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d01c0-333">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d01c0-334">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d01c0-334">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d01c0-335">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d01c0-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-336">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d01c0-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d01c0-337">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="d01c0-337">Last error code reported by the logical device.</span></span>

<span data-ttu-id="d01c0-338">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d01c0-338">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d01c0-339">**LowerThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="d01c0-339">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d01c0-340">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d01c0-340">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-341">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d01c0-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-342">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Probe corrente elettrica DMTF \| 001,13 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliampere ")</span><span class="sxs-lookup"><span data-stu-id="d01c0-342">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.13"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="d01c0-343">I valori di soglia del sensore specificano gli intervalli (valori minimo e massimo) per determinare se il sensore funziona in condizioni normali, non critiche, critiche o irreversibili.</span><span class="sxs-lookup"><span data-stu-id="d01c0-343">Sensor threshold values specify the ranges (minimum and maximum values) to determine whether or not the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="d01c0-344">Se **CurrentReading** è compreso tra **LowerThresholdCritical** e **LowerThresholdFatal**, lo stato corrente è critico.</span><span class="sxs-lookup"><span data-stu-id="d01c0-344">If **CurrentReading** is between **LowerThresholdCritical** and **LowerThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="d01c0-345">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d01c0-345">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d01c0-346">**LowerThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="d01c0-346">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d01c0-347">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d01c0-347">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-348">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d01c0-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-349">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Probe corrente elettrica DMTF \| 001,15 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliampere ")</span><span class="sxs-lookup"><span data-stu-id="d01c0-349">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="d01c0-350">I valori di soglia del sensore specificano gli intervalli (valori minimo e massimo) per determinare se il sensore funziona in condizioni normali, non critiche, critiche o irreversibili.</span><span class="sxs-lookup"><span data-stu-id="d01c0-350">Sensor's threshold values specify the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="d01c0-351">Se **CurrentReading** è inferiore a **LowerThresholdFatal**, lo stato corrente è irreversibile.</span><span class="sxs-lookup"><span data-stu-id="d01c0-351">If **CurrentReading** is below **LowerThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="d01c0-352">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d01c0-352">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d01c0-353">**LowerThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="d01c0-353">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d01c0-354">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d01c0-354">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-355">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d01c0-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-356">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Probe corrente elettrica DMTF \| 001,11 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliampere ")</span><span class="sxs-lookup"><span data-stu-id="d01c0-356">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="d01c0-357">I valori di soglia del sensore specificano gli intervalli (valori minimo e massimo) per determinare se il sensore funziona in condizioni normali, non critiche, critiche o irreversibili.</span><span class="sxs-lookup"><span data-stu-id="d01c0-357">Sensor's threshold values specify the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="d01c0-358">Se **CurrentReading** è compreso tra **LowerThresholdNonCritical** e **UpperThresholdNonCritical**, il sensore segnala un valore normale.</span><span class="sxs-lookup"><span data-stu-id="d01c0-358">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="d01c0-359">Se **CurrentReading** è compreso tra **LowerThresholdNonCritical** e **LowerThresholdCritical**, lo stato corrente è non critico.</span><span class="sxs-lookup"><span data-stu-id="d01c0-359">If **CurrentReading** is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="d01c0-360">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d01c0-360">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d01c0-361">**MaxReadable**</span><span class="sxs-lookup"><span data-stu-id="d01c0-361">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d01c0-362">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d01c0-362">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-363">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d01c0-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-364">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Probe corrente elettrica DMTF \| 001,9 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliampere ")</span><span class="sxs-lookup"><span data-stu-id="d01c0-364">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.9"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="d01c0-365">Valore più grande della proprietà misurata che può essere letta dal sensore numerico.</span><span class="sxs-lookup"><span data-stu-id="d01c0-365">Largest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="d01c0-366">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d01c0-366">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d01c0-367">**MinReadable**</span><span class="sxs-lookup"><span data-stu-id="d01c0-367">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d01c0-368">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d01c0-368">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-369">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d01c0-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-370">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Probe corrente elettrica DMTF \| 001,10 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliampere ")</span><span class="sxs-lookup"><span data-stu-id="d01c0-370">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="d01c0-371">Valore più piccolo della proprietà misurata che può essere letta dal sensore numerico.</span><span class="sxs-lookup"><span data-stu-id="d01c0-371">Smallest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="d01c0-372">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d01c0-372">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d01c0-373">**Nome**</span><span class="sxs-lookup"><span data-stu-id="d01c0-373">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d01c0-374">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d01c0-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-375">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d01c0-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-376">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="d01c0-376">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="d01c0-377">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="d01c0-377">Label by which the object is known.</span></span> <span data-ttu-id="d01c0-378">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="d01c0-378">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="d01c0-379">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d01c0-379">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d01c0-380">**NominalReading**</span><span class="sxs-lookup"><span data-stu-id="d01c0-380">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d01c0-381">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d01c0-381">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-382">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d01c0-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-383">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Probe corrente elettrica DMTF \| 001,6 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliampere ")</span><span class="sxs-lookup"><span data-stu-id="d01c0-383">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="d01c0-384">Valore normale o previsto per il sensore numerico.</span><span class="sxs-lookup"><span data-stu-id="d01c0-384">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="d01c0-385">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d01c0-385">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d01c0-386">**NormalMax**</span><span class="sxs-lookup"><span data-stu-id="d01c0-386">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d01c0-387">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d01c0-387">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-388">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d01c0-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-389">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Probe corrente elettrica DMTF \| 001,7 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliampere ")</span><span class="sxs-lookup"><span data-stu-id="d01c0-389">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="d01c0-390">Valore normale o previsto per il sensore numerico.</span><span class="sxs-lookup"><span data-stu-id="d01c0-390">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="d01c0-391">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d01c0-391">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d01c0-392">**NormalMin**</span><span class="sxs-lookup"><span data-stu-id="d01c0-392">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d01c0-393">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d01c0-393">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-394">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d01c0-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-395">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Probe corrente elettrica DMTF \| 001,8 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliampere ")</span><span class="sxs-lookup"><span data-stu-id="d01c0-395">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="d01c0-396">Linee guida per l'utente sull'intervallo minimo normale per il sensore numerico.</span><span class="sxs-lookup"><span data-stu-id="d01c0-396">Guidance for the user as to the normal minimum range for the numeric sensor.</span></span>

<span data-ttu-id="d01c0-397">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d01c0-397">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d01c0-398">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="d01c0-398">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d01c0-399">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d01c0-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-400">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d01c0-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-401">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d01c0-401">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d01c0-402">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="d01c0-402">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="d01c0-403">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d01c0-403">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="d01c0-404">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="d01c0-404">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="d01c0-405">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d01c0-405">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d01c0-406">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d01c0-406">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-407">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d01c0-407">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d01c0-408">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="d01c0-408">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="d01c0-409">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="d01c0-409">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d01c0-410"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="d01c0-410"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="d01c0-411"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="d01c0-411"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d01c0-412"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="d01c0-412"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d01c0-413"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="d01c0-413"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-414">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="d01c0-414">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="d01c0-415"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="d01c0-415"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-416">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="d01c0-416">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="d01c0-417"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="d01c0-417"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-418">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="d01c0-418">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="d01c0-419">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="d01c0-419">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="d01c0-420">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="d01c0-420">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="d01c0-421"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="d01c0-421"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-422">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="d01c0-422">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="d01c0-423"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="d01c0-423"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="d01c0-424">Tempo Power-On supportato</span><span class="sxs-lookup"><span data-stu-id="d01c0-424">Timed Power-On Supported</span></span>

<span data-ttu-id="d01c0-425">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="d01c0-425">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d01c0-426">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="d01c0-426">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d01c0-427">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d01c0-427">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-428">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d01c0-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d01c0-429">Se **true**, il dispositivo può essere gestito dal risparmio di energia (può essere impostato in modalità di sospensione e così via).</span><span class="sxs-lookup"><span data-stu-id="d01c0-429">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="d01c0-430">La proprietà non indica che le funzionalità di risparmio energia sono attualmente abilitate, solo che il dispositivo logico è in grado di gestire il risparmio di energia.</span><span class="sxs-lookup"><span data-stu-id="d01c0-430">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="d01c0-431">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d01c0-431">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d01c0-432">**Risoluzione**</span><span class="sxs-lookup"><span data-stu-id="d01c0-432">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d01c0-433">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d01c0-433">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-434">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d01c0-434">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-435">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Probe corrente elettrico \| 001,17 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" decimi di milliampere ")</span><span class="sxs-lookup"><span data-stu-id="d01c0-435">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.17"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="d01c0-436">Capacità del sensore di risolvere le differenze nella proprietà misurata.</span><span class="sxs-lookup"><span data-stu-id="d01c0-436">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="d01c0-437">Questo valore può variare a seconda che il dispositivo sia lineare sull'intervallo dinamico.</span><span class="sxs-lookup"><span data-stu-id="d01c0-437">This value may vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="d01c0-438">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d01c0-438">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d01c0-439">**Status**</span><span class="sxs-lookup"><span data-stu-id="d01c0-439">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d01c0-440">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d01c0-440">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-441">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d01c0-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-442">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="d01c0-442">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d01c0-443">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d01c0-443">Current status of the object.</span></span> <span data-ttu-id="d01c0-444">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="d01c0-444">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="d01c0-445">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="d01c0-445">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="d01c0-446">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="d01c0-446">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d01c0-447">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="d01c0-447">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d01c0-448">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="d01c0-448">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d01c0-449">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d01c0-449">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d01c0-450">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="d01c0-450">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d01c0-451">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="d01c0-451">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d01c0-452">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="d01c0-452">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d01c0-453">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="d01c0-453">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d01c0-454">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="d01c0-454">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d01c0-455">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="d01c0-455">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d01c0-456">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="d01c0-456">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d01c0-457">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="d01c0-457">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d01c0-458">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="d01c0-458">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d01c0-459">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="d01c0-459">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d01c0-460">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="d01c0-460">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d01c0-461">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="d01c0-461">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d01c0-462">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="d01c0-462">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d01c0-463">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="d01c0-463">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d01c0-464">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d01c0-464">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-465">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d01c0-465">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-466">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="d01c0-466">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="d01c0-467">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="d01c0-467">State of the logical device.</span></span> <span data-ttu-id="d01c0-468">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="d01c0-468">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="d01c0-469">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d01c0-469">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d01c0-470">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="d01c0-470">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d01c0-471">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="d01c0-471">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d01c0-472">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="d01c0-472">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d01c0-473">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="d01c0-473">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d01c0-474">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="d01c0-474">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d01c0-475">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d01c0-475">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d01c0-476">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d01c0-476">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-477">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d01c0-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-478">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d01c0-478">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d01c0-479">Valore per la proprietà **CreationClassName** del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="d01c0-479">Value for the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="d01c0-480">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d01c0-480">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d01c0-481">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="d01c0-481">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d01c0-482">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d01c0-482">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-483">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d01c0-483">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-484">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d01c0-484">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d01c0-485">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="d01c0-485">Name of the scoping system.</span></span>

<span data-ttu-id="d01c0-486">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d01c0-486">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d01c0-487">**Tolleranza**</span><span class="sxs-lookup"><span data-stu-id="d01c0-487">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d01c0-488">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d01c0-488">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-489">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d01c0-489">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-490">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Probe corrente elettrica DMTF \| 001,18 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliampere ")</span><span class="sxs-lookup"><span data-stu-id="d01c0-490">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.18"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="d01c0-491">Tolleranza del sensore per la proprietà misurata.</span><span class="sxs-lookup"><span data-stu-id="d01c0-491">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="d01c0-492">La tolleranza, insieme a risoluzione e accuratezza, viene utilizzata per calcolare il valore effettivo della proprietà fisica misurata.</span><span class="sxs-lookup"><span data-stu-id="d01c0-492">Tolerance, along with resolution and accuracy, is used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="d01c0-493">La tolleranza può variare a seconda che il dispositivo sia lineare sull'intervallo dinamico.</span><span class="sxs-lookup"><span data-stu-id="d01c0-493">Tolerance may vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="d01c0-494">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d01c0-494">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d01c0-495">**UpperThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="d01c0-495">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d01c0-496">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d01c0-496">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-497">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d01c0-497">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-498">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Probe corrente elettrica DMTF \| 001,14 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliampere ")</span><span class="sxs-lookup"><span data-stu-id="d01c0-498">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.14"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="d01c0-499">I valori di soglia del sensore specificano gli intervalli (valori minimo e massimo) per determinare se il sensore funziona in condizioni normali, non critiche, critiche o irreversibili.</span><span class="sxs-lookup"><span data-stu-id="d01c0-499">Sensor's threshold values specify the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="d01c0-500">Se **CurrentReading** è compreso tra **UpperThresholdCritical** e **UpperThresholdFatal**, lo stato corrente è critico.</span><span class="sxs-lookup"><span data-stu-id="d01c0-500">If **CurrentReading** is between **UpperThresholdCritical** and **UpperThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="d01c0-501">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d01c0-501">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d01c0-502">**UpperThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="d01c0-502">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d01c0-503">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d01c0-503">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-504">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d01c0-504">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-505">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Probe corrente elettrica DMTF \| 001,16 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliampere ")</span><span class="sxs-lookup"><span data-stu-id="d01c0-505">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.16"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="d01c0-506">I valori di soglia del sensore specificano gli intervalli (valori minimo e massimo) per determinare se il sensore funziona in condizioni normali, non critiche, critiche o irreversibili.</span><span class="sxs-lookup"><span data-stu-id="d01c0-506">Sensor's threshold values specify the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="d01c0-507">Se **CurrentReading** è maggiore di **UpperThresholdFatal**, lo stato corrente è irreversibile.</span><span class="sxs-lookup"><span data-stu-id="d01c0-507">If **CurrentReading** is above **UpperThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="d01c0-508">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d01c0-508">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d01c0-509">**UpperThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="d01c0-509">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d01c0-510">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d01c0-510">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-511">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d01c0-511">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d01c0-512">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Probe corrente elettrica DMTF \| 001,12 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliampere ")</span><span class="sxs-lookup"><span data-stu-id="d01c0-512">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="d01c0-513">I valori di soglia del sensore specificano gli intervalli (valori minimo e massimo) per determinare se il sensore funziona in condizioni normali, non critiche, critiche o irreversibili.</span><span class="sxs-lookup"><span data-stu-id="d01c0-513">Sensor's threshold values specify the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="d01c0-514">Se **CurrentReading** è compreso tra **LowerThresholdNonCritical** e **UpperThresholdNonCritical**, il sensore segnala un valore normale.</span><span class="sxs-lookup"><span data-stu-id="d01c0-514">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="d01c0-515">Se **CurrentReading** è compreso tra **UpperThresholdNonCritical** e **UpperThresholdCritical**, lo stato corrente è non critico.</span><span class="sxs-lookup"><span data-stu-id="d01c0-515">If **CurrentReading** is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="d01c0-516">Questa proprietà viene ereditata da [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d01c0-516">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d01c0-517">Commenti</span><span class="sxs-lookup"><span data-stu-id="d01c0-517">Remarks</span></span>

<span data-ttu-id="d01c0-518">La classe **Win32 \_ CurrentProbe** è derivata da [**CIM \_ CurrentSensor**](cim-currentsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d01c0-518">The **Win32\_CurrentProbe** class is derived from [**CIM\_CurrentSensor**](cim-currentsensor.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d01c0-519">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d01c0-519">Requirements</span></span>



| <span data-ttu-id="d01c0-520">Requisito</span><span class="sxs-lookup"><span data-stu-id="d01c0-520">Requirement</span></span> | <span data-ttu-id="d01c0-521">Valore</span><span class="sxs-lookup"><span data-stu-id="d01c0-521">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d01c0-522">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d01c0-522">Minimum supported client</span></span><br/> | <span data-ttu-id="d01c0-523">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d01c0-523">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d01c0-524">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d01c0-524">Minimum supported server</span></span><br/> | <span data-ttu-id="d01c0-525">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d01c0-525">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d01c0-526">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d01c0-526">Namespace</span></span><br/>                | <span data-ttu-id="d01c0-527">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="d01c0-527">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d01c0-528">MOF</span><span class="sxs-lookup"><span data-stu-id="d01c0-528">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d01c0-529"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d01c0-529"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d01c0-530">DLL</span><span class="sxs-lookup"><span data-stu-id="d01c0-530">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d01c0-531"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d01c0-531"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d01c0-532">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d01c0-532">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d01c0-533">**\_CURRENTSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="d01c0-533">**CIM\_CurrentSensor**</span></span>](cim-currentsensor.md)
</dt> <dt>

[<span data-ttu-id="d01c0-534">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="d01c0-534">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 


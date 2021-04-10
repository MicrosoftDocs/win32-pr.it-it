---
description: La \_ classe CIM alimentatore rappresenta le funzionalità e la gestione del dispositivo logico dell'alimentatore.
ms.assetid: a9b79564-01d9-42a4-8586-782f179c179f
ms.tgt_platform: multiple
title: Classe CIM_PowerSupply
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PowerSupply
- CIM_PowerSupply.ActiveInputVoltage
- CIM_PowerSupply.Availability
- CIM_PowerSupply.Caption
- CIM_PowerSupply.ConfigManagerErrorCode
- CIM_PowerSupply.ConfigManagerUserConfig
- CIM_PowerSupply.CreationClassName
- CIM_PowerSupply.Description
- CIM_PowerSupply.DeviceID
- CIM_PowerSupply.ErrorCleared
- CIM_PowerSupply.ErrorDescription
- CIM_PowerSupply.InstallDate
- CIM_PowerSupply.IsSwitchingSupply
- CIM_PowerSupply.LastErrorCode
- CIM_PowerSupply.Name
- CIM_PowerSupply.PNPDeviceID
- CIM_PowerSupply.PowerManagementCapabilities
- CIM_PowerSupply.PowerManagementSupported
- CIM_PowerSupply.Range1InputFrequencyHigh
- CIM_PowerSupply.Range1InputFrequencyLow
- CIM_PowerSupply.Range1InputVoltageHigh
- CIM_PowerSupply.Range1InputVoltageLow
- CIM_PowerSupply.Range2InputFrequencyHigh
- CIM_PowerSupply.Range2InputFrequencyLow
- CIM_PowerSupply.Range2InputVoltageHigh
- CIM_PowerSupply.Range2InputVoltageLow
- CIM_PowerSupply.Status
- CIM_PowerSupply.StatusInfo
- CIM_PowerSupply.SystemCreationClassName
- CIM_PowerSupply.SystemName
- CIM_PowerSupply.TotalOutputPower
- CIM_PowerSupply.TypeOfRangeSwitching
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 35a1eb73c258b800bb8b33ad7aa75ea86cd0ef4c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225619"
---
# <a name="cim_powersupply-class"></a><span data-ttu-id="a83b1-103">CIM \_ alimentatore (classe)</span><span class="sxs-lookup"><span data-stu-id="a83b1-103">CIM\_PowerSupply class</span></span>

<span data-ttu-id="a83b1-104">La classe **CIM \_ alimentatore** rappresenta le funzionalità e la gestione del dispositivo logico dell'alimentatore.</span><span class="sxs-lookup"><span data-stu-id="a83b1-104">The **CIM\_PowerSupply** class represents the capabilities and management of the power supply logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a83b1-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="a83b1-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a83b1-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a83b1-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a83b1-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a83b1-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="a83b1-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="a83b1-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a83b1-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a83b1-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C547-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_PowerSupply : CIM_LogicalDevice
{
  uint16   ActiveInputVoltage;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  boolean  IsSwitchingSupply;
  uint32   LastErrorCode;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   Range1InputFrequencyHigh;
  uint32   Range1InputFrequencyLow;
  uint32   Range1InputVoltageHigh;
  uint32   Range1InputVoltageLow;
  uint32   Range2InputFrequencyHigh;
  uint32   Range2InputFrequencyLow;
  uint32   Range2InputVoltageHigh;
  uint32   Range2InputVoltageLow;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   TotalOutputPower;
  uint16   TypeOfRangeSwitching;
};
```

## <a name="members"></a><span data-ttu-id="a83b1-110">Members</span><span class="sxs-lookup"><span data-stu-id="a83b1-110">Members</span></span>

<span data-ttu-id="a83b1-111">La classe **CIM \_ alimentatore** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a83b1-111">The **CIM\_PowerSupply** class has these types of members:</span></span>

-   [<span data-ttu-id="a83b1-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="a83b1-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="a83b1-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a83b1-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a83b1-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="a83b1-114">Methods</span></span>

<span data-ttu-id="a83b1-115">La classe **CIM \_ alimentatore** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a83b1-115">The **CIM\_PowerSupply** class has these methods.</span></span>



| <span data-ttu-id="a83b1-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="a83b1-116">Method</span></span>                                                                 | <span data-ttu-id="a83b1-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a83b1-117">Description</span></span>                                                                                                                              |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a83b1-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="a83b1-118">**Reset**</span></span>](reset-method-in-class-cim-powersupply.md)                 | <span data-ttu-id="a83b1-119">Richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="a83b1-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="a83b1-120">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="a83b1-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="a83b1-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="a83b1-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-powersupply.md) | <span data-ttu-id="a83b1-122">Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="a83b1-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="a83b1-123">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="a83b1-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a83b1-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a83b1-124">Properties</span></span>

<span data-ttu-id="a83b1-125">La classe **CIM \_ alimentatore** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a83b1-125">The **CIM\_PowerSupply** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a83b1-126">**ActiveInputVoltage**</span><span class="sxs-lookup"><span data-stu-id="a83b1-126">**ActiveInputVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a83b1-127">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a83b1-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a83b1-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-129">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Alimentatore DMTF \| \| 002,15 ")</span><span class="sxs-lookup"><span data-stu-id="a83b1-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.15")</span></span>
</dt> </dl>

<span data-ttu-id="a83b1-130">Intervallo di tensione attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="a83b1-130">Voltage range that is currently in use.</span></span> <span data-ttu-id="a83b1-131">Se la fornitura non è attualmente in fase di disegno, è possibile specificare il valore 6 ("nessuno").</span><span class="sxs-lookup"><span data-stu-id="a83b1-131">If the supply is not currently drawing power, the value 6 ("Neither") can be specified.</span></span> <span data-ttu-id="a83b1-132">Queste informazioni sono necessarie nel caso di un gruppo di continuità (UPS, Power Supply), una sottoclasse di **CIM \_ alimentatore**.</span><span class="sxs-lookup"><span data-stu-id="a83b1-132">This information is necessary in the case of an uninterruptible power supply (UPS), a subclass of **CIM\_PowerSupply**.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a83b1-133">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="a83b1-133">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a83b1-134">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="a83b1-134">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>

<span data-ttu-id="a83b1-135">**Intervallo 1** (3)</span><span class="sxs-lookup"><span data-stu-id="a83b1-135">**Range 1** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>

<span data-ttu-id="a83b1-136">**Intervallo 2** (4)</span><span class="sxs-lookup"><span data-stu-id="a83b1-136">**Range 2** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="a83b1-137">**Entrambi** (5)</span><span class="sxs-lookup"><span data-stu-id="a83b1-137">**Both** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Neither"></span><span id="neither"></span><span id="NEITHER"></span>

<span data-ttu-id="a83b1-138">**Nessuno** (6)</span><span class="sxs-lookup"><span data-stu-id="a83b1-138">**Neither** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a83b1-139">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="a83b1-139">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a83b1-140">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a83b1-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a83b1-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-142">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="a83b1-142">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="a83b1-143">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a83b1-143">Availability and status of the device.</span></span>

<span data-ttu-id="a83b1-144">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a83b1-144">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a83b1-145"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="a83b1-145"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a83b1-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="a83b1-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="a83b1-147"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="a83b1-147"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-148">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="a83b1-148">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="a83b1-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="a83b1-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="a83b1-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="a83b1-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a83b1-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="a83b1-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="a83b1-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="a83b1-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="a83b1-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="a83b1-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="a83b1-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="a83b1-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a83b1-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="a83b1-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="a83b1-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="a83b1-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="a83b1-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="a83b1-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="a83b1-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="a83b1-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-159">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="a83b1-159">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="a83b1-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="a83b1-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-161">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="a83b1-161">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="a83b1-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="a83b1-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-163">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="a83b1-163">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="a83b1-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="a83b1-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="a83b1-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="a83b1-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-166">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="a83b1-166">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="a83b1-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="a83b1-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-168">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="a83b1-168">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="a83b1-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="a83b1-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-170">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="a83b1-170">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="a83b1-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="a83b1-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-172">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="a83b1-172">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="a83b1-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="a83b1-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-174">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="a83b1-174">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a83b1-175">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="a83b1-175">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a83b1-176">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a83b1-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-177">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a83b1-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-178">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a83b1-178">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a83b1-179">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a83b1-179">Short textual description of the object.</span></span>

<span data-ttu-id="a83b1-180">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a83b1-180">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a83b1-181">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="a83b1-181">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a83b1-182">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a83b1-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a83b1-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-184">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a83b1-184">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a83b1-185">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="a83b1-185">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="a83b1-186">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a83b1-186">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="a83b1-187"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="a83b1-187"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="a83b1-188"> (0)</span><span class="sxs-lookup"><span data-stu-id="a83b1-188">(0)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-189">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="a83b1-189">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="a83b1-190"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="a83b1-190"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="a83b1-191">(1)</span><span class="sxs-lookup"><span data-stu-id="a83b1-191">(1)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-192">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="a83b1-192">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a83b1-193"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a83b1-193"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="a83b1-194">(2)</span><span class="sxs-lookup"><span data-stu-id="a83b1-194">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="a83b1-195"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="a83b1-195"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="a83b1-196">(3)</span><span class="sxs-lookup"><span data-stu-id="a83b1-196">(3)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-197">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="a83b1-197">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="a83b1-198"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="a83b1-198"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="a83b1-199">(4)</span><span class="sxs-lookup"><span data-stu-id="a83b1-199">(4)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-200">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="a83b1-200">Device is not working properly.</span></span> <span data-ttu-id="a83b1-201">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="a83b1-201">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="a83b1-202"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="a83b1-202"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="a83b1-203">(5)</span><span class="sxs-lookup"><span data-stu-id="a83b1-203">(5)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-204">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="a83b1-204">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="a83b1-205"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="a83b1-205"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="a83b1-206"> (6)</span><span class="sxs-lookup"><span data-stu-id="a83b1-206">(6)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-207">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="a83b1-207">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="a83b1-208"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="a83b1-208"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="a83b1-209">(7)</span><span class="sxs-lookup"><span data-stu-id="a83b1-209">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="a83b1-210"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="a83b1-210"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="a83b1-211">(8)</span><span class="sxs-lookup"><span data-stu-id="a83b1-211">(8)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-212">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="a83b1-212">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="a83b1-213"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="a83b1-213"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="a83b1-214">(9)</span><span class="sxs-lookup"><span data-stu-id="a83b1-214">(9)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-215">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="a83b1-215">Device is not working properly.</span></span> <span data-ttu-id="a83b1-216">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a83b1-216">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="a83b1-217"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a83b1-217"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="a83b1-218">(10)</span><span class="sxs-lookup"><span data-stu-id="a83b1-218">(10)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-219">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a83b1-219">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="a83b1-220"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a83b1-220"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="a83b1-221">(11)</span><span class="sxs-lookup"><span data-stu-id="a83b1-221">(11)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-222">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a83b1-222">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="a83b1-223"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="a83b1-223"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="a83b1-224">12</span><span class="sxs-lookup"><span data-stu-id="a83b1-224">(12)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-225">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="a83b1-225">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="a83b1-226"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a83b1-226"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="a83b1-227">(13)</span><span class="sxs-lookup"><span data-stu-id="a83b1-227">(13)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-228">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a83b1-228">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="a83b1-229"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="a83b1-229"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="a83b1-230">(14)</span><span class="sxs-lookup"><span data-stu-id="a83b1-230">(14)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-231">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="a83b1-231">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="a83b1-232"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="a83b1-232"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="a83b1-233">(15)</span><span class="sxs-lookup"><span data-stu-id="a83b1-233">(15)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-234">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="a83b1-234">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="a83b1-235"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a83b1-235"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="a83b1-236">(16)</span><span class="sxs-lookup"><span data-stu-id="a83b1-236">(16)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-237">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a83b1-237">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="a83b1-238"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="a83b1-238"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="a83b1-239">(17)</span><span class="sxs-lookup"><span data-stu-id="a83b1-239">(17)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-240">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="a83b1-240">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a83b1-241"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a83b1-241"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="a83b1-242">(18)</span><span class="sxs-lookup"><span data-stu-id="a83b1-242">(18)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-243">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a83b1-243">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="a83b1-244"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="a83b1-244"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="a83b1-245">(19)</span><span class="sxs-lookup"><span data-stu-id="a83b1-245">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="a83b1-246"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="a83b1-246"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="a83b1-247">(20)</span><span class="sxs-lookup"><span data-stu-id="a83b1-247">(20)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-248">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="a83b1-248">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="a83b1-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a83b1-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="a83b1-250">(21)</span><span class="sxs-lookup"><span data-stu-id="a83b1-250">(21)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-251">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="a83b1-251">System failure.</span></span> <span data-ttu-id="a83b1-252">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="a83b1-252">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="a83b1-253">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a83b1-253">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="a83b1-254"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="a83b1-254"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="a83b1-255">(22)</span><span class="sxs-lookup"><span data-stu-id="a83b1-255">(22)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-256">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="a83b1-256">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="a83b1-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="a83b1-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="a83b1-258">(23)</span><span class="sxs-lookup"><span data-stu-id="a83b1-258">(23)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-259">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="a83b1-259">System failure.</span></span> <span data-ttu-id="a83b1-260">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="a83b1-260">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="a83b1-261"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="a83b1-261"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="a83b1-262">(24)</span><span class="sxs-lookup"><span data-stu-id="a83b1-262">(24)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-263">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="a83b1-263">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="a83b1-264"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a83b1-264"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="a83b1-265">(25)</span><span class="sxs-lookup"><span data-stu-id="a83b1-265">(25)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-266">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a83b1-266">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="a83b1-267"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a83b1-267"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="a83b1-268">(26)</span><span class="sxs-lookup"><span data-stu-id="a83b1-268">(26)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-269">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a83b1-269">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="a83b1-270"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="a83b1-270"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="a83b1-271">(27)</span><span class="sxs-lookup"><span data-stu-id="a83b1-271">(27)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-272">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="a83b1-272">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="a83b1-273"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="a83b1-273"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="a83b1-274">(28)</span><span class="sxs-lookup"><span data-stu-id="a83b1-274">(28)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-275">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="a83b1-275">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="a83b1-276"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="a83b1-276"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="a83b1-277">(29)</span><span class="sxs-lookup"><span data-stu-id="a83b1-277">(29)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-278">Il dispositivo è disabilitato; il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="a83b1-278">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="a83b1-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a83b1-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="a83b1-280">(30)</span><span class="sxs-lookup"><span data-stu-id="a83b1-280">(30)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-281">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a83b1-281">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a83b1-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a83b1-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="a83b1-283">31</span><span class="sxs-lookup"><span data-stu-id="a83b1-283">(31)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-284">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="a83b1-284">Device is not working properly.</span></span> <span data-ttu-id="a83b1-285">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="a83b1-285">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a83b1-286">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="a83b1-286">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a83b1-287">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a83b1-287">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-288">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a83b1-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-289">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a83b1-289">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a83b1-290">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="a83b1-290">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="a83b1-291">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a83b1-291">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a83b1-292">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a83b1-292">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a83b1-293">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a83b1-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-294">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a83b1-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-295">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a83b1-295">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a83b1-296">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="a83b1-296">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="a83b1-297">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="a83b1-297">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="a83b1-298">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a83b1-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a83b1-299">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="a83b1-299">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a83b1-300">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a83b1-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-301">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a83b1-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-302">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="a83b1-302">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a83b1-303">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a83b1-303">Textual description of the object.</span></span>

<span data-ttu-id="a83b1-304">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a83b1-304">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a83b1-305">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="a83b1-305">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a83b1-306">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a83b1-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-307">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a83b1-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-308">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a83b1-308">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a83b1-309">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="a83b1-309">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="a83b1-310">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a83b1-310">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a83b1-311">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="a83b1-311">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a83b1-312">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a83b1-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-313">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a83b1-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a83b1-314">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="a83b1-314">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="a83b1-315">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a83b1-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a83b1-316">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="a83b1-316">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a83b1-317">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a83b1-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-318">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a83b1-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a83b1-319">Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.</span><span class="sxs-lookup"><span data-stu-id="a83b1-319">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="a83b1-320">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a83b1-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a83b1-321">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a83b1-321">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a83b1-322">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a83b1-322">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-323">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a83b1-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-324">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="a83b1-324">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a83b1-325">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a83b1-325">Date and time the object was installed.</span></span> <span data-ttu-id="a83b1-326">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="a83b1-326">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="a83b1-327">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a83b1-327">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a83b1-328">**IsSwitchingSupply**</span><span class="sxs-lookup"><span data-stu-id="a83b1-328">**IsSwitchingSupply**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a83b1-329">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a83b1-329">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-330">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a83b1-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a83b1-331">Se **true**, l'alimentatore è un rifornimento di cambio (rispetto lineare).</span><span class="sxs-lookup"><span data-stu-id="a83b1-331">If **TRUE**, the power supply is a switching (versus linear) supply.</span></span>

</dd> <dt>

<span data-ttu-id="a83b1-332">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="a83b1-332">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a83b1-333">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a83b1-333">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-334">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a83b1-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a83b1-335">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="a83b1-335">Last error code reported by the logical device.</span></span>

<span data-ttu-id="a83b1-336">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a83b1-336">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a83b1-337">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a83b1-337">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a83b1-338">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a83b1-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-339">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a83b1-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-340">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="a83b1-340">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="a83b1-341">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="a83b1-341">Label by which the object is known.</span></span> <span data-ttu-id="a83b1-342">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="a83b1-342">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="a83b1-343">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a83b1-343">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a83b1-344">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="a83b1-344">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a83b1-345">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a83b1-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-346">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a83b1-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-347">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a83b1-347">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a83b1-348">Win32 Plug and Play identificatore dispositivo del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="a83b1-348">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="a83b1-349">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a83b1-349">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="a83b1-350">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="a83b1-350">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="a83b1-351">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="a83b1-351">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a83b1-352">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a83b1-352">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-353">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a83b1-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a83b1-354">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="a83b1-354">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="a83b1-355">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="a83b1-355">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a83b1-356"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="a83b1-356"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="a83b1-357"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="a83b1-357"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a83b1-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="a83b1-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a83b1-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="a83b1-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-360">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="a83b1-360">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="a83b1-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="a83b1-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-362">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="a83b1-362">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="a83b1-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="a83b1-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-364">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="a83b1-364">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="a83b1-365">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="a83b1-365">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="a83b1-366">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="a83b1-366">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="a83b1-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="a83b1-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-368">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="a83b1-368">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="a83b1-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="a83b1-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="a83b1-370">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="a83b1-370">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a83b1-371">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="a83b1-371">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a83b1-372">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a83b1-372">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-373">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a83b1-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a83b1-374">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="a83b1-374">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="a83b1-375">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="a83b1-375">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="a83b1-376">Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="a83b1-376">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="a83b1-377">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="a83b1-377">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="a83b1-378">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a83b1-378">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a83b1-379">**Range1InputFrequencyHigh**</span><span class="sxs-lookup"><span data-stu-id="a83b1-379">**Range1InputFrequencyHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a83b1-380">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a83b1-380">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-381">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a83b1-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-382">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz")</span><span class="sxs-lookup"><span data-stu-id="a83b1-382">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="a83b1-383">Frequenza, espressa in Hertz, alla fine dell'intervallo di frequenza di input 1 dell'alimentatore.</span><span class="sxs-lookup"><span data-stu-id="a83b1-383">Frequency (in hertz) at the high-end of the power supply's input frequency range 1.</span></span> <span data-ttu-id="a83b1-384">Il valore 0 implica il controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="a83b1-384">A value of 0 implies DC.</span></span>

</dd> <dt>

<span data-ttu-id="a83b1-385">**Range1InputFrequencyLow**</span><span class="sxs-lookup"><span data-stu-id="a83b1-385">**Range1InputFrequencyLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a83b1-386">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a83b1-386">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-387">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a83b1-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-388">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Alimentatore DMTF \| \| 002,17 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="a83b1-388">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.17"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="a83b1-389">Frequenza (in Hertz) al lato inferiore dell'intervallo di frequenza di input dell'alimentatore 1.</span><span class="sxs-lookup"><span data-stu-id="a83b1-389">Frequency (in hertz) at the low-end of the power supply's input frequency range 1.</span></span> <span data-ttu-id="a83b1-390">Il valore 0 implica il controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="a83b1-390">A value of 0 implies DC.</span></span>

</dd> <dt>

<span data-ttu-id="a83b1-391">**Range1InputVoltageHigh**</span><span class="sxs-lookup"><span data-stu-id="a83b1-391">**Range1InputVoltageHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a83b1-392">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a83b1-392">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-393">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a83b1-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-394">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Alimentatore DMTF \| \| 002,8 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" millivolt ")</span><span class="sxs-lookup"><span data-stu-id="a83b1-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="a83b1-395">Tensione elevata dell'intervallo di tensione di input 1 per l'alimentatore, in millivolt.</span><span class="sxs-lookup"><span data-stu-id="a83b1-395">High voltage of input voltage range 1 for the power supply, in millivolts.</span></span> <span data-ttu-id="a83b1-396">Il valore 0 indica "Unknown".</span><span class="sxs-lookup"><span data-stu-id="a83b1-396">A value of 0 denotes "Unknown".</span></span>

</dd> <dt>

<span data-ttu-id="a83b1-397">**Range1InputVoltageLow**</span><span class="sxs-lookup"><span data-stu-id="a83b1-397">**Range1InputVoltageLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a83b1-398">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a83b1-398">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-399">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a83b1-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-400">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Alimentatore DMTF \| \| 002,7 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" millivolt ")</span><span class="sxs-lookup"><span data-stu-id="a83b1-400">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="a83b1-401">Bassa tensione dell'intervallo di tensione di input 1 per l'alimentatore, in millivolt.</span><span class="sxs-lookup"><span data-stu-id="a83b1-401">Low voltage of input voltage range 1 for the power supply, in millivolts.</span></span> <span data-ttu-id="a83b1-402">Il valore 0 indica "Unknown".</span><span class="sxs-lookup"><span data-stu-id="a83b1-402">A value of 0 denotes "Unknown".</span></span>

</dd> <dt>

<span data-ttu-id="a83b1-403">**Range2InputFrequencyHigh**</span><span class="sxs-lookup"><span data-stu-id="a83b1-403">**Range2InputFrequencyHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a83b1-404">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a83b1-404">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-405">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a83b1-405">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-406">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Alimentatore DMTF \| \| 002,20 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="a83b1-406">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.20"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="a83b1-407">Frequenza (espressa in Hertz) alla fine dell'intervallo di frequenza di input dell'alimentatore 2.</span><span class="sxs-lookup"><span data-stu-id="a83b1-407">Frequency (in hertz) at the high-end of the power supply's input frequency range 2.</span></span> <span data-ttu-id="a83b1-408">Il valore 0 implica il controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="a83b1-408">A value of 0 implies DC.</span></span>

</dd> <dt>

<span data-ttu-id="a83b1-409">**Range2InputFrequencyLow**</span><span class="sxs-lookup"><span data-stu-id="a83b1-409">**Range2InputFrequencyLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a83b1-410">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a83b1-410">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-411">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a83b1-411">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-412">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Alimentatore DMTF \| \| 002,19 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="a83b1-412">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.19"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="a83b1-413">Frequenza (in Hertz) al lato inferiore dell'intervallo di frequenza di input dell'alimentatore 2.</span><span class="sxs-lookup"><span data-stu-id="a83b1-413">Frequency (in hertz) at the low-end of the power supply's input frequency range 2.</span></span> <span data-ttu-id="a83b1-414">Il valore 0 implica il controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="a83b1-414">A value of 0 implies DC.</span></span>

</dd> <dt>

<span data-ttu-id="a83b1-415">**Range2InputVoltageHigh**</span><span class="sxs-lookup"><span data-stu-id="a83b1-415">**Range2InputVoltageHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a83b1-416">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a83b1-416">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-417">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a83b1-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-418">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Alimentatore DMTF \| \| 002,12 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" millivolt ")</span><span class="sxs-lookup"><span data-stu-id="a83b1-418">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="a83b1-419">Tensione elevata dell'intervallo di tensione di input 2 per l'alimentatore, in millivolt.</span><span class="sxs-lookup"><span data-stu-id="a83b1-419">High voltage of input voltage range 2 for the power supply, in millivolts.</span></span> <span data-ttu-id="a83b1-420">Il valore 0 indica "Unknown".</span><span class="sxs-lookup"><span data-stu-id="a83b1-420">A value of 0 denotes "Unknown".</span></span>

</dd> <dt>

<span data-ttu-id="a83b1-421">**Range2InputVoltageLow**</span><span class="sxs-lookup"><span data-stu-id="a83b1-421">**Range2InputVoltageLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a83b1-422">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a83b1-422">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-423">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a83b1-423">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-424">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Alimentatore DMTF \| \| 002,11 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" millivolt ")</span><span class="sxs-lookup"><span data-stu-id="a83b1-424">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="a83b1-425">Bassa tensione dell'intervallo di tensione di input 2 per questo alimentatore, in millivolt.</span><span class="sxs-lookup"><span data-stu-id="a83b1-425">Low voltage of input voltage range 2 for this power supply, in Millivolts.</span></span> <span data-ttu-id="a83b1-426">Il valore 0 indica "Unknown".</span><span class="sxs-lookup"><span data-stu-id="a83b1-426">A value of 0 denotes "Unknown".</span></span>

</dd> <dt>

<span data-ttu-id="a83b1-427">**Status**</span><span class="sxs-lookup"><span data-stu-id="a83b1-427">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a83b1-428">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a83b1-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-429">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a83b1-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-430">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="a83b1-430">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a83b1-431">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a83b1-431">Current status of the object.</span></span>

<span data-ttu-id="a83b1-432">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a83b1-432">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a83b1-433">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="a83b1-433">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a83b1-434">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="a83b1-434">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a83b1-435">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="a83b1-435">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a83b1-436">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="a83b1-436">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a83b1-437">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="a83b1-437">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a83b1-438">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="a83b1-438">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a83b1-439">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="a83b1-439">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a83b1-440">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="a83b1-440">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a83b1-441">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="a83b1-441">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a83b1-442">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="a83b1-442">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a83b1-443">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="a83b1-443">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a83b1-444">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="a83b1-444">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a83b1-445">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="a83b1-445">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a83b1-446">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="a83b1-446">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a83b1-447">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a83b1-447">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-448">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a83b1-448">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-449">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="a83b1-449">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="a83b1-450">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="a83b1-450">State of the logical device.</span></span> <span data-ttu-id="a83b1-451">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="a83b1-451">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="a83b1-452">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a83b1-452">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a83b1-453">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="a83b1-453">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a83b1-454">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="a83b1-454">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a83b1-455">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="a83b1-455">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a83b1-456">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="a83b1-456">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a83b1-457">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="a83b1-457">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a83b1-458">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a83b1-458">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a83b1-459">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a83b1-459">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-460">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a83b1-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-461">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a83b1-461">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a83b1-462">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="a83b1-462">Scoping system's creation class name.</span></span>

<span data-ttu-id="a83b1-463">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a83b1-463">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a83b1-464">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="a83b1-464">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a83b1-465">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a83b1-465">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-466">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a83b1-466">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-467">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a83b1-467">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a83b1-468">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="a83b1-468">Scoping system's name.</span></span>

<span data-ttu-id="a83b1-469">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a83b1-469">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a83b1-470">**TotalOutputPower**</span><span class="sxs-lookup"><span data-stu-id="a83b1-470">**TotalOutputPower**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a83b1-471">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a83b1-471">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-472">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a83b1-472">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-473">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Alimentatore DMTF \| \| 002,21 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliwatt ")</span><span class="sxs-lookup"><span data-stu-id="a83b1-473">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.21"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatts")</span></span>
</dt> </dl>

<span data-ttu-id="a83b1-474">Potenza di output totale dell'alimentatore, in milliwatt.</span><span class="sxs-lookup"><span data-stu-id="a83b1-474">Total output power of the power supply, in milliwatts.</span></span> <span data-ttu-id="a83b1-475">Il valore 0 indica "Unknown".</span><span class="sxs-lookup"><span data-stu-id="a83b1-475">A value of 0 denotes "Unknown".</span></span>

</dd> <dt>

<span data-ttu-id="a83b1-476">**TypeOfRangeSwitching**</span><span class="sxs-lookup"><span data-stu-id="a83b1-476">**TypeOfRangeSwitching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a83b1-477">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a83b1-477">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-478">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a83b1-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a83b1-479">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Alimentatore DMTF \| \| 002,16 ")</span><span class="sxs-lookup"><span data-stu-id="a83b1-479">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.16")</span></span>
</dt> </dl>

<span data-ttu-id="a83b1-480">Tipo di cambio di intervallo di tensione di input implementato nell'alimentatore.</span><span class="sxs-lookup"><span data-stu-id="a83b1-480">Type of input voltage range switching implemented in the power supply.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a83b1-481">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="a83b1-481">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a83b1-482">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="a83b1-482">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="a83b1-483">**Manuale** (3)</span><span class="sxs-lookup"><span data-stu-id="a83b1-483">**Manual** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Autoswitch"></span><span id="autoswitch"></span><span id="AUTOSWITCH"></span>

<span data-ttu-id="a83b1-484">**Autoswitch** (4)</span><span class="sxs-lookup"><span data-stu-id="a83b1-484">**Autoswitch** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Wide_Range"></span><span id="wide_range"></span><span id="WIDE_RANGE"></span>

<span data-ttu-id="a83b1-485">**Ampio intervallo** (5)</span><span class="sxs-lookup"><span data-stu-id="a83b1-485">**Wide Range** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a83b1-486">**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="a83b1-486">**Not Applicable** (6)</span></span>


<span data-ttu-id="a83b1-487"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a83b1-487"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="a83b1-488">Commenti</span><span class="sxs-lookup"><span data-stu-id="a83b1-488">Remarks</span></span>

<span data-ttu-id="a83b1-489">La classe **CIM \_ alimentatore** è derivata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a83b1-489">The **CIM\_PowerSupply** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="a83b1-490">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="a83b1-490">WMI does not implement this class.</span></span> <span data-ttu-id="a83b1-491">Per WMI con classi derivate da **CIM \_ alimentatore**, vedere [le classi Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a83b1-491">For WMI classed derived from **CIM\_PowerSupply**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="a83b1-492">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="a83b1-492">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a83b1-493">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="a83b1-493">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a83b1-494">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a83b1-494">Requirements</span></span>



| <span data-ttu-id="a83b1-495">Requisito</span><span class="sxs-lookup"><span data-stu-id="a83b1-495">Requirement</span></span> | <span data-ttu-id="a83b1-496">Valore</span><span class="sxs-lookup"><span data-stu-id="a83b1-496">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a83b1-497">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a83b1-497">Minimum supported client</span></span><br/> | <span data-ttu-id="a83b1-498">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a83b1-498">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a83b1-499">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a83b1-499">Minimum supported server</span></span><br/> | <span data-ttu-id="a83b1-500">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a83b1-500">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a83b1-501">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a83b1-501">Namespace</span></span><br/>                | <span data-ttu-id="a83b1-502">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="a83b1-502">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a83b1-503">MOF</span><span class="sxs-lookup"><span data-stu-id="a83b1-503">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a83b1-504"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a83b1-504"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a83b1-505">DLL</span><span class="sxs-lookup"><span data-stu-id="a83b1-505">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a83b1-506"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a83b1-506"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a83b1-507">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a83b1-507">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a83b1-508">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="a83b1-508">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 


---
description: La \_ classe WMI HeatPipe Win32 rappresenta le proprietà di un dispositivo di raffreddamento della pipe di calore.
ms.assetid: c6e24cb2-e29a-4cd5-af62-b8e48a5936f9
ms.tgt_platform: multiple
title: Classe Win32_HeatPipe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_HeatPipe
- Win32_HeatPipe.Reset
- Win32_HeatPipe.SetPowerState
- Win32_HeatPipe.ActiveCooling
- Win32_HeatPipe.Availability
- Win32_HeatPipe.Caption
- Win32_HeatPipe.ConfigManagerErrorCode
- Win32_HeatPipe.ConfigManagerUserConfig
- Win32_HeatPipe.CreationClassName
- Win32_HeatPipe.Description
- Win32_HeatPipe.DeviceID
- Win32_HeatPipe.ErrorCleared
- Win32_HeatPipe.ErrorDescription
- Win32_HeatPipe.InstallDate
- Win32_HeatPipe.LastErrorCode
- Win32_HeatPipe.Name
- Win32_HeatPipe.PNPDeviceID
- Win32_HeatPipe.PowerManagementCapabilities
- Win32_HeatPipe.PowerManagementSupported
- Win32_HeatPipe.Status
- Win32_HeatPipe.StatusInfo
- Win32_HeatPipe.SystemCreationClassName
- Win32_HeatPipe.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f89b8f059a5c80f4d40c70007d8870211e79f93f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049244"
---
# <a name="win32_heatpipe-class"></a><span data-ttu-id="d1c25-103">Win32 \_ HeatPipe (classe)</span><span class="sxs-lookup"><span data-stu-id="d1c25-103">Win32\_HeatPipe class</span></span>

<span data-ttu-id="d1c25-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ HeatPipe Win32** rappresenta le proprietà di un dispositivo di raffreddamento della pipe di calore.</span><span class="sxs-lookup"><span data-stu-id="d1c25-104">The **Win32\_HeatPipe** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a heat pipe cooling device.</span></span>

<span data-ttu-id="d1c25-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="d1c25-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1c25-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d1c25-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{464FFAB7-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class Win32_HeatPipe : CIM_HeatPipe
{
  boolean  ActiveCooling;
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
  uint32   LastErrorCode;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="d1c25-107">Members</span><span class="sxs-lookup"><span data-stu-id="d1c25-107">Members</span></span>

<span data-ttu-id="d1c25-108">La classe **Win32 \_ HeatPipe** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d1c25-108">The **Win32\_HeatPipe** class has these types of members:</span></span>

-   [<span data-ttu-id="d1c25-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="d1c25-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="d1c25-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d1c25-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d1c25-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="d1c25-111">Methods</span></span>

<span data-ttu-id="d1c25-112">La classe **Win32 \_ HeatPipe** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="d1c25-112">The **Win32\_HeatPipe** class has these methods.</span></span>



| <span data-ttu-id="d1c25-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="d1c25-113">Method</span></span>            | <span data-ttu-id="d1c25-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1c25-114">Description</span></span>                                                                                                                                                                                            |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1c25-115">**Reimpostazione**</span><span class="sxs-lookup"><span data-stu-id="d1c25-115">**Reset**</span></span>         | <span data-ttu-id="d1c25-116">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="d1c25-116">Not implemented.</span></span> <span data-ttu-id="d1c25-117">Per implementare questo metodo, vedere il metodo [**Reset**](reset-method-in-class-cim-controller.md) in [**CIM \_ HeatPipe**](cim-heatpipe.md) per la documentazione.</span><span class="sxs-lookup"><span data-stu-id="d1c25-117">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_HeatPipe**](cim-heatpipe.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="d1c25-118">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="d1c25-118">**SetPowerState**</span></span> | <span data-ttu-id="d1c25-119">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="d1c25-119">Not implemented.</span></span> <span data-ttu-id="d1c25-120">Per implementare questo metodo, vedere il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) in [**CIM \_ HeatPipe**](cim-heatpipe.md) per la documentazione.</span><span class="sxs-lookup"><span data-stu-id="d1c25-120">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_HeatPipe**](cim-heatpipe.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d1c25-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d1c25-121">Properties</span></span>

<span data-ttu-id="d1c25-122">La classe **Win32 \_ HeatPipe** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d1c25-122">The **Win32\_HeatPipe** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d1c25-123">**ActiveCooling**</span><span class="sxs-lookup"><span data-stu-id="d1c25-123">**ActiveCooling**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1c25-124">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d1c25-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1c25-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d1c25-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1c25-126">Se **true**, il dispositivo di raffreddamento fornisce il raffreddamento attivo non passivo.</span><span class="sxs-lookup"><span data-stu-id="d1c25-126">If **TRUE**, the cooling device provides active cooling not passive.</span></span>

<span data-ttu-id="d1c25-127">Questa proprietà viene ereditata da [**CIM \_ CoolingDevice**](cim-coolingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="d1c25-127">This property is inherited from [**CIM\_CoolingDevice**](cim-coolingdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1c25-128">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="d1c25-128">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1c25-129">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d1c25-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d1c25-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d1c25-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1c25-131">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="d1c25-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="d1c25-132">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d1c25-132">Availability and status of the device.</span></span>

<span data-ttu-id="d1c25-133">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d1c25-133">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d1c25-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="d1c25-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d1c25-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="d1c25-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="d1c25-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="d1c25-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-137">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="d1c25-137">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="d1c25-138"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="d1c25-138"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="d1c25-139"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="d1c25-139"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d1c25-140"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="d1c25-140"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="d1c25-141"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="d1c25-141"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="d1c25-142"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="d1c25-142"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="d1c25-143"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="d1c25-143"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d1c25-144"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="d1c25-144"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="d1c25-145"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="d1c25-145"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="d1c25-146"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="d1c25-146"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="d1c25-147"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="d1c25-147"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-148">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="d1c25-148">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="d1c25-149"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="d1c25-149"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-150">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="d1c25-150">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="d1c25-151"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="d1c25-151"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-152">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="d1c25-152">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="d1c25-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="d1c25-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="d1c25-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="d1c25-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-155">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="d1c25-155">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="d1c25-156"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="d1c25-156"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-157">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="d1c25-157">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="d1c25-158"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="d1c25-158"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-159">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="d1c25-159">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="d1c25-160"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="d1c25-160"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-161">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="d1c25-161">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="d1c25-162"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="d1c25-162"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-163">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="d1c25-163">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d1c25-164">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="d1c25-164">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1c25-165">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d1c25-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1c25-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d1c25-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1c25-167">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="d1c25-167">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d1c25-168">Breve descrizione dell'oggetto stringa a una riga.</span><span class="sxs-lookup"><span data-stu-id="d1c25-168">Short description of the object a one-line string.</span></span>

<span data-ttu-id="d1c25-169">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1c25-169">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1c25-170">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d1c25-170">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1c25-171">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1c25-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1c25-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d1c25-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1c25-173">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d1c25-173">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d1c25-174">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d1c25-174">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="d1c25-175">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d1c25-175">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="d1c25-176"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="d1c25-176"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="d1c25-177"> (0)</span><span class="sxs-lookup"><span data-stu-id="d1c25-177">(0)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-178">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="d1c25-178">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="d1c25-179"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="d1c25-179"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="d1c25-180">(1)</span><span class="sxs-lookup"><span data-stu-id="d1c25-180">(1)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-181">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="d1c25-181">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d1c25-182"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d1c25-182"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="d1c25-183">(2)</span><span class="sxs-lookup"><span data-stu-id="d1c25-183">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="d1c25-184"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="d1c25-184"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="d1c25-185">(3)</span><span class="sxs-lookup"><span data-stu-id="d1c25-185">(3)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-186">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="d1c25-186">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="d1c25-187"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="d1c25-187"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="d1c25-188">(4)</span><span class="sxs-lookup"><span data-stu-id="d1c25-188">(4)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-189">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="d1c25-189">Device is not working properly.</span></span> <span data-ttu-id="d1c25-190">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="d1c25-190">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="d1c25-191"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="d1c25-191"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="d1c25-192">(5)</span><span class="sxs-lookup"><span data-stu-id="d1c25-192">(5)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-193">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="d1c25-193">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="d1c25-194"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="d1c25-194"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="d1c25-195"> (6)</span><span class="sxs-lookup"><span data-stu-id="d1c25-195">(6)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-196">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="d1c25-196">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="d1c25-197"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="d1c25-197"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="d1c25-198">(7)</span><span class="sxs-lookup"><span data-stu-id="d1c25-198">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="d1c25-199"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="d1c25-199"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="d1c25-200">(8)</span><span class="sxs-lookup"><span data-stu-id="d1c25-200">(8)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-201">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="d1c25-201">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="d1c25-202"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="d1c25-202"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="d1c25-203">(9)</span><span class="sxs-lookup"><span data-stu-id="d1c25-203">(9)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-204">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="d1c25-204">Device is not working properly.</span></span> <span data-ttu-id="d1c25-205">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d1c25-205">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="d1c25-206"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d1c25-206"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="d1c25-207">(10)</span><span class="sxs-lookup"><span data-stu-id="d1c25-207">(10)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-208">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d1c25-208">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="d1c25-209"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d1c25-209"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="d1c25-210">(11)</span><span class="sxs-lookup"><span data-stu-id="d1c25-210">(11)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-211">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d1c25-211">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="d1c25-212"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="d1c25-212"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="d1c25-213">12</span><span class="sxs-lookup"><span data-stu-id="d1c25-213">(12)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-214">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="d1c25-214">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="d1c25-215"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d1c25-215"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="d1c25-216">(13)</span><span class="sxs-lookup"><span data-stu-id="d1c25-216">(13)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-217">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d1c25-217">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="d1c25-218"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="d1c25-218"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="d1c25-219">(14)</span><span class="sxs-lookup"><span data-stu-id="d1c25-219">(14)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-220">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="d1c25-220">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="d1c25-221"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="d1c25-221"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="d1c25-222">(15)</span><span class="sxs-lookup"><span data-stu-id="d1c25-222">(15)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-223">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="d1c25-223">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="d1c25-224"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d1c25-224"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="d1c25-225">(16)</span><span class="sxs-lookup"><span data-stu-id="d1c25-225">(16)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-226">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d1c25-226">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="d1c25-227"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="d1c25-227"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="d1c25-228">(17)</span><span class="sxs-lookup"><span data-stu-id="d1c25-228">(17)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-229">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="d1c25-229">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d1c25-230"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d1c25-230"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="d1c25-231">(18)</span><span class="sxs-lookup"><span data-stu-id="d1c25-231">(18)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-232">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d1c25-232">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="d1c25-233"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="d1c25-233"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="d1c25-234">(19)</span><span class="sxs-lookup"><span data-stu-id="d1c25-234">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="d1c25-235"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="d1c25-235"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="d1c25-236">(20)</span><span class="sxs-lookup"><span data-stu-id="d1c25-236">(20)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-237">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="d1c25-237">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="d1c25-238"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d1c25-238"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="d1c25-239">(21)</span><span class="sxs-lookup"><span data-stu-id="d1c25-239">(21)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-240">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="d1c25-240">System failure.</span></span> <span data-ttu-id="d1c25-241">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="d1c25-241">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="d1c25-242">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d1c25-242">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="d1c25-243"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="d1c25-243"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="d1c25-244">(22)</span><span class="sxs-lookup"><span data-stu-id="d1c25-244">(22)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-245">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="d1c25-245">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="d1c25-246"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="d1c25-246"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="d1c25-247">(23)</span><span class="sxs-lookup"><span data-stu-id="d1c25-247">(23)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-248">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="d1c25-248">System failure.</span></span> <span data-ttu-id="d1c25-249">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="d1c25-249">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="d1c25-250"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="d1c25-250"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="d1c25-251">(24)</span><span class="sxs-lookup"><span data-stu-id="d1c25-251">(24)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-252">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="d1c25-252">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="d1c25-253"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d1c25-253"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="d1c25-254">(25)</span><span class="sxs-lookup"><span data-stu-id="d1c25-254">(25)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-255">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d1c25-255">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="d1c25-256"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d1c25-256"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="d1c25-257">(26)</span><span class="sxs-lookup"><span data-stu-id="d1c25-257">(26)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-258">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d1c25-258">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="d1c25-259"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="d1c25-259"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="d1c25-260">(27)</span><span class="sxs-lookup"><span data-stu-id="d1c25-260">(27)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-261">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="d1c25-261">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="d1c25-262"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="d1c25-262"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="d1c25-263">(28)</span><span class="sxs-lookup"><span data-stu-id="d1c25-263">(28)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-264">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="d1c25-264">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="d1c25-265"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="d1c25-265"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="d1c25-266">(29)</span><span class="sxs-lookup"><span data-stu-id="d1c25-266">(29)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-267">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="d1c25-267">Device is disabled.</span></span> <span data-ttu-id="d1c25-268">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="d1c25-268">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="d1c25-269"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d1c25-269"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="d1c25-270">(30)</span><span class="sxs-lookup"><span data-stu-id="d1c25-270">(30)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-271">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d1c25-271">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d1c25-272"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d1c25-272"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="d1c25-273">31</span><span class="sxs-lookup"><span data-stu-id="d1c25-273">(31)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-274">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="d1c25-274">Device is not working properly.</span></span> <span data-ttu-id="d1c25-275">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="d1c25-275">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d1c25-276">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="d1c25-276">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1c25-277">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d1c25-277">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1c25-278">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d1c25-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1c25-279">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d1c25-279">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d1c25-280">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="d1c25-280">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="d1c25-281">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d1c25-281">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1c25-282">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d1c25-282">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1c25-283">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d1c25-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1c25-284">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d1c25-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1c25-285">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d1c25-285">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d1c25-286">Nome della prima classe concreta visualizzata nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="d1c25-286">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="d1c25-287">Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="d1c25-287">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="d1c25-288">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d1c25-288">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1c25-289">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="d1c25-289">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1c25-290">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d1c25-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1c25-291">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d1c25-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1c25-292">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="d1c25-292">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d1c25-293">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d1c25-293">Description of the object.</span></span>

<span data-ttu-id="d1c25-294">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1c25-294">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1c25-295">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="d1c25-295">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1c25-296">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d1c25-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1c25-297">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d1c25-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1c25-298">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="d1c25-298">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="d1c25-299">Identificatore univoco della pipe di calore.</span><span class="sxs-lookup"><span data-stu-id="d1c25-299">Unique identifier of the heat pipe.</span></span>

<span data-ttu-id="d1c25-300">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d1c25-300">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1c25-301">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="d1c25-301">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1c25-302">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d1c25-302">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1c25-303">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d1c25-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1c25-304">Se **true**, l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="d1c25-304">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="d1c25-305">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d1c25-305">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1c25-306">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="d1c25-306">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1c25-307">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d1c25-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1c25-308">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d1c25-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1c25-309">Altre informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="d1c25-309">More information about the error that is recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="d1c25-310">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d1c25-310">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1c25-311">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d1c25-311">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1c25-312">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d1c25-312">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d1c25-313">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d1c25-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1c25-314">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="d1c25-314">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d1c25-315">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d1c25-315">Date and time the object was installed.</span></span> <span data-ttu-id="d1c25-316">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="d1c25-316">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="d1c25-317">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1c25-317">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1c25-318">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d1c25-318">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1c25-319">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1c25-319">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1c25-320">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d1c25-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1c25-321">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="d1c25-321">Last error code reported by the logical device.</span></span>

<span data-ttu-id="d1c25-322">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d1c25-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1c25-323">**Nome**</span><span class="sxs-lookup"><span data-stu-id="d1c25-323">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1c25-324">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d1c25-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1c25-325">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d1c25-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1c25-326">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="d1c25-326">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="d1c25-327">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="d1c25-327">Label by which the object is known.</span></span> <span data-ttu-id="d1c25-328">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="d1c25-328">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="d1c25-329">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1c25-329">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1c25-330">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="d1c25-330">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1c25-331">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d1c25-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1c25-332">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d1c25-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1c25-333">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d1c25-333">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d1c25-334">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="d1c25-334">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="d1c25-335">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d1c25-335">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="d1c25-336">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="d1c25-336">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="d1c25-337">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d1c25-337">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1c25-338">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d1c25-338">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d1c25-339">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d1c25-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1c25-340">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="d1c25-340">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="d1c25-341">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="d1c25-341">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d1c25-342"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="d1c25-342"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="d1c25-343"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="d1c25-343"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-344">Le capacità relative al risparmio di energia non sono supportate per questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d1c25-344">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d1c25-345"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="d1c25-345"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d1c25-346"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="d1c25-346"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-347">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="d1c25-347">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="d1c25-348"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="d1c25-348"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-349">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="d1c25-349">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="d1c25-350"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="d1c25-350"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-351">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="d1c25-351">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="d1c25-352">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="d1c25-352">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="d1c25-353">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="d1c25-353">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="d1c25-354"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="d1c25-354"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-355">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="d1c25-355">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="d1c25-356"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="d1c25-356"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="d1c25-357">Tempo Power-On supportato</span><span class="sxs-lookup"><span data-stu-id="d1c25-357">Timed Power-On Supported</span></span>

<span data-ttu-id="d1c25-358">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="d1c25-358">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d1c25-359">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="d1c25-359">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1c25-360">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d1c25-360">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1c25-361">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d1c25-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1c25-362">Se **true**, il dispositivo può essere inserito in modalità di sospensione e così via.</span><span class="sxs-lookup"><span data-stu-id="d1c25-362">If **TRUE**, the device can be power-managed put into suspend mode, and so on.</span></span> <span data-ttu-id="d1c25-363">La proprietà non indica che le funzionalità di risparmio energia sono attualmente abilitate, solo che il dispositivo logico è in grado di gestire il risparmio di energia.</span><span class="sxs-lookup"><span data-stu-id="d1c25-363">The property does not indicate that power management features are enabled currently, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="d1c25-364">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d1c25-364">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1c25-365">**Status**</span><span class="sxs-lookup"><span data-stu-id="d1c25-365">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1c25-366">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d1c25-366">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1c25-367">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d1c25-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1c25-368">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="d1c25-368">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d1c25-369">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d1c25-369">Current status of the object.</span></span> <span data-ttu-id="d1c25-370">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="d1c25-370">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="d1c25-371">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="d1c25-371">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="d1c25-372">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="d1c25-372">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d1c25-373">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="d1c25-373">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d1c25-374">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="d1c25-374">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d1c25-375">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1c25-375">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d1c25-376">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="d1c25-376">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d1c25-377">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="d1c25-377">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d1c25-378">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="d1c25-378">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d1c25-379">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="d1c25-379">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d1c25-380">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="d1c25-380">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d1c25-381">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="d1c25-381">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d1c25-382">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="d1c25-382">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d1c25-383">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="d1c25-383">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d1c25-384">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="d1c25-384">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d1c25-385">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="d1c25-385">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d1c25-386">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="d1c25-386">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d1c25-387">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="d1c25-387">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d1c25-388">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="d1c25-388">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d1c25-389">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="d1c25-389">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1c25-390">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d1c25-390">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d1c25-391">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d1c25-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1c25-392">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="d1c25-392">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="d1c25-393">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="d1c25-393">State of the logical device.</span></span> <span data-ttu-id="d1c25-394">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="d1c25-394">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="d1c25-395">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d1c25-395">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d1c25-396">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="d1c25-396">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d1c25-397">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="d1c25-397">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d1c25-398">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="d1c25-398">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d1c25-399">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="d1c25-399">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d1c25-400">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="d1c25-400">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d1c25-401">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d1c25-401">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1c25-402">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d1c25-402">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1c25-403">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d1c25-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1c25-404">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d1c25-404">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d1c25-405">Valore per la proprietà **CreationClassName** del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="d1c25-405">Value for the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="d1c25-406">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d1c25-406">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1c25-407">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="d1c25-407">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1c25-408">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d1c25-408">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1c25-409">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d1c25-409">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1c25-410">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d1c25-410">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d1c25-411">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="d1c25-411">Name of the scoping system.</span></span>

<span data-ttu-id="d1c25-412">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d1c25-412">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1c25-413">Commenti</span><span class="sxs-lookup"><span data-stu-id="d1c25-413">Remarks</span></span>

<span data-ttu-id="d1c25-414">La classe **Win32 \_ HeatPipe** è derivata da [**CIM \_ HeatPipe**](cim-heatpipe.md).</span><span class="sxs-lookup"><span data-stu-id="d1c25-414">The **Win32\_HeatPipe** class is derived from [**CIM\_HeatPipe**](cim-heatpipe.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d1c25-415">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d1c25-415">Requirements</span></span>



| <span data-ttu-id="d1c25-416">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1c25-416">Requirement</span></span> | <span data-ttu-id="d1c25-417">Valore</span><span class="sxs-lookup"><span data-stu-id="d1c25-417">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1c25-418">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1c25-418">Minimum supported client</span></span><br/> | <span data-ttu-id="d1c25-419">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d1c25-419">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d1c25-420">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1c25-420">Minimum supported server</span></span><br/> | <span data-ttu-id="d1c25-421">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1c25-421">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d1c25-422">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d1c25-422">Namespace</span></span><br/>                | <span data-ttu-id="d1c25-423">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="d1c25-423">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d1c25-424">MOF</span><span class="sxs-lookup"><span data-stu-id="d1c25-424">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1c25-425"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d1c25-425"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1c25-426">DLL</span><span class="sxs-lookup"><span data-stu-id="d1c25-426">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1c25-427"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1c25-427"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1c25-428">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d1c25-428">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1c25-429">**\_HEATPIPE CIM**</span><span class="sxs-lookup"><span data-stu-id="d1c25-429">**CIM\_HeatPipe**</span></span>](cim-heatpipe.md)
</dt> <dt>

[<span data-ttu-id="d1c25-430">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="d1c25-430">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 


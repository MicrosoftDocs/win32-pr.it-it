---
description: La \_ classe WMI della ventola Win32 rappresenta le proprietà di un dispositivo ventola nel computer. Ad esempio, la ventola di raffreddamento della CPU.
ms.assetid: ff48b788-d759-45cf-812f-a80dba0c9192
ms.tgt_platform: multiple
title: Classe Win32_Fan
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Fan
- Win32_Fan.Reset
- Win32_Fan.SetPowerState
- Win32_Fan.SetSpeed
- Win32_Fan.ActiveCooling
- Win32_Fan.Availability
- Win32_Fan.Caption
- Win32_Fan.ConfigManagerErrorCode
- Win32_Fan.ConfigManagerUserConfig
- Win32_Fan.CreationClassName
- Win32_Fan.Description
- Win32_Fan.DesiredSpeed
- Win32_Fan.DeviceID
- Win32_Fan.ErrorCleared
- Win32_Fan.ErrorDescription
- Win32_Fan.InstallDate
- Win32_Fan.LastErrorCode
- Win32_Fan.Name
- Win32_Fan.PNPDeviceID
- Win32_Fan.PowerManagementCapabilities
- Win32_Fan.PowerManagementSupported
- Win32_Fan.Status
- Win32_Fan.StatusInfo
- Win32_Fan.SystemCreationClassName
- Win32_Fan.SystemName
- Win32_Fan.VariableSpeed
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 67f248b74fa665f30c9c3b9ffa51cb8cee5a5782
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523090"
---
# <a name="win32_fan-class"></a><span data-ttu-id="b06e7-104">\_Classe fan Win32</span><span class="sxs-lookup"><span data-stu-id="b06e7-104">Win32\_Fan class</span></span>

<span data-ttu-id="b06e7-105">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) della **\_ ventola Win32** rappresenta le proprietà di un dispositivo ventola nel computer.</span><span class="sxs-lookup"><span data-stu-id="b06e7-105">The **Win32\_Fan** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a fan device in the computer system.</span></span> <span data-ttu-id="b06e7-106">Ad esempio, la ventola di raffreddamento della CPU.</span><span class="sxs-lookup"><span data-stu-id="b06e7-106">For example, the CPU cooling fan.</span></span>

<span data-ttu-id="b06e7-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b06e7-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b06e7-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="b06e7-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b06e7-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b06e7-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{464FFAB5-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class Win32_Fan : CIM_Fan
{
  boolean  ActiveCooling;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  uint64   DesiredSpeed;
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
  boolean  VariableSpeed;
};
```

## <a name="members"></a><span data-ttu-id="b06e7-110">Members</span><span class="sxs-lookup"><span data-stu-id="b06e7-110">Members</span></span>

<span data-ttu-id="b06e7-111">I tipi di membri della classe **\_ fan Win32** sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b06e7-111">The **Win32\_Fan** class has these types of members:</span></span>

-   [<span data-ttu-id="b06e7-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="b06e7-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="b06e7-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b06e7-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b06e7-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="b06e7-114">Methods</span></span>

<span data-ttu-id="b06e7-115">Per la classe **\_ fan Win32** sono disponibili questi metodi.</span><span class="sxs-lookup"><span data-stu-id="b06e7-115">The **Win32\_Fan** class has these methods.</span></span>



| <span data-ttu-id="b06e7-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="b06e7-116">Method</span></span>            | <span data-ttu-id="b06e7-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b06e7-117">Description</span></span>                                                                                                                                                                                  |
|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b06e7-118">**Reimpostazione**</span><span class="sxs-lookup"><span data-stu-id="b06e7-118">**Reset**</span></span>         | <span data-ttu-id="b06e7-119">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="b06e7-119">Not implemented.</span></span> <span data-ttu-id="b06e7-120">Per implementare questo metodo, vedere il metodo [**Reset**](reset-method-in-class-cim-controller.md) nella [**\_ ventola CIM**](cim-fan.md) per la documentazione.</span><span class="sxs-lookup"><span data-stu-id="b06e7-120">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_Fan**](cim-fan.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="b06e7-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="b06e7-121">**SetPowerState**</span></span> | <span data-ttu-id="b06e7-122">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="b06e7-122">Not implemented.</span></span> <span data-ttu-id="b06e7-123">Per implementare questo metodo, vedere il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) nella [**\_ ventola CIM**](cim-fan.md) per la documentazione.</span><span class="sxs-lookup"><span data-stu-id="b06e7-123">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_Fan**](cim-fan.md) for documentation.</span></span><br/> |
| <span data-ttu-id="b06e7-124">**Velocità**</span><span class="sxs-lookup"><span data-stu-id="b06e7-124">**SetSpeed**</span></span>      | <span data-ttu-id="b06e7-125">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="b06e7-125">Not implemented.</span></span><br/>                                                                                                                                                                  |



 

### <a name="properties"></a><span data-ttu-id="b06e7-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b06e7-126">Properties</span></span>

<span data-ttu-id="b06e7-127">Per la classe **\_ fan Win32** sono presenti queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b06e7-127">The **Win32\_Fan** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b06e7-128">**ActiveCooling**</span><span class="sxs-lookup"><span data-stu-id="b06e7-128">**ActiveCooling**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06e7-129">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b06e7-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b06e7-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b06e7-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b06e7-131">Se **true**, il dispositivo di raffreddamento fornisce il raffreddamento attivo (anziché passivo).</span><span class="sxs-lookup"><span data-stu-id="b06e7-131">If **True**, the cooling device provides active (as opposed to passive) cooling.</span></span>

<span data-ttu-id="b06e7-132">Questa proprietà viene ereditata da [**CIM \_ CoolingDevice**](cim-coolingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b06e7-132">This property is inherited from [**CIM\_CoolingDevice**](cim-coolingdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b06e7-133">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="b06e7-133">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06e7-134">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b06e7-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b06e7-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b06e7-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b06e7-136">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="b06e7-136">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="b06e7-137">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b06e7-137">Availability and status of the device.</span></span>

<span data-ttu-id="b06e7-138">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b06e7-138">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b06e7-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="b06e7-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b06e7-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="b06e7-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="b06e7-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="b06e7-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-142">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="b06e7-142">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="b06e7-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="b06e7-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="b06e7-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="b06e7-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b06e7-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="b06e7-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="b06e7-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="b06e7-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="b06e7-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="b06e7-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="b06e7-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="b06e7-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b06e7-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="b06e7-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="b06e7-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="b06e7-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="b06e7-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="b06e7-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="b06e7-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="b06e7-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-153">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="b06e7-153">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="b06e7-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="b06e7-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-155">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="b06e7-155">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="b06e7-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="b06e7-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-157">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="b06e7-157">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="b06e7-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="b06e7-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="b06e7-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="b06e7-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-160">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="b06e7-160">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="b06e7-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="b06e7-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-162">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="b06e7-162">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="b06e7-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="b06e7-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-164">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="b06e7-164">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="b06e7-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="b06e7-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-166">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="b06e7-166">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="b06e7-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="b06e7-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-168">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="b06e7-168">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b06e7-169">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="b06e7-169">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06e7-170">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b06e7-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b06e7-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b06e7-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b06e7-172">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b06e7-172">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b06e7-173">Breve descrizione dell'oggetto stringa a una riga.</span><span class="sxs-lookup"><span data-stu-id="b06e7-173">Short description of the object a one-line string.</span></span>

<span data-ttu-id="b06e7-174">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b06e7-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b06e7-175">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b06e7-175">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06e7-176">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b06e7-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b06e7-177">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b06e7-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b06e7-178">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b06e7-178">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b06e7-179">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="b06e7-179">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="b06e7-180">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b06e7-180">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="b06e7-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="b06e7-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="b06e7-182"> (0)</span><span class="sxs-lookup"><span data-stu-id="b06e7-182">(0)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-183">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="b06e7-183">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="b06e7-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="b06e7-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="b06e7-185">(1)</span><span class="sxs-lookup"><span data-stu-id="b06e7-185">(1)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-186">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="b06e7-186">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b06e7-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b06e7-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="b06e7-188">(2)</span><span class="sxs-lookup"><span data-stu-id="b06e7-188">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="b06e7-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="b06e7-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="b06e7-190">(3)</span><span class="sxs-lookup"><span data-stu-id="b06e7-190">(3)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-191">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="b06e7-191">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b06e7-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="b06e7-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="b06e7-193">(4)</span><span class="sxs-lookup"><span data-stu-id="b06e7-193">(4)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-194">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="b06e7-194">Device is not working properly.</span></span> <span data-ttu-id="b06e7-195">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="b06e7-195">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="b06e7-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="b06e7-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="b06e7-197">(5)</span><span class="sxs-lookup"><span data-stu-id="b06e7-197">(5)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-198">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="b06e7-198">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="b06e7-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="b06e7-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="b06e7-200"> (6)</span><span class="sxs-lookup"><span data-stu-id="b06e7-200">(6)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-201">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="b06e7-201">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="b06e7-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="b06e7-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="b06e7-203">(7)</span><span class="sxs-lookup"><span data-stu-id="b06e7-203">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="b06e7-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="b06e7-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="b06e7-205">(8)</span><span class="sxs-lookup"><span data-stu-id="b06e7-205">(8)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-206">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="b06e7-206">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="b06e7-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="b06e7-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="b06e7-208">(9)</span><span class="sxs-lookup"><span data-stu-id="b06e7-208">(9)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-209">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="b06e7-209">Device is not working properly.</span></span> <span data-ttu-id="b06e7-210">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b06e7-210">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="b06e7-211"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b06e7-211"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="b06e7-212">(10)</span><span class="sxs-lookup"><span data-stu-id="b06e7-212">(10)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-213">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b06e7-213">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="b06e7-214"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b06e7-214"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="b06e7-215">(11)</span><span class="sxs-lookup"><span data-stu-id="b06e7-215">(11)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-216">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b06e7-216">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="b06e7-217"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="b06e7-217"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="b06e7-218">12</span><span class="sxs-lookup"><span data-stu-id="b06e7-218">(12)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-219">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="b06e7-219">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="b06e7-220"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b06e7-220"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="b06e7-221">(13)</span><span class="sxs-lookup"><span data-stu-id="b06e7-221">(13)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-222">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b06e7-222">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="b06e7-223"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="b06e7-223"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="b06e7-224">(14)</span><span class="sxs-lookup"><span data-stu-id="b06e7-224">(14)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-225">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="b06e7-225">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="b06e7-226"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="b06e7-226"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="b06e7-227">(15)</span><span class="sxs-lookup"><span data-stu-id="b06e7-227">(15)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-228">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="b06e7-228">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="b06e7-229"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b06e7-229"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="b06e7-230">(16)</span><span class="sxs-lookup"><span data-stu-id="b06e7-230">(16)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-231">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b06e7-231">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="b06e7-232"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="b06e7-232"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="b06e7-233">(17)</span><span class="sxs-lookup"><span data-stu-id="b06e7-233">(17)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-234">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="b06e7-234">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b06e7-235"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b06e7-235"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="b06e7-236">(18)</span><span class="sxs-lookup"><span data-stu-id="b06e7-236">(18)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-237">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b06e7-237">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="b06e7-238"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="b06e7-238"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="b06e7-239">(19)</span><span class="sxs-lookup"><span data-stu-id="b06e7-239">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b06e7-240"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="b06e7-240"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="b06e7-241">(20)</span><span class="sxs-lookup"><span data-stu-id="b06e7-241">(20)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-242">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="b06e7-242">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="b06e7-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b06e7-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="b06e7-244">(21)</span><span class="sxs-lookup"><span data-stu-id="b06e7-244">(21)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-245">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="b06e7-245">System failure.</span></span> <span data-ttu-id="b06e7-246">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="b06e7-246">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="b06e7-247">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b06e7-247">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="b06e7-248"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="b06e7-248"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="b06e7-249">(22)</span><span class="sxs-lookup"><span data-stu-id="b06e7-249">(22)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-250">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="b06e7-250">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="b06e7-251"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="b06e7-251"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="b06e7-252">(23)</span><span class="sxs-lookup"><span data-stu-id="b06e7-252">(23)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-253">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="b06e7-253">System failure.</span></span> <span data-ttu-id="b06e7-254">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="b06e7-254">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="b06e7-255"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="b06e7-255"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="b06e7-256">(24)</span><span class="sxs-lookup"><span data-stu-id="b06e7-256">(24)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-257">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="b06e7-257">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b06e7-258"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b06e7-258"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b06e7-259">(25)</span><span class="sxs-lookup"><span data-stu-id="b06e7-259">(25)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-260">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b06e7-260">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b06e7-261"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b06e7-261"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b06e7-262">(26)</span><span class="sxs-lookup"><span data-stu-id="b06e7-262">(26)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-263">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b06e7-263">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="b06e7-264"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="b06e7-264"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="b06e7-265">(27)</span><span class="sxs-lookup"><span data-stu-id="b06e7-265">(27)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-266">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="b06e7-266">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="b06e7-267"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="b06e7-267"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="b06e7-268">(28)</span><span class="sxs-lookup"><span data-stu-id="b06e7-268">(28)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-269">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="b06e7-269">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="b06e7-270"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="b06e7-270"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="b06e7-271">(29)</span><span class="sxs-lookup"><span data-stu-id="b06e7-271">(29)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-272">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="b06e7-272">Device is disabled.</span></span> <span data-ttu-id="b06e7-273">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="b06e7-273">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="b06e7-274"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b06e7-274"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="b06e7-275">(30)</span><span class="sxs-lookup"><span data-stu-id="b06e7-275">(30)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-276">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b06e7-276">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b06e7-277"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b06e7-277"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="b06e7-278">31</span><span class="sxs-lookup"><span data-stu-id="b06e7-278">(31)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-279">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="b06e7-279">Device is not working properly.</span></span> <span data-ttu-id="b06e7-280">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="b06e7-280">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b06e7-281">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="b06e7-281">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06e7-282">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b06e7-282">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b06e7-283">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b06e7-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b06e7-284">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b06e7-284">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b06e7-285">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="b06e7-285">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="b06e7-286">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b06e7-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b06e7-287">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b06e7-287">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06e7-288">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b06e7-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b06e7-289">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b06e7-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b06e7-290">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b06e7-290">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b06e7-291">Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="b06e7-291">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="b06e7-292">Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="b06e7-292">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="b06e7-293">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b06e7-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b06e7-294">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="b06e7-294">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06e7-295">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b06e7-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b06e7-296">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b06e7-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b06e7-297">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="b06e7-297">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b06e7-298">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b06e7-298">Description of the object.</span></span>

<span data-ttu-id="b06e7-299">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b06e7-299">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b06e7-300">**DesiredSpeed**</span><span class="sxs-lookup"><span data-stu-id="b06e7-300">**DesiredSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06e7-301">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b06e7-301">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b06e7-302">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b06e7-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b06e7-303">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("rivoluzioni al minuto")</span><span class="sxs-lookup"><span data-stu-id="b06e7-303">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="b06e7-304">Velocità della ventola attualmente richiesta, definita in rivoluzioni al minuto, quando è supportata una ventola di velocità variabile (**VariableSpeed** è **true**).</span><span class="sxs-lookup"><span data-stu-id="b06e7-304">Currently requested fan speed, defined in revolutions per minute, when a variable speed fan is supported (**VariableSpeed** is **TRUE**).</span></span> <span data-ttu-id="b06e7-305">La velocità corrente è determinata da un sensore ([**\_ contagiri CIM**](cim-tachometer.md)) associato alla ventola con la relazione [**CIM \_ AssociatedSensor**](cim-associatedsensor.md) .</span><span class="sxs-lookup"><span data-stu-id="b06e7-305">The current speed is determined by a sensor ([**CIM\_Tachometer**](cim-tachometer.md)) that is associated with the fan using the [**CIM\_AssociatedSensor**](cim-associatedsensor.md) relationship.</span></span>

<span data-ttu-id="b06e7-306">Questa proprietà viene ereditata [**dalla \_ ventola CIM**](cim-fan.md).</span><span class="sxs-lookup"><span data-stu-id="b06e7-306">This property is inherited from [**CIM\_Fan**](cim-fan.md).</span></span>

<span data-ttu-id="b06e7-307">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b06e7-307">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b06e7-308">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="b06e7-308">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06e7-309">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b06e7-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b06e7-310">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b06e7-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b06e7-311">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="b06e7-311">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b06e7-312">Identifica il dispositivo della ventola.</span><span class="sxs-lookup"><span data-stu-id="b06e7-312">Identifies the fan device.</span></span> <span data-ttu-id="b06e7-313">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b06e7-313">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b06e7-314">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="b06e7-314">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06e7-315">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b06e7-315">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b06e7-316">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b06e7-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b06e7-317">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="b06e7-317">If **True**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="b06e7-318">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b06e7-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b06e7-319">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="b06e7-319">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06e7-320">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b06e7-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b06e7-321">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b06e7-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b06e7-322">Stringa in formato libero che fornisce ulteriori informazioni sull'errore registrato nella proprietà **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="b06e7-322">Free-form string supplying more information about the error recorded in **LastErrorCode** property, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="b06e7-323">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b06e7-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b06e7-324">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b06e7-324">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06e7-325">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b06e7-325">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b06e7-326">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b06e7-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b06e7-327">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="b06e7-327">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b06e7-328">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b06e7-328">Date and time the object was installed.</span></span> <span data-ttu-id="b06e7-329">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="b06e7-329">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b06e7-330">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b06e7-330">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b06e7-331">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b06e7-331">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06e7-332">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b06e7-332">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b06e7-333">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b06e7-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b06e7-334">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="b06e7-334">Last error code reported by the logical device.</span></span>

<span data-ttu-id="b06e7-335">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b06e7-335">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b06e7-336">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b06e7-336">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06e7-337">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b06e7-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b06e7-338">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b06e7-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b06e7-339">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="b06e7-339">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b06e7-340">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="b06e7-340">Label by which the object is known.</span></span> <span data-ttu-id="b06e7-341">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="b06e7-341">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="b06e7-342">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b06e7-342">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b06e7-343">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="b06e7-343">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06e7-344">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b06e7-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b06e7-345">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b06e7-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b06e7-346">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b06e7-346">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b06e7-347">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="b06e7-347">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="b06e7-348">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b06e7-348">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="b06e7-349">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="b06e7-349">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="b06e7-350">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="b06e7-350">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06e7-351">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b06e7-351">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b06e7-352">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b06e7-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b06e7-353">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="b06e7-353">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="b06e7-354">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="b06e7-354">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b06e7-355"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="b06e7-355"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="b06e7-356"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="b06e7-356"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-357">Le capacità relative al risparmio di energia non sono supportate per questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b06e7-357">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b06e7-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="b06e7-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b06e7-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="b06e7-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-360">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="b06e7-360">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="b06e7-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="b06e7-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-362">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="b06e7-362">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="b06e7-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="b06e7-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-364">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="b06e7-364">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="b06e7-365">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="b06e7-365">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="b06e7-366">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="b06e7-366">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="b06e7-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="b06e7-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-368">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="b06e7-368">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="b06e7-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="b06e7-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b06e7-370">Tempo Power-On supportato</span><span class="sxs-lookup"><span data-stu-id="b06e7-370">Timed Power-On Supported</span></span>

<span data-ttu-id="b06e7-371">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="b06e7-371">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b06e7-372">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="b06e7-372">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06e7-373">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b06e7-373">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b06e7-374">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b06e7-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b06e7-375">Se **true**, il dispositivo può essere gestito dal risparmio di energia (può essere impostato in modalità di sospensione e così via).</span><span class="sxs-lookup"><span data-stu-id="b06e7-375">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="b06e7-376">La proprietà non indica che le funzionalità di risparmio energia sono attualmente abilitate, solo che il dispositivo logico è in grado di gestire il risparmio di energia.</span><span class="sxs-lookup"><span data-stu-id="b06e7-376">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="b06e7-377">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b06e7-377">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b06e7-378">**Status**</span><span class="sxs-lookup"><span data-stu-id="b06e7-378">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06e7-379">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b06e7-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b06e7-380">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b06e7-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b06e7-381">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="b06e7-381">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b06e7-382">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b06e7-382">Current status of the object.</span></span> <span data-ttu-id="b06e7-383">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="b06e7-383">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="b06e7-384">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="b06e7-384">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="b06e7-385">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="b06e7-385">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b06e7-386">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="b06e7-386">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b06e7-387">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="b06e7-387">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b06e7-388">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b06e7-388">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b06e7-389">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="b06e7-389">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b06e7-390">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="b06e7-390">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b06e7-391">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="b06e7-391">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b06e7-392">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="b06e7-392">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b06e7-393">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="b06e7-393">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b06e7-394">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="b06e7-394">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b06e7-395">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="b06e7-395">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b06e7-396">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="b06e7-396">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b06e7-397">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="b06e7-397">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b06e7-398">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="b06e7-398">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b06e7-399">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="b06e7-399">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b06e7-400">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="b06e7-400">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b06e7-401">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="b06e7-401">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b06e7-402">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="b06e7-402">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06e7-403">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b06e7-403">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b06e7-404">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b06e7-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b06e7-405">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="b06e7-405">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="b06e7-406">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="b06e7-406">State of the logical device.</span></span> <span data-ttu-id="b06e7-407">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="b06e7-407">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="b06e7-408">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b06e7-408">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b06e7-409">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="b06e7-409">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b06e7-410">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="b06e7-410">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b06e7-411">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="b06e7-411">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b06e7-412">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="b06e7-412">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b06e7-413">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="b06e7-413">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b06e7-414">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b06e7-414">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06e7-415">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b06e7-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b06e7-416">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b06e7-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b06e7-417">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b06e7-417">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b06e7-418">Valore della proprietà **CreationClassName** del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="b06e7-418">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="b06e7-419">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b06e7-419">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b06e7-420">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b06e7-420">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06e7-421">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b06e7-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b06e7-422">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b06e7-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b06e7-423">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b06e7-423">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b06e7-424">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="b06e7-424">Name of the scoping system.</span></span>

<span data-ttu-id="b06e7-425">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b06e7-425">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b06e7-426">**VariableSpeed**</span><span class="sxs-lookup"><span data-stu-id="b06e7-426">**VariableSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06e7-427">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b06e7-427">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b06e7-428">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b06e7-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b06e7-429">Se **true**, la ventola supporta le velocità variabili.</span><span class="sxs-lookup"><span data-stu-id="b06e7-429">If **True**, the fan supports variable speeds.</span></span>

<span data-ttu-id="b06e7-430">Questa proprietà viene ereditata [**dalla \_ ventola CIM**](cim-fan.md).</span><span class="sxs-lookup"><span data-stu-id="b06e7-430">This property is inherited from [**CIM\_Fan**](cim-fan.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b06e7-431">Commenti</span><span class="sxs-lookup"><span data-stu-id="b06e7-431">Remarks</span></span>

<span data-ttu-id="b06e7-432">La **classe \_ ventola Win32** è derivata dalla [**\_ ventola CIM**](cim-fan.md).</span><span class="sxs-lookup"><span data-stu-id="b06e7-432">The **Win32\_Fan** class is derived from [**CIM\_Fan**](cim-fan.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b06e7-433">Esempio</span><span class="sxs-lookup"><span data-stu-id="b06e7-433">Examples</span></span>

<span data-ttu-id="b06e7-434">L'esempio [list computer fan Information](https://Gallery.TechNet.Microsoft.Com/d1534503-704f-4450-8dab-f3e760bf818c) PowerShell recupera informazioni sulle ventole di raffreddamento installate in un computer.</span><span class="sxs-lookup"><span data-stu-id="b06e7-434">The [List Computer Fan Information](https://Gallery.TechNet.Microsoft.Com/d1534503-704f-4450-8dab-f3e760bf818c) PowerShell sample retrieves information about the cooling fans installed in a computer.</span></span>

<span data-ttu-id="b06e7-435">Nell'esempio seguente vengono recuperate informazioni sulle ventole di raffreddamento installate in un computer.</span><span class="sxs-lookup"><span data-stu-id="b06e7-435">The following sample retrieves information about the cooling fans installed on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_Fan") 
 
For Each objItem in colItems 
    Wscript.Echo "Active Cooling: " & objItem.ActiveCooling 
    Wscript.Echo "Availability: " & objItem.Availability 
    Wscript.Echo "Device ID: " & objItem.DeviceID 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "Status Information: " & objItem.StatusInfo 
    Wscript.Echo 
Next
```


```PowerShell
$colItems = Get-WmiObject Win32_Fan -Namespace "root\cimv2"
foreach ($objItem in $colItems)
{
    "Active Cooling: " + $objItem.ActiveCooling 
    "Availability: " + $objItem.Availability 
    "Device ID: " + $objItem.DeviceID 
    "Name: " + $objItem.Name 
    "Status Information: " + $objItem.StatusInfo 
}
```





## <a name="requirements"></a><span data-ttu-id="b06e7-436">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b06e7-436">Requirements</span></span>



| <span data-ttu-id="b06e7-437">Requisito</span><span class="sxs-lookup"><span data-stu-id="b06e7-437">Requirement</span></span> | <span data-ttu-id="b06e7-438">Valore</span><span class="sxs-lookup"><span data-stu-id="b06e7-438">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b06e7-439">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b06e7-439">Minimum supported client</span></span><br/> | <span data-ttu-id="b06e7-440">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b06e7-440">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b06e7-441">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b06e7-441">Minimum supported server</span></span><br/> | <span data-ttu-id="b06e7-442">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b06e7-442">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b06e7-443">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b06e7-443">Namespace</span></span><br/>                | <span data-ttu-id="b06e7-444">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="b06e7-444">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b06e7-445">MOF</span><span class="sxs-lookup"><span data-stu-id="b06e7-445">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b06e7-446"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b06e7-446"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b06e7-447">DLL</span><span class="sxs-lookup"><span data-stu-id="b06e7-447">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b06e7-448"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b06e7-448"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b06e7-449">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b06e7-449">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b06e7-450">**\_Ventola CIM**</span><span class="sxs-lookup"><span data-stu-id="b06e7-450">**CIM\_Fan**</span></span>](cim-fan.md)
</dt> <dt>

[<span data-ttu-id="b06e7-451">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="b06e7-451">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 


---
description: La \_ classe CIM AlarmDevice è un dispositivo di allarme che emette indicazioni udibili o visibili correlate alla situazione di un problema.
ms.assetid: 1f64aea4-d0a4-480b-9802-e2c21e71c754
ms.tgt_platform: multiple
title: Classe CIM_AlarmDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AlarmDevice
- CIM_AlarmDevice.Caption
- CIM_AlarmDevice.Description
- CIM_AlarmDevice.InstallDate
- CIM_AlarmDevice.Name
- CIM_AlarmDevice.Status
- CIM_AlarmDevice.Availability
- CIM_AlarmDevice.ConfigManagerErrorCode
- CIM_AlarmDevice.ConfigManagerUserConfig
- CIM_AlarmDevice.CreationClassName
- CIM_AlarmDevice.DeviceID
- CIM_AlarmDevice.PowerManagementCapabilities
- CIM_AlarmDevice.ErrorCleared
- CIM_AlarmDevice.ErrorDescription
- CIM_AlarmDevice.LastErrorCode
- CIM_AlarmDevice.PNPDeviceID
- CIM_AlarmDevice.PowerManagementSupported
- CIM_AlarmDevice.StatusInfo
- CIM_AlarmDevice.SystemCreationClassName
- CIM_AlarmDevice.SystemName
- CIM_AlarmDevice.AudibleAlarm
- CIM_AlarmDevice.Urgency
- CIM_AlarmDevice.VisibleAlarm
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 622a6031f36140e23514b925835cebae84b35025
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523897"
---
# <a name="cim_alarmdevice-class"></a><span data-ttu-id="7958d-103">CIM \_ AlarmDevice (classe)</span><span class="sxs-lookup"><span data-stu-id="7958d-103">CIM\_AlarmDevice class</span></span>

<span data-ttu-id="7958d-104">La classe **CIM \_ AlarmDevice** è un dispositivo di allarme che emette indicazioni udibili o visibili correlate alla situazione di un problema.</span><span class="sxs-lookup"><span data-stu-id="7958d-104">The **CIM\_AlarmDevice** class is an alarm device that emits audible or visible indications related to a problem situation.</span></span>

<span data-ttu-id="7958d-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="7958d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="7958d-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="7958d-106">Properties are listed in alphabetic order, not MOF order.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7958d-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="7958d-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7958d-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7958d-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="7958d-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7958d-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B66-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_AlarmDevice : CIM_LogicalDevice
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
  boolean  AudibleAlarm;
  uint16   Urgency;
  boolean  VisibleAlarm;
};
```

## <a name="members"></a><span data-ttu-id="7958d-110">Members</span><span class="sxs-lookup"><span data-stu-id="7958d-110">Members</span></span>

<span data-ttu-id="7958d-111">La classe **CIM \_ AlarmDevice** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7958d-111">The **CIM\_AlarmDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="7958d-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="7958d-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="7958d-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7958d-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7958d-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="7958d-114">Methods</span></span>

<span data-ttu-id="7958d-115">La classe **CIM \_ AlarmDevice** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="7958d-115">The **CIM\_AlarmDevice** class has these methods.</span></span>



| <span data-ttu-id="7958d-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="7958d-116">Method</span></span>                                                                 | <span data-ttu-id="7958d-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7958d-117">Description</span></span>                                                                                                                             |
|:-----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7958d-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="7958d-118">**Reset**</span></span>](reset-method-in-class-cim-alarmdevice.md)                 | <span data-ttu-id="7958d-119">Richiede la reimpostazione di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="7958d-119">Requests a logical device reset.</span></span> <span data-ttu-id="7958d-120">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="7958d-120">Not implemented by WMI.</span></span><br/>                                                                     |
| [<span data-ttu-id="7958d-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="7958d-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-alarmdevice.md) | <span data-ttu-id="7958d-122">Imposta lo stato di alimentazione desiderato per un dispositivo logico e quando il dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="7958d-122">Sets the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="7958d-123">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="7958d-123">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="7958d-124">**SetUrgency**</span><span class="sxs-lookup"><span data-stu-id="7958d-124">**SetUrgency**</span></span>](seturgency-method-in-class-cim-alarmdevice.md)       | <span data-ttu-id="7958d-125">Imposta il livello di urgenza desiderato per l'allarme.</span><span class="sxs-lookup"><span data-stu-id="7958d-125">Sets the desired urgency level for the alarm.</span></span> <span data-ttu-id="7958d-126">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="7958d-126">Not implemented by WMI.</span></span><br/>                                                        |



 

### <a name="properties"></a><span data-ttu-id="7958d-127">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7958d-127">Properties</span></span>

<span data-ttu-id="7958d-128">La classe **CIM \_ AlarmDevice** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7958d-128">The **CIM\_AlarmDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7958d-129">**AudibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="7958d-129">**AudibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7958d-130">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7958d-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7958d-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7958d-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7958d-132">Se **true**, l'allarme è acustico.</span><span class="sxs-lookup"><span data-stu-id="7958d-132">If **TRUE**, the alarm is audible.</span></span>

</dd> <dt>

<span data-ttu-id="7958d-133">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="7958d-133">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7958d-134">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7958d-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7958d-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7958d-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7958d-136">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="7958d-136">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="7958d-137">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7958d-137">Availability and status of the device.</span></span>

<span data-ttu-id="7958d-138">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7958d-138">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7958d-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="7958d-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7958d-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="7958d-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="7958d-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="7958d-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="7958d-142"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="7958d-142"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="7958d-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="7958d-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="7958d-144"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="7958d-144"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="7958d-145"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="7958d-145"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="7958d-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="7958d-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="7958d-147"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="7958d-147"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7958d-148"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="7958d-148"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="7958d-149"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="7958d-149"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="7958d-150"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="7958d-150"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="7958d-151"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="7958d-151"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="7958d-152">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="7958d-152">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="7958d-153"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="7958d-153"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="7958d-154">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="7958d-154">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="7958d-155"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="7958d-155"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="7958d-156">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="7958d-156">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="7958d-157"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="7958d-157"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="7958d-158"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="7958d-158"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="7958d-159">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="7958d-159">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="7958d-160"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="7958d-160"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="7958d-161">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="7958d-161">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="7958d-162"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="7958d-162"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="7958d-163">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="7958d-163">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="7958d-164"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="7958d-164"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="7958d-165">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="7958d-165">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="7958d-166"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="7958d-166"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="7958d-167">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="7958d-167">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7958d-168">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="7958d-168">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7958d-169">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7958d-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7958d-170">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7958d-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7958d-171">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="7958d-171">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="7958d-172">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7958d-172">A short textual description of the object.</span></span>

<span data-ttu-id="7958d-173">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7958d-173">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7958d-174">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="7958d-174">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7958d-175">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7958d-175">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7958d-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7958d-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7958d-177">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="7958d-177">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7958d-178">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="7958d-178">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="7958d-179">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7958d-179">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="7958d-180">**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="7958d-180">**This device is working properly.**</span></span> <span data-ttu-id="7958d-181"> (0)</span><span class="sxs-lookup"><span data-stu-id="7958d-181">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="7958d-182">**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="7958d-182">**This device is not configured correctly.**</span></span> <span data-ttu-id="7958d-183">(1)</span><span class="sxs-lookup"><span data-stu-id="7958d-183">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7958d-184">**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7958d-184">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="7958d-185">(2)</span><span class="sxs-lookup"><span data-stu-id="7958d-185">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="7958d-186">**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="7958d-186">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="7958d-187">(3)</span><span class="sxs-lookup"><span data-stu-id="7958d-187">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="7958d-188">**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="7958d-188">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="7958d-189">(4)</span><span class="sxs-lookup"><span data-stu-id="7958d-189">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="7958d-190">**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="7958d-190">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="7958d-191">(5)</span><span class="sxs-lookup"><span data-stu-id="7958d-191">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="7958d-192">**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="7958d-192">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="7958d-193"> (6)</span><span class="sxs-lookup"><span data-stu-id="7958d-193">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="7958d-194">**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="7958d-194">**Cannot filter.**</span></span> <span data-ttu-id="7958d-195">(7)</span><span class="sxs-lookup"><span data-stu-id="7958d-195">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="7958d-196">**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="7958d-196">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="7958d-197">(8)</span><span class="sxs-lookup"><span data-stu-id="7958d-197">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="7958d-198">**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="7958d-198">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="7958d-199">(9)</span><span class="sxs-lookup"><span data-stu-id="7958d-199">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="7958d-200">**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7958d-200">**This device cannot start.**</span></span> <span data-ttu-id="7958d-201">(10)</span><span class="sxs-lookup"><span data-stu-id="7958d-201">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="7958d-202">**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7958d-202">**This device failed.**</span></span> <span data-ttu-id="7958d-203">(11)</span><span class="sxs-lookup"><span data-stu-id="7958d-203">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="7958d-204">**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="7958d-204">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="7958d-205">12</span><span class="sxs-lookup"><span data-stu-id="7958d-205">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="7958d-206">**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7958d-206">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="7958d-207">(13)</span><span class="sxs-lookup"><span data-stu-id="7958d-207">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="7958d-208">**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="7958d-208">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="7958d-209">(14)</span><span class="sxs-lookup"><span data-stu-id="7958d-209">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="7958d-210">**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="7958d-210">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="7958d-211">(15)</span><span class="sxs-lookup"><span data-stu-id="7958d-211">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="7958d-212">**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7958d-212">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="7958d-213">(16)</span><span class="sxs-lookup"><span data-stu-id="7958d-213">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="7958d-214">**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="7958d-214">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="7958d-215">(17)</span><span class="sxs-lookup"><span data-stu-id="7958d-215">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7958d-216">**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7958d-216">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="7958d-217">(18)</span><span class="sxs-lookup"><span data-stu-id="7958d-217">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="7958d-218">**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="7958d-218">**Failure using the VxD loader.**</span></span> <span data-ttu-id="7958d-219">(19)</span><span class="sxs-lookup"><span data-stu-id="7958d-219">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="7958d-220">**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="7958d-220">**Your registry might be corrupted.**</span></span> <span data-ttu-id="7958d-221">(20)</span><span class="sxs-lookup"><span data-stu-id="7958d-221">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="7958d-222">**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7958d-222">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="7958d-223">(21)</span><span class="sxs-lookup"><span data-stu-id="7958d-223">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="7958d-224">**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="7958d-224">**This device is disabled.**</span></span> <span data-ttu-id="7958d-225">(22)</span><span class="sxs-lookup"><span data-stu-id="7958d-225">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="7958d-226">**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="7958d-226">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="7958d-227">(23)</span><span class="sxs-lookup"><span data-stu-id="7958d-227">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="7958d-228">**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="7958d-228">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="7958d-229">(24)</span><span class="sxs-lookup"><span data-stu-id="7958d-229">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="7958d-230">**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7958d-230">**Windows is still setting up this device.**</span></span> <span data-ttu-id="7958d-231">(25)</span><span class="sxs-lookup"><span data-stu-id="7958d-231">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="7958d-232">**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7958d-232">**Windows is still setting up this device.**</span></span> <span data-ttu-id="7958d-233">(26)</span><span class="sxs-lookup"><span data-stu-id="7958d-233">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="7958d-234">**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="7958d-234">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="7958d-235">(27)</span><span class="sxs-lookup"><span data-stu-id="7958d-235">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="7958d-236">**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="7958d-236">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="7958d-237">(28)</span><span class="sxs-lookup"><span data-stu-id="7958d-237">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="7958d-238">**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="7958d-238">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="7958d-239">(29)</span><span class="sxs-lookup"><span data-stu-id="7958d-239">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="7958d-240">**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7958d-240">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="7958d-241">(30)</span><span class="sxs-lookup"><span data-stu-id="7958d-241">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7958d-242">**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7958d-242">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="7958d-243">31</span><span class="sxs-lookup"><span data-stu-id="7958d-243">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7958d-244">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="7958d-244">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7958d-245">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7958d-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7958d-246">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7958d-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7958d-247">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="7958d-247">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7958d-248">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="7958d-248">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="7958d-249">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7958d-249">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7958d-250">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7958d-250">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7958d-251">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7958d-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7958d-252">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7958d-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7958d-253">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7958d-253">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7958d-254">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="7958d-254">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="7958d-255">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="7958d-255">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="7958d-256">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7958d-256">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7958d-257">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="7958d-257">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7958d-258">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7958d-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7958d-259">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7958d-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7958d-260">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="7958d-260">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="7958d-261">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7958d-261">A textual description of the object.</span></span>

<span data-ttu-id="7958d-262">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7958d-262">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7958d-263">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="7958d-263">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7958d-264">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7958d-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7958d-265">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7958d-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7958d-266">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7958d-266">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7958d-267">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="7958d-267">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="7958d-268">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7958d-268">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7958d-269">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="7958d-269">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7958d-270">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7958d-270">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7958d-271">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7958d-271">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7958d-272">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="7958d-272">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="7958d-273">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7958d-273">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7958d-274">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="7958d-274">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7958d-275">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7958d-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7958d-276">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7958d-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7958d-277">Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.</span><span class="sxs-lookup"><span data-stu-id="7958d-277">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="7958d-278">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7958d-278">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7958d-279">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7958d-279">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7958d-280">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7958d-280">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7958d-281">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7958d-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7958d-282">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="7958d-282">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="7958d-283">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="7958d-283">Indicates when the object was installed.</span></span> <span data-ttu-id="7958d-284">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="7958d-284">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="7958d-285">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7958d-285">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7958d-286">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="7958d-286">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7958d-287">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7958d-287">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7958d-288">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7958d-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7958d-289">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="7958d-289">Last error code reported by the logical device.</span></span>

<span data-ttu-id="7958d-290">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7958d-290">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7958d-291">**Nome**</span><span class="sxs-lookup"><span data-stu-id="7958d-291">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7958d-292">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7958d-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7958d-293">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7958d-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7958d-294">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="7958d-294">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="7958d-295">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="7958d-295">Label by which the object is known.</span></span> <span data-ttu-id="7958d-296">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="7958d-296">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="7958d-297">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7958d-297">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7958d-298">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="7958d-298">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7958d-299">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7958d-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7958d-300">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7958d-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7958d-301">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="7958d-301">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7958d-302">Indica l'identificatore del dispositivo Plug and Play Win32 del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="7958d-302">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="7958d-303">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="7958d-303">Example: "\*PNP030b"</span></span>

<span data-ttu-id="7958d-304">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7958d-304">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7958d-305">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="7958d-305">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7958d-306">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7958d-306">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7958d-307">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7958d-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7958d-308">Indica le funzionalità specifiche relative al risparmio di energia del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="7958d-308">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="7958d-309">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7958d-309">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7958d-310"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="7958d-310"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="7958d-311">Le capacità relative al risparmio di energia sono sconosciute.</span><span class="sxs-lookup"><span data-stu-id="7958d-311">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="7958d-312"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="7958d-312"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="7958d-313">Le capacità relative al risparmio di energia non sono supportate per questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7958d-313">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="7958d-314"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="7958d-314"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="7958d-315">Le capacità correlate all'alimentazione sono state disabilitate.</span><span class="sxs-lookup"><span data-stu-id="7958d-315">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="7958d-316"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="7958d-316"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7958d-317">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="7958d-317">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="7958d-318"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="7958d-318"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="7958d-319">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="7958d-319">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="7958d-320"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="7958d-320"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="7958d-321">Il metodo **SetPowerState** è supportato.</span><span class="sxs-lookup"><span data-stu-id="7958d-321">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="7958d-322">Questo metodo è disponibile nella classe [**\_ LogicalDevice CIM**](cim-logicaldevice.md) padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="7958d-322">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="7958d-323">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="7958d-323">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="7958d-324"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="7958d-324"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="7958d-325">Il metodo **SetPowerState** può essere richiamato con il parametro *PowerState* impostato su 5 ("ciclo di alimentazione").</span><span class="sxs-lookup"><span data-stu-id="7958d-325">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="7958d-326"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="7958d-326"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="7958d-327">Il metodo **SetPowerState** può essere richiamato con il parametro *PowerState* impostato su 5 ("ciclo di alimentazione") e il parametro *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="7958d-327">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7958d-328">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="7958d-328">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7958d-329">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7958d-329">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7958d-330">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7958d-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7958d-331">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="7958d-331">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="7958d-332">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="7958d-332">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="7958d-333">Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="7958d-333">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="7958d-334">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="7958d-334">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="7958d-335">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7958d-335">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7958d-336">**Status**</span><span class="sxs-lookup"><span data-stu-id="7958d-336">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7958d-337">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7958d-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7958d-338">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7958d-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7958d-339">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="7958d-339">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="7958d-340">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7958d-340">String that indicates the current status of the object.</span></span> <span data-ttu-id="7958d-341">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="7958d-341">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="7958d-342">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="7958d-342">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="7958d-343">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="7958d-343">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="7958d-344">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="7958d-344">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="7958d-345">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="7958d-345">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="7958d-346">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="7958d-346">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="7958d-347">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7958d-347">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="7958d-348">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="7958d-348">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="7958d-349">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="7958d-349">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="7958d-350">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="7958d-350">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7958d-351">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="7958d-351">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7958d-352">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="7958d-352">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="7958d-353">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="7958d-353">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="7958d-354">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="7958d-354">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="7958d-355">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="7958d-355">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="7958d-356">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="7958d-356">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="7958d-357">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="7958d-357">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="7958d-358">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="7958d-358">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="7958d-359">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="7958d-359">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="7958d-360">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="7958d-360">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7958d-361">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="7958d-361">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7958d-362">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7958d-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7958d-363">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7958d-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7958d-364">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="7958d-364">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="7958d-365">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="7958d-365">State of the logical device.</span></span> <span data-ttu-id="7958d-366">Se questa proprietà non è applicabile al dispositivo logico, è necessario utilizzare il valore 5 ("non applicabile").</span><span class="sxs-lookup"><span data-stu-id="7958d-366">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="7958d-367">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7958d-367">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7958d-368">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="7958d-368">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7958d-369">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="7958d-369">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="7958d-370">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="7958d-370">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="7958d-371">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="7958d-371">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="7958d-372">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="7958d-372">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7958d-373">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7958d-373">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7958d-374">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7958d-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7958d-375">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7958d-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7958d-376">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7958d-376">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7958d-377">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="7958d-377">The scoping system's creation class name.</span></span>

<span data-ttu-id="7958d-378">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7958d-378">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7958d-379">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="7958d-379">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7958d-380">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7958d-380">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7958d-381">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7958d-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7958d-382">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7958d-382">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7958d-383">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="7958d-383">The scoping system's name.</span></span>

<span data-ttu-id="7958d-384">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7958d-384">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7958d-385">**Urgenza**</span><span class="sxs-lookup"><span data-stu-id="7958d-385">**Urgency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7958d-386">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7958d-386">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7958d-387">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7958d-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7958d-388">Valore enumerato che indica la frequenza relativa con cui l'allarme lampeggia, vibra o emette toni acustici.</span><span class="sxs-lookup"><span data-stu-id="7958d-388">Enumerated value that indicates the relative frequency at which the alarm flashes, vibrates, or emits audible tones.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7958d-389"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="7958d-389"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="7958d-390">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="7958d-390">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7958d-391"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="7958d-391"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="7958d-392">Altro.</span><span class="sxs-lookup"><span data-stu-id="7958d-392">Other.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="7958d-393"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (2)</span><span class="sxs-lookup"><span data-stu-id="7958d-393"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (2)</span></span>


</dt> <dd>

<span data-ttu-id="7958d-394">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="7958d-394">Not supported.</span></span>

</dd> <dt>

<span id="Informational"></span><span id="informational"></span><span id="INFORMATIONAL"></span>

<span data-ttu-id="7958d-395"><span id="Informational"></span><span id="informational"></span><span id="INFORMATIONAL"></span>**Informativo** (3)</span><span class="sxs-lookup"><span data-stu-id="7958d-395"><span id="Informational"></span><span id="informational"></span><span id="INFORMATIONAL"></span>**Informational** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7958d-396">Si tratta di un messaggio informativo.</span><span class="sxs-lookup"><span data-stu-id="7958d-396">Informational.</span></span>

</dd> <dt>

<span id="Non-Critical"></span><span id="non-critical"></span><span id="NON-CRITICAL"></span>

<span data-ttu-id="7958d-397"><span id="Non-Critical"></span><span id="non-critical"></span><span id="NON-CRITICAL"></span>**Non critico** (4)</span><span class="sxs-lookup"><span data-stu-id="7958d-397"><span id="Non-Critical"></span><span id="non-critical"></span><span id="NON-CRITICAL"></span>**Non-Critical** (4)</span></span>


</dt> <dd>

<span data-ttu-id="7958d-398">Non critico.</span><span class="sxs-lookup"><span data-stu-id="7958d-398">Non-critical.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="7958d-399"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critico** (5)</span><span class="sxs-lookup"><span data-stu-id="7958d-399"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (5)</span></span>


</dt> <dd>

<span data-ttu-id="7958d-400">Critica.</span><span class="sxs-lookup"><span data-stu-id="7958d-400">Critical.</span></span>

</dd> <dt>

<span id="Unrecoverable"></span><span id="unrecoverable"></span><span id="UNRECOVERABLE"></span>

<span data-ttu-id="7958d-401"><span id="Unrecoverable"></span><span id="unrecoverable"></span><span id="UNRECOVERABLE"></span>**Irreversibile** (6)</span><span class="sxs-lookup"><span data-stu-id="7958d-401"><span id="Unrecoverable"></span><span id="unrecoverable"></span><span id="UNRECOVERABLE"></span>**Unrecoverable** (6)</span></span>


</dt> <dd>

<span data-ttu-id="7958d-402">Irreversibile.</span><span class="sxs-lookup"><span data-stu-id="7958d-402">Unrecoverable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7958d-403">**VisibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="7958d-403">**VisibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7958d-404">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7958d-404">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7958d-405">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7958d-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7958d-406">Se **true**, l'allarme è visibile.</span><span class="sxs-lookup"><span data-stu-id="7958d-406">If **TRUE**, the alarm is visible.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7958d-407">Commenti</span><span class="sxs-lookup"><span data-stu-id="7958d-407">Remarks</span></span>

<span data-ttu-id="7958d-408">La classe **CIM \_ AlarmDevice** è derivata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7958d-408">The **CIM\_AlarmDevice** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="7958d-409">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="7958d-409">WMI does not implement this class.</span></span>

<span data-ttu-id="7958d-410">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="7958d-410">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7958d-411">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="7958d-411">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7958d-412">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7958d-412">Requirements</span></span>



| <span data-ttu-id="7958d-413">Requisito</span><span class="sxs-lookup"><span data-stu-id="7958d-413">Requirement</span></span> | <span data-ttu-id="7958d-414">Valore</span><span class="sxs-lookup"><span data-stu-id="7958d-414">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7958d-415">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7958d-415">Minimum supported client</span></span><br/> | <span data-ttu-id="7958d-416">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7958d-416">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7958d-417">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7958d-417">Minimum supported server</span></span><br/> | <span data-ttu-id="7958d-418">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7958d-418">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7958d-419">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7958d-419">Namespace</span></span><br/>                | <span data-ttu-id="7958d-420">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="7958d-420">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7958d-421">MOF</span><span class="sxs-lookup"><span data-stu-id="7958d-421">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7958d-422"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7958d-422"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7958d-423">DLL</span><span class="sxs-lookup"><span data-stu-id="7958d-423">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7958d-424"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7958d-424"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7958d-425">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7958d-425">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7958d-426">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="7958d-426">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 


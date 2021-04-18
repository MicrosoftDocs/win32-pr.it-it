---
description: La \_ classe del processore CIM rappresenta le funzionalità e la gestione del dispositivo logico del processore.
ms.assetid: 7af3208f-f1d5-4911-b6ab-46b54eec0b69
ms.tgt_platform: multiple
title: Classe CIM_Processor (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Processor
- CIM_Processor.AddressWidth
- CIM_Processor.Availability
- CIM_Processor.Caption
- CIM_Processor.ConfigManagerErrorCode
- CIM_Processor.ConfigManagerUserConfig
- CIM_Processor.CreationClassName
- CIM_Processor.CurrentClockSpeed
- CIM_Processor.DataWidth
- CIM_Processor.Description
- CIM_Processor.DeviceID
- CIM_Processor.ErrorCleared
- CIM_Processor.ErrorDescription
- CIM_Processor.Family
- CIM_Processor.InstallDate
- CIM_Processor.LastErrorCode
- CIM_Processor.LoadPercentage
- CIM_Processor.MaxClockSpeed
- CIM_Processor.Name
- CIM_Processor.OtherFamilyDescription
- CIM_Processor.PNPDeviceID
- CIM_Processor.PowerManagementCapabilities
- CIM_Processor.PowerManagementSupported
- CIM_Processor.Role
- CIM_Processor.Status
- CIM_Processor.StatusInfo
- CIM_Processor.Stepping
- CIM_Processor.SystemCreationClassName
- CIM_Processor.SystemName
- CIM_Processor.UniqueId
- CIM_Processor.UpgradeMethod
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0120ce0327c21098b8c2950bd5dfa9a9fe2a709c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482997"
---
# <a name="cim_processor-class-cimwin32-wmi-providers"></a><span data-ttu-id="8c2eb-103">Classe CIM_Processor (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-103">CIM_Processor class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="8c2eb-104">La classe del **\_ processore CIM** rappresenta le funzionalità e la gestione del dispositivo logico del processore.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-104">The **CIM\_Processor** class represents the capabilities and management of the processor logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8c2eb-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8c2eb-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8c2eb-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8c2eb-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="8c2eb-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c2eb-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8c2eb-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C54B-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Processor : CIM_LogicalDevice
{
  uint16   AddressWidth;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint32   CurrentClockSpeed;
  uint16   DataWidth;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint16   Family;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint16   LoadPercentage;
  uint32   MaxClockSpeed;
  string   Name;
  string   OtherFamilyDescription;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Role;
  string   Status;
  uint16   StatusInfo;
  string   Stepping;
  string   SystemCreationClassName;
  string   SystemName;
  string   UniqueId;
  uint16   UpgradeMethod;
};
```

## <a name="members"></a><span data-ttu-id="8c2eb-110">Members</span><span class="sxs-lookup"><span data-stu-id="8c2eb-110">Members</span></span>

<span data-ttu-id="8c2eb-111">La classe del **\_ processore CIM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8c2eb-111">The **CIM\_Processor** class has these types of members:</span></span>

-   [<span data-ttu-id="8c2eb-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="8c2eb-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="8c2eb-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8c2eb-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8c2eb-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="8c2eb-114">Methods</span></span>

<span data-ttu-id="8c2eb-115">La classe del **\_ processore CIM** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-115">The **CIM\_Processor** class has these methods.</span></span>



| <span data-ttu-id="8c2eb-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="8c2eb-116">Method</span></span>                                                               | <span data-ttu-id="8c2eb-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8c2eb-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8c2eb-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-118">**Reset**</span></span>](reset-method-in-class-cim-processor.md)                 | <span data-ttu-id="8c2eb-119">Richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="8c2eb-120">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="8c2eb-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-processor.md) | <span data-ttu-id="8c2eb-122">Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="8c2eb-123">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8c2eb-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8c2eb-124">Properties</span></span>

<span data-ttu-id="8c2eb-125">La classe del **\_ processore CIM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-125">The **CIM\_Processor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8c2eb-126">**AddressWidth**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-126">**AddressWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2eb-127">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c2eb-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-129">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="8c2eb-129">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="8c2eb-130">Larghezza degli indirizzi del processore, in bit.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-130">Processor address width, in bits.</span></span>

</dd> <dt>

<span data-ttu-id="8c2eb-131">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-131">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2eb-132">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c2eb-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-134">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="8c2eb-134">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="8c2eb-135">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-135">Availability and status of the device.</span></span>

<span data-ttu-id="8c2eb-136">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8c2eb-136">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8c2eb-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8c2eb-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="8c2eb-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-140">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="8c2eb-140">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="8c2eb-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="8c2eb-142"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-142"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="8c2eb-143"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-143"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="8c2eb-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="8c2eb-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="8c2eb-145"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="8c2eb-145"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="8c2eb-146"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-146"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8c2eb-147"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-147"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="8c2eb-148"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-148"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="8c2eb-149"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-149"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="8c2eb-150"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-150"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-151">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-151">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="8c2eb-152"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-152"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-153">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-153">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="8c2eb-154"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-154"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-155">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-155">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="8c2eb-156"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-156"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="8c2eb-157"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-157"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-158">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-158">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="8c2eb-159"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-159"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-160">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-160">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="8c2eb-161"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-161"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-162">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-162">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="8c2eb-163"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-163"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-164">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-164">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="8c2eb-165"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-165"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-166">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-166">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8c2eb-167">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-167">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2eb-168">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c2eb-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-170">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="8c2eb-170">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="8c2eb-171">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-171">Short textual description of the object.</span></span>

<span data-ttu-id="8c2eb-172">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8c2eb-172">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c2eb-173">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-173">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2eb-174">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c2eb-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-176">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="8c2eb-176">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="8c2eb-177">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-177">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="8c2eb-178">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8c2eb-178">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="8c2eb-179"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-179"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="8c2eb-180"> (0)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-180">(0)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-181">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-181">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="8c2eb-182"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-182"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="8c2eb-183">(1)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-183">(1)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-184">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-184">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="8c2eb-185"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-185"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="8c2eb-186">(2)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-186">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="8c2eb-187"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-187"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="8c2eb-188">(3)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-188">(3)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-189">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-189">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="8c2eb-190"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-190"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="8c2eb-191">(4)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-191">(4)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-192">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-192">Device is not working properly.</span></span> <span data-ttu-id="8c2eb-193">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-193">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="8c2eb-194"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-194"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="8c2eb-195">(5)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-195">(5)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-196">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-196">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="8c2eb-197"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-197"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="8c2eb-198"> (6)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-198">(6)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-199">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-199">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="8c2eb-200"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-200"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="8c2eb-201">(7)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-201">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="8c2eb-202"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-202"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="8c2eb-203">(8)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-203">(8)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-204">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-204">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="8c2eb-205"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-205"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="8c2eb-206">(9)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-206">(9)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-207">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-207">Device is not working properly.</span></span> <span data-ttu-id="8c2eb-208">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-208">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="8c2eb-209"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-209"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="8c2eb-210">(10)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-210">(10)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-211">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-211">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="8c2eb-212"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-212"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="8c2eb-213">(11)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-213">(11)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-214">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-214">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="8c2eb-215"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-215"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="8c2eb-216">12</span><span class="sxs-lookup"><span data-stu-id="8c2eb-216">(12)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-217">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-217">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="8c2eb-218"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-218"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="8c2eb-219">(13)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-219">(13)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-220">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-220">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="8c2eb-221"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-221"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="8c2eb-222">(14)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-222">(14)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-223">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-223">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="8c2eb-224"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-224"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="8c2eb-225">(15)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-225">(15)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-226">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-226">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="8c2eb-227"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-227"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="8c2eb-228">(16)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-228">(16)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-229">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-229">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="8c2eb-230"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-230"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="8c2eb-231">(17)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-231">(17)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-232">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-232">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="8c2eb-233"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-233"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="8c2eb-234">(18)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-234">(18)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-235">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-235">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="8c2eb-236"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-236"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="8c2eb-237">(19)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-237">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="8c2eb-238"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-238"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="8c2eb-239">(20)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-239">(20)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-240">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-240">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="8c2eb-241"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-241"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="8c2eb-242">(21)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-242">(21)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-243">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-243">System failure.</span></span> <span data-ttu-id="8c2eb-244">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-244">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="8c2eb-245">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-245">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="8c2eb-246"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-246"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="8c2eb-247">(22)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-247">(22)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-248">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-248">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="8c2eb-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="8c2eb-250">(23)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-250">(23)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-251">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-251">System failure.</span></span> <span data-ttu-id="8c2eb-252">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-252">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="8c2eb-253"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-253"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="8c2eb-254">(24)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-254">(24)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-255">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-255">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="8c2eb-256"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-256"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="8c2eb-257">(25)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-257">(25)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-258">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-258">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="8c2eb-259"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-259"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="8c2eb-260">(26)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-260">(26)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-261">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-261">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="8c2eb-262"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-262"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="8c2eb-263">(27)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-263">(27)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-264">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-264">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="8c2eb-265"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-265"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="8c2eb-266">(28)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-266">(28)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-267">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-267">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="8c2eb-268"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-268"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="8c2eb-269">(29)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-269">(29)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-270">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-270">Device is disabled.</span></span> <span data-ttu-id="8c2eb-271">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-271">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="8c2eb-272"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-272"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="8c2eb-273">(30)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-273">(30)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-274">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-274">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="8c2eb-275"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-275"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="8c2eb-276">31</span><span class="sxs-lookup"><span data-stu-id="8c2eb-276">(31)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-277">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-277">Device is not working properly.</span></span> <span data-ttu-id="8c2eb-278">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-278">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8c2eb-279">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-279">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2eb-280">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-280">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-281">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c2eb-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-282">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="8c2eb-282">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="8c2eb-283">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-283">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="8c2eb-284">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8c2eb-284">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c2eb-285">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-285">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2eb-286">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-287">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c2eb-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-288">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-288">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8c2eb-289">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-289">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="8c2eb-290">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-290">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="8c2eb-291">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8c2eb-291">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c2eb-292">**CurrentClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-292">**CurrentClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2eb-293">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-293">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-294">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c2eb-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-295">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Processore DMTF \| 006,6 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" megahertz ")</span><span class="sxs-lookup"><span data-stu-id="8c2eb-295">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Processor\|006.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span></span>
</dt> </dl>

<span data-ttu-id="8c2eb-296">Velocità corrente (in megahertz) del processore.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-296">Current speed (in megahertz) of the processor.</span></span>

</dd> <dt>

<span data-ttu-id="8c2eb-297">**DataWidth**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-297">**DataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2eb-298">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-298">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-299">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c2eb-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-300">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="8c2eb-300">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="8c2eb-301">Larghezza dei dati del processore, in bit.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-301">Processor data width, in bits.</span></span>

</dd> <dt>

<span data-ttu-id="8c2eb-302">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-302">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2eb-303">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-304">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c2eb-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-305">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="8c2eb-305">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="8c2eb-306">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-306">Textual description of the object.</span></span>

<span data-ttu-id="8c2eb-307">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8c2eb-307">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c2eb-308">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-308">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2eb-309">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-310">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c2eb-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-311">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-311">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8c2eb-312">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-312">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="8c2eb-313">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8c2eb-313">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c2eb-314">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-314">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2eb-315">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-315">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-316">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c2eb-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c2eb-317">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-317">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="8c2eb-318">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8c2eb-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c2eb-319">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-319">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2eb-320">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-321">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c2eb-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c2eb-322">Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-322">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="8c2eb-323">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8c2eb-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c2eb-324">**Famiglia**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-324">**Family**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2eb-325">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-325">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-326">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c2eb-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-327">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Processore DMTF \| 014,3 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ processore CIM**.**OtherFamilyDescription**")</span><span class="sxs-lookup"><span data-stu-id="8c2eb-327">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Processor\|014.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Processor**.**OtherFamilyDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="8c2eb-328">Tipo di famiglia del processore.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-328">Processor family type.</span></span>

<span data-ttu-id="8c2eb-329">Questa proprietà viene ereditata **dal \_ processore CIM**.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-329">This property is inherited from **CIM\_Processor**.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8c2eb-330"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-330"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8c2eb-331"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-331"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="8086"></span>

<span data-ttu-id="8c2eb-332"><span id="8086"></span>**8086** (3)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-332"><span id="8086"></span>**8086** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="80286"></span>

<span data-ttu-id="8c2eb-333"><span id="80286"></span>**80286** (4)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-333"><span id="80286"></span>**80286** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="80386"></span>

<span data-ttu-id="8c2eb-334"><span id="80386"></span>**80386** (5)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-334"><span id="80386"></span>**80386** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="80486"></span>

<span data-ttu-id="8c2eb-335"><span id="80486"></span>**80486** (6)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-335"><span id="80486"></span>**80486** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8087"></span>

<span data-ttu-id="8c2eb-336"><span id="8087"></span>**8087** (7)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-336"><span id="8087"></span>**8087** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="80287"></span>

<span data-ttu-id="8c2eb-337"><span id="80287"></span>**80287** (8)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-337"><span id="80287"></span>**80287** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="80387"></span>

<span data-ttu-id="8c2eb-338"><span id="80387"></span>**80387** (9)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-338"><span id="80387"></span>**80387** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="80487"></span>

<span data-ttu-id="8c2eb-339"><span id="80487"></span>**80487** (10)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-339"><span id="80487"></span>**80487** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Pentium_R__brand"></span><span id="pentium_r__brand"></span><span id="PENTIUM_R__BRAND"></span>

<span data-ttu-id="8c2eb-340"><span id="Pentium_R__brand"></span><span id="pentium_r__brand"></span><span id="PENTIUM_R__BRAND"></span>**Pentium (R) brand** (11)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-340"><span id="Pentium_R__brand"></span><span id="pentium_r__brand"></span><span id="PENTIUM_R__BRAND"></span>**Pentium(R) brand** (11)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-341">Marchio Pentium</span><span class="sxs-lookup"><span data-stu-id="8c2eb-341">Pentium brand</span></span>

</dd> <dt>

<span id="Pentium_R__Pro"></span><span id="pentium_r__pro"></span><span id="PENTIUM_R__PRO"></span>

<span data-ttu-id="8c2eb-342"><span id="Pentium_R__Pro"></span><span id="pentium_r__pro"></span><span id="PENTIUM_R__PRO"></span>**Pentium (R) Pro** (12)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-342"><span id="Pentium_R__Pro"></span><span id="pentium_r__pro"></span><span id="PENTIUM_R__PRO"></span>**Pentium(R) Pro** (12)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-343">Pentium Pro</span><span class="sxs-lookup"><span data-stu-id="8c2eb-343">Pentium Pro</span></span>

</dd> <dt>

<span id="Pentium_R__II"></span><span id="pentium_r__ii"></span><span id="PENTIUM_R__II"></span>

<span data-ttu-id="8c2eb-344"><span id="Pentium_R__II"></span><span id="pentium_r__ii"></span><span id="PENTIUM_R__II"></span>**Pentium (R) II** (13)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-344"><span id="Pentium_R__II"></span><span id="pentium_r__ii"></span><span id="PENTIUM_R__II"></span>**Pentium(R) II** (13)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-345">Pentium II</span><span class="sxs-lookup"><span data-stu-id="8c2eb-345">Pentium II</span></span>

</dd> <dt>

<span id="Pentium_R__processor_with_MMX_TM__technology"></span><span id="pentium_r__processor_with_mmx_tm__technology"></span><span id="PENTIUM_R__PROCESSOR_WITH_MMX_TM__TECHNOLOGY"></span>

<span data-ttu-id="8c2eb-346"><span id="Pentium_R__processor_with_MMX_TM__technology"></span><span id="pentium_r__processor_with_mmx_tm__technology"></span><span id="PENTIUM_R__PROCESSOR_WITH_MMX_TM__TECHNOLOGY"></span>**Processore Pentium (R) con tecnologia MMX (TM)** (14)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-346"><span id="Pentium_R__processor_with_MMX_TM__technology"></span><span id="pentium_r__processor_with_mmx_tm__technology"></span><span id="PENTIUM_R__PROCESSOR_WITH_MMX_TM__TECHNOLOGY"></span>**Pentium(R) processor with MMX(TM) technology** (14)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-347">Processore Pentium con tecnologia MMX</span><span class="sxs-lookup"><span data-stu-id="8c2eb-347">Pentium processor with MMX technology</span></span>

</dd> <dt>

<span id="Celeron_TM_"></span><span id="celeron_tm_"></span><span id="CELERON_TM_"></span>

<span data-ttu-id="8c2eb-348"><span id="Celeron_TM_"></span><span id="celeron_tm_"></span><span id="CELERON_TM_"></span>**Celeron (TM)** (15)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-348"><span id="Celeron_TM_"></span><span id="celeron_tm_"></span><span id="CELERON_TM_"></span>**Celeron(TM)** (15)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-349">Celeron</span><span class="sxs-lookup"><span data-stu-id="8c2eb-349">Celeron</span></span>

</dd> <dt>

<span id="Pentium_R__II_Xeon_TM_"></span><span id="pentium_r__ii_xeon_tm_"></span><span id="PENTIUM_R__II_XEON_TM_"></span>

<span data-ttu-id="8c2eb-350"><span id="Pentium_R__II_Xeon_TM_"></span><span id="pentium_r_:xeon_tm_"></span><span id="PENTIUM_R__II_XEON_TM_"></span>**Pentium (R) II Xeon (TM)** (16)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-350"><span id="Pentium_R__II_Xeon_TM_"></span><span id="pentium_r__ii_xeon_tm_"></span><span id="PENTIUM_R__II_XEON_TM_"></span>**Pentium(R) II Xeon(TM)** (16)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-351">Xeon Pentium II</span><span class="sxs-lookup"><span data-stu-id="8c2eb-351">Pentium II Xeon</span></span>

</dd> <dt>

<span id="Pentium_R__III"></span><span id="pentium_r__iii"></span><span id="PENTIUM_R__III"></span>

<span data-ttu-id="8c2eb-352"><span id="Pentium_R__III"></span><span id="pentium_r__iii"></span><span id="PENTIUM_R__III"></span>**Pentium (R) III** (17)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-352"><span id="Pentium_R__III"></span><span id="pentium_r__iii"></span><span id="PENTIUM_R__III"></span>**Pentium(R) III** (17)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-353">Pentium III</span><span class="sxs-lookup"><span data-stu-id="8c2eb-353">Pentium III</span></span>

</dd> <dt>

<span id="M1_Family"></span><span id="m1_family"></span><span id="M1_FAMILY"></span>

<span data-ttu-id="8c2eb-354"><span id="M1_Family"></span><span id="m1_family"></span><span id="M1_FAMILY"></span>**Famiglia M1** (18)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-354"><span id="M1_Family"></span><span id="m1_family"></span><span id="M1_FAMILY"></span>**M1 Family** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="M2_Family"></span><span id="m2_family"></span><span id="M2_FAMILY"></span>

<span data-ttu-id="8c2eb-355"><span id="M2_Family"></span><span id="m2_family"></span><span id="M2_FAMILY"></span>**Famiglia m2** (19)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-355"><span id="M2_Family"></span><span id="m2_family"></span><span id="M2_FAMILY"></span>**M2 Family** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="K5_Family"></span><span id="k5_family"></span><span id="K5_FAMILY"></span>

<span data-ttu-id="8c2eb-356"><span id="K5_Family"></span><span id="k5_family"></span><span id="K5_FAMILY"></span>**Famiglia K5** (24)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-356"><span id="K5_Family"></span><span id="k5_family"></span><span id="K5_FAMILY"></span>**K5 Family** (24)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-357">Famiglia di processori AMD Duron</span><span class="sxs-lookup"><span data-stu-id="8c2eb-357">AMD Duron  Processor Family</span></span>

</dd> <dt>

<span id="K6_Family"></span><span id="k6_family"></span><span id="K6_FAMILY"></span>

<span data-ttu-id="8c2eb-358"><span id="K6_Family"></span><span id="k6_family"></span><span id="K6_FAMILY"></span>**Famiglia K6** (25)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-358"><span id="K6_Family"></span><span id="k6_family"></span><span id="K6_FAMILY"></span>**K6 Family** (25)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-359">Famiglia K5</span><span class="sxs-lookup"><span data-stu-id="8c2eb-359">K5 Family</span></span>

</dd> <dt>

<span id="K6-2"></span><span id="k6-2"></span>

<span data-ttu-id="8c2eb-360"><span id="K6-2"></span><span id="k6-2"></span>**K6-2** (26)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-360"><span id="K6-2"></span><span id="k6-2"></span>**K6-2** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="K6-3"></span><span id="k6-3"></span>

<span data-ttu-id="8c2eb-361"><span id="K6-3"></span><span id="k6-3"></span>**K6-3** (27)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-361"><span id="K6-3"></span><span id="k6-3"></span>**K6-3** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__Processor_Family"></span><span id="amd_athlon_tm__processor_family"></span><span id="AMD_ATHLON_TM__PROCESSOR_FAMILY"></span>

<span data-ttu-id="8c2eb-362"><span id="AMD_Athlon_TM__Processor_Family"></span><span id="amd_athlon_tm__processor_family"></span><span id="AMD_ATHLON_TM__PROCESSOR_FAMILY"></span>**Famiglia di processori AMD Athlon (TM)** (28)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-362"><span id="AMD_Athlon_TM__Processor_Family"></span><span id="amd_athlon_tm__processor_family"></span><span id="AMD_ATHLON_TM__PROCESSOR_FAMILY"></span>**AMD Athlon(TM) Processor Family** (28)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-363">Famiglia di processori AMD Athlon</span><span class="sxs-lookup"><span data-stu-id="8c2eb-363">AMD Athlon Processor Family</span></span>

</dd> <dt>

<span id="AMD_R__Duron_TM__Processor"></span><span id="amd_r__duron_tm__processor"></span><span id="AMD_R__DURON_TM__PROCESSOR"></span>

<span data-ttu-id="8c2eb-364"><span id="AMD_R__Duron_TM__Processor"></span><span id="amd_r__duron_tm__processor"></span><span id="AMD_R__DURON_TM__PROCESSOR"></span>**Processore AMD (R) Duron (TM)** (29)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-364"><span id="AMD_R__Duron_TM__Processor"></span><span id="amd_r__duron_tm__processor"></span><span id="AMD_R__DURON_TM__PROCESSOR"></span>**AMD(R) Duron(TM) Processor** (29)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-365">Processore AMD Duron</span><span class="sxs-lookup"><span data-stu-id="8c2eb-365">AMD  Duron Processor</span></span>

</dd> <dt>

<span id="AMD29000_Family"></span><span id="amd29000_family"></span><span id="AMD29000_FAMILY"></span>

<span data-ttu-id="8c2eb-366"><span id="AMD29000_Family"></span><span id="amd29000_family"></span><span id="AMD29000_FAMILY"></span>**Famiglia AMD29000** (30)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-366"><span id="AMD29000_Family"></span><span id="amd29000_family"></span><span id="AMD29000_FAMILY"></span>**AMD29000 Family** (30)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-367">Famiglia AMD2900</span><span class="sxs-lookup"><span data-stu-id="8c2eb-367">AMD2900 Family</span></span>

</dd> <dt>

<span id="K6-2_"></span><span id="k6-2_"></span>

<span data-ttu-id="8c2eb-368"><span id="K6-2_"></span><span id="k6-2_"></span>**K6-2 +** (31)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-368"><span id="K6-2_"></span><span id="k6-2_"></span>**K6-2+** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_Family"></span><span id="power_pc_family"></span><span id="POWER_PC_FAMILY"></span>

<span data-ttu-id="8c2eb-369"><span id="Power_PC_Family"></span><span id="power_pc_family"></span><span id="POWER_PC_FAMILY"></span>**Famiglia Power PC** (32)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-369"><span id="Power_PC_Family"></span><span id="power_pc_family"></span><span id="POWER_PC_FAMILY"></span>**Power PC Family** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_601"></span><span id="power_pc_601"></span><span id="POWER_PC_601"></span>

<span data-ttu-id="8c2eb-370"><span id="Power_PC_601"></span><span id="power_pc_601"></span><span id="POWER_PC_601"></span>**Power PC 601** (33)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-370"><span id="Power_PC_601"></span><span id="power_pc_601"></span><span id="POWER_PC_601"></span>**Power PC 601** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_603"></span><span id="power_pc_603"></span><span id="POWER_PC_603"></span>

<span data-ttu-id="8c2eb-371"><span id="Power_PC_603"></span><span id="power_pc_603"></span><span id="POWER_PC_603"></span>**Power PC 603** (34)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-371"><span id="Power_PC_603"></span><span id="power_pc_603"></span><span id="POWER_PC_603"></span>**Power PC 603** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_603_"></span><span id="power_pc_603_"></span><span id="POWER_PC_603_"></span>

<span data-ttu-id="8c2eb-372"><span id="Power_PC_603_"></span><span id="power_pc_603_"></span><span id="POWER_PC_603_"></span>**Power PC 603 +** (35)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-372"><span id="Power_PC_603_"></span><span id="power_pc_603_"></span><span id="POWER_PC_603_"></span>**Power PC 603+** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_604"></span><span id="power_pc_604"></span><span id="POWER_PC_604"></span>

<span data-ttu-id="8c2eb-373"><span id="Power_PC_604"></span><span id="power_pc_604"></span><span id="POWER_PC_604"></span>**Power PC 604** (36)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-373"><span id="Power_PC_604"></span><span id="power_pc_604"></span><span id="POWER_PC_604"></span>**Power PC 604** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_620"></span><span id="power_pc_620"></span><span id="POWER_PC_620"></span>

<span data-ttu-id="8c2eb-374"><span id="Power_PC_620"></span><span id="power_pc_620"></span><span id="POWER_PC_620"></span>**Power PC 620** (37)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-374"><span id="Power_PC_620"></span><span id="power_pc_620"></span><span id="POWER_PC_620"></span>**Power PC 620** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_X704"></span><span id="power_pc_x704"></span><span id="POWER_PC_X704"></span>

<span data-ttu-id="8c2eb-375"><span id="Power_PC_X704"></span><span id="power_pc_x704"></span><span id="POWER_PC_X704"></span>**Power PC x704** (38)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-375"><span id="Power_PC_X704"></span><span id="power_pc_x704"></span><span id="POWER_PC_X704"></span>**Power PC X704** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_750"></span><span id="power_pc_750"></span><span id="POWER_PC_750"></span>

<span data-ttu-id="8c2eb-376"><span id="Power_PC_750"></span><span id="power_pc_750"></span><span id="POWER_PC_750"></span>**Power PC 750** (39)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-376"><span id="Power_PC_750"></span><span id="power_pc_750"></span><span id="POWER_PC_750"></span>**Power PC 750** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_Family"></span><span id="alpha_family"></span><span id="ALPHA_FAMILY"></span>

<span data-ttu-id="8c2eb-377"><span id="Alpha_Family"></span><span id="alpha_family"></span><span id="ALPHA_FAMILY"></span>**Famiglia alfa** (48)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-377"><span id="Alpha_Family"></span><span id="alpha_family"></span><span id="ALPHA_FAMILY"></span>**Alpha Family** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21064"></span><span id="alpha_21064"></span><span id="ALPHA_21064"></span>

<span data-ttu-id="8c2eb-378"><span id="Alpha_21064"></span><span id="alpha_21064"></span><span id="ALPHA_21064"></span>**Alfa 21064** (49)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-378"><span id="Alpha_21064"></span><span id="alpha_21064"></span><span id="ALPHA_21064"></span>**Alpha 21064** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21066"></span><span id="alpha_21066"></span><span id="ALPHA_21066"></span>

<span data-ttu-id="8c2eb-379"><span id="Alpha_21066"></span><span id="alpha_21066"></span><span id="ALPHA_21066"></span>**Alfa 21066** (50)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-379"><span id="Alpha_21066"></span><span id="alpha_21066"></span><span id="ALPHA_21066"></span>**Alpha 21066** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21164"></span><span id="alpha_21164"></span><span id="ALPHA_21164"></span>

<span data-ttu-id="8c2eb-380"><span id="Alpha_21164"></span><span id="alpha_21164"></span><span id="ALPHA_21164"></span>**Alfa 21164** (51)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-380"><span id="Alpha_21164"></span><span id="alpha_21164"></span><span id="ALPHA_21164"></span>**Alpha 21164** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21164PC"></span><span id="alpha_21164pc"></span><span id="ALPHA_21164PC"></span>

<span data-ttu-id="8c2eb-381"><span id="Alpha_21164PC"></span><span id="alpha_21164pc"></span><span id="ALPHA_21164PC"></span>**21164PC alfa** (52)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-381"><span id="Alpha_21164PC"></span><span id="alpha_21164pc"></span><span id="ALPHA_21164PC"></span>**Alpha 21164PC** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21164a"></span><span id="alpha_21164a"></span><span id="ALPHA_21164A"></span>

<span data-ttu-id="8c2eb-382"><span id="Alpha_21164a"></span><span id="alpha_21164a"></span><span id="ALPHA_21164A"></span>**21164A alfa** (53)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-382"><span id="Alpha_21164a"></span><span id="alpha_21164a"></span><span id="ALPHA_21164A"></span>**Alpha 21164a** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21264"></span><span id="alpha_21264"></span><span id="ALPHA_21264"></span>

<span data-ttu-id="8c2eb-383"><span id="Alpha_21264"></span><span id="alpha_21264"></span><span id="ALPHA_21264"></span>**Alfa 21264** (54)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-383"><span id="Alpha_21264"></span><span id="alpha_21264"></span><span id="ALPHA_21264"></span>**Alpha 21264** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21364"></span><span id="alpha_21364"></span><span id="ALPHA_21364"></span>

<span data-ttu-id="8c2eb-384"><span id="Alpha_21364"></span><span id="alpha_21364"></span><span id="ALPHA_21364"></span>**Alfa 21364** (55)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-384"><span id="Alpha_21364"></span><span id="alpha_21364"></span><span id="ALPHA_21364"></span>**Alpha 21364** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_Family"></span><span id="mips_family"></span><span id="MIPS_FAMILY"></span>

<span data-ttu-id="8c2eb-385"><span id="MIPS_Family"></span><span id="mips_family"></span><span id="MIPS_FAMILY"></span>**Famiglia MIPS** (64)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-385"><span id="MIPS_Family"></span><span id="mips_family"></span><span id="MIPS_FAMILY"></span>**MIPS Family** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R4000"></span><span id="mips_r4000"></span>

<span data-ttu-id="8c2eb-386"><span id="MIPS_R4000"></span><span id="mips_r4000"></span>**R4000 MIPS** (65)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-386"><span id="MIPS_R4000"></span><span id="mips_r4000"></span>**MIPS R4000** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R4200"></span><span id="mips_r4200"></span>

<span data-ttu-id="8c2eb-387"><span id="MIPS_R4200"></span><span id="mips_r4200"></span>**R4200 MIPS** (66)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-387"><span id="MIPS_R4200"></span><span id="mips_r4200"></span>**MIPS R4200** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R4400"></span><span id="mips_r4400"></span>

<span data-ttu-id="8c2eb-388"><span id="MIPS_R4400"></span><span id="mips_r4400"></span>**R4400 MIPS** (67)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-388"><span id="MIPS_R4400"></span><span id="mips_r4400"></span>**MIPS R4400** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R4600"></span><span id="mips_r4600"></span>

<span data-ttu-id="8c2eb-389"><span id="MIPS_R4600"></span><span id="mips_r4600"></span>**R4600 MIPS** (68)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-389"><span id="MIPS_R4600"></span><span id="mips_r4600"></span>**MIPS R4600** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R10000"></span><span id="mips_r10000"></span>

<span data-ttu-id="8c2eb-390"><span id="MIPS_R10000"></span><span id="mips_r10000"></span>**R10000 MIPS** (69)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-390"><span id="MIPS_R10000"></span><span id="mips_r10000"></span>**MIPS R10000** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="SPARC_Family"></span><span id="sparc_family"></span><span id="SPARC_FAMILY"></span>

<span data-ttu-id="8c2eb-391"><span id="SPARC_Family"></span><span id="sparc_family"></span><span id="SPARC_FAMILY"></span>**Famiglia Sparc** (80)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-391"><span id="SPARC_Family"></span><span id="sparc_family"></span><span id="SPARC_FAMILY"></span>**SPARC Family** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="SuperSPARC"></span><span id="supersparc"></span><span id="SUPERSPARC"></span>

<span data-ttu-id="8c2eb-392"><span id="SuperSPARC"></span><span id="supersparc"></span><span id="SUPERSPARC"></span>**SuperSPARC** (81)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-392"><span id="SuperSPARC"></span><span id="supersparc"></span><span id="SUPERSPARC"></span>**SuperSPARC** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="microSPARC_II"></span><span id="microsparc_ii"></span><span id="MICROSPARC_II"></span>

<span data-ttu-id="8c2eb-393"><span id="microSPARC_II"></span><span id="microsparc_ii"></span><span id="MICROSPARC_II"></span>**MICROSPARC II** (82)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-393"><span id="microSPARC_II"></span><span id="microsparc_ii"></span><span id="MICROSPARC_II"></span>**microSPARC II** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="microSPARC_IIep"></span><span id="microsparc_iiep"></span><span id="MICROSPARC_IIEP"></span>

<span data-ttu-id="8c2eb-394"><span id="microSPARC_IIep"></span><span id="microsparc_iiep"></span><span id="MICROSPARC_IIEP"></span>**MicroSparc IIep** (83)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-394"><span id="microSPARC_IIep"></span><span id="microsparc_iiep"></span><span id="MICROSPARC_IIEP"></span>**microSPARC IIep** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC"></span><span id="ultrasparc"></span><span id="ULTRASPARC"></span>

<span data-ttu-id="8c2eb-395"><span id="UltraSPARC"></span><span id="ultrasparc"></span><span id="ULTRASPARC"></span>**UltraSPARC** (84)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-395"><span id="UltraSPARC"></span><span id="ultrasparc"></span><span id="ULTRASPARC"></span>**UltraSPARC** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC_II"></span><span id="ultrasparc_ii"></span><span id="ULTRASPARC_II"></span>

<span data-ttu-id="8c2eb-396"><span id="UltraSPARC_II"></span><span id="ultrasparc_ii"></span><span id="ULTRASPARC_II"></span>**ULTRASPARC II** (85)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-396"><span id="UltraSPARC_II"></span><span id="ultrasparc_ii"></span><span id="ULTRASPARC_II"></span>**UltraSPARC II** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC_IIi"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>

<span data-ttu-id="8c2eb-397"><span id="UltraSPARC_IIi"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>**UltraSPARC III** (86)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-397"><span id="UltraSPARC_IIi"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>**UltraSPARC IIi** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC_III"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>

<span data-ttu-id="8c2eb-398"><span id="UltraSPARC_III"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>**ULTRASPARC III** (87)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-398"><span id="UltraSPARC_III"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>**UltraSPARC III** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC_IIIi"></span><span id="ultrasparc_iiii"></span><span id="ULTRASPARC_IIII"></span>

<span data-ttu-id="8c2eb-399"><span id="UltraSPARC_IIIi"></span><span id="ultrasparc_iiii"></span><span id="ULTRASPARC_IIII"></span>**UltraSPARC IIII** (88)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-399"><span id="UltraSPARC_IIIi"></span><span id="ultrasparc_iiii"></span><span id="ULTRASPARC_IIII"></span>**UltraSPARC IIIi** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="68040"></span>

<span data-ttu-id="8c2eb-400"><span id="68040"></span>**68040** (96)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-400"><span id="68040"></span>**68040** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="68xxx_Family"></span><span id="68xxx_family"></span><span id="68XXX_FAMILY"></span>

<span data-ttu-id="8c2eb-401"><span id="68xxx_Family"></span><span id="68xxx_family"></span><span id="68XXX_FAMILY"></span>**famiglia 68xxx** (97)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-401"><span id="68xxx_Family"></span><span id="68xxx_family"></span><span id="68XXX_FAMILY"></span>**68xxx Family** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="68000"></span>

<span data-ttu-id="8c2eb-402"><span id="68000"></span>**68000** (98)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-402"><span id="68000"></span>**68000** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="68010"></span>

<span data-ttu-id="8c2eb-403"><span id="68010"></span>**68010** (99)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-403"><span id="68010"></span>**68010** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="68020"></span>

<span data-ttu-id="8c2eb-404"><span id="68020"></span>**68020** (100)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-404"><span id="68020"></span>**68020** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="68030"></span>

<span data-ttu-id="8c2eb-405"><span id="68030"></span>**68030** (101)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-405"><span id="68030"></span>**68030** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="Hobbit_Family"></span><span id="hobbit_family"></span><span id="HOBBIT_FAMILY"></span>

<span data-ttu-id="8c2eb-406"><span id="Hobbit_Family"></span><span id="hobbit_family"></span><span id="HOBBIT_FAMILY"></span>**Famiglia Hobbit** (112)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-406"><span id="Hobbit_Family"></span><span id="hobbit_family"></span><span id="HOBBIT_FAMILY"></span>**Hobbit Family** (112)</span></span>


</dt> <dd></dd> <dt>

<span id="Crusoe_TM__TM5000_Family"></span><span id="crusoe_tm__tm5000_family"></span><span id="CRUSOE_TM__TM5000_FAMILY"></span>

<span data-ttu-id="8c2eb-407"><span id="Crusoe_TM__TM5000_Family"></span><span id="crusoe_tm__tm5000_family"></span><span id="CRUSOE_TM__TM5000_FAMILY"></span>**Crusoe (TM) TM5000 Family** (120)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-407"><span id="Crusoe_TM__TM5000_Family"></span><span id="crusoe_tm__tm5000_family"></span><span id="CRUSOE_TM__TM5000_FAMILY"></span>**Crusoe(TM) TM5000 Family** (120)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-408">Famiglia Crusoe TM5000</span><span class="sxs-lookup"><span data-stu-id="8c2eb-408">Crusoe TM5000 Family</span></span>

</dd> <dt>

<span id="Crusoe_TM__TM3000_Family"></span><span id="crusoe_tm__tm3000_family"></span><span id="CRUSOE_TM__TM3000_FAMILY"></span>

<span data-ttu-id="8c2eb-409"><span id="Crusoe_TM__TM3000_Family"></span><span id="crusoe_tm__tm3000_family"></span><span id="CRUSOE_TM__TM3000_FAMILY"></span>**Crusoe (TM) TM3000 Family** (121)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-409"><span id="Crusoe_TM__TM3000_Family"></span><span id="crusoe_tm__tm3000_family"></span><span id="CRUSOE_TM__TM3000_FAMILY"></span>**Crusoe(TM) TM3000 Family** (121)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-410">Famiglia Crusoe TM3000</span><span class="sxs-lookup"><span data-stu-id="8c2eb-410">Crusoe TM3000 Family</span></span>

</dd> <dt>

<span id="Efficeon_TM__TM8000_Family"></span><span id="efficeon_tm__tm8000_family"></span><span id="EFFICEON_TM__TM8000_FAMILY"></span>

<span data-ttu-id="8c2eb-411"><span id="Efficeon_TM__TM8000_Family"></span><span id="efficeon_tm__tm8000_family"></span><span id="EFFICEON_TM__TM8000_FAMILY"></span>**Efficeon (TM) TM8000 Family** (122)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-411"><span id="Efficeon_TM__TM8000_Family"></span><span id="efficeon_tm__tm8000_family"></span><span id="EFFICEON_TM__TM8000_FAMILY"></span>**Efficeon(TM) TM8000 Family** (122)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-412">Famiglia Efficeon8000</span><span class="sxs-lookup"><span data-stu-id="8c2eb-412">Efficeon8000 Family</span></span>

</dd> <dt>

<span id="Weitek"></span><span id="weitek"></span><span id="WEITEK"></span>

<span data-ttu-id="8c2eb-413"><span id="Weitek"></span><span id="weitek"></span><span id="WEITEK"></span>**Weitek** (128)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-413"><span id="Weitek"></span><span id="weitek"></span><span id="WEITEK"></span>**Weitek** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="Itanium_TM__Processor"></span><span id="itanium_tm__processor"></span><span id="ITANIUM_TM__PROCESSOR"></span>

<span data-ttu-id="8c2eb-414"><span id="Itanium_TM__Processor"></span><span id="itanium_tm__processor"></span><span id="ITANIUM_TM__PROCESSOR"></span>**Processore Itanium (TM)** (130)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-414"><span id="Itanium_TM__Processor"></span><span id="itanium_tm__processor"></span><span id="ITANIUM_TM__PROCESSOR"></span>**Itanium(TM) Processor** (130)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-415">Processore Itanium</span><span class="sxs-lookup"><span data-stu-id="8c2eb-415">Itanium  Processor</span></span>

</dd> <dt>

<span id="AMD_Athlon_TM__64_Processor_Family"></span><span id="amd_athlon_tm__64_processor_family"></span><span id="AMD_ATHLON_TM__64_PROCESSOR_FAMILY"></span>

<span data-ttu-id="8c2eb-416"><span id="AMD_Athlon_TM__64_Processor_Family"></span><span id="amd_athlon_tm__64_processor_family"></span><span id="AMD_ATHLON_TM__64_PROCESSOR_FAMILY"></span>**Famiglia di processori AMD Athlon (TM) 64** (131)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-416"><span id="AMD_Athlon_TM__64_Processor_Family"></span><span id="amd_athlon_tm__64_processor_family"></span><span id="AMD_ATHLON_TM__64_PROCESSOR_FAMILY"></span>**AMD Athlon(TM) 64 Processor Family** (131)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-417">AMD Athlon</span><span class="sxs-lookup"><span data-stu-id="8c2eb-417">AMD Athlon</span></span> 

</dd> <dt>

<span id="AMD_Opteron_TM__Family"></span><span id="amd_opteron_tm__family"></span><span id="AMD_OPTERON_TM__FAMILY"></span>

<span data-ttu-id="8c2eb-418"><span id="AMD_Opteron_TM__Family"></span><span id="amd_opteron_tm__family"></span><span id="AMD_OPTERON_TM__FAMILY"></span>**Famiglia AMD Opteron (TM)** (132)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-418"><span id="AMD_Opteron_TM__Family"></span><span id="amd_opteron_tm__family"></span><span id="AMD_OPTERON_TM__FAMILY"></span>**AMD Opteron(TM) Family** (132)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-419">Famiglia AMD Opteron</span><span class="sxs-lookup"><span data-stu-id="8c2eb-419">AMD Opteron  Family</span></span>

</dd> <dt>

<span id="PA-RISC_Family"></span><span id="pa-risc_family"></span><span id="PA-RISC_FAMILY"></span>

<span data-ttu-id="8c2eb-420"><span id="PA-RISC_Family"></span><span id="pa-risc_family"></span><span id="PA-RISC_FAMILY"></span>**Famiglia PA-RISC** (144)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-420"><span id="PA-RISC_Family"></span><span id="pa-risc_family"></span><span id="PA-RISC_FAMILY"></span>**PA-RISC Family** (144)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_8500"></span><span id="pa-risc_8500"></span>

<span data-ttu-id="8c2eb-421"><span id="PA-RISC_8500"></span><span id="pa-risc_8500"></span>**PA-RISC 8500** (145)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-421"><span id="PA-RISC_8500"></span><span id="pa-risc_8500"></span>**PA-RISC 8500** (145)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_8000"></span><span id="pa-risc_8000"></span>

<span data-ttu-id="8c2eb-422"><span id="PA-RISC_8000"></span><span id="pa-risc_8000"></span>**PA-RISC 8000** (146)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-422"><span id="PA-RISC_8000"></span><span id="pa-risc_8000"></span>**PA-RISC 8000** (146)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_7300LC"></span><span id="pa-risc_7300lc"></span>

<span data-ttu-id="8c2eb-423"><span id="PA-RISC_7300LC"></span><span id="pa-risc_7300lc"></span>**PA-RISC 7300LC** (147)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-423"><span id="PA-RISC_7300LC"></span><span id="pa-risc_7300lc"></span>**PA-RISC 7300LC** (147)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_7200"></span><span id="pa-risc_7200"></span>

<span data-ttu-id="8c2eb-424"><span id="PA-RISC_7200"></span><span id="pa-risc_7200"></span>**PA-RISC 7200** (148)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-424"><span id="PA-RISC_7200"></span><span id="pa-risc_7200"></span>**PA-RISC 7200** (148)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_7100LC"></span><span id="pa-risc_7100lc"></span>

<span data-ttu-id="8c2eb-425"><span id="PA-RISC_7100LC"></span><span id="pa-risc_7100lc"></span>**PA-RISC 7100LC** (149)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-425"><span id="PA-RISC_7100LC"></span><span id="pa-risc_7100lc"></span>**PA-RISC 7100LC** (149)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_7100"></span><span id="pa-risc_7100"></span>

<span data-ttu-id="8c2eb-426"><span id="PA-RISC_7100"></span><span id="pa-risc_7100"></span>**PA-RISC 7100** (150)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-426"><span id="PA-RISC_7100"></span><span id="pa-risc_7100"></span>**PA-RISC 7100** (150)</span></span>


</dt> <dd></dd> <dt>

<span id="V30_Family"></span><span id="v30_family"></span><span id="V30_FAMILY"></span>

<span data-ttu-id="8c2eb-427"><span id="V30_Family"></span><span id="v30_family"></span><span id="V30_FAMILY"></span>**Famiglia V30** (160)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-427"><span id="V30_Family"></span><span id="v30_family"></span><span id="V30_FAMILY"></span>**V30 Family** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="Pentium_R__III_Xeon_TM_"></span><span id="pentium_r__iii_xeon_tm_"></span><span id="PENTIUM_R__III_XEON_TM_"></span>

<span data-ttu-id="8c2eb-428"><span id="Pentium_R__III_Xeon_TM_"></span><span id="pentium_r__iii_xeon_tm_"></span><span id="PENTIUM_R__III_XEON_TM_"></span>**Pentium (R) III Xeon (TM)** (176)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-428"><span id="Pentium_R__III_Xeon_TM_"></span><span id="pentium_r__iii_xeon_tm_"></span><span id="PENTIUM_R__III_XEON_TM_"></span>**Pentium(R) III Xeon(TM)** (176)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-429">Xeon Pentium III</span><span class="sxs-lookup"><span data-stu-id="8c2eb-429">Pentium III Xeon</span></span>

</dd> <dt>

<span id="Pentium_R__III_Processor_with_Intel_R__SpeedStep_TM__Technology"></span><span id="pentium_r__iii_processor_with_intel_r__speedstep_tm__technology"></span><span id="PENTIUM_R__III_PROCESSOR_WITH_INTEL_R__SPEEDSTEP_TM__TECHNOLOGY"></span>

<span data-ttu-id="8c2eb-430"><span id="Pentium_R__III_Processor_with_Intel_R__SpeedStep_TM__Technology"></span><span id="pentium_r__iii_processor_with_intel_r__speedstep_tm__technology"></span><span id="PENTIUM_R__III_PROCESSOR_WITH_INTEL_R__SPEEDSTEP_TM__TECHNOLOGY"></span>**Processore Pentium (r) III con tecnologia Intel (r) SpeedStep (TM)** (177)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-430"><span id="Pentium_R__III_Processor_with_Intel_R__SpeedStep_TM__Technology"></span><span id="pentium_r__iii_processor_with_intel_r__speedstep_tm__technology"></span><span id="PENTIUM_R__III_PROCESSOR_WITH_INTEL_R__SPEEDSTEP_TM__TECHNOLOGY"></span>**Pentium(R) III Processor with Intel(R) SpeedStep(TM) Technology** (177)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-431">Processore Pentium III con tecnologia Intel SpeedStep</span><span class="sxs-lookup"><span data-stu-id="8c2eb-431">Pentium III Processor with Intel SpeedStep Technology</span></span>

</dd> <dt>

<span id="Pentium_R__4"></span><span id="pentium_r__4"></span><span id="PENTIUM_R__4"></span>

<span data-ttu-id="8c2eb-432"><span id="Pentium_R__4"></span><span id="pentium_r__4"></span><span id="PENTIUM_R__4"></span>**Pentium (R) 4** (178)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-432"><span id="Pentium_R__4"></span><span id="pentium_r__4"></span><span id="PENTIUM_R__4"></span>**Pentium(R) 4** (178)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-433">Pentium 4</span><span class="sxs-lookup"><span data-stu-id="8c2eb-433">Pentium 4</span></span>

</dd> <dt>

<span id="Intel_R__Xeon_TM_"></span><span id="intel_r__xeon_tm_"></span><span id="INTEL_R__XEON_TM_"></span>

<span data-ttu-id="8c2eb-434"><span id="Intel_R__Xeon_TM_"></span><span id="intel_r__xeon_tm_"></span><span id="INTEL_R__XEON_TM_"></span>**Intel (R) Xeon (TM)** (179)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-434"><span id="Intel_R__Xeon_TM_"></span><span id="intel_r__xeon_tm_"></span><span id="INTEL_R__XEON_TM_"></span>**Intel(R) Xeon(TM)** (179)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-435">Intel Xeon</span><span class="sxs-lookup"><span data-stu-id="8c2eb-435">Intel Xeon</span></span>

</dd> <dt>

<span id="AS400_Family"></span><span id="as400_family"></span><span id="AS400_FAMILY"></span>

<span data-ttu-id="8c2eb-436"><span id="AS400_Family"></span><span id="as400_family"></span><span id="AS400_FAMILY"></span>**Famiglia AS400** (180)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-436"><span id="AS400_Family"></span><span id="as400_family"></span><span id="AS400_FAMILY"></span>**AS400 Family** (180)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Xeon_TM__processor_MP"></span><span id="intel_r__xeon_tm__processor_mp"></span><span id="INTEL_R__XEON_TM__PROCESSOR_MP"></span>

<span data-ttu-id="8c2eb-437"><span id="Intel_R__Xeon_TM__processor_MP"></span><span id="intel_r__xeon_tm__processor_mp"></span><span id="INTEL_R__XEON_TM__PROCESSOR_MP"></span>**MP processore Intel (R) Xeon (TM)** (181)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-437"><span id="Intel_R__Xeon_TM__processor_MP"></span><span id="intel_r__xeon_tm__processor_mp"></span><span id="INTEL_R__XEON_TM__PROCESSOR_MP"></span>**Intel(R) Xeon(TM) processor MP** (181)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-438">MP processore Intel Xeon</span><span class="sxs-lookup"><span data-stu-id="8c2eb-438">Intel Xeon Processor MP</span></span>

</dd> <dt>

<span id="AMD_AthlonXP_TM__Family"></span><span id="amd_athlonxp_tm__family"></span><span id="AMD_ATHLONXP_TM__FAMILY"></span>

<span data-ttu-id="8c2eb-439"><span id="AMD_AthlonXP_TM__Family"></span><span id="amd_athlonxp_tm__family"></span><span id="AMD_ATHLONXP_TM__FAMILY"></span>**Famiglia AMD AthlonXP (TM)** (182)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-439"><span id="AMD_AthlonXP_TM__Family"></span><span id="amd_athlonxp_tm__family"></span><span id="AMD_ATHLONXP_TM__FAMILY"></span>**AMD AthlonXP(TM) Family** (182)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-440">Famiglia AMD AthlonXP</span><span class="sxs-lookup"><span data-stu-id="8c2eb-440">AMD AthlonXP Family</span></span>

</dd> <dt>

<span id="AMD_AthlonMP_TM__Family"></span><span id="amd_athlonmp_tm__family"></span><span id="AMD_ATHLONMP_TM__FAMILY"></span>

<span data-ttu-id="8c2eb-441"><span id="AMD_AthlonMP_TM__Family"></span><span id="amd_athlonmp_tm__family"></span><span id="AMD_ATHLONMP_TM__FAMILY"></span>**Famiglia AMD AthlonMP (TM)** (183)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-441"><span id="AMD_AthlonMP_TM__Family"></span><span id="amd_athlonmp_tm__family"></span><span id="AMD_ATHLONMP_TM__FAMILY"></span>**AMD AthlonMP(TM) Family** (183)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-442">Famiglia AMD AthlonMP</span><span class="sxs-lookup"><span data-stu-id="8c2eb-442">AMD AthlonMP Family</span></span>

</dd> <dt>

<span id="Intel_R__Itanium_R__2"></span><span id="intel_r__itanium_r__2"></span><span id="INTEL_R__ITANIUM_R__2"></span>

<span data-ttu-id="8c2eb-443"><span id="Intel_R__Itanium_R__2"></span><span id="intel_r__itanium_r__2"></span><span id="INTEL_R__ITANIUM_R__2"></span>**Intel (r) Itanium (r) 2** (184)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-443"><span id="Intel_R__Itanium_R__2"></span><span id="intel_r__itanium_r__2"></span><span id="INTEL_R__ITANIUM_R__2"></span>**Intel(R) Itanium(R) 2** (184)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-444">Intel Itanium 2</span><span class="sxs-lookup"><span data-stu-id="8c2eb-444">Intel Itanium 2</span></span>

</dd> <dt>

<span id="Intel_Pentium_M_Processor"></span><span id="intel_pentium_m_processor"></span><span id="INTEL_PENTIUM_M_PROCESSOR"></span>

<span data-ttu-id="8c2eb-445"><span id="Intel_Pentium_M_Processor"></span><span id="intel_pentium_m_processor"></span><span id="INTEL_PENTIUM_M_PROCESSOR"></span>**Processore Intel Pentium M** (185)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-445"><span id="Intel_Pentium_M_Processor"></span><span id="intel_pentium_m_processor"></span><span id="INTEL_PENTIUM_M_PROCESSOR"></span>**Intel Pentium M Processor** (185)</span></span>


</dt> <dd></dd> <dt>

<span id="K7"></span><span id="k7"></span>

<span data-ttu-id="8c2eb-446"><span id="K7"></span><span id="k7"></span>**K7** (190)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-446"><span id="K7"></span><span id="k7"></span>**K7** (190)</span></span>


</dt> <dd></dd> <dt>

<span id="IBM390_Family"></span><span id="ibm390_family"></span><span id="IBM390_FAMILY"></span>

<span data-ttu-id="8c2eb-447"><span id="IBM390_Family"></span><span id="ibm390_family"></span><span id="IBM390_FAMILY"></span>**Famiglia IBM390** (200)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-447"><span id="IBM390_Family"></span><span id="ibm390_family"></span><span id="IBM390_FAMILY"></span>**IBM390 Family** (200)</span></span>


</dt> <dd></dd> <dt>

<span id="G4"></span><span id="g4"></span>

<span data-ttu-id="8c2eb-448"><span id="G4"></span><span id="g4"></span>**G4** (201)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-448"><span id="G4"></span><span id="g4"></span>**G4** (201)</span></span>


</dt> <dd></dd> <dt>

<span id="G5"></span><span id="g5"></span>

<span data-ttu-id="8c2eb-449"><span id="G5"></span><span id="g5"></span>**G5** (202)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-449"><span id="G5"></span><span id="g5"></span>**G5** (202)</span></span>


</dt> <dd></dd> <dt>

<span id="G6"></span><span id="g6"></span>

<span data-ttu-id="8c2eb-450"><span id="G6"></span><span id="g6"></span>**G6** (203)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-450"><span id="G6"></span><span id="g6"></span>**G6** (203)</span></span>


</dt> <dd></dd> <dt>

<span id="z_Architecture_base"></span><span id="z_architecture_base"></span><span id="Z_ARCHITECTURE_BASE"></span>

<span data-ttu-id="8c2eb-451"><span id="z_Architecture_base"></span><span id="z_architecture_base"></span><span id="Z_ARCHITECTURE_BASE"></span>**base z/Architecture** (204)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-451"><span id="z_Architecture_base"></span><span id="z_architecture_base"></span><span id="Z_ARCHITECTURE_BASE"></span>**z/Architecture base** (204)</span></span>


</dt> <dd></dd> <dt>

<span id="i860"></span><span id="I860"></span>

<span data-ttu-id="8c2eb-452"><span id="i860"></span><span id="I860"></span>**i860** (250)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-452"><span id="i860"></span><span id="I860"></span>**i860** (250)</span></span>


</dt> <dd></dd> <dt>

<span id="i960"></span><span id="I960"></span>

<span data-ttu-id="8c2eb-453"><span id="i960"></span><span id="I960"></span>**1960** (251)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-453"><span id="i960"></span><span id="I960"></span>**i960** (251)</span></span>


</dt> <dd></dd> <dt>

<span id="SH-3"></span><span id="sh-3"></span>

<span data-ttu-id="8c2eb-454"><span id="SH-3"></span><span id="sh-3"></span>**SH-3** (260)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-454"><span id="SH-3"></span><span id="sh-3"></span>**SH-3** (260)</span></span>


</dt> <dd></dd> <dt>

<span id="SH-4"></span><span id="sh-4"></span>

<span data-ttu-id="8c2eb-455"><span id="SH-4"></span><span id="sh-4"></span>**SH-4** (261)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-455"><span id="SH-4"></span><span id="sh-4"></span>**SH-4** (261)</span></span>


</dt> <dd></dd> <dt>

<span id="ARM"></span><span id="arm"></span>

<span data-ttu-id="8c2eb-456"><span id="ARM"></span><span id="arm"></span>**ARM** (280)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-456"><span id="ARM"></span><span id="arm"></span>**ARM** (280)</span></span>


</dt> <dd></dd> <dt>

<span id="StrongARM"></span><span id="strongarm"></span><span id="STRONGARM"></span>

<span data-ttu-id="8c2eb-457"><span id="StrongARM"></span><span id="strongarm"></span><span id="STRONGARM"></span>**StrongARM** (281)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-457"><span id="StrongARM"></span><span id="strongarm"></span><span id="STRONGARM"></span>**StrongARM** (281)</span></span>


</dt> <dd></dd> <dt>

<span id="6x86"></span><span id="6X86"></span>

<span data-ttu-id="8c2eb-458"><span id="6x86"></span><span id="6X86"></span>**6 x86** (300)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-458"><span id="6x86"></span><span id="6X86"></span>**6x86** (300)</span></span>


</dt> <dd></dd> <dt>

<span id="MediaGX"></span><span id="mediagx"></span><span id="MEDIAGX"></span>

<span data-ttu-id="8c2eb-459"><span id="MediaGX"></span><span id="mediagx"></span><span id="MEDIAGX"></span>**MediaGX** (301)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-459"><span id="MediaGX"></span><span id="mediagx"></span><span id="MEDIAGX"></span>**MediaGX** (301)</span></span>


</dt> <dd></dd> <dt>

<span id="MII"></span><span id="mii"></span>

<span data-ttu-id="8c2eb-460"><span id="MII"></span><span id="mii"></span>**Mii** (302)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-460"><span id="MII"></span><span id="mii"></span>**MII** (302)</span></span>


</dt> <dd></dd> <dt>

<span id="WinChip"></span><span id="winchip"></span><span id="WINCHIP"></span>

<span data-ttu-id="8c2eb-461"><span id="WinChip"></span><span id="winchip"></span><span id="WINCHIP"></span>**WinChip** (320)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-461"><span id="WinChip"></span><span id="winchip"></span><span id="WINCHIP"></span>**WinChip** (320)</span></span>


</dt> <dd></dd> <dt>

<span id="DSP"></span><span id="dsp"></span>

<span data-ttu-id="8c2eb-462"><span id="DSP"></span><span id="dsp"></span>**DSP** (350)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-462"><span id="DSP"></span><span id="dsp"></span>**DSP** (350)</span></span>


</dt> <dd></dd> <dt>

<span id="Video_Processor"></span><span id="video_processor"></span><span id="VIDEO_PROCESSOR"></span>

<span data-ttu-id="8c2eb-463"><span id="Video_Processor"></span><span id="video_processor"></span><span id="VIDEO_PROCESSOR"></span>**Processore video** (500)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-463"><span id="Video_Processor"></span><span id="video_processor"></span><span id="VIDEO_PROCESSOR"></span>**Video Processor** (500)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8c2eb-464">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-464">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2eb-465">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-465">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-466">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c2eb-466">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-467">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="8c2eb-467">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="8c2eb-468">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-468">Date and time the object was installed.</span></span> <span data-ttu-id="8c2eb-469">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-469">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="8c2eb-470">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8c2eb-470">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c2eb-471">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-471">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2eb-472">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-472">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-473">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c2eb-473">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c2eb-474">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-474">Last error code reported by the logical device.</span></span>

<span data-ttu-id="8c2eb-475">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8c2eb-475">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c2eb-476">**LoadPercentage**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-476">**LoadPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2eb-477">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-477">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-478">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c2eb-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-479">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-Resources-MIB. hrProcessorLoad "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" percentuale ")</span><span class="sxs-lookup"><span data-stu-id="8c2eb-479">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrProcessorLoad"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="8c2eb-480">Caricamento del processore, medio nell'ultimo minuto, in percentuale.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-480">Loading of the processor, averaged over the last minute, in a percentage.</span></span>

</dd> <dt>

<span data-ttu-id="8c2eb-481">**MaxClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-481">**MaxClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2eb-482">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-482">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-483">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c2eb-483">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-484">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Processore DMTF \| 006,5 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" megahertz ")</span><span class="sxs-lookup"><span data-stu-id="8c2eb-484">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Processor\|006.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span></span>
</dt> </dl>

<span data-ttu-id="8c2eb-485">Velocità massima (in megahertz) del processore.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-485">Maximum speed (in megahertz) of the processor.</span></span>

</dd> <dt>

<span data-ttu-id="8c2eb-486">**Nome**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-486">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2eb-487">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-488">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c2eb-488">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-489">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="8c2eb-489">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="8c2eb-490">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-490">Label by which the object is known.</span></span> <span data-ttu-id="8c2eb-491">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-491">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="8c2eb-492">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8c2eb-492">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c2eb-493">**OtherFamilyDescription**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-493">**OtherFamilyDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2eb-494">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-494">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-495">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c2eb-495">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-496">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ processore CIM**.**Famiglia**")</span><span class="sxs-lookup"><span data-stu-id="8c2eb-496">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Processor**.**Family**")</span></span>
</dt> </dl>

<span data-ttu-id="8c2eb-497">Descrizione del tipo di famiglia del processore.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-497">Description of the processor family type.</span></span> <span data-ttu-id="8c2eb-498">Questa proprietà viene utilizzata quando la proprietà **Family** è impostata su 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="8c2eb-498">This property is used when the **Family** property is set to 1 ("Other").</span></span> <span data-ttu-id="8c2eb-499">Questa stringa deve essere impostata su null se la proprietà **Family** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-499">This string should be set to null when the **Family** property is a value other than 1.</span></span>

</dd> <dt>

<span data-ttu-id="8c2eb-500">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-500">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2eb-501">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-501">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-502">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c2eb-502">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-503">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="8c2eb-503">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="8c2eb-504">Identificatore Plug and Play dispositivo del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-504">Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="8c2eb-505">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8c2eb-505">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="8c2eb-506">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="8c2eb-506">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="8c2eb-507">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-507">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2eb-508">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-508">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-509">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c2eb-509">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c2eb-510">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-510">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="8c2eb-511">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-511">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8c2eb-512"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-512"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="8c2eb-513"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-513"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8c2eb-514"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-514"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8c2eb-515"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-515"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-516">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-516">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="8c2eb-517"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-517"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-518">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-518">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="8c2eb-519"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-519"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-520">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-520">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="8c2eb-521">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-521">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="8c2eb-522">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="8c2eb-522">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="8c2eb-523"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-523"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-524">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="8c2eb-524">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="8c2eb-525"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-525"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-526">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-526">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8c2eb-527">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-527">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2eb-528">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-528">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-529">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c2eb-529">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c2eb-530">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-530">If **True**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="8c2eb-531">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="8c2eb-531">If **False**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="8c2eb-532">Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-532">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="8c2eb-533">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="8c2eb-533">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="8c2eb-534">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8c2eb-534">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c2eb-535">**Ruolo**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-535">**Role**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2eb-536">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-536">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-537">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c2eb-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c2eb-538">Stringa in formato libero che descrive il ruolo del processore.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-538">Free-form string that describes the role of the processor.</span></span> <span data-ttu-id="8c2eb-539">Ad esempio, "Central Processor" o "Math Processor".</span><span class="sxs-lookup"><span data-stu-id="8c2eb-539">For example, "Central Processor" or "Math Processor".</span></span>

</dd> <dt>

<span data-ttu-id="8c2eb-540">**Status**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-540">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2eb-541">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-542">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c2eb-542">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-543">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="8c2eb-543">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="8c2eb-544">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-544">Current status of the object.</span></span>

<span data-ttu-id="8c2eb-545">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8c2eb-545">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="8c2eb-546">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="8c2eb-546">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="8c2eb-547">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="8c2eb-547">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="8c2eb-548">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="8c2eb-548">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8c2eb-549">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="8c2eb-549">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8c2eb-550">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="8c2eb-550">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="8c2eb-551">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="8c2eb-551">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="8c2eb-552">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="8c2eb-552">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="8c2eb-553">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="8c2eb-553">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="8c2eb-554">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="8c2eb-554">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="8c2eb-555">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-555">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="8c2eb-556">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="8c2eb-556">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="8c2eb-557">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="8c2eb-557">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="8c2eb-558">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="8c2eb-558">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8c2eb-559">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-559">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2eb-560">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-560">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-561">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c2eb-561">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-562">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="8c2eb-562">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="8c2eb-563">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-563">State of the logical device.</span></span> <span data-ttu-id="8c2eb-564">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="8c2eb-564">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="8c2eb-565">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8c2eb-565">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8c2eb-566">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-566">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8c2eb-567">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-567">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8c2eb-568">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-568">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8c2eb-569">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-569">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="8c2eb-570">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-570">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8c2eb-571">**Esecuzione di istruzioni**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-571">**Stepping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2eb-572">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-572">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-573">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c2eb-573">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-574">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ processore CIM**.**Famiglia**")</span><span class="sxs-lookup"><span data-stu-id="8c2eb-574">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Processor**.**Family**")</span></span>
</dt> </dl>

<span data-ttu-id="8c2eb-575">Stringa in formato libero che indica il livello di revisione del processore all'interno della famiglia di processori.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-575">Free-form string that indicates the revision level of the processor within the processor family.</span></span>

</dd> <dt>

<span data-ttu-id="8c2eb-576">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-576">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2eb-577">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-578">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c2eb-578">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-579">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-579">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8c2eb-580">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-580">Scoping system's creation class name.</span></span>

<span data-ttu-id="8c2eb-581">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8c2eb-581">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c2eb-582">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-582">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2eb-583">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-583">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-584">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c2eb-584">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-585">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-585">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8c2eb-586">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-586">Scoping system's name.</span></span>

<span data-ttu-id="8c2eb-587">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8c2eb-587">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c2eb-588">**UniqueId**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-588">**UniqueId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2eb-589">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-590">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c2eb-590">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c2eb-591">Identificatore univoco globale per il processore.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-591">Globally unique identifier for the processor.</span></span> <span data-ttu-id="8c2eb-592">Questo identificatore può essere univoco solo all'interno di una famiglia di processori.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-592">This identifier can only be unique within a processor family.</span></span>

</dd> <dt>

<span data-ttu-id="8c2eb-593">**UpgradeMethod**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-593">**UpgradeMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2eb-594">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-594">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-595">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c2eb-595">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c2eb-596">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Processore DMTF \| 006,7 ")</span><span class="sxs-lookup"><span data-stu-id="8c2eb-596">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Processor\|006.7")</span></span>
</dt> </dl>

<span data-ttu-id="8c2eb-597">Informazioni sul socket della CPU, che includono i dati su come aggiornare il processore (se sono supportati gli aggiornamenti).</span><span class="sxs-lookup"><span data-stu-id="8c2eb-597">CPU socket information, which includes data on how to upgrade the processor (if upgrades are supported).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8c2eb-598"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-598"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8c2eb-599"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-599"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Daughter_Board"></span><span id="daughter_board"></span><span id="DAUGHTER_BOARD"></span>

<span data-ttu-id="8c2eb-600"><span id="Daughter_Board"></span><span id="daughter_board"></span><span id="DAUGHTER_BOARD"></span>**Scheda figlia** (3)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-600"><span id="Daughter_Board"></span><span id="daughter_board"></span><span id="DAUGHTER_BOARD"></span>**Daughter Board** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ZIF_Socket"></span><span id="zif_socket"></span><span id="ZIF_SOCKET"></span>

<span data-ttu-id="8c2eb-601"><span id="ZIF_Socket"></span><span id="zif_socket"></span><span id="ZIF_SOCKET"></span>**Socket** se (4)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-601"><span id="ZIF_Socket"></span><span id="zif_socket"></span><span id="ZIF_SOCKET"></span>**ZIF Socket** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Replacement_Piggy_Back"></span><span id="replacement_piggy_back"></span><span id="REPLACEMENT_PIGGY_BACK"></span>

<span data-ttu-id="8c2eb-602"><span id="Replacement_Piggy_Back"></span><span id="replacement_piggy_back"></span><span id="REPLACEMENT_PIGGY_BACK"></span>**Sostituzione/piggy indietro** (5)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-602"><span id="Replacement_Piggy_Back"></span><span id="replacement_piggy_back"></span><span id="REPLACEMENT_PIGGY_BACK"></span>**Replacement/Piggy Back** (5)</span></span>


</dt> <dd>

<span data-ttu-id="8c2eb-603">Sostituzione o Piggy Back</span><span class="sxs-lookup"><span data-stu-id="8c2eb-603">Replacement or piggy back</span></span>

</dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="8c2eb-604"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Nessuno** (6)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-604"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="LIF_Socket"></span><span id="lif_socket"></span><span id="LIF_SOCKET"></span>

<span data-ttu-id="8c2eb-605"><span id="LIF_Socket"></span><span id="lif_socket"></span><span id="LIF_SOCKET"></span>**Socket LIF** (7)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-605"><span id="LIF_Socket"></span><span id="lif_socket"></span><span id="LIF_SOCKET"></span>**LIF Socket** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Slot_1"></span><span id="slot_1"></span><span id="SLOT_1"></span>

<span data-ttu-id="8c2eb-606"><span id="Slot_1"></span><span id="slot_1"></span><span id="SLOT_1"></span>**Slot 1** (8)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-606"><span id="Slot_1"></span><span id="slot_1"></span><span id="SLOT_1"></span>**Slot 1** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Slot_2"></span><span id="slot_2"></span><span id="SLOT_2"></span>

<span data-ttu-id="8c2eb-607"><span id="Slot_2"></span><span id="slot_2"></span><span id="SLOT_2"></span>**Slot 2** (9)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-607"><span id="Slot_2"></span><span id="slot_2"></span><span id="SLOT_2"></span>**Slot 2** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="370_Pin_Socket"></span><span id="370_pin_socket"></span><span id="370_PIN_SOCKET"></span>

<span data-ttu-id="8c2eb-608"><span id="370_Pin_Socket"></span><span id="370_pin_socket"></span><span id="370_PIN_SOCKET"></span>**socket Pin 370** (10)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-608"><span id="370_Pin_Socket"></span><span id="370_pin_socket"></span><span id="370_PIN_SOCKET"></span>**370 Pin Socket** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Slot_A"></span><span id="slot_a"></span><span id="SLOT_A"></span>

<span data-ttu-id="8c2eb-609"><span id="Slot_A"></span><span id="slot_a"></span><span id="SLOT_A"></span>**Slot A** (11)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-609"><span id="Slot_A"></span><span id="slot_a"></span><span id="SLOT_A"></span>**Slot A** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Slot_M"></span><span id="slot_m"></span><span id="SLOT_M"></span>

<span data-ttu-id="8c2eb-610"><span id="Slot_M"></span><span id="slot_m"></span><span id="SLOT_M"></span>**Slot M** (12)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-610"><span id="Slot_M"></span><span id="slot_m"></span><span id="SLOT_M"></span>**Slot M** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_423"></span><span id="socket_423"></span><span id="SOCKET_423"></span>

<span data-ttu-id="8c2eb-611"><span id="Socket_423"></span><span id="socket_423"></span><span id="SOCKET_423"></span>**Socket 423** (13)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-611"><span id="Socket_423"></span><span id="socket_423"></span><span id="SOCKET_423"></span>**Socket 423** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_A__Socket_462_"></span><span id="socket_a__socket_462_"></span><span id="SOCKET_A__SOCKET_462_"></span>

<span data-ttu-id="8c2eb-612"><span id="Socket_A__Socket_462_"></span><span id="socket_a__socket_462_"></span><span id="SOCKET_A__SOCKET_462_"></span>**Socket A (socket 462)** (14)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-612"><span id="Socket_A__Socket_462_"></span><span id="socket_a__socket_462_"></span><span id="SOCKET_A__SOCKET_462_"></span>**Socket A (Socket 462)** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_478"></span><span id="socket_478"></span><span id="SOCKET_478"></span>

<span data-ttu-id="8c2eb-613"><span id="Socket_478"></span><span id="socket_478"></span><span id="SOCKET_478"></span>**Socket 478** (15)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-613"><span id="Socket_478"></span><span id="socket_478"></span><span id="SOCKET_478"></span>**Socket 478** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_754"></span><span id="socket_754"></span><span id="SOCKET_754"></span>

<span data-ttu-id="8c2eb-614"><span id="Socket_754"></span><span id="socket_754"></span><span id="SOCKET_754"></span>**Socket 754** (16)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-614"><span id="Socket_754"></span><span id="socket_754"></span><span id="SOCKET_754"></span>**Socket 754** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_940"></span><span id="socket_940"></span><span id="SOCKET_940"></span>

<span data-ttu-id="8c2eb-615"><span id="Socket_940"></span><span id="socket_940"></span><span id="SOCKET_940"></span>**Socket 940** (17)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-615"><span id="Socket_940"></span><span id="socket_940"></span><span id="SOCKET_940"></span>**Socket 940** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_939"></span><span id="socket_939"></span><span id="SOCKET_939"></span>

<span data-ttu-id="8c2eb-616"><span id="Socket_939"></span><span id="socket_939"></span><span id="SOCKET_939"></span>**Socket 939** (18)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-616"><span id="Socket_939"></span><span id="socket_939"></span><span id="SOCKET_939"></span>**Socket 939** (18)</span></span>


<span data-ttu-id="8c2eb-617"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="8c2eb-617"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="8c2eb-618">Commenti</span><span class="sxs-lookup"><span data-stu-id="8c2eb-618">Remarks</span></span>

<span data-ttu-id="8c2eb-619">La classe del **\_ processore CIM** è derivata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8c2eb-619">The **CIM\_Processor** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="8c2eb-620">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-620">WMI does not implement this class.</span></span> <span data-ttu-id="8c2eb-621">Per le classi WMI derivate dal **\_ processore CIM**, vedere [classi Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="8c2eb-621">For WMI classes derived from **CIM\_Processor**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="8c2eb-622">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-622">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8c2eb-623">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-623">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c2eb-624">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8c2eb-624">Requirements</span></span>



| <span data-ttu-id="8c2eb-625">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c2eb-625">Requirement</span></span> | <span data-ttu-id="8c2eb-626">Valore</span><span class="sxs-lookup"><span data-stu-id="8c2eb-626">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c2eb-627">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c2eb-627">Minimum supported client</span></span><br/> | <span data-ttu-id="8c2eb-628">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8c2eb-628">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8c2eb-629">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c2eb-629">Minimum supported server</span></span><br/> | <span data-ttu-id="8c2eb-630">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8c2eb-630">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8c2eb-631">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8c2eb-631">Namespace</span></span><br/>                | <span data-ttu-id="8c2eb-632">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="8c2eb-632">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8c2eb-633">MOF</span><span class="sxs-lookup"><span data-stu-id="8c2eb-633">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8c2eb-634"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8c2eb-634"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8c2eb-635">DLL</span><span class="sxs-lookup"><span data-stu-id="8c2eb-635">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c2eb-636"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c2eb-636"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c2eb-637">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8c2eb-637">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c2eb-638">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="8c2eb-638">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 


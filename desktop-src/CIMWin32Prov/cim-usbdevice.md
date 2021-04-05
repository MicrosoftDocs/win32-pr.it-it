---
description: La \_ classe CIM usbdevice rappresenta le caratteristiche di gestione di un dispositivo USB.
ms.assetid: 0ff39701-826a-434b-a628-0af586600a80
ms.tgt_platform: multiple
title: Classe CIM_USBDevice (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBDevice
- CIM_USBDevice.Availability
- CIM_USBDevice.Caption
- CIM_USBDevice.ClassCode
- CIM_USBDevice.ConfigManagerErrorCode
- CIM_USBDevice.ConfigManagerUserConfig
- CIM_USBDevice.CreationClassName
- CIM_USBDevice.CurrentAlternateSettings
- CIM_USBDevice.CurrentConfigValue
- CIM_USBDevice.Description
- CIM_USBDevice.DeviceID
- CIM_USBDevice.ErrorCleared
- CIM_USBDevice.ErrorDescription
- CIM_USBDevice.InstallDate
- CIM_USBDevice.LastErrorCode
- CIM_USBDevice.Name
- CIM_USBDevice.NumberOfConfigs
- CIM_USBDevice.PNPDeviceID
- CIM_USBDevice.PowerManagementCapabilities
- CIM_USBDevice.PowerManagementSupported
- CIM_USBDevice.ProtocolCode
- CIM_USBDevice.Status
- CIM_USBDevice.StatusInfo
- CIM_USBDevice.SubclassCode
- CIM_USBDevice.SystemCreationClassName
- CIM_USBDevice.SystemName
- CIM_USBDevice.USBVersion
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 21b927980716d4ee7ee2e22a352c5c3b34b363dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125823"
---
# <a name="cim_usbdevice-class-cimwin32-wmi-providers"></a><span data-ttu-id="f3951-103">Classe CIM_USBDevice (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="f3951-103">CIM_USBDevice class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="f3951-104">La classe **CIM \_ usbdevice** rappresenta le caratteristiche di gestione di un dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="f3951-104">The **CIM\_USBDevice** class represents the management characteristics of a USB device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f3951-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="f3951-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f3951-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f3951-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f3951-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f3951-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="f3951-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="f3951-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3951-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f3951-109">Syntax</span></span>

``` syntax
[AMENDMENT]
class CIM_USBDevice : CIM_LogicalDevice
{
  uint16   Availability;
  string   Caption;
  uint8    ClassCode;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint8    CurrentAlternateSettings[];
  uint8    CurrentConfigValue;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint8    NumberOfConfigs;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint8    ProtocolCode;
  string   Status;
  uint16   StatusInfo;
  uint8    SubclassCode;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   USBVersion;
};
```

## <a name="members"></a><span data-ttu-id="f3951-110">Members</span><span class="sxs-lookup"><span data-stu-id="f3951-110">Members</span></span>

<span data-ttu-id="f3951-111">La classe **CIM \_ usbdevice** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f3951-111">The **CIM\_USBDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="f3951-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="f3951-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="f3951-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f3951-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f3951-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="f3951-114">Methods</span></span>

<span data-ttu-id="f3951-115">La classe **CIM \_ usbdevice** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="f3951-115">The **CIM\_USBDevice** class has these methods.</span></span>



| <span data-ttu-id="f3951-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="f3951-116">Method</span></span>                                                               | <span data-ttu-id="f3951-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3951-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f3951-118">**GetDescriptor**</span><span class="sxs-lookup"><span data-stu-id="f3951-118">**GetDescriptor**</span></span>](getdescriptor-method-in-class-cim-usbdevice.md) | <span data-ttu-id="f3951-119">Restituisce il descrittore del dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="f3951-119">Returns the USB device descriptor.</span></span> <span data-ttu-id="f3951-120">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="f3951-120">Not implemented by WMI.</span></span><br/>                                                                    |
| [<span data-ttu-id="f3951-121">**Reset**</span><span class="sxs-lookup"><span data-stu-id="f3951-121">**Reset**</span></span>](reset-method-in-class-cim-usbdevice.md)                 | <span data-ttu-id="f3951-122">Richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="f3951-122">Requests a reset of the logical device.</span></span> <span data-ttu-id="f3951-123">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="f3951-123">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="f3951-124">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="f3951-124">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-usbdevice.md) | <span data-ttu-id="f3951-125">Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="f3951-125">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="f3951-126">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="f3951-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f3951-127">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f3951-127">Properties</span></span>

<span data-ttu-id="f3951-128">La classe **CIM \_ usbdevice** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f3951-128">The **CIM\_USBDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f3951-129">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="f3951-129">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3951-130">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f3951-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f3951-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3951-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3951-132">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="f3951-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="f3951-133">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3951-133">Availability and status of the device.</span></span>

<span data-ttu-id="f3951-134">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f3951-134">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f3951-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="f3951-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f3951-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="f3951-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="f3951-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="f3951-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-138">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="f3951-138">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="f3951-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="f3951-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="f3951-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="f3951-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f3951-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="f3951-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="f3951-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="f3951-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="f3951-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="f3951-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="f3951-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="f3951-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f3951-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="f3951-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="f3951-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="f3951-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="f3951-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="f3951-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="f3951-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="f3951-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-149">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="f3951-149">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="f3951-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="f3951-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-151">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="f3951-151">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="f3951-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="f3951-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-153">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="f3951-153">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="f3951-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="f3951-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="f3951-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="f3951-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-156">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="f3951-156">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="f3951-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="f3951-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-158">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="f3951-158">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="f3951-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="f3951-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-160">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="f3951-160">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="f3951-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="f3951-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-162">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="f3951-162">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="f3951-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="f3951-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-164">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="f3951-164">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f3951-165">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="f3951-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3951-166">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f3951-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3951-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3951-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3951-168">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="f3951-168">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f3951-169">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f3951-169">Short textual description of the object.</span></span>

<span data-ttu-id="f3951-170">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f3951-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3951-171">**ClassCode**</span><span class="sxs-lookup"><span data-stu-id="f3951-171">**ClassCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3951-172">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="f3951-172">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="f3951-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3951-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3951-174">Codice della classe USB.</span><span class="sxs-lookup"><span data-stu-id="f3951-174">USB class code.</span></span>

</dd> <dt>

<span data-ttu-id="f3951-175">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="f3951-175">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3951-176">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3951-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3951-177">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3951-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3951-178">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f3951-178">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f3951-179">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="f3951-179">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="f3951-180">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f3951-180">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="f3951-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="f3951-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="f3951-182"> (0)</span><span class="sxs-lookup"><span data-stu-id="f3951-182">(0)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-183">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="f3951-183">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="f3951-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="f3951-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="f3951-185">(1)</span><span class="sxs-lookup"><span data-stu-id="f3951-185">(1)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-186">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="f3951-186">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f3951-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f3951-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="f3951-188">(2)</span><span class="sxs-lookup"><span data-stu-id="f3951-188">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="f3951-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="f3951-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="f3951-190">(3)</span><span class="sxs-lookup"><span data-stu-id="f3951-190">(3)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-191">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="f3951-191">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="f3951-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="f3951-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="f3951-193">(4)</span><span class="sxs-lookup"><span data-stu-id="f3951-193">(4)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-194">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="f3951-194">Device is not working properly.</span></span> <span data-ttu-id="f3951-195">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="f3951-195">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="f3951-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="f3951-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="f3951-197">(5)</span><span class="sxs-lookup"><span data-stu-id="f3951-197">(5)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-198">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="f3951-198">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="f3951-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="f3951-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="f3951-200"> (6)</span><span class="sxs-lookup"><span data-stu-id="f3951-200">(6)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-201">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="f3951-201">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="f3951-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="f3951-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="f3951-203">(7)</span><span class="sxs-lookup"><span data-stu-id="f3951-203">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="f3951-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="f3951-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="f3951-205">(8)</span><span class="sxs-lookup"><span data-stu-id="f3951-205">(8)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-206">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="f3951-206">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="f3951-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="f3951-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="f3951-208">(9)</span><span class="sxs-lookup"><span data-stu-id="f3951-208">(9)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-209">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="f3951-209">Device is not working properly.</span></span> <span data-ttu-id="f3951-210">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3951-210">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="f3951-211"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f3951-211"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="f3951-212">(10)</span><span class="sxs-lookup"><span data-stu-id="f3951-212">(10)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-213">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3951-213">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="f3951-214"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f3951-214"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="f3951-215">(11)</span><span class="sxs-lookup"><span data-stu-id="f3951-215">(11)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-216">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3951-216">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="f3951-217"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="f3951-217"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="f3951-218">12</span><span class="sxs-lookup"><span data-stu-id="f3951-218">(12)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-219">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="f3951-219">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="f3951-220"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f3951-220"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="f3951-221">(13)</span><span class="sxs-lookup"><span data-stu-id="f3951-221">(13)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-222">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3951-222">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="f3951-223"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="f3951-223"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="f3951-224">(14)</span><span class="sxs-lookup"><span data-stu-id="f3951-224">(14)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-225">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="f3951-225">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="f3951-226"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="f3951-226"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="f3951-227">(15)</span><span class="sxs-lookup"><span data-stu-id="f3951-227">(15)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-228">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="f3951-228">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="f3951-229"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f3951-229"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="f3951-230">(16)</span><span class="sxs-lookup"><span data-stu-id="f3951-230">(16)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-231">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3951-231">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="f3951-232"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="f3951-232"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="f3951-233">(17)</span><span class="sxs-lookup"><span data-stu-id="f3951-233">(17)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-234">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="f3951-234">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f3951-235"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f3951-235"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="f3951-236">(18)</span><span class="sxs-lookup"><span data-stu-id="f3951-236">(18)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-237">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3951-237">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="f3951-238"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="f3951-238"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="f3951-239">(19)</span><span class="sxs-lookup"><span data-stu-id="f3951-239">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="f3951-240"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="f3951-240"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="f3951-241">(20)</span><span class="sxs-lookup"><span data-stu-id="f3951-241">(20)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-242">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="f3951-242">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="f3951-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f3951-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="f3951-244">(21)</span><span class="sxs-lookup"><span data-stu-id="f3951-244">(21)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-245">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="f3951-245">System failure.</span></span> <span data-ttu-id="f3951-246">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="f3951-246">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="f3951-247">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3951-247">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="f3951-248"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="f3951-248"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="f3951-249">(22)</span><span class="sxs-lookup"><span data-stu-id="f3951-249">(22)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-250">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="f3951-250">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="f3951-251"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="f3951-251"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="f3951-252">(23)</span><span class="sxs-lookup"><span data-stu-id="f3951-252">(23)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-253">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="f3951-253">System failure.</span></span> <span data-ttu-id="f3951-254">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="f3951-254">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="f3951-255"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="f3951-255"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="f3951-256">(24)</span><span class="sxs-lookup"><span data-stu-id="f3951-256">(24)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-257">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="f3951-257">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="f3951-258"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f3951-258"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="f3951-259">(25)</span><span class="sxs-lookup"><span data-stu-id="f3951-259">(25)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-260">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3951-260">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="f3951-261"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f3951-261"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="f3951-262">(26)</span><span class="sxs-lookup"><span data-stu-id="f3951-262">(26)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-263">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3951-263">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="f3951-264"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="f3951-264"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="f3951-265">(27)</span><span class="sxs-lookup"><span data-stu-id="f3951-265">(27)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-266">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="f3951-266">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="f3951-267"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="f3951-267"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="f3951-268">(28)</span><span class="sxs-lookup"><span data-stu-id="f3951-268">(28)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-269">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="f3951-269">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="f3951-270"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="f3951-270"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="f3951-271">(29)</span><span class="sxs-lookup"><span data-stu-id="f3951-271">(29)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-272">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="f3951-272">Device is disabled.</span></span> <span data-ttu-id="f3951-273">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="f3951-273">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="f3951-274"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f3951-274"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="f3951-275">(30)</span><span class="sxs-lookup"><span data-stu-id="f3951-275">(30)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-276">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3951-276">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f3951-277"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f3951-277"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="f3951-278">31</span><span class="sxs-lookup"><span data-stu-id="f3951-278">(31)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-279">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="f3951-279">Device is not working properly.</span></span> <span data-ttu-id="f3951-280">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="f3951-280">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f3951-281">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="f3951-281">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3951-282">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f3951-282">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f3951-283">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3951-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3951-284">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f3951-284">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f3951-285">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="f3951-285">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="f3951-286">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f3951-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3951-287">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f3951-287">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3951-288">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f3951-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3951-289">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3951-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3951-290">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f3951-290">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f3951-291">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="f3951-291">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="f3951-292">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="f3951-292">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="f3951-293">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f3951-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3951-294">**CurrentAlternateSettings**</span><span class="sxs-lookup"><span data-stu-id="f3951-294">**CurrentAlternateSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3951-295">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="f3951-295">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="f3951-296">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3951-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3951-297">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ usbdevice**.**CurrentConfigValue**")</span><span class="sxs-lookup"><span data-stu-id="f3951-297">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_USBDevice**.**CurrentConfigValue**")</span></span>
</dt> </dl>

<span data-ttu-id="f3951-298">Impostazioni alternative USB per ogni interfaccia della configurazione attualmente selezionata (indicata dalla proprietà **CurrentConfigValue** ).</span><span class="sxs-lookup"><span data-stu-id="f3951-298">USB alternate settings for each interface in the currently selected configuration (indicated by the **CurrentConfigValue** property).</span></span> <span data-ttu-id="f3951-299">Questa matrice include una voce per ogni interfaccia della configurazione.</span><span class="sxs-lookup"><span data-stu-id="f3951-299">This array has one entry for each interface in the configuration.</span></span> <span data-ttu-id="f3951-300">Se la proprietà **CurrentConfigValue** ha un valore pari a 0 (zero), che indica che il dispositivo non è configurato, la matrice non è definita.</span><span class="sxs-lookup"><span data-stu-id="f3951-300">If the **CurrentConfigValue** property has a value of 0 (zero), which indicates that the device is not configured, the array is undefined.</span></span> <span data-ttu-id="f3951-301">Per ulteriori informazioni sull'analisi di questa stringa ottetto, vedere la specifica USB.</span><span class="sxs-lookup"><span data-stu-id="f3951-301">For more information about parsing this octet string, see the USB specification.</span></span>

</dd> <dt>

<span data-ttu-id="f3951-302">**CurrentConfigValue**</span><span class="sxs-lookup"><span data-stu-id="f3951-302">**CurrentConfigValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3951-303">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="f3951-303">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="f3951-304">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3951-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3951-305">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ usbdevice**.**CurrentAlternateSettings**")</span><span class="sxs-lookup"><span data-stu-id="f3951-305">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_USBDevice**.**CurrentAlternateSettings**")</span></span>
</dt> </dl>

<span data-ttu-id="f3951-306">Configurazione attualmente selezionata per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3951-306">Configuration currently selected for the device.</span></span> <span data-ttu-id="f3951-307">Se il valore è 0 (zero), il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="f3951-307">If the value is 0 (zero), the device is unconfigured.</span></span>

</dd> <dt>

<span data-ttu-id="f3951-308">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="f3951-308">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3951-309">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f3951-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3951-310">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3951-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3951-311">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="f3951-311">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f3951-312">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f3951-312">Textual description of the object.</span></span>

<span data-ttu-id="f3951-313">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f3951-313">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3951-314">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="f3951-314">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3951-315">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f3951-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3951-316">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3951-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3951-317">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f3951-317">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f3951-318">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="f3951-318">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="f3951-319">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f3951-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3951-320">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="f3951-320">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3951-321">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f3951-321">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f3951-322">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3951-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3951-323">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="f3951-323">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="f3951-324">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f3951-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3951-325">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="f3951-325">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3951-326">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f3951-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3951-327">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3951-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3951-328">Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.</span><span class="sxs-lookup"><span data-stu-id="f3951-328">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="f3951-329">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f3951-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3951-330">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f3951-330">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3951-331">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f3951-331">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f3951-332">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3951-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3951-333">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="f3951-333">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f3951-334">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f3951-334">Date and time the object was installed.</span></span> <span data-ttu-id="f3951-335">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="f3951-335">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="f3951-336">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f3951-336">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3951-337">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="f3951-337">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3951-338">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3951-338">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3951-339">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3951-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3951-340">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="f3951-340">Last error code reported by the logical device.</span></span>

<span data-ttu-id="f3951-341">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f3951-341">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3951-342">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f3951-342">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3951-343">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f3951-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3951-344">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3951-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3951-345">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="f3951-345">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="f3951-346">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="f3951-346">Label by which the object is known.</span></span> <span data-ttu-id="f3951-347">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="f3951-347">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="f3951-348">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f3951-348">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3951-349">**NumberOfConfigs**</span><span class="sxs-lookup"><span data-stu-id="f3951-349">**NumberOfConfigs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3951-350">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="f3951-350">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="f3951-351">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3951-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3951-352">Numero di configurazioni del dispositivo definite per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3951-352">Number of device configurations that are defined for the device.</span></span>

</dd> <dt>

<span data-ttu-id="f3951-353">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="f3951-353">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3951-354">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f3951-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3951-355">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3951-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3951-356">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f3951-356">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f3951-357">Win32 Plug and Play identificatore dispositivo del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="f3951-357">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="f3951-358">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f3951-358">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="f3951-359">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="f3951-359">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="f3951-360">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="f3951-360">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3951-361">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f3951-361">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f3951-362">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3951-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3951-363">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="f3951-363">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="f3951-364">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="f3951-364">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f3951-365"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="f3951-365"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="f3951-366"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="f3951-366"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f3951-367"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="f3951-367"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f3951-368"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="f3951-368"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-369">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="f3951-369">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="f3951-370"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="f3951-370"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-371">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="f3951-371">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="f3951-372"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="f3951-372"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-373">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="f3951-373">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="f3951-374">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="f3951-374">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="f3951-375">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="f3951-375">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="f3951-376"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="f3951-376"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-377">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="f3951-377">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="f3951-378"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="f3951-378"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="f3951-379">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="f3951-379">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f3951-380">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="f3951-380">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3951-381">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f3951-381">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f3951-382">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3951-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3951-383">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="f3951-383">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="f3951-384">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="f3951-384">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="f3951-385">Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="f3951-385">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="f3951-386">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="f3951-386">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="f3951-387">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f3951-387">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3951-388">**ProtocolCode**</span><span class="sxs-lookup"><span data-stu-id="f3951-388">**ProtocolCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3951-389">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="f3951-389">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="f3951-390">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3951-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3951-391">Codice di protocollo USB.</span><span class="sxs-lookup"><span data-stu-id="f3951-391">USB protocol code.</span></span>

</dd> <dt>

<span data-ttu-id="f3951-392">**Status**</span><span class="sxs-lookup"><span data-stu-id="f3951-392">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3951-393">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f3951-393">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3951-394">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3951-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3951-395">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="f3951-395">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f3951-396">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f3951-396">Current status of the object.</span></span> <span data-ttu-id="f3951-397">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f3951-397">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f3951-398">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="f3951-398">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f3951-399">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="f3951-399">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f3951-400">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="f3951-400">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f3951-401">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="f3951-401">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f3951-402">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="f3951-402">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f3951-403">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="f3951-403">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f3951-404">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="f3951-404">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f3951-405">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="f3951-405">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f3951-406">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="f3951-406">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f3951-407">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="f3951-407">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f3951-408">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="f3951-408">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f3951-409">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="f3951-409">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f3951-410">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="f3951-410">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f3951-411">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="f3951-411">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3951-412">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f3951-412">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f3951-413">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3951-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3951-414">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="f3951-414">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="f3951-415">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="f3951-415">State of the logical device.</span></span> <span data-ttu-id="f3951-416">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="f3951-416">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="f3951-417">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f3951-417">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f3951-418">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="f3951-418">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f3951-419">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="f3951-419">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f3951-420">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="f3951-420">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f3951-421">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="f3951-421">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f3951-422">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="f3951-422">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f3951-423">**SubclassCode**</span><span class="sxs-lookup"><span data-stu-id="f3951-423">**SubclassCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3951-424">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="f3951-424">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="f3951-425">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3951-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3951-426">Codice della sottoclasse USB.</span><span class="sxs-lookup"><span data-stu-id="f3951-426">USB subclass code.</span></span>

</dd> <dt>

<span data-ttu-id="f3951-427">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f3951-427">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3951-428">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f3951-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3951-429">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3951-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3951-430">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f3951-430">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f3951-431">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="f3951-431">Scoping system's creation class name.</span></span>

<span data-ttu-id="f3951-432">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f3951-432">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3951-433">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="f3951-433">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3951-434">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f3951-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3951-435">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3951-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3951-436">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f3951-436">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f3951-437">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="f3951-437">Scoping system's name.</span></span>

<span data-ttu-id="f3951-438">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f3951-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3951-439">**USBVersion**</span><span class="sxs-lookup"><span data-stu-id="f3951-439">**USBVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3951-440">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f3951-440">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f3951-441">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3951-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3951-442">Versione USB più recente supportata dal dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="f3951-442">Latest USB version supported by the USB device.</span></span> <span data-ttu-id="f3951-443">Questa proprietà viene espressa come un separatore decimale (BCD) con codifica binaria in cui un separatore decimale è implicito tra la seconda e la terza cifra.</span><span class="sxs-lookup"><span data-stu-id="f3951-443">This property is expressed as a binary-coded decimal (BCD) where a decimal point is implied between the second and third digits.</span></span> <span data-ttu-id="f3951-444">Ad esempio, il valore 0x201 indica che la versione 2,01 è supportata.</span><span class="sxs-lookup"><span data-stu-id="f3951-444">For example, a value of 0x201 indicates that version 2.01 is supported.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f3951-445">Commenti</span><span class="sxs-lookup"><span data-stu-id="f3951-445">Remarks</span></span>

<span data-ttu-id="f3951-446">La classe **CIM \_ usbdevice** è derivata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f3951-446">The **CIM\_USBDevice** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="f3951-447">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="f3951-447">WMI does not implement this class.</span></span> <span data-ttu-id="f3951-448">Per le classi WMI che implementano **CIM \_ usbdevice**, vedere [classi Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f3951-448">For WMI classes that implement **CIM\_USBDevice**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="f3951-449">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="f3951-449">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f3951-450">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="f3951-450">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3951-451">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3951-451">Requirements</span></span>



| <span data-ttu-id="f3951-452">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3951-452">Requirement</span></span> | <span data-ttu-id="f3951-453">Valore</span><span class="sxs-lookup"><span data-stu-id="f3951-453">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3951-454">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3951-454">Minimum supported client</span></span><br/> | <span data-ttu-id="f3951-455">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f3951-455">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f3951-456">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3951-456">Minimum supported server</span></span><br/> | <span data-ttu-id="f3951-457">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f3951-457">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f3951-458">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f3951-458">Namespace</span></span><br/>                | <span data-ttu-id="f3951-459">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="f3951-459">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f3951-460">MOF</span><span class="sxs-lookup"><span data-stu-id="f3951-460">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f3951-461"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f3951-461"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f3951-462">DLL</span><span class="sxs-lookup"><span data-stu-id="f3951-462">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3951-463"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3951-463"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3951-464">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3951-464">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3951-465">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="f3951-465">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 


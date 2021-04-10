---
description: La \_ classe WMI InfraredDevice Win32 rappresenta le funzionalità e la gestione di un dispositivo a infrarossi.
ms.assetid: f129e7ce-4d50-44d0-877c-968f4865b781
ms.tgt_platform: multiple
title: Classe Win32_InfraredDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_InfraredDevice
- Win32_InfraredDevice.Reset
- Win32_InfraredDevice.SetPowerState
- Win32_InfraredDevice.Availability
- Win32_InfraredDevice.Caption
- Win32_InfraredDevice.ConfigManagerErrorCode
- Win32_InfraredDevice.ConfigManagerUserConfig
- Win32_InfraredDevice.CreationClassName
- Win32_InfraredDevice.Description
- Win32_InfraredDevice.DeviceID
- Win32_InfraredDevice.ErrorCleared
- Win32_InfraredDevice.ErrorDescription
- Win32_InfraredDevice.InstallDate
- Win32_InfraredDevice.LastErrorCode
- Win32_InfraredDevice.Manufacturer
- Win32_InfraredDevice.MaxNumberControlled
- Win32_InfraredDevice.Name
- Win32_InfraredDevice.PNPDeviceID
- Win32_InfraredDevice.PowerManagementCapabilities
- Win32_InfraredDevice.PowerManagementSupported
- Win32_InfraredDevice.ProtocolSupported
- Win32_InfraredDevice.Status
- Win32_InfraredDevice.StatusInfo
- Win32_InfraredDevice.SystemCreationClassName
- Win32_InfraredDevice.SystemName
- Win32_InfraredDevice.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8a71946eeda3a8c304e1a6dda0ab2cc92e7b4489
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126258"
---
# <a name="win32_infrareddevice-class"></a><span data-ttu-id="b78bb-103">Win32 \_ InfraredDevice (classe)</span><span class="sxs-lookup"><span data-stu-id="b78bb-103">Win32\_InfraredDevice class</span></span>

<span data-ttu-id="b78bb-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ InfraredDevice Win32** rappresenta le funzionalità e la gestione di un dispositivo a infrarossi.</span><span class="sxs-lookup"><span data-stu-id="b78bb-104">The **Win32\_InfraredDevice** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the capabilities and management of an infrared device.</span></span>

<span data-ttu-id="b78bb-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b78bb-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b78bb-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="b78bb-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b78bb-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b78bb-107">Syntax</span></span>

``` syntax
[dynamic, provider("CIMWin32"), UUID("{67F74295-BA42-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class Win32_InfraredDevice : CIM_InfraredController
{
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
  string   Manufacturer;
  uint32   MaxNumberControlled;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtocolSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="b78bb-108">Members</span><span class="sxs-lookup"><span data-stu-id="b78bb-108">Members</span></span>

<span data-ttu-id="b78bb-109">La classe **Win32 \_ InfraredDevice** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b78bb-109">The **Win32\_InfraredDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="b78bb-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="b78bb-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="b78bb-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b78bb-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b78bb-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="b78bb-112">Methods</span></span>

<span data-ttu-id="b78bb-113">La classe **Win32 \_ InfraredDevice** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="b78bb-113">The **Win32\_InfraredDevice** class has these methods.</span></span>



| <span data-ttu-id="b78bb-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="b78bb-114">Method</span></span>            | <span data-ttu-id="b78bb-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b78bb-115">Description</span></span>                                                                                                                                                                                                                |
|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b78bb-116">**Reimpostazione**</span><span class="sxs-lookup"><span data-stu-id="b78bb-116">**Reset**</span></span>         | <span data-ttu-id="b78bb-117">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="b78bb-117">Not implemented.</span></span> <span data-ttu-id="b78bb-118">Per implementare questo metodo, vedere il metodo [**Reset**](reset-method-in-class-cim-controller.md) in [**CIM \_ InfraredController**](cim-infraredcontroller.md) per la documentazione.</span><span class="sxs-lookup"><span data-stu-id="b78bb-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_InfraredController**](cim-infraredcontroller.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="b78bb-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="b78bb-119">**SetPowerState**</span></span> | <span data-ttu-id="b78bb-120">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="b78bb-120">Not implemented.</span></span> <span data-ttu-id="b78bb-121">Per implementare questo metodo, vedere il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) in [**CIM \_ InfraredController**](cim-infraredcontroller.md) per la documentazione.</span><span class="sxs-lookup"><span data-stu-id="b78bb-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_InfraredController**](cim-infraredcontroller.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b78bb-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b78bb-122">Properties</span></span>

<span data-ttu-id="b78bb-123">La classe **Win32 \_ InfraredDevice** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b78bb-123">The **Win32\_InfraredDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b78bb-124">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="b78bb-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b78bb-125">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b78bb-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b78bb-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-127">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="b78bb-127">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="b78bb-128">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b78bb-128">Availability and status of the device.</span></span>

<span data-ttu-id="b78bb-129">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b78bb-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b78bb-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="b78bb-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b78bb-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="b78bb-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="b78bb-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="b78bb-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-133">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="b78bb-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="b78bb-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="b78bb-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="b78bb-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="b78bb-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b78bb-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="b78bb-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="b78bb-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="b78bb-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="b78bb-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="b78bb-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="b78bb-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="b78bb-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b78bb-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="b78bb-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="b78bb-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="b78bb-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="b78bb-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="b78bb-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="b78bb-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="b78bb-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-144">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="b78bb-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="b78bb-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="b78bb-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-146">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="b78bb-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="b78bb-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="b78bb-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-148">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="b78bb-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="b78bb-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="b78bb-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="b78bb-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="b78bb-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-151">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="b78bb-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="b78bb-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="b78bb-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-153">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="b78bb-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="b78bb-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="b78bb-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-155">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="b78bb-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="b78bb-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="b78bb-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-157">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="b78bb-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="b78bb-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="b78bb-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-159">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="b78bb-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b78bb-160">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="b78bb-160">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b78bb-161">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b78bb-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b78bb-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-163">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b78bb-163">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b78bb-164">Breve descrizione dell'oggetto stringa a una riga.</span><span class="sxs-lookup"><span data-stu-id="b78bb-164">Short description of the object a one-line string.</span></span>

<span data-ttu-id="b78bb-165">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b78bb-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b78bb-166">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b78bb-166">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b78bb-167">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b78bb-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b78bb-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-169">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b78bb-169">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b78bb-170">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="b78bb-170">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="b78bb-171">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b78bb-171">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="b78bb-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="b78bb-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="b78bb-173"> (0)</span><span class="sxs-lookup"><span data-stu-id="b78bb-173">(0)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-174">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="b78bb-174">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="b78bb-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="b78bb-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="b78bb-176">(1)</span><span class="sxs-lookup"><span data-stu-id="b78bb-176">(1)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-177">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="b78bb-177">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b78bb-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b78bb-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="b78bb-179">(2)</span><span class="sxs-lookup"><span data-stu-id="b78bb-179">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="b78bb-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="b78bb-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="b78bb-181">(3)</span><span class="sxs-lookup"><span data-stu-id="b78bb-181">(3)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-182">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="b78bb-182">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b78bb-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="b78bb-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="b78bb-184">(4)</span><span class="sxs-lookup"><span data-stu-id="b78bb-184">(4)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-185">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="b78bb-185">Device is not working properly.</span></span> <span data-ttu-id="b78bb-186">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="b78bb-186">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="b78bb-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="b78bb-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="b78bb-188">(5)</span><span class="sxs-lookup"><span data-stu-id="b78bb-188">(5)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-189">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="b78bb-189">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="b78bb-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="b78bb-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="b78bb-191"> (6)</span><span class="sxs-lookup"><span data-stu-id="b78bb-191">(6)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-192">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="b78bb-192">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="b78bb-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="b78bb-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="b78bb-194">(7)</span><span class="sxs-lookup"><span data-stu-id="b78bb-194">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="b78bb-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="b78bb-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="b78bb-196">(8)</span><span class="sxs-lookup"><span data-stu-id="b78bb-196">(8)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-197">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="b78bb-197">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="b78bb-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="b78bb-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="b78bb-199">(9)</span><span class="sxs-lookup"><span data-stu-id="b78bb-199">(9)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-200">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="b78bb-200">Device is not working properly.</span></span> <span data-ttu-id="b78bb-201">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b78bb-201">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="b78bb-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b78bb-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="b78bb-203">(10)</span><span class="sxs-lookup"><span data-stu-id="b78bb-203">(10)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-204">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b78bb-204">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="b78bb-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b78bb-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="b78bb-206">(11)</span><span class="sxs-lookup"><span data-stu-id="b78bb-206">(11)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-207">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b78bb-207">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="b78bb-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="b78bb-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="b78bb-209">12</span><span class="sxs-lookup"><span data-stu-id="b78bb-209">(12)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-210">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="b78bb-210">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="b78bb-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b78bb-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="b78bb-212">(13)</span><span class="sxs-lookup"><span data-stu-id="b78bb-212">(13)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-213">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b78bb-213">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="b78bb-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="b78bb-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="b78bb-215">(14)</span><span class="sxs-lookup"><span data-stu-id="b78bb-215">(14)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-216">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="b78bb-216">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="b78bb-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="b78bb-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="b78bb-218">(15)</span><span class="sxs-lookup"><span data-stu-id="b78bb-218">(15)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-219">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="b78bb-219">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="b78bb-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b78bb-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="b78bb-221">(16)</span><span class="sxs-lookup"><span data-stu-id="b78bb-221">(16)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-222">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b78bb-222">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="b78bb-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="b78bb-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="b78bb-224">(17)</span><span class="sxs-lookup"><span data-stu-id="b78bb-224">(17)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-225">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="b78bb-225">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b78bb-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b78bb-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="b78bb-227">(18)</span><span class="sxs-lookup"><span data-stu-id="b78bb-227">(18)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-228">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b78bb-228">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="b78bb-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="b78bb-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="b78bb-230">(19)</span><span class="sxs-lookup"><span data-stu-id="b78bb-230">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b78bb-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="b78bb-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="b78bb-232">(20)</span><span class="sxs-lookup"><span data-stu-id="b78bb-232">(20)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-233">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="b78bb-233">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="b78bb-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b78bb-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="b78bb-235">(21)</span><span class="sxs-lookup"><span data-stu-id="b78bb-235">(21)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-236">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="b78bb-236">System failure.</span></span> <span data-ttu-id="b78bb-237">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="b78bb-237">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="b78bb-238">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b78bb-238">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="b78bb-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="b78bb-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="b78bb-240">(22)</span><span class="sxs-lookup"><span data-stu-id="b78bb-240">(22)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-241">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="b78bb-241">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="b78bb-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="b78bb-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="b78bb-243">(23)</span><span class="sxs-lookup"><span data-stu-id="b78bb-243">(23)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-244">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="b78bb-244">System failure.</span></span> <span data-ttu-id="b78bb-245">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="b78bb-245">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="b78bb-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="b78bb-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="b78bb-247">(24)</span><span class="sxs-lookup"><span data-stu-id="b78bb-247">(24)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-248">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="b78bb-248">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b78bb-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b78bb-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b78bb-250">(25)</span><span class="sxs-lookup"><span data-stu-id="b78bb-250">(25)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-251">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b78bb-251">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b78bb-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b78bb-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b78bb-253">(26)</span><span class="sxs-lookup"><span data-stu-id="b78bb-253">(26)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-254">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b78bb-254">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="b78bb-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="b78bb-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="b78bb-256">(27)</span><span class="sxs-lookup"><span data-stu-id="b78bb-256">(27)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-257">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="b78bb-257">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="b78bb-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="b78bb-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="b78bb-259">(28)</span><span class="sxs-lookup"><span data-stu-id="b78bb-259">(28)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-260">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="b78bb-260">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="b78bb-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="b78bb-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="b78bb-262">(29)</span><span class="sxs-lookup"><span data-stu-id="b78bb-262">(29)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-263">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="b78bb-263">Device is disabled.</span></span> <span data-ttu-id="b78bb-264">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="b78bb-264">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="b78bb-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b78bb-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="b78bb-266">(30)</span><span class="sxs-lookup"><span data-stu-id="b78bb-266">(30)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-267">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b78bb-267">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b78bb-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b78bb-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="b78bb-269">31</span><span class="sxs-lookup"><span data-stu-id="b78bb-269">(31)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-270">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="b78bb-270">Device is not working properly.</span></span> <span data-ttu-id="b78bb-271">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="b78bb-271">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b78bb-272">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="b78bb-272">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b78bb-273">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b78bb-273">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-274">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b78bb-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-275">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b78bb-275">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b78bb-276">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="b78bb-276">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="b78bb-277">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b78bb-277">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b78bb-278">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b78bb-278">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b78bb-279">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b78bb-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-280">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b78bb-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-281">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b78bb-281">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b78bb-282">Nome della prima classe concreta visualizzata nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="b78bb-282">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="b78bb-283">Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="b78bb-283">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="b78bb-284">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b78bb-284">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b78bb-285">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="b78bb-285">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b78bb-286">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b78bb-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-287">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b78bb-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-288">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="b78bb-288">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b78bb-289">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b78bb-289">Description of the object.</span></span>

<span data-ttu-id="b78bb-290">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b78bb-290">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b78bb-291">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="b78bb-291">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b78bb-292">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b78bb-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-293">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b78bb-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-294">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="b78bb-294">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b78bb-295">Identificatore univoco del dispositivo a infrarossi.</span><span class="sxs-lookup"><span data-stu-id="b78bb-295">Unique identifier of the infrared device.</span></span>

<span data-ttu-id="b78bb-296">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b78bb-296">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b78bb-297">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="b78bb-297">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b78bb-298">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b78bb-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-299">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b78bb-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b78bb-300">Se **true**, l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="b78bb-300">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="b78bb-301">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b78bb-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b78bb-302">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="b78bb-302">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b78bb-303">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b78bb-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-304">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b78bb-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b78bb-305">Altre informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="b78bb-305">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="b78bb-306">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b78bb-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b78bb-307">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b78bb-307">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b78bb-308">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b78bb-308">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-309">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b78bb-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-310">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="b78bb-310">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b78bb-311">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b78bb-311">Date and time the object was installed.</span></span> <span data-ttu-id="b78bb-312">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="b78bb-312">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b78bb-313">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b78bb-313">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b78bb-314">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b78bb-314">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b78bb-315">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b78bb-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-316">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b78bb-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b78bb-317">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="b78bb-317">Last error code reported by the logical device.</span></span>

<span data-ttu-id="b78bb-318">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b78bb-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b78bb-319">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="b78bb-319">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b78bb-320">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b78bb-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-321">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b78bb-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-322">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="b78bb-322">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="b78bb-323">Produttore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b78bb-323">Manufacturer of the device.</span></span>

</dd> <dt>

<span data-ttu-id="b78bb-324">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="b78bb-324">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b78bb-325">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b78bb-325">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-326">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b78bb-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-327">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta bus DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="b78bb-327">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="b78bb-328">Numero massimo di entità indirizzabili direttamente supportate da questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b78bb-328">Maximum number of directly addressable entities supportable by this device.</span></span> <span data-ttu-id="b78bb-329">Se il numero è sconosciuto, è necessario usare un valore pari a 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="b78bb-329">A value of 0 (zero) should be used if the number is unknown.</span></span>

<span data-ttu-id="b78bb-330">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="b78bb-330">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="b78bb-331">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b78bb-331">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b78bb-332">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b78bb-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-333">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b78bb-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-334">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="b78bb-334">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b78bb-335">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="b78bb-335">Label by which the object is known.</span></span> <span data-ttu-id="b78bb-336">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="b78bb-336">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="b78bb-337">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b78bb-337">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b78bb-338">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="b78bb-338">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b78bb-339">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b78bb-339">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-340">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b78bb-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-341">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b78bb-341">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b78bb-342">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="b78bb-342">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="b78bb-343">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b78bb-343">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="b78bb-344">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="b78bb-344">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="b78bb-345">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="b78bb-345">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b78bb-346">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b78bb-346">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-347">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b78bb-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b78bb-348">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="b78bb-348">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="b78bb-349">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="b78bb-349">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b78bb-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="b78bb-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="b78bb-351"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="b78bb-351"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b78bb-352"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="b78bb-352"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b78bb-353"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="b78bb-353"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-354">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="b78bb-354">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="b78bb-355"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="b78bb-355"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-356">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="b78bb-356">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="b78bb-357"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="b78bb-357"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-358">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="b78bb-358">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="b78bb-359">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="b78bb-359">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="b78bb-360">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="b78bb-360">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="b78bb-361"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="b78bb-361"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-362">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="b78bb-362">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="b78bb-363"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="b78bb-363"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b78bb-364">Tempo Power-On supportato</span><span class="sxs-lookup"><span data-stu-id="b78bb-364">Timed Power-On Supported</span></span>

<span data-ttu-id="b78bb-365">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="b78bb-365">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b78bb-366">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="b78bb-366">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b78bb-367">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b78bb-367">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-368">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b78bb-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b78bb-369">Se **true**, il dispositivo può essere gestito dal risparmio di energia (può essere impostato in modalità di sospensione e così via).</span><span class="sxs-lookup"><span data-stu-id="b78bb-369">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="b78bb-370">La proprietà non indica che le funzionalità di risparmio energia sono attualmente abilitate, solo che il dispositivo logico è in grado di gestire il risparmio di energia.</span><span class="sxs-lookup"><span data-stu-id="b78bb-370">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="b78bb-371">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b78bb-371">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b78bb-372">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="b78bb-372">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b78bb-373">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b78bb-373">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-374">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b78bb-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-375">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta bus DMTF \| 001,2 "," MIF. \|Dischi DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="b78bb-375">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="b78bb-376">Protocollo usato dal controller per accedere ai dispositivi "controllati".</span><span class="sxs-lookup"><span data-stu-id="b78bb-376">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="b78bb-377">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="b78bb-377">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="b78bb-378">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="b78bb-378">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b78bb-379">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="b78bb-379">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b78bb-380">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="b78bb-380">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="b78bb-381">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="b78bb-381">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="b78bb-382">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="b78bb-382">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="b78bb-383">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="b78bb-383">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="b78bb-384">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="b78bb-384">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="b78bb-385">**Dischetto flessibile** (7)</span><span class="sxs-lookup"><span data-stu-id="b78bb-385">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="b78bb-386">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="b78bb-386">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="b78bb-387">**Interfaccia parallela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="b78bb-387">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="b78bb-388">**Protocollo di Fibre Channel SCSI** (10)</span><span class="sxs-lookup"><span data-stu-id="b78bb-388">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="b78bb-389">**Protocollo bus seriale SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="b78bb-389">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="b78bb-390">**Protocollo bus seriale SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="b78bb-390">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="b78bb-391">**Architettura di archiviazione seriale SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="b78bb-391">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="b78bb-392">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="b78bb-392">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="b78bb-393">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="b78bb-393">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="b78bb-394">**Bus seriale universale** (16)</span><span class="sxs-lookup"><span data-stu-id="b78bb-394">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="b78bb-395">**Protocollo parallelo** (17)</span><span class="sxs-lookup"><span data-stu-id="b78bb-395">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="b78bb-396">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="b78bb-396">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="b78bb-397">**Diagnostica** (19)</span><span class="sxs-lookup"><span data-stu-id="b78bb-397">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="b78bb-398">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="b78bb-398">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="b78bb-399">**Potenza** (21)</span><span class="sxs-lookup"><span data-stu-id="b78bb-399">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="b78bb-400">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="b78bb-400">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="b78bb-401">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="b78bb-401">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="b78bb-402">**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="b78bb-402">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="b78bb-403">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="b78bb-403">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="b78bb-404">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="b78bb-404">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="b78bb-405">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="b78bb-405">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="b78bb-406">**IEEE 802,3 10Base5** (28)</span><span class="sxs-lookup"><span data-stu-id="b78bb-406">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="b78bb-407">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="b78bb-407">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="b78bb-408">**IEEE 802,3 1Base5** (30)</span><span class="sxs-lookup"><span data-stu-id="b78bb-408">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="b78bb-409">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="b78bb-409">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="b78bb-410">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="b78bb-410">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="b78bb-411">**Token-ring IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="b78bb-411">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="b78bb-412">**ANSI X3T 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="b78bb-412">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="b78bb-413">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="b78bb-413">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="b78bb-414">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="b78bb-414">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="b78bb-415">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="b78bb-415">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="b78bb-416">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="b78bb-416">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="b78bb-417">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="b78bb-417">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="b78bb-418">**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="b78bb-418">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="b78bb-419">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="b78bb-419">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="b78bb-420">**ATA/IDE avanzato** (42)</span><span class="sxs-lookup"><span data-stu-id="b78bb-420">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="b78bb-421">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="b78bb-421">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="b78bb-422">**TWIRP (infrarossi bidirezionali)** (44)</span><span class="sxs-lookup"><span data-stu-id="b78bb-422">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="b78bb-423">**FIR (infrarossi veloci)** (45)</span><span class="sxs-lookup"><span data-stu-id="b78bb-423">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="b78bb-424">**Sir (Serial Infrared)** (46)</span><span class="sxs-lookup"><span data-stu-id="b78bb-424">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="b78bb-425">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="b78bb-425">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b78bb-426">**Status**</span><span class="sxs-lookup"><span data-stu-id="b78bb-426">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b78bb-427">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b78bb-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-428">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b78bb-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-429">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="b78bb-429">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b78bb-430">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b78bb-430">Current status of the object.</span></span> <span data-ttu-id="b78bb-431">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="b78bb-431">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="b78bb-432">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="b78bb-432">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="b78bb-433">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="b78bb-433">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b78bb-434">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="b78bb-434">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b78bb-435">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="b78bb-435">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b78bb-436">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b78bb-436">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b78bb-437">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="b78bb-437">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b78bb-438">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="b78bb-438">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b78bb-439">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="b78bb-439">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b78bb-440">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="b78bb-440">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b78bb-441">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="b78bb-441">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b78bb-442">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="b78bb-442">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b78bb-443">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="b78bb-443">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b78bb-444">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="b78bb-444">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b78bb-445">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="b78bb-445">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b78bb-446">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="b78bb-446">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b78bb-447">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="b78bb-447">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b78bb-448">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="b78bb-448">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b78bb-449">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="b78bb-449">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b78bb-450">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="b78bb-450">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b78bb-451">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b78bb-451">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-452">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b78bb-452">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-453">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="b78bb-453">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="b78bb-454">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="b78bb-454">State of the logical device.</span></span> <span data-ttu-id="b78bb-455">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="b78bb-455">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="b78bb-456">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b78bb-456">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b78bb-457">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="b78bb-457">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b78bb-458">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="b78bb-458">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b78bb-459">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="b78bb-459">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b78bb-460">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="b78bb-460">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b78bb-461">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="b78bb-461">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b78bb-462">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b78bb-462">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b78bb-463">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b78bb-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-464">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b78bb-464">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-465">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b78bb-465">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b78bb-466">Valore per la proprietà **CreationClassName** del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="b78bb-466">Value for the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="b78bb-467">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b78bb-467">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b78bb-468">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b78bb-468">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b78bb-469">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b78bb-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-470">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b78bb-470">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-471">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b78bb-471">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b78bb-472">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="b78bb-472">Name of the scoping system.</span></span>

<span data-ttu-id="b78bb-473">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b78bb-473">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b78bb-474">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="b78bb-474">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b78bb-475">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b78bb-475">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b78bb-476">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b78bb-476">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b78bb-477">Data e ora dell'ultima reimpostazione del controller.</span><span class="sxs-lookup"><span data-stu-id="b78bb-477">Date and time the controller was last reset.</span></span> <span data-ttu-id="b78bb-478">Questo potrebbe significare che il controller è stato spento o reinizializzato.</span><span class="sxs-lookup"><span data-stu-id="b78bb-478">This could mean the controller was powered down, or reinitialized.</span></span>

<span data-ttu-id="b78bb-479">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="b78bb-479">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b78bb-480">Commenti</span><span class="sxs-lookup"><span data-stu-id="b78bb-480">Remarks</span></span>

<span data-ttu-id="b78bb-481">La classe **Win32 \_ InfraredDevice** è derivata da [**CIM \_ InfraredController**](cim-infraredcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="b78bb-481">The **Win32\_InfraredDevice** class is derived from [**CIM\_InfraredController**](cim-infraredcontroller.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b78bb-482">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b78bb-482">Requirements</span></span>



| <span data-ttu-id="b78bb-483">Requisito</span><span class="sxs-lookup"><span data-stu-id="b78bb-483">Requirement</span></span> | <span data-ttu-id="b78bb-484">Valore</span><span class="sxs-lookup"><span data-stu-id="b78bb-484">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b78bb-485">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b78bb-485">Minimum supported client</span></span><br/> | <span data-ttu-id="b78bb-486">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b78bb-486">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b78bb-487">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b78bb-487">Minimum supported server</span></span><br/> | <span data-ttu-id="b78bb-488">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b78bb-488">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b78bb-489">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b78bb-489">Namespace</span></span><br/>                | <span data-ttu-id="b78bb-490">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="b78bb-490">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b78bb-491">MOF</span><span class="sxs-lookup"><span data-stu-id="b78bb-491">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b78bb-492"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b78bb-492"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b78bb-493">DLL</span><span class="sxs-lookup"><span data-stu-id="b78bb-493">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b78bb-494"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b78bb-494"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b78bb-495">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b78bb-495">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b78bb-496">**\_INFRAREDCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="b78bb-496">**CIM\_InfraredController**</span></span>](cim-infraredcontroller.md)
</dt> <dt>

[<span data-ttu-id="b78bb-497">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="b78bb-497">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 


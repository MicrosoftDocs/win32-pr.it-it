---
description: La \_ classe WMI FloppyController Win32 rappresenta le funzionalità e la capacità di gestione di un controller di unità disco floppy.
ms.assetid: 8c02847c-8329-4adc-b2a5-149b36aead88
ms.tgt_platform: multiple
title: Classe Win32_FloppyController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_FloppyController
- Win32_FloppyController.Reset
- Win32_FloppyController.SetPowerState
- Win32_FloppyController.Availability
- Win32_FloppyController.Caption
- Win32_FloppyController.ConfigManagerErrorCode
- Win32_FloppyController.ConfigManagerUserConfig
- Win32_FloppyController.CreationClassName
- Win32_FloppyController.Description
- Win32_FloppyController.DeviceID
- Win32_FloppyController.ErrorCleared
- Win32_FloppyController.ErrorDescription
- Win32_FloppyController.InstallDate
- Win32_FloppyController.LastErrorCode
- Win32_FloppyController.Manufacturer
- Win32_FloppyController.MaxNumberControlled
- Win32_FloppyController.Name
- Win32_FloppyController.PNPDeviceID
- Win32_FloppyController.PowerManagementCapabilities
- Win32_FloppyController.PowerManagementSupported
- Win32_FloppyController.ProtocolSupported
- Win32_FloppyController.Status
- Win32_FloppyController.StatusInfo
- Win32_FloppyController.SystemCreationClassName
- Win32_FloppyController.SystemName
- Win32_FloppyController.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7aac44fb8e2b0a91ca3794f234a31cd4c25a4b5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966263"
---
# <a name="win32_floppycontroller-class"></a><span data-ttu-id="16dac-103">Win32 \_ FloppyController (classe)</span><span class="sxs-lookup"><span data-stu-id="16dac-103">Win32\_FloppyController class</span></span>

<span data-ttu-id="16dac-104">\[**Win32 \_ FloppyController** non è più disponibile per l'uso a partire da Windows 10 e Windows Server 2016.\]</span><span class="sxs-lookup"><span data-stu-id="16dac-104">\[**Win32\_FloppyController** is no longer available for use as of Windows 10 and Windows Server 2016.\]</span></span>

<span data-ttu-id="16dac-105">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ FloppyController Win32** rappresenta le funzionalità e la capacità di gestione di un controller di unità disco floppy.</span><span class="sxs-lookup"><span data-stu-id="16dac-105">The **Win32\_FloppyController** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the capabilities and management capacity of a floppy disk drive controller.</span></span>

<span data-ttu-id="16dac-106">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="16dac-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="16dac-107">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="16dac-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="16dac-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="16dac-108">Syntax</span></span>

``` syntax
[dynamic, provider("CIMWin32"), UUID("{2A7DC003-BAEF-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class Win32_FloppyController : CIM_Controller
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

## <a name="members"></a><span data-ttu-id="16dac-109">Members</span><span class="sxs-lookup"><span data-stu-id="16dac-109">Members</span></span>

<span data-ttu-id="16dac-110">La classe **Win32 \_ FloppyController** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="16dac-110">The **Win32\_FloppyController** class has these types of members:</span></span>

-   [<span data-ttu-id="16dac-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="16dac-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="16dac-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="16dac-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="16dac-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="16dac-113">Methods</span></span>

<span data-ttu-id="16dac-114">La classe **Win32 \_ FloppyController** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="16dac-114">The **Win32\_FloppyController** class has these methods.</span></span>



| <span data-ttu-id="16dac-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="16dac-115">Method</span></span>            | <span data-ttu-id="16dac-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16dac-116">Description</span></span>                                                                                                                                                                                                |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16dac-117">**Reimpostazione**</span><span class="sxs-lookup"><span data-stu-id="16dac-117">**Reset**</span></span>         | <span data-ttu-id="16dac-118">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="16dac-118">Not implemented.</span></span> <span data-ttu-id="16dac-119">Per implementare questo metodo, vedere il metodo [**Reset**](reset-method-in-class-cim-controller.md) nel [**\_ controller CIM**](cim-controller.md) per la documentazione.</span><span class="sxs-lookup"><span data-stu-id="16dac-119">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_Controller**](cim-controller.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="16dac-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="16dac-120">**SetPowerState**</span></span> | <span data-ttu-id="16dac-121">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="16dac-121">Not implemented.</span></span> <span data-ttu-id="16dac-122">Per implementare questo metodo, vedere il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) nel [**\_ controller CIM**](cim-controller.md) per la documentazione.</span><span class="sxs-lookup"><span data-stu-id="16dac-122">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_Controller**](cim-controller.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="16dac-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="16dac-123">Properties</span></span>

<span data-ttu-id="16dac-124">La classe **Win32 \_ FloppyController** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="16dac-124">The **Win32\_FloppyController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="16dac-125">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="16dac-125">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16dac-126">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="16dac-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="16dac-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="16dac-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16dac-128">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="16dac-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="16dac-129">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="16dac-129">Availability and status of the device.</span></span>

<span data-ttu-id="16dac-130">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="16dac-130">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="16dac-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="16dac-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="16dac-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="16dac-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="16dac-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="16dac-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-134">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="16dac-134">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="16dac-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="16dac-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="16dac-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="16dac-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="16dac-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="16dac-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="16dac-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="16dac-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="16dac-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="16dac-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="16dac-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="16dac-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="16dac-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="16dac-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="16dac-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="16dac-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="16dac-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="16dac-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="16dac-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="16dac-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-145">Risparmio energia-sconosciuto</span><span class="sxs-lookup"><span data-stu-id="16dac-145">Power Save - Unknown</span></span>

<span data-ttu-id="16dac-146">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="16dac-146">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="16dac-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="16dac-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-148">Risparmio energia-modalità a basso consumo</span><span class="sxs-lookup"><span data-stu-id="16dac-148">Power Save - Low Power Mode</span></span>

<span data-ttu-id="16dac-149">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="16dac-149">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="16dac-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="16dac-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-151">Risparmio energia-standby</span><span class="sxs-lookup"><span data-stu-id="16dac-151">Power Save - Standby</span></span>

<span data-ttu-id="16dac-152">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="16dac-152">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="16dac-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="16dac-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="16dac-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="16dac-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-155">Risparmio energia-avviso</span><span class="sxs-lookup"><span data-stu-id="16dac-155">Power Save - Warning</span></span>

<span data-ttu-id="16dac-156">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="16dac-156">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="16dac-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="16dac-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-158">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="16dac-158">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="16dac-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="16dac-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-160">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="16dac-160">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="16dac-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="16dac-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-162">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="16dac-162">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="16dac-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="16dac-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-164">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="16dac-164">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="16dac-165">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="16dac-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16dac-166">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="16dac-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16dac-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="16dac-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16dac-168">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="16dac-168">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="16dac-169">Breve descrizione dell'oggetto stringa a una riga.</span><span class="sxs-lookup"><span data-stu-id="16dac-169">Short description of the object a one-line string.</span></span>

<span data-ttu-id="16dac-170">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="16dac-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="16dac-171">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="16dac-171">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16dac-172">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="16dac-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="16dac-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="16dac-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16dac-174">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="16dac-174">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="16dac-175">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="16dac-175">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="16dac-176">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="16dac-176">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="16dac-177"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="16dac-177"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="16dac-178"> (0)</span><span class="sxs-lookup"><span data-stu-id="16dac-178">(0)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-179">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="16dac-179">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="16dac-180"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="16dac-180"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="16dac-181">(1)</span><span class="sxs-lookup"><span data-stu-id="16dac-181">(1)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-182">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="16dac-182">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="16dac-183"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="16dac-183"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="16dac-184">(2)</span><span class="sxs-lookup"><span data-stu-id="16dac-184">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="16dac-185"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="16dac-185"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="16dac-186">(3)</span><span class="sxs-lookup"><span data-stu-id="16dac-186">(3)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-187">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="16dac-187">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="16dac-188"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="16dac-188"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="16dac-189">(4)</span><span class="sxs-lookup"><span data-stu-id="16dac-189">(4)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-190">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="16dac-190">Device is not working properly.</span></span> <span data-ttu-id="16dac-191">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="16dac-191">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="16dac-192"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="16dac-192"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="16dac-193">(5)</span><span class="sxs-lookup"><span data-stu-id="16dac-193">(5)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-194">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="16dac-194">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="16dac-195"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="16dac-195"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="16dac-196"> (6)</span><span class="sxs-lookup"><span data-stu-id="16dac-196">(6)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-197">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="16dac-197">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="16dac-198"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="16dac-198"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="16dac-199">(7)</span><span class="sxs-lookup"><span data-stu-id="16dac-199">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="16dac-200"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="16dac-200"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="16dac-201">(8)</span><span class="sxs-lookup"><span data-stu-id="16dac-201">(8)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-202">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="16dac-202">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="16dac-203"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="16dac-203"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="16dac-204">(9)</span><span class="sxs-lookup"><span data-stu-id="16dac-204">(9)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-205">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="16dac-205">Device is not working properly.</span></span> <span data-ttu-id="16dac-206">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="16dac-206">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="16dac-207"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="16dac-207"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="16dac-208">(10)</span><span class="sxs-lookup"><span data-stu-id="16dac-208">(10)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-209">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="16dac-209">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="16dac-210"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="16dac-210"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="16dac-211">(11)</span><span class="sxs-lookup"><span data-stu-id="16dac-211">(11)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-212">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="16dac-212">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="16dac-213"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="16dac-213"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="16dac-214">12</span><span class="sxs-lookup"><span data-stu-id="16dac-214">(12)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-215">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="16dac-215">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="16dac-216"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="16dac-216"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="16dac-217">(13)</span><span class="sxs-lookup"><span data-stu-id="16dac-217">(13)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-218">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="16dac-218">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="16dac-219"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="16dac-219"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="16dac-220">(14)</span><span class="sxs-lookup"><span data-stu-id="16dac-220">(14)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-221">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="16dac-221">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="16dac-222"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="16dac-222"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="16dac-223">(15)</span><span class="sxs-lookup"><span data-stu-id="16dac-223">(15)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-224">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="16dac-224">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="16dac-225"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="16dac-225"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="16dac-226">(16)</span><span class="sxs-lookup"><span data-stu-id="16dac-226">(16)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-227">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="16dac-227">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="16dac-228"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="16dac-228"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="16dac-229">(17)</span><span class="sxs-lookup"><span data-stu-id="16dac-229">(17)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-230">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="16dac-230">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="16dac-231"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="16dac-231"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="16dac-232">(18)</span><span class="sxs-lookup"><span data-stu-id="16dac-232">(18)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-233">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="16dac-233">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="16dac-234"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="16dac-234"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="16dac-235">(19)</span><span class="sxs-lookup"><span data-stu-id="16dac-235">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="16dac-236"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="16dac-236"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="16dac-237">(20)</span><span class="sxs-lookup"><span data-stu-id="16dac-237">(20)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-238">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="16dac-238">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="16dac-239"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="16dac-239"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="16dac-240">(21)</span><span class="sxs-lookup"><span data-stu-id="16dac-240">(21)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-241">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="16dac-241">System failure.</span></span> <span data-ttu-id="16dac-242">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="16dac-242">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="16dac-243">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="16dac-243">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="16dac-244"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="16dac-244"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="16dac-245">(22)</span><span class="sxs-lookup"><span data-stu-id="16dac-245">(22)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-246">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="16dac-246">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="16dac-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="16dac-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="16dac-248">(23)</span><span class="sxs-lookup"><span data-stu-id="16dac-248">(23)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-249">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="16dac-249">System failure.</span></span> <span data-ttu-id="16dac-250">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="16dac-250">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="16dac-251"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="16dac-251"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="16dac-252">(24)</span><span class="sxs-lookup"><span data-stu-id="16dac-252">(24)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-253">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="16dac-253">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="16dac-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="16dac-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="16dac-255">(25)</span><span class="sxs-lookup"><span data-stu-id="16dac-255">(25)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-256">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="16dac-256">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="16dac-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="16dac-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="16dac-258">(26)</span><span class="sxs-lookup"><span data-stu-id="16dac-258">(26)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-259">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="16dac-259">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="16dac-260"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="16dac-260"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="16dac-261">(27)</span><span class="sxs-lookup"><span data-stu-id="16dac-261">(27)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-262">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="16dac-262">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="16dac-263"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="16dac-263"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="16dac-264">(28)</span><span class="sxs-lookup"><span data-stu-id="16dac-264">(28)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-265">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="16dac-265">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="16dac-266"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="16dac-266"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="16dac-267">(29)</span><span class="sxs-lookup"><span data-stu-id="16dac-267">(29)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-268">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="16dac-268">Device is disabled.</span></span> <span data-ttu-id="16dac-269">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="16dac-269">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="16dac-270"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="16dac-270"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="16dac-271">(30)</span><span class="sxs-lookup"><span data-stu-id="16dac-271">(30)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-272">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="16dac-272">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="16dac-273"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="16dac-273"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="16dac-274">31</span><span class="sxs-lookup"><span data-stu-id="16dac-274">(31)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-275">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="16dac-275">Device is not working properly.</span></span> <span data-ttu-id="16dac-276">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="16dac-276">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="16dac-277">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="16dac-277">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16dac-278">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="16dac-278">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="16dac-279">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="16dac-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16dac-280">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="16dac-280">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="16dac-281">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="16dac-281">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="16dac-282">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="16dac-282">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="16dac-283">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="16dac-283">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16dac-284">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="16dac-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16dac-285">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="16dac-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16dac-286">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="16dac-286">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="16dac-287">Nome della prima classe concreta visualizzata nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="16dac-287">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="16dac-288">Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="16dac-288">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="16dac-289">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="16dac-289">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="16dac-290">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="16dac-290">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16dac-291">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="16dac-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16dac-292">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="16dac-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16dac-293">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="16dac-293">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="16dac-294">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="16dac-294">Description of the object.</span></span>

<span data-ttu-id="16dac-295">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="16dac-295">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="16dac-296">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="16dac-296">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16dac-297">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="16dac-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16dac-298">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="16dac-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16dac-299">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="16dac-299">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="16dac-300">Identificatore univoco del controller floppy.</span><span class="sxs-lookup"><span data-stu-id="16dac-300">Unique identifier of the floppy controller.</span></span>

<span data-ttu-id="16dac-301">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="16dac-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="16dac-302">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="16dac-302">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16dac-303">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="16dac-303">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="16dac-304">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="16dac-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16dac-305">Se **true**, l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="16dac-305">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="16dac-306">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="16dac-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="16dac-307">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="16dac-307">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16dac-308">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="16dac-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16dac-309">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="16dac-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16dac-310">Altre informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="16dac-310">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="16dac-311">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="16dac-311">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="16dac-312">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="16dac-312">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16dac-313">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="16dac-313">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="16dac-314">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="16dac-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16dac-315">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="16dac-315">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="16dac-316">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="16dac-316">Date and time the object is installed.</span></span> <span data-ttu-id="16dac-317">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="16dac-317">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="16dac-318">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="16dac-318">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="16dac-319">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="16dac-319">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16dac-320">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="16dac-320">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="16dac-321">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="16dac-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16dac-322">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="16dac-322">Last error code reported by the logical device.</span></span>

<span data-ttu-id="16dac-323">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="16dac-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="16dac-324">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="16dac-324">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16dac-325">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="16dac-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16dac-326">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="16dac-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16dac-327">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="16dac-327">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="16dac-328">Nome del produttore del controller floppy.</span><span class="sxs-lookup"><span data-stu-id="16dac-328">Name of the floppy controller manufacturer.</span></span>

<span data-ttu-id="16dac-329">Esempio: "Microsoft"</span><span class="sxs-lookup"><span data-stu-id="16dac-329">Example: "Microsoft"</span></span>

</dd> <dt>

<span data-ttu-id="16dac-330">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="16dac-330">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16dac-331">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="16dac-331">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="16dac-332">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="16dac-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16dac-333">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta bus DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="16dac-333">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="16dac-334">Numero massimo di entità indirizzabili direttamente supportate dal controller.</span><span class="sxs-lookup"><span data-stu-id="16dac-334">Maximum number of directly addressable entities that this controller supports.</span></span> <span data-ttu-id="16dac-335">Se il numero è sconosciuto, è necessario usare un valore pari a 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="16dac-335">A value of 0 (zero) should be used if the number is unknown.</span></span>

<span data-ttu-id="16dac-336">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="16dac-336">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="16dac-337">**Nome**</span><span class="sxs-lookup"><span data-stu-id="16dac-337">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16dac-338">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="16dac-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16dac-339">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="16dac-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16dac-340">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="16dac-340">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="16dac-341">Etichetta per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="16dac-341">Label for the object.</span></span> <span data-ttu-id="16dac-342">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="16dac-342">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="16dac-343">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="16dac-343">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="16dac-344">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="16dac-344">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16dac-345">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="16dac-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16dac-346">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="16dac-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16dac-347">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="16dac-347">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="16dac-348">Identificatore del dispositivo Plug and Play Windows per il dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="16dac-348">Windows Plug and Play device identifier for the logical device.</span></span>

<span data-ttu-id="16dac-349">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="16dac-349">Example: "\*PNP030b"</span></span>

<span data-ttu-id="16dac-350">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="16dac-350">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="16dac-351">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="16dac-351">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16dac-352">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="16dac-352">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="16dac-353">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="16dac-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16dac-354">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="16dac-354">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="16dac-355">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="16dac-355">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="16dac-356"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="16dac-356"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="16dac-357"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="16dac-357"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="16dac-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="16dac-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="16dac-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="16dac-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-360">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="16dac-360">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="16dac-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="16dac-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-362">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="16dac-362">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="16dac-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="16dac-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-364">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="16dac-364">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="16dac-365">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="16dac-365">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="16dac-366">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="16dac-366">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="16dac-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="16dac-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-368">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="16dac-368">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="16dac-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="16dac-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="16dac-370">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="16dac-370">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="16dac-371">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="16dac-371">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16dac-372">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="16dac-372">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="16dac-373">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="16dac-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16dac-374">Se **true**, il dispositivo può essere gestito dal risparmio energia, il che significa che può essere messo in modalità di sospensione e così via.</span><span class="sxs-lookup"><span data-stu-id="16dac-374">If **TRUE**, the device can be power-managed, which means that it can be put into suspend mode, and so on.</span></span> <span data-ttu-id="16dac-375">La proprietà non indica che le funzionalità di risparmio energia sono attualmente abilitate, solo che il dispositivo logico è in grado di gestire il risparmio di energia.</span><span class="sxs-lookup"><span data-stu-id="16dac-375">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="16dac-376">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="16dac-376">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="16dac-377">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="16dac-377">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16dac-378">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="16dac-378">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="16dac-379">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="16dac-379">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16dac-380">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta bus DMTF \| 001,2 "," MIF. \|Dischi DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="16dac-380">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="16dac-381">Protocollo usato dal controller per accedere ai dispositivi "controllati".</span><span class="sxs-lookup"><span data-stu-id="16dac-381">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="16dac-382">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="16dac-382">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="16dac-383">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="16dac-383">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="16dac-384">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="16dac-384">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="16dac-385">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="16dac-385">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="16dac-386">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="16dac-386">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="16dac-387">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="16dac-387">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="16dac-388">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="16dac-388">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="16dac-389">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="16dac-389">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="16dac-390">**Dischetto flessibile** (7)</span><span class="sxs-lookup"><span data-stu-id="16dac-390">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="16dac-391">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="16dac-391">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="16dac-392">**Interfaccia parallela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="16dac-392">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="16dac-393">**Protocollo di Fibre Channel SCSI** (10)</span><span class="sxs-lookup"><span data-stu-id="16dac-393">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="16dac-394">**Protocollo bus seriale SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="16dac-394">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="16dac-395">**Protocollo bus seriale SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="16dac-395">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="16dac-396">**Architettura di archiviazione seriale SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="16dac-396">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="16dac-397">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="16dac-397">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="16dac-398">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="16dac-398">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="16dac-399">**Bus seriale universale** (16)</span><span class="sxs-lookup"><span data-stu-id="16dac-399">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="16dac-400">**Protocollo parallelo** (17)</span><span class="sxs-lookup"><span data-stu-id="16dac-400">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="16dac-401">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="16dac-401">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="16dac-402">**Diagnostica** (19)</span><span class="sxs-lookup"><span data-stu-id="16dac-402">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="16dac-403">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="16dac-403">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="16dac-404">**Potenza** (21)</span><span class="sxs-lookup"><span data-stu-id="16dac-404">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="16dac-405">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="16dac-405">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="16dac-406">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="16dac-406">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="16dac-407">**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="16dac-407">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="16dac-408">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="16dac-408">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="16dac-409">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="16dac-409">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="16dac-410">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="16dac-410">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="16dac-411">**IEEE 802,3 10Base5** (28)</span><span class="sxs-lookup"><span data-stu-id="16dac-411">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="16dac-412">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="16dac-412">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="16dac-413">**IEEE 802,3 1Base5** (30)</span><span class="sxs-lookup"><span data-stu-id="16dac-413">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="16dac-414">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="16dac-414">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="16dac-415">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="16dac-415">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="16dac-416">**Token-ring IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="16dac-416">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="16dac-417">**ANSI X3T 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="16dac-417">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="16dac-418">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="16dac-418">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="16dac-419">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="16dac-419">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="16dac-420">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="16dac-420">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="16dac-421">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="16dac-421">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="16dac-422">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="16dac-422">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="16dac-423">**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="16dac-423">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="16dac-424">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="16dac-424">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="16dac-425">**ATA/IDE avanzato** (42)</span><span class="sxs-lookup"><span data-stu-id="16dac-425">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="16dac-426">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="16dac-426">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="16dac-427">**TWIRP (infrarossi bidirezionali)** (44)</span><span class="sxs-lookup"><span data-stu-id="16dac-427">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="16dac-428">**FIR (infrarossi veloci)** (45)</span><span class="sxs-lookup"><span data-stu-id="16dac-428">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="16dac-429">**Sir (Serial Infrared)** (46)</span><span class="sxs-lookup"><span data-stu-id="16dac-429">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="16dac-430">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="16dac-430">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="16dac-431">**Status**</span><span class="sxs-lookup"><span data-stu-id="16dac-431">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16dac-432">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="16dac-432">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16dac-433">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="16dac-433">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16dac-434">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="16dac-434">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="16dac-435">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="16dac-435">Current status of the object.</span></span> <span data-ttu-id="16dac-436">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="16dac-436">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="16dac-437">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="16dac-437">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="16dac-438">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="16dac-438">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="16dac-439">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="16dac-439">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="16dac-440">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="16dac-440">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="16dac-441">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="16dac-441">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="16dac-442">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="16dac-442">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="16dac-443">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="16dac-443">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="16dac-444">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="16dac-444">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="16dac-445">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="16dac-445">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="16dac-446">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="16dac-446">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="16dac-447">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="16dac-447">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="16dac-448">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="16dac-448">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="16dac-449">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="16dac-449">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="16dac-450">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="16dac-450">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="16dac-451">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="16dac-451">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="16dac-452">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="16dac-452">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="16dac-453">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="16dac-453">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="16dac-454">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="16dac-454">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="16dac-455">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="16dac-455">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16dac-456">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="16dac-456">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="16dac-457">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="16dac-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16dac-458">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="16dac-458">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="16dac-459">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="16dac-459">State of the logical device.</span></span> <span data-ttu-id="16dac-460">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="16dac-460">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="16dac-461">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="16dac-461">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="16dac-462">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="16dac-462">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="16dac-463">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="16dac-463">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="16dac-464">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="16dac-464">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="16dac-465">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="16dac-465">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="16dac-466">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="16dac-466">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="16dac-467">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="16dac-467">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16dac-468">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="16dac-468">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16dac-469">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="16dac-469">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16dac-470">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="16dac-470">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="16dac-471">Valore della proprietà **CreationClassName** del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="16dac-471">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="16dac-472">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="16dac-472">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="16dac-473">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="16dac-473">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16dac-474">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="16dac-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16dac-475">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="16dac-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16dac-476">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="16dac-476">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="16dac-477">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="16dac-477">Name of the scoping system.</span></span>

<span data-ttu-id="16dac-478">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="16dac-478">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="16dac-479">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="16dac-479">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16dac-480">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="16dac-480">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="16dac-481">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="16dac-481">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16dac-482">Data e ora dell'ultima reimpostazione del controller.</span><span class="sxs-lookup"><span data-stu-id="16dac-482">Date and time the controller was last reset.</span></span> <span data-ttu-id="16dac-483">Questo potrebbe significare che il controller è stato spento o reinizializzato.</span><span class="sxs-lookup"><span data-stu-id="16dac-483">This could mean the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="16dac-484">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="16dac-484">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="16dac-485">Commenti</span><span class="sxs-lookup"><span data-stu-id="16dac-485">Remarks</span></span>

<span data-ttu-id="16dac-486">La classe **Win32 \_ FloppyController** è derivata dal [**\_ controller CIM**](cim-controller.md) che deriva da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="16dac-486">The **Win32\_FloppyController** class is derived from [**CIM\_Controller**](cim-controller.md) which derives from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="16dac-487">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16dac-487">Requirements</span></span>



| <span data-ttu-id="16dac-488">Requisito</span><span class="sxs-lookup"><span data-stu-id="16dac-488">Requirement</span></span> | <span data-ttu-id="16dac-489">Valore</span><span class="sxs-lookup"><span data-stu-id="16dac-489">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16dac-490">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16dac-490">Minimum supported client</span></span><br/> | <span data-ttu-id="16dac-491">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="16dac-491">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="16dac-492">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16dac-492">Minimum supported server</span></span><br/> | <span data-ttu-id="16dac-493">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="16dac-493">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="16dac-494">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="16dac-494">End of client support</span></span><br/>    | <span data-ttu-id="16dac-495">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="16dac-495">Windows 8.1</span></span><br/>                                                                  |
| <span data-ttu-id="16dac-496">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="16dac-496">End of server support</span></span><br/>    | <span data-ttu-id="16dac-497">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="16dac-497">Windows Server 2012 R2</span></span><br/>                                                       |
| <span data-ttu-id="16dac-498">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="16dac-498">Namespace</span></span><br/>                | <span data-ttu-id="16dac-499">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="16dac-499">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="16dac-500">MOF</span><span class="sxs-lookup"><span data-stu-id="16dac-500">MOF</span></span><br/>                      | <dl> <span data-ttu-id="16dac-501"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="16dac-501"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="16dac-502">DLL</span><span class="sxs-lookup"><span data-stu-id="16dac-502">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16dac-503"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16dac-503"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16dac-504">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="16dac-504">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16dac-505">**\_Controller CIM**</span><span class="sxs-lookup"><span data-stu-id="16dac-505">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> <dt>

[<span data-ttu-id="16dac-506">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="16dac-506">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 


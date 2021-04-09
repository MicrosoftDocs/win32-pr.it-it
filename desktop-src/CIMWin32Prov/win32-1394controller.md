---
description: Rappresenta le funzionalità e la gestione di un controller 1394.
ms.assetid: 5297b1d1-65b5-4bb7-add4-9dc07b4ddc6c
ms.tgt_platform: multiple
title: Classe Win32_1394Controller
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_1394Controller
- Win32_1394Controller.Reset
- Win32_1394Controller.SetPowerState
- Win32_1394Controller.Availability
- Win32_1394Controller.Caption
- Win32_1394Controller.ConfigManagerErrorCode
- Win32_1394Controller.ConfigManagerUserConfig
- Win32_1394Controller.CreationClassName
- Win32_1394Controller.Description
- Win32_1394Controller.DeviceID
- Win32_1394Controller.ErrorCleared
- Win32_1394Controller.ErrorDescription
- Win32_1394Controller.InstallDate
- Win32_1394Controller.LastErrorCode
- Win32_1394Controller.Manufacturer
- Win32_1394Controller.MaxNumberControlled
- Win32_1394Controller.Name
- Win32_1394Controller.PNPDeviceID
- Win32_1394Controller.PowerManagementCapabilities
- Win32_1394Controller.PowerManagementSupported
- Win32_1394Controller.ProtocolSupported
- Win32_1394Controller.Status
- Win32_1394Controller.StatusInfo
- Win32_1394Controller.SystemCreationClassName
- Win32_1394Controller.SystemName
- Win32_1394Controller.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c788469e258a79e70bcc8311c26b43e1f24c26e1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966300"
---
# <a name="win32_1394controller-class"></a><span data-ttu-id="9c04f-103">Win32 \_ 1394Controller (classe)</span><span class="sxs-lookup"><span data-stu-id="9c04f-103">Win32\_1394Controller class</span></span>

<span data-ttu-id="9c04f-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ 1394Controller Win32** rappresenta le funzionalità e la gestione di un controller 1394.</span><span class="sxs-lookup"><span data-stu-id="9c04f-104">The **Win32\_1394Controller** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the capabilities and management of a 1394 controller.</span></span> <span data-ttu-id="9c04f-105">IEEE 1394 è una specifica per un bus seriale ad alta velocità.</span><span class="sxs-lookup"><span data-stu-id="9c04f-105">IEEE 1394 is a specification for a high-speed serial bus.</span></span>

<span data-ttu-id="9c04f-106">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="9c04f-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="9c04f-107">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="9c04f-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c04f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9c04f-108">Syntax</span></span>

``` syntax
[dynamic, provider("CIMWin32"), UUID("{2A7DC003-BAEF-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class Win32_1394Controller : CIM_Controller
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

## <a name="members"></a><span data-ttu-id="9c04f-109">Members</span><span class="sxs-lookup"><span data-stu-id="9c04f-109">Members</span></span>

<span data-ttu-id="9c04f-110">La classe **Win32 \_ 1394Controller** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9c04f-110">The **Win32\_1394Controller** class has these types of members:</span></span>

-   [<span data-ttu-id="9c04f-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="9c04f-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="9c04f-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9c04f-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9c04f-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="9c04f-113">Methods</span></span>

<span data-ttu-id="9c04f-114">La classe **Win32 \_ 1394Controller** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="9c04f-114">The **Win32\_1394Controller** class has these methods.</span></span>



| <span data-ttu-id="9c04f-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="9c04f-115">Method</span></span>            | <span data-ttu-id="9c04f-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9c04f-116">Description</span></span>                                                                                                                                                                                                |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c04f-117">**Reimpostazione**</span><span class="sxs-lookup"><span data-stu-id="9c04f-117">**Reset**</span></span>         | <span data-ttu-id="9c04f-118">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="9c04f-118">Not implemented.</span></span> <span data-ttu-id="9c04f-119">Per implementare questo metodo, vedere il metodo [**Reset**](reset-method-in-class-cim-controller.md) nel [**\_ controller CIM**](cim-controller.md) per la documentazione.</span><span class="sxs-lookup"><span data-stu-id="9c04f-119">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_Controller**](cim-controller.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="9c04f-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="9c04f-120">**SetPowerState**</span></span> | <span data-ttu-id="9c04f-121">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="9c04f-121">Not implemented.</span></span> <span data-ttu-id="9c04f-122">Per implementare questo metodo, vedere il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) nel [**\_ controller CIM**](cim-controller.md) per la documentazione.</span><span class="sxs-lookup"><span data-stu-id="9c04f-122">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_Controller**](cim-controller.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9c04f-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9c04f-123">Properties</span></span>

<span data-ttu-id="9c04f-124">La classe **Win32 \_ 1394Controller** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9c04f-124">The **Win32\_1394Controller** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9c04f-125">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="9c04f-125">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c04f-126">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9c04f-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c04f-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-128">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="9c04f-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="9c04f-129">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c04f-129">Availability and status of the device.</span></span>

<span data-ttu-id="9c04f-130">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9c04f-130">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9c04f-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="9c04f-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9c04f-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="9c04f-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="9c04f-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="9c04f-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-134">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="9c04f-134">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="9c04f-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="9c04f-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="9c04f-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="9c04f-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="9c04f-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="9c04f-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="9c04f-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="9c04f-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="9c04f-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="9c04f-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="9c04f-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="9c04f-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9c04f-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="9c04f-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="9c04f-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="9c04f-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="9c04f-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="9c04f-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="9c04f-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="9c04f-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-145">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="9c04f-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="9c04f-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="9c04f-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-147">Il dispositivo è in uno stato di risparmio energia, ma è ancora funzionante e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="9c04f-147">The device is in a power save state but is still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="9c04f-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="9c04f-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-149">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="9c04f-149">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="9c04f-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="9c04f-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="9c04f-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="9c04f-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-152">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="9c04f-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="9c04f-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="9c04f-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-154">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="9c04f-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="9c04f-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="9c04f-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-156">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="9c04f-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="9c04f-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="9c04f-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-158">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="9c04f-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="9c04f-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="9c04f-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-160">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="9c04f-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9c04f-161">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="9c04f-161">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c04f-162">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9c04f-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c04f-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-164">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="9c04f-164">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="9c04f-165">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9c04f-165">Short description of the object.</span></span>

<span data-ttu-id="9c04f-166">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9c04f-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c04f-167">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="9c04f-167">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c04f-168">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c04f-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c04f-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-170">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9c04f-170">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9c04f-171">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="9c04f-171">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="9c04f-172">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9c04f-172">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="9c04f-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="9c04f-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="9c04f-174"> (0)</span><span class="sxs-lookup"><span data-stu-id="9c04f-174">(0)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-175">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="9c04f-175">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="9c04f-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="9c04f-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="9c04f-177">(1)</span><span class="sxs-lookup"><span data-stu-id="9c04f-177">(1)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-178">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="9c04f-178">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9c04f-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9c04f-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="9c04f-180">(2)</span><span class="sxs-lookup"><span data-stu-id="9c04f-180">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="9c04f-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="9c04f-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="9c04f-182">(3)</span><span class="sxs-lookup"><span data-stu-id="9c04f-182">(3)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-183">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="9c04f-183">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="9c04f-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="9c04f-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="9c04f-185">(4)</span><span class="sxs-lookup"><span data-stu-id="9c04f-185">(4)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-186">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="9c04f-186">Device is not working properly.</span></span> <span data-ttu-id="9c04f-187">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="9c04f-187">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="9c04f-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="9c04f-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="9c04f-189">(5)</span><span class="sxs-lookup"><span data-stu-id="9c04f-189">(5)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-190">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="9c04f-190">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="9c04f-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="9c04f-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="9c04f-192"> (6)</span><span class="sxs-lookup"><span data-stu-id="9c04f-192">(6)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-193">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="9c04f-193">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="9c04f-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="9c04f-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="9c04f-195">(7)</span><span class="sxs-lookup"><span data-stu-id="9c04f-195">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="9c04f-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="9c04f-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="9c04f-197">(8)</span><span class="sxs-lookup"><span data-stu-id="9c04f-197">(8)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-198">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="9c04f-198">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="9c04f-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="9c04f-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="9c04f-200">(9)</span><span class="sxs-lookup"><span data-stu-id="9c04f-200">(9)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-201">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="9c04f-201">Device is not working properly.</span></span> <span data-ttu-id="9c04f-202">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c04f-202">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="9c04f-203"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9c04f-203"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="9c04f-204">(10)</span><span class="sxs-lookup"><span data-stu-id="9c04f-204">(10)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-205">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c04f-205">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="9c04f-206"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9c04f-206"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="9c04f-207">(11)</span><span class="sxs-lookup"><span data-stu-id="9c04f-207">(11)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-208">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c04f-208">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="9c04f-209"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="9c04f-209"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="9c04f-210">12</span><span class="sxs-lookup"><span data-stu-id="9c04f-210">(12)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-211">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="9c04f-211">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="9c04f-212"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9c04f-212"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="9c04f-213">(13)</span><span class="sxs-lookup"><span data-stu-id="9c04f-213">(13)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-214">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c04f-214">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="9c04f-215"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="9c04f-215"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="9c04f-216">(14)</span><span class="sxs-lookup"><span data-stu-id="9c04f-216">(14)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-217">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="9c04f-217">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="9c04f-218"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="9c04f-218"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="9c04f-219">(15)</span><span class="sxs-lookup"><span data-stu-id="9c04f-219">(15)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-220">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="9c04f-220">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="9c04f-221"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9c04f-221"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="9c04f-222">(16)</span><span class="sxs-lookup"><span data-stu-id="9c04f-222">(16)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-223">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c04f-223">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="9c04f-224"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="9c04f-224"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="9c04f-225">(17)</span><span class="sxs-lookup"><span data-stu-id="9c04f-225">(17)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-226">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="9c04f-226">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9c04f-227"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9c04f-227"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="9c04f-228">(18)</span><span class="sxs-lookup"><span data-stu-id="9c04f-228">(18)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-229">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c04f-229">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="9c04f-230"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="9c04f-230"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="9c04f-231">(19)</span><span class="sxs-lookup"><span data-stu-id="9c04f-231">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="9c04f-232"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="9c04f-232"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="9c04f-233">(20)</span><span class="sxs-lookup"><span data-stu-id="9c04f-233">(20)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-234">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="9c04f-234">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="9c04f-235"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9c04f-235"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="9c04f-236">(21)</span><span class="sxs-lookup"><span data-stu-id="9c04f-236">(21)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-237">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="9c04f-237">System failure.</span></span> <span data-ttu-id="9c04f-238">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="9c04f-238">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="9c04f-239">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c04f-239">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="9c04f-240"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="9c04f-240"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="9c04f-241">(22)</span><span class="sxs-lookup"><span data-stu-id="9c04f-241">(22)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-242">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="9c04f-242">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="9c04f-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="9c04f-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="9c04f-244">(23)</span><span class="sxs-lookup"><span data-stu-id="9c04f-244">(23)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-245">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="9c04f-245">System failure.</span></span> <span data-ttu-id="9c04f-246">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="9c04f-246">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="9c04f-247"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="9c04f-247"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="9c04f-248">(24)</span><span class="sxs-lookup"><span data-stu-id="9c04f-248">(24)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-249">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="9c04f-249">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="9c04f-250"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9c04f-250"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="9c04f-251">(25)</span><span class="sxs-lookup"><span data-stu-id="9c04f-251">(25)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-252">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c04f-252">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="9c04f-253"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9c04f-253"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="9c04f-254">(26)</span><span class="sxs-lookup"><span data-stu-id="9c04f-254">(26)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-255">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c04f-255">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="9c04f-256"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="9c04f-256"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="9c04f-257">(27)</span><span class="sxs-lookup"><span data-stu-id="9c04f-257">(27)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-258">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="9c04f-258">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="9c04f-259"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="9c04f-259"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="9c04f-260">(28)</span><span class="sxs-lookup"><span data-stu-id="9c04f-260">(28)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-261">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="9c04f-261">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="9c04f-262"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="9c04f-262"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="9c04f-263">(29)</span><span class="sxs-lookup"><span data-stu-id="9c04f-263">(29)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-264">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="9c04f-264">Device is disabled.</span></span> <span data-ttu-id="9c04f-265">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="9c04f-265">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="9c04f-266"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9c04f-266"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="9c04f-267">(30)</span><span class="sxs-lookup"><span data-stu-id="9c04f-267">(30)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-268">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c04f-268">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9c04f-269"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9c04f-269"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="9c04f-270">31</span><span class="sxs-lookup"><span data-stu-id="9c04f-270">(31)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-271">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="9c04f-271">Device is not working properly.</span></span> <span data-ttu-id="9c04f-272">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="9c04f-272">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9c04f-273">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="9c04f-273">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c04f-274">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="9c04f-274">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-275">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c04f-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-276">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9c04f-276">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9c04f-277">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="9c04f-277">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="9c04f-278">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9c04f-278">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c04f-279">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9c04f-279">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c04f-280">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9c04f-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-281">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c04f-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-282">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9c04f-282">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9c04f-283">Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="9c04f-283">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="9c04f-284">Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="9c04f-284">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="9c04f-285">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9c04f-285">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c04f-286">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="9c04f-286">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c04f-287">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9c04f-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-288">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c04f-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-289">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="9c04f-289">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="9c04f-290">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9c04f-290">Description of the object.</span></span>

<span data-ttu-id="9c04f-291">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9c04f-291">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c04f-292">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="9c04f-292">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c04f-293">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9c04f-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-294">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c04f-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-295">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="9c04f-295">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="9c04f-296">Identificatore univoco del controller.</span><span class="sxs-lookup"><span data-stu-id="9c04f-296">Unique identifier of this controller.</span></span>

<span data-ttu-id="9c04f-297">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9c04f-297">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c04f-298">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="9c04f-298">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c04f-299">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="9c04f-299">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-300">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c04f-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c04f-301">Se **true**, l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="9c04f-301">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="9c04f-302">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9c04f-302">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c04f-303">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="9c04f-303">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c04f-304">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9c04f-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-305">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c04f-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c04f-306">Altre informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="9c04f-306">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="9c04f-307">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9c04f-307">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c04f-308">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9c04f-308">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c04f-309">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9c04f-309">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-310">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c04f-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-311">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="9c04f-311">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="9c04f-312">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9c04f-312">Date and time the object was installed.</span></span> <span data-ttu-id="9c04f-313">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="9c04f-313">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="9c04f-314">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9c04f-314">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c04f-315">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="9c04f-315">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c04f-316">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c04f-316">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-317">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c04f-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c04f-318">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="9c04f-318">Last error code reported by the logical device.</span></span>

<span data-ttu-id="9c04f-319">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9c04f-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c04f-320">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="9c04f-320">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c04f-321">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9c04f-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-322">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c04f-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-323">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="9c04f-323">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="9c04f-324">Produttore del controller.</span><span class="sxs-lookup"><span data-stu-id="9c04f-324">Manufacturer of the controller.</span></span>

</dd> <dt>

<span data-ttu-id="9c04f-325">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="9c04f-325">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c04f-326">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c04f-326">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-327">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c04f-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-328">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta bus DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="9c04f-328">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="9c04f-329">Numero massimo di entità indirizzabili direttamente supportato da questo controller.</span><span class="sxs-lookup"><span data-stu-id="9c04f-329">Maximum number of directly addressable entities supportable by this controller.</span></span> <span data-ttu-id="9c04f-330">Se il numero è sconosciuto, è necessario usare un valore pari a 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="9c04f-330">A value of 0 (zero) should be used if the number is unknown.</span></span>

<span data-ttu-id="9c04f-331">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="9c04f-331">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c04f-332">**Nome**</span><span class="sxs-lookup"><span data-stu-id="9c04f-332">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c04f-333">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9c04f-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-334">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c04f-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-335">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="9c04f-335">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="9c04f-336">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="9c04f-336">Label by which the object is known.</span></span> <span data-ttu-id="9c04f-337">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="9c04f-337">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="9c04f-338">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9c04f-338">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c04f-339">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="9c04f-339">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c04f-340">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9c04f-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-341">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c04f-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-342">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9c04f-342">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9c04f-343">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="9c04f-343">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="9c04f-344">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9c04f-344">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="9c04f-345">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="9c04f-345">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="9c04f-346">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="9c04f-346">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c04f-347">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9c04f-347">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-348">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c04f-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c04f-349">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="9c04f-349">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="9c04f-350">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="9c04f-350">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9c04f-351"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="9c04f-351"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="9c04f-352"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="9c04f-352"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9c04f-353"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="9c04f-353"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9c04f-354"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="9c04f-354"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-355">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="9c04f-355">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="9c04f-356"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="9c04f-356"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-357">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="9c04f-357">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="9c04f-358"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="9c04f-358"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-359">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="9c04f-359">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="9c04f-360">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="9c04f-360">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="9c04f-361">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="9c04f-361">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="9c04f-362"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="9c04f-362"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-363">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="9c04f-363">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="9c04f-364"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="9c04f-364"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="9c04f-365">Tempo Power-On supportato</span><span class="sxs-lookup"><span data-stu-id="9c04f-365">Timed Power-On Supported</span></span>

<span data-ttu-id="9c04f-366">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="9c04f-366">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9c04f-367">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="9c04f-367">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c04f-368">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="9c04f-368">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-369">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c04f-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c04f-370">Se **true**, il dispositivo può essere gestito dal risparmio di energia (può essere impostato in modalità di sospensione e così via).</span><span class="sxs-lookup"><span data-stu-id="9c04f-370">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="9c04f-371">La proprietà non indica che le funzionalità di risparmio energia sono attualmente abilitate, solo che il dispositivo logico è in grado di gestire il risparmio di energia.</span><span class="sxs-lookup"><span data-stu-id="9c04f-371">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="9c04f-372">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9c04f-372">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c04f-373">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="9c04f-373">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c04f-374">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9c04f-374">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-375">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c04f-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-376">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta bus DMTF \| 001,2 "," MIF. \|Dischi DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="9c04f-376">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="9c04f-377">Protocollo usato dal controller per accedere ai dispositivi "controllati".</span><span class="sxs-lookup"><span data-stu-id="9c04f-377">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="9c04f-378">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="9c04f-378">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9c04f-379">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="9c04f-379">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9c04f-380">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="9c04f-380">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="9c04f-381">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="9c04f-381">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="9c04f-382">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="9c04f-382">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="9c04f-383">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="9c04f-383">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="9c04f-384">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="9c04f-384">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="9c04f-385">**Dischetto flessibile** (7)</span><span class="sxs-lookup"><span data-stu-id="9c04f-385">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="9c04f-386">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="9c04f-386">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="9c04f-387">**Interfaccia parallela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="9c04f-387">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="9c04f-388">**Protocollo di Fibre Channel SCSI** (10)</span><span class="sxs-lookup"><span data-stu-id="9c04f-388">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="9c04f-389">**Protocollo bus seriale SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="9c04f-389">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="9c04f-390">**Protocollo bus seriale SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="9c04f-390">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="9c04f-391">**Architettura di archiviazione seriale SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="9c04f-391">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="9c04f-392">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="9c04f-392">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="9c04f-393">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="9c04f-393">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="9c04f-394">**Bus seriale universale** (16)</span><span class="sxs-lookup"><span data-stu-id="9c04f-394">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="9c04f-395">**Protocollo parallelo** (17)</span><span class="sxs-lookup"><span data-stu-id="9c04f-395">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="9c04f-396">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="9c04f-396">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="9c04f-397">**Diagnostica** (19)</span><span class="sxs-lookup"><span data-stu-id="9c04f-397">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="9c04f-398">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="9c04f-398">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="9c04f-399">**Potenza** (21)</span><span class="sxs-lookup"><span data-stu-id="9c04f-399">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="9c04f-400">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="9c04f-400">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="9c04f-401">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="9c04f-401">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="9c04f-402">**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="9c04f-402">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="9c04f-403">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="9c04f-403">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="9c04f-404">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="9c04f-404">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="9c04f-405">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="9c04f-405">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="9c04f-406">**IEEE 802,3 10Base5** (28)</span><span class="sxs-lookup"><span data-stu-id="9c04f-406">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="9c04f-407">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="9c04f-407">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="9c04f-408">**IEEE 802,3 1Base5** (30)</span><span class="sxs-lookup"><span data-stu-id="9c04f-408">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="9c04f-409">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="9c04f-409">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="9c04f-410">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="9c04f-410">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="9c04f-411">**Token-ring IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="9c04f-411">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="9c04f-412">**ANSI X3T 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="9c04f-412">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="9c04f-413">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="9c04f-413">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="9c04f-414">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="9c04f-414">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="9c04f-415">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="9c04f-415">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="9c04f-416">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="9c04f-416">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="9c04f-417">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="9c04f-417">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="9c04f-418">**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="9c04f-418">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="9c04f-419">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="9c04f-419">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="9c04f-420">**ATA/IDE avanzato** (42)</span><span class="sxs-lookup"><span data-stu-id="9c04f-420">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="9c04f-421">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="9c04f-421">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="9c04f-422">**TWIRP (infrarossi bidirezionali)** (44)</span><span class="sxs-lookup"><span data-stu-id="9c04f-422">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="9c04f-423">**FIR (infrarossi veloci)** (45)</span><span class="sxs-lookup"><span data-stu-id="9c04f-423">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="9c04f-424">**Sir (Serial Infrared)** (46)</span><span class="sxs-lookup"><span data-stu-id="9c04f-424">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="9c04f-425">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="9c04f-425">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9c04f-426">**Status**</span><span class="sxs-lookup"><span data-stu-id="9c04f-426">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c04f-427">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9c04f-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-428">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c04f-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-429">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="9c04f-429">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="9c04f-430">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9c04f-430">Current status of the object.</span></span> <span data-ttu-id="9c04f-431">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="9c04f-431">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="9c04f-432">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="9c04f-432">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="9c04f-433">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="9c04f-433">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="9c04f-434">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="9c04f-434">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="9c04f-435">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="9c04f-435">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="9c04f-436">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9c04f-436">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="9c04f-437">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="9c04f-437">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="9c04f-438">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="9c04f-438">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="9c04f-439">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="9c04f-439">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9c04f-440">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="9c04f-440">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9c04f-441">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="9c04f-441">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="9c04f-442">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="9c04f-442">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="9c04f-443">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="9c04f-443">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="9c04f-444">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="9c04f-444">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9c04f-445">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="9c04f-445">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="9c04f-446">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="9c04f-446">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="9c04f-447">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="9c04f-447">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="9c04f-448">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="9c04f-448">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="9c04f-449">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="9c04f-449">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9c04f-450">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="9c04f-450">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c04f-451">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9c04f-451">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-452">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c04f-452">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-453">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="9c04f-453">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="9c04f-454">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="9c04f-454">State of the logical device.</span></span> <span data-ttu-id="9c04f-455">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="9c04f-455">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="9c04f-456">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9c04f-456">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9c04f-457">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="9c04f-457">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9c04f-458">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="9c04f-458">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9c04f-459">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="9c04f-459">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9c04f-460">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="9c04f-460">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="9c04f-461">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="9c04f-461">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9c04f-462">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9c04f-462">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c04f-463">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9c04f-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-464">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c04f-464">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-465">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9c04f-465">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9c04f-466">Valore per la proprietà **CreationClassName** del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="9c04f-466">Value for the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="9c04f-467">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9c04f-467">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c04f-468">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="9c04f-468">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c04f-469">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9c04f-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-470">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c04f-470">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-471">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9c04f-471">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9c04f-472">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="9c04f-472">Name of the scoping system.</span></span>

<span data-ttu-id="9c04f-473">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9c04f-473">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c04f-474">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="9c04f-474">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c04f-475">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9c04f-475">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9c04f-476">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c04f-476">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c04f-477">Data e ora dell'ultima reimpostazione del controller.</span><span class="sxs-lookup"><span data-stu-id="9c04f-477">Date and time controller was last reset.</span></span> <span data-ttu-id="9c04f-478">Questo potrebbe significare che il controller è stato spento o reinizializzato.</span><span class="sxs-lookup"><span data-stu-id="9c04f-478">This could mean the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="9c04f-479">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="9c04f-479">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9c04f-480">Commenti</span><span class="sxs-lookup"><span data-stu-id="9c04f-480">Remarks</span></span>

<span data-ttu-id="9c04f-481">La classe **Win32 \_ 1394Controller** è derivata dal [**\_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="9c04f-481">The **Win32\_1394Controller** class is derived from [**CIM\_Controller**](cim-controller.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9c04f-482">Esempio</span><span class="sxs-lookup"><span data-stu-id="9c04f-482">Examples</span></span>

<span data-ttu-id="9c04f-483">L'esempio di codice PowerShell seguente recupera le informazioni sul controller.</span><span class="sxs-lookup"><span data-stu-id="9c04f-483">The following PowerShell code sample retrieves controller information.</span></span>


```PowerShell
  function Get-Availability {
param ([uint16] $char)
# Helper function to return characterics of the 1394 Controller
# parse and return values
 If ($char -ge 1 -and $char -le 17) {
   switch ($char) {
  1  {"01-Other"}
  2  {"02-Unkown"}
  3  {"03-Running/Full Power"}
  4  {"04-Warning"}
  5  {"05-In Test"}
  6  {"06-Not Applicable"}
  7  {"07-POwer Off"}
  8  {"08-Off  Line"}
  9  {"09-Off Duty"}
  10  {"10-Degraded"}
  11  {"11-Not Installed"}
  12  {"12-InstallError"}
  13  {"13-Power Save - Unknown"}
  14  {"14-Power Save - Low Power Mode"}
  15  {"15-Power Save - Standby"}
  16  {"16-Power Cycle"}
  17  {"17-Power Save - Warning"}
}
}

Else
 {"{0} - invalid code" -f $char}
 Return
 }

# Get Controller information from WMI
$controllers = Get-WMIObject Win32_1394Controller
    # Display Details
"Win32_1394 WMI Information"
"--------------------------"
$count=$controllers.count
if (!$count) {$count++} 
"{0} 1394 controller(s) found" -f $count
""
"Controller {0} - Characteristics" -f ++$i
"--------------------------------"
foreach ($cont in $controllers) {
$avail=Get-Availability($cont.availability)
"Availability                :  {0}" -f $avail
"Caption                     :  {0}" -f $cont.caption
"Config Manager Error Code   :  {0}" -f $cont.ConfigManagerErrorCode
"Config Manager User Config  :  {0}" -f $cont.ConfigManagerUserConfig 
"Creation Class Name         :  {0}" -f $cont.CreationClassName
"Description                 :  {0}" -f $cont.Description
"Device ID                   :  {0}" -f $cont.DeviceID
"Error Cleared               :  {0}" -f $cont.ErrorCleared
"Error Description           :  {0}" -f $cont.ErrorDescription
"InstallDate                 :  {0}" -f $cont.InstallDate 
"Last Error Code             :  {0}" -f $cont.LastErrorCode
"Manufacturer                :  {0}" -f $cont.Manufacturer
"MaxNumberControlled         :  {0}" -f $cont.MaxNumberControlled
"Name                        :  {0}" -f $cont.Name
"PNPDeviceID                 :  {0}" -f $cont.PNPDeviceId
"PowerManagementCapabilities :  {0}" -f $cont.PowerManagementCapabilities
"PowerManagementSupported    :  {0}" -f $cont.PowerManagementSupported
"Protocols Supported         :  {0}" -f $cont.ProtocolsSupported
"Status                      :  {0}" -f $cont.Status
"Status Information          :  {0}" -f $cont.StatusInfo
"System Creation Class Name  :  {0}" -f $cont.SystemCreationClassName
"System Name                 :  {0}" -f $cont.SystemName
"Time of Last Reset          :  {0}" -f $cont.TimeOfLastReset
""
}
```



<span data-ttu-id="9c04f-484">Nell'esempio di codice precedente vengono restituite le informazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="9c04f-484">The previous code sample returns the following information:</span></span>

``` syntax
## Win32_1394 WMI Information

1 1394 controller(s) found

## Controller 1 - Characteristics

Availability                :  0 - invalid code
Caption                     :  OHCI Compliant IEEE 1394 Host Controller
Config Manager Error Code   :  0
Config Manager User Config  :  False
Creation Class Name         :  Win32_1394Controller
Description                 :  OHCI Compliant IEEE 1394 Host Controller
Device ID                   :  PCI\VEN_1217&DEV_00F7&SUBSYS_01CC1028&REV_02\4&2FE911E8&0&0CF0
Error Cleared               :
Error Description           :
InstallDate                 :
Last Error Code             :
Manufacturer                :  IEEE 1394 OHCI Compliant Host Controller Vendor
MaxNumberControlled         :
Name                        :  OHCI Compliant IEEE 1394 Host Controller
PNPDeviceID                 :  PCI\VEN_1217&DEV_00F7&SUBSYS_01CC1028&REV_02\4&2FE911E8&0&0CF0
PowerManagementCapabilities :
PowerManagementSupported    :
Protocols Supported         :
Status                      :  OK
Status Information          :
System Creation Class Name  :  Win32_ComputerSystem
System Name                 :  UK0N055
Time of Last Reset          :
```

## <a name="requirements"></a><span data-ttu-id="9c04f-485">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9c04f-485">Requirements</span></span>



| <span data-ttu-id="9c04f-486">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c04f-486">Requirement</span></span> | <span data-ttu-id="9c04f-487">Valore</span><span class="sxs-lookup"><span data-stu-id="9c04f-487">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c04f-488">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c04f-488">Minimum supported client</span></span><br/> | <span data-ttu-id="9c04f-489">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c04f-489">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9c04f-490">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c04f-490">Minimum supported server</span></span><br/> | <span data-ttu-id="9c04f-491">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9c04f-491">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9c04f-492">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9c04f-492">Namespace</span></span><br/>                | <span data-ttu-id="9c04f-493">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="9c04f-493">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9c04f-494">MOF</span><span class="sxs-lookup"><span data-stu-id="9c04f-494">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9c04f-495"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9c04f-495"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9c04f-496">DLL</span><span class="sxs-lookup"><span data-stu-id="9c04f-496">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c04f-497"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c04f-497"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c04f-498">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9c04f-498">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c04f-499">**\_Controller CIM**</span><span class="sxs-lookup"><span data-stu-id="9c04f-499">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> <dt>

[<span data-ttu-id="9c04f-500">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="9c04f-500">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 


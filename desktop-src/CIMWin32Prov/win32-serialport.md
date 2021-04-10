---
description: La \_ classe WMI SerialPort Win32 rappresenta una porta seriale in un sistema di computer che esegue Windows.
ms.assetid: f2e5cc5a-a12b-4079-92e1-6bb62fe797a0
ms.tgt_platform: multiple
title: Classe Win32_SerialPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SerialPort
- Win32_SerialPort.Reset
- Win32_SerialPort.SetPowerState
- Win32_SerialPort.Availability
- Win32_SerialPort.Binary
- Win32_SerialPort.Capabilities
- Win32_SerialPort.CapabilityDescriptions
- Win32_SerialPort.Caption
- Win32_SerialPort.ConfigManagerErrorCode
- Win32_SerialPort.ConfigManagerUserConfig
- Win32_SerialPort.CreationClassName
- Win32_SerialPort.Description
- Win32_SerialPort.DeviceID
- Win32_SerialPort.ErrorCleared
- Win32_SerialPort.ErrorDescription
- Win32_SerialPort.InstallDate
- Win32_SerialPort.LastErrorCode
- Win32_SerialPort.MaxBaudRate
- Win32_SerialPort.MaximumInputBufferSize
- Win32_SerialPort.MaximumOutputBufferSize
- Win32_SerialPort.MaxNumberControlled
- Win32_SerialPort.Name
- Win32_SerialPort.OSAutoDiscovered
- Win32_SerialPort.PNPDeviceID
- Win32_SerialPort.PowerManagementCapabilities
- Win32_SerialPort.PowerManagementSupported
- Win32_SerialPort.ProtocolSupported
- Win32_SerialPort.ProviderType
- Win32_SerialPort.SettableBaudRate
- Win32_SerialPort.SettableDataBits
- Win32_SerialPort.SettableFlowControl
- Win32_SerialPort.SettableParity
- Win32_SerialPort.SettableParityCheck
- Win32_SerialPort.SettableRLSD
- Win32_SerialPort.SettableStopBits
- Win32_SerialPort.Status
- Win32_SerialPort.StatusInfo
- Win32_SerialPort.Supports16BitMode
- Win32_SerialPort.SupportsDTRDSR
- Win32_SerialPort.SupportsElapsedTimeouts
- Win32_SerialPort.SupportsIntTimeouts
- Win32_SerialPort.SupportsParityCheck
- Win32_SerialPort.SupportsRLSD
- Win32_SerialPort.SupportsRTSCTS
- Win32_SerialPort.SupportsSpecialCharacters
- Win32_SerialPort.SupportsXOnXOff
- Win32_SerialPort.SupportsXOnXOffSet
- Win32_SerialPort.SystemCreationClassName
- Win32_SerialPort.SystemName
- Win32_SerialPort.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b7fc2f25bc88d880ba9b10f10b5efde284a62624
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125988"
---
# <a name="win32_serialport-class"></a><span data-ttu-id="bc53c-103">\_Classe SerialPort Win32</span><span class="sxs-lookup"><span data-stu-id="bc53c-103">Win32\_SerialPort class</span></span>

<span data-ttu-id="bc53c-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ SerialPort Win32** rappresenta una porta seriale in un sistema di computer che esegue Windows.</span><span class="sxs-lookup"><span data-stu-id="bc53c-104">The **Win32\_SerialPort** [WMI class](../wmisdk/retrieving-a-class.md) represents a serial port on a computer system running Windows.</span></span>

<span data-ttu-id="bc53c-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="bc53c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="bc53c-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="bc53c-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc53c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bc53c-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4BF-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SerialPort : CIM_SerialController
{
  uint16   Availability;
  boolean  Binary;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
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
  uint32   MaxBaudRate;
  uint32   MaximumInputBufferSize;
  uint32   MaximumOutputBufferSize;
  uint32   MaxNumberControlled;
  string   Name;
  boolean  OSAutoDiscovered;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtocolSupported;
  string   ProviderType;
  boolean  SettableBaudRate;
  boolean  SettableDataBits;
  boolean  SettableFlowControl;
  boolean  SettableParity;
  boolean  SettableParityCheck;
  boolean  SettableRLSD;
  boolean  SettableStopBits;
  string   Status;
  uint16   StatusInfo;
  boolean  Supports16BitMode;
  boolean  SupportsDTRDSR;
  boolean  SupportsElapsedTimeouts;
  boolean  SupportsIntTimeouts;
  boolean  SupportsParityCheck;
  boolean  SupportsRLSD;
  boolean  SupportsRTSCTS;
  boolean  SupportsSpecialCharacters;
  boolean  SupportsXOnXOff;
  boolean  SupportsXOnXOffSet;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="bc53c-108">Members</span><span class="sxs-lookup"><span data-stu-id="bc53c-108">Members</span></span>

<span data-ttu-id="bc53c-109">La **classe \_ SerialPort Win32** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="bc53c-109">The **Win32\_SerialPort** class has these types of members:</span></span>

-   [<span data-ttu-id="bc53c-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="bc53c-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="bc53c-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bc53c-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bc53c-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="bc53c-112">Methods</span></span>

<span data-ttu-id="bc53c-113">La **classe \_ SerialPort Win32** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="bc53c-113">The **Win32\_SerialPort** class has these methods.</span></span>



| <span data-ttu-id="bc53c-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="bc53c-114">Method</span></span>            | <span data-ttu-id="bc53c-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc53c-115">Description</span></span>                                                                                                                                                                                          |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc53c-116">**Reimpostazione**</span><span class="sxs-lookup"><span data-stu-id="bc53c-116">**Reset**</span></span>         | <span data-ttu-id="bc53c-117">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="bc53c-117">Not implemented.</span></span> <span data-ttu-id="bc53c-118">Per implementare questo metodo, vedere il metodo [**Reset**](reset-method-in-class-cim-controller.md) in [**CIM \_ controller seriale**](cim-serialcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="bc53c-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_SerialController**](cim-serialcontroller.md).</span></span><br/>                 |
| <span data-ttu-id="bc53c-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="bc53c-119">**SetPowerState**</span></span> | <span data-ttu-id="bc53c-120">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="bc53c-120">Not implemented.</span></span> <span data-ttu-id="bc53c-121">Per implementare questo metodo, vedere il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) in [**CIM \_ controller seriale**](cim-serialcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="bc53c-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_SerialController**](cim-serialcontroller.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="bc53c-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bc53c-122">Properties</span></span>

<span data-ttu-id="bc53c-123">La **classe \_ SerialPort Win32** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="bc53c-123">The **Win32\_SerialPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bc53c-124">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="bc53c-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-125">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bc53c-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-127">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="bc53c-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-128">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bc53c-128">Availability and status of the device.</span></span>

<span data-ttu-id="bc53c-129">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bc53c-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bc53c-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="bc53c-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bc53c-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="bc53c-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="bc53c-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="bc53c-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-133">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="bc53c-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="bc53c-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="bc53c-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="bc53c-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="bc53c-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="bc53c-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="bc53c-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="bc53c-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="bc53c-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="bc53c-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="bc53c-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="bc53c-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="bc53c-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="bc53c-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="bc53c-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="bc53c-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="bc53c-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="bc53c-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="bc53c-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="bc53c-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="bc53c-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-144">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="bc53c-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="bc53c-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="bc53c-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-146">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="bc53c-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="bc53c-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="bc53c-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-148">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="bc53c-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="bc53c-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="bc53c-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="bc53c-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="bc53c-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-151">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="bc53c-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="bc53c-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="bc53c-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-153">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="bc53c-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="bc53c-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="bc53c-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-155">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="bc53c-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="bc53c-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="bc53c-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-157">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="bc53c-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="bc53c-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="bc53c-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-159">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="bc53c-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bc53c-160">**Binario**</span><span class="sxs-lookup"><span data-stu-id="bc53c-160">**Binary**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-161">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bc53c-161">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-163">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fBinary")</span><span class="sxs-lookup"><span data-stu-id="bc53c-163">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fBinary")</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-164">Se **true**, la porta seriale è configurata per il trasferimento di dati binari.</span><span class="sxs-lookup"><span data-stu-id="bc53c-164">If **TRUE**, the serial port is configured for binary data transfer.</span></span> <span data-ttu-id="bc53c-165">Poiché l'API Windows non supporta i trasferimenti in modalità non binaria, questa proprietà deve essere **true**.</span><span class="sxs-lookup"><span data-stu-id="bc53c-165">Because the Windows API does not support nonbinary mode transfers, this property must be **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="bc53c-166">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="bc53c-166">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-167">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bc53c-167">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-169">Qualificatori: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Porte seriali DMTF \| 004,7 "), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ controller seriale**](cim-serialcontroller.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="bc53c-169">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Serial Ports\|004.7"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_SerialController**](cim-serialcontroller.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-170">Matrice di compatibilità a livello di chip per il controller seriale.</span><span class="sxs-lookup"><span data-stu-id="bc53c-170">Array of chip-level compatibility for the serial controller.</span></span> <span data-ttu-id="bc53c-171">Questa proprietà descrive il buffering e altre funzionalità del controller seriale che possono essere intrinseche nell'hardware del chip.</span><span class="sxs-lookup"><span data-stu-id="bc53c-171">This property describes the buffering and other capabilities of the serial controller that may be inherent in the chip hardware.</span></span> <span data-ttu-id="bc53c-172">La proprietà è un intero enumerato.</span><span class="sxs-lookup"><span data-stu-id="bc53c-172">The property is an enumerated integer.</span></span>

<span data-ttu-id="bc53c-173">Questa proprietà viene ereditata da [**CIM \_ controller seriale**](cim-serialcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="bc53c-173">This property is inherited from [**CIM\_SerialController**](cim-serialcontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bc53c-174">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="bc53c-174">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bc53c-175">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="bc53c-175">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="XT_AT_Compatible"></span><span id="xt_at_compatible"></span><span id="XT_AT_COMPATIBLE"></span>

<span data-ttu-id="bc53c-176">**XT/AT Compatible** (3)</span><span class="sxs-lookup"><span data-stu-id="bc53c-176">**XT/AT Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="16450_Compatible"></span><span id="16450_compatible"></span><span id="16450_COMPATIBLE"></span>

<span data-ttu-id="bc53c-177">**16450 compatibile** (4)</span><span class="sxs-lookup"><span data-stu-id="bc53c-177">**16450 Compatible** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="16550_Compatible"></span><span id="16550_compatible"></span><span id="16550_COMPATIBLE"></span>

<span data-ttu-id="bc53c-178">**16550 compatibile** (5)</span><span class="sxs-lookup"><span data-stu-id="bc53c-178">**16550 Compatible** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="16550A_Compatible"></span><span id="16550a_compatible"></span><span id="16550A_COMPATIBLE"></span>

<span data-ttu-id="bc53c-179">**compatibile con 16550A** (6)</span><span class="sxs-lookup"><span data-stu-id="bc53c-179">**16550A Compatible** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8251_Compatible"></span><span id="8251_compatible"></span><span id="8251_COMPATIBLE"></span>

<span data-ttu-id="bc53c-180">**8251 compatibile** (160)</span><span class="sxs-lookup"><span data-stu-id="bc53c-180">**8251 Compatible** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="8251FIFO_Compatible"></span><span id="8251fifo_compatible"></span><span id="8251FIFO_COMPATIBLE"></span>

<span data-ttu-id="bc53c-181">**compatibile con 8251FIFO** (161)</span><span class="sxs-lookup"><span data-stu-id="bc53c-181">**8251FIFO Compatible** (161)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bc53c-182">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="bc53c-182">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-183">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="bc53c-183">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-185">Qualificatori: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ controller seriale**](cim-serialcontroller.md).**Funzionalità**")</span><span class="sxs-lookup"><span data-stu-id="bc53c-185">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_SerialController**](cim-serialcontroller.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-186">Matrice di stringhe in formato libero che fornisce spiegazioni più dettagliate per tutte le funzionalità del controller seriale indicate nell'array delle **funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="bc53c-186">Array of free-form strings providing more detailed explanations for any of the serial controller features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="bc53c-187">Si noti che ogni voce di questa matrice è correlata alla voce nella matrice delle **funzionalità** che si trova nello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="bc53c-187">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="bc53c-188">Questa proprietà viene ereditata da [**CIM \_ controller seriale**](cim-serialcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="bc53c-188">This property is inherited from [**CIM\_SerialController**](cim-serialcontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="bc53c-189">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="bc53c-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-190">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bc53c-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-192">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="bc53c-192">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-193">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bc53c-193">Short description of the object.</span></span>

<span data-ttu-id="bc53c-194">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bc53c-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bc53c-195">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="bc53c-195">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-196">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bc53c-196">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-197">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-198">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="bc53c-198">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-199">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="bc53c-199">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="bc53c-200">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bc53c-200">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="bc53c-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="bc53c-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="bc53c-202"> (0)</span><span class="sxs-lookup"><span data-stu-id="bc53c-202">(0)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-203">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="bc53c-203">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="bc53c-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="bc53c-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="bc53c-205">(1)</span><span class="sxs-lookup"><span data-stu-id="bc53c-205">(1)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-206">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="bc53c-206">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="bc53c-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="bc53c-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="bc53c-208">(2)</span><span class="sxs-lookup"><span data-stu-id="bc53c-208">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="bc53c-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="bc53c-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="bc53c-210">(3)</span><span class="sxs-lookup"><span data-stu-id="bc53c-210">(3)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-211">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="bc53c-211">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="bc53c-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="bc53c-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="bc53c-213">(4)</span><span class="sxs-lookup"><span data-stu-id="bc53c-213">(4)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-214">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="bc53c-214">Device is not working properly.</span></span> <span data-ttu-id="bc53c-215">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="bc53c-215">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="bc53c-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="bc53c-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="bc53c-217">(5)</span><span class="sxs-lookup"><span data-stu-id="bc53c-217">(5)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-218">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="bc53c-218">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="bc53c-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="bc53c-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="bc53c-220"> (6)</span><span class="sxs-lookup"><span data-stu-id="bc53c-220">(6)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-221">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="bc53c-221">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="bc53c-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="bc53c-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="bc53c-223">(7)</span><span class="sxs-lookup"><span data-stu-id="bc53c-223">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="bc53c-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="bc53c-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="bc53c-225">(8)</span><span class="sxs-lookup"><span data-stu-id="bc53c-225">(8)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-226">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="bc53c-226">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="bc53c-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="bc53c-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="bc53c-228">(9)</span><span class="sxs-lookup"><span data-stu-id="bc53c-228">(9)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-229">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="bc53c-229">Device is not working properly.</span></span> <span data-ttu-id="bc53c-230">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bc53c-230">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="bc53c-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="bc53c-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="bc53c-232">(10)</span><span class="sxs-lookup"><span data-stu-id="bc53c-232">(10)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-233">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bc53c-233">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="bc53c-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="bc53c-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="bc53c-235">(11)</span><span class="sxs-lookup"><span data-stu-id="bc53c-235">(11)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-236">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bc53c-236">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="bc53c-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="bc53c-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="bc53c-238">12</span><span class="sxs-lookup"><span data-stu-id="bc53c-238">(12)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-239">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="bc53c-239">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="bc53c-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="bc53c-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="bc53c-241">(13)</span><span class="sxs-lookup"><span data-stu-id="bc53c-241">(13)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-242">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bc53c-242">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="bc53c-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="bc53c-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="bc53c-244">(14)</span><span class="sxs-lookup"><span data-stu-id="bc53c-244">(14)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-245">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="bc53c-245">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="bc53c-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="bc53c-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="bc53c-247">(15)</span><span class="sxs-lookup"><span data-stu-id="bc53c-247">(15)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-248">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="bc53c-248">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="bc53c-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="bc53c-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="bc53c-250">(16)</span><span class="sxs-lookup"><span data-stu-id="bc53c-250">(16)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-251">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bc53c-251">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="bc53c-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="bc53c-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="bc53c-253">(17)</span><span class="sxs-lookup"><span data-stu-id="bc53c-253">(17)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-254">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="bc53c-254">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="bc53c-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="bc53c-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="bc53c-256">(18)</span><span class="sxs-lookup"><span data-stu-id="bc53c-256">(18)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-257">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bc53c-257">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="bc53c-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="bc53c-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="bc53c-259">(19)</span><span class="sxs-lookup"><span data-stu-id="bc53c-259">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="bc53c-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="bc53c-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="bc53c-261">(20)</span><span class="sxs-lookup"><span data-stu-id="bc53c-261">(20)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-262">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="bc53c-262">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="bc53c-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="bc53c-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="bc53c-264">(21)</span><span class="sxs-lookup"><span data-stu-id="bc53c-264">(21)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-265">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="bc53c-265">System failure.</span></span> <span data-ttu-id="bc53c-266">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="bc53c-266">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="bc53c-267">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bc53c-267">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="bc53c-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="bc53c-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="bc53c-269">(22)</span><span class="sxs-lookup"><span data-stu-id="bc53c-269">(22)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-270">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="bc53c-270">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="bc53c-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="bc53c-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="bc53c-272">(23)</span><span class="sxs-lookup"><span data-stu-id="bc53c-272">(23)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-273">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="bc53c-273">System failure.</span></span> <span data-ttu-id="bc53c-274">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="bc53c-274">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="bc53c-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="bc53c-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="bc53c-276">(24)</span><span class="sxs-lookup"><span data-stu-id="bc53c-276">(24)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-277">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="bc53c-277">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="bc53c-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="bc53c-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="bc53c-279">(25)</span><span class="sxs-lookup"><span data-stu-id="bc53c-279">(25)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-280">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bc53c-280">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="bc53c-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="bc53c-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="bc53c-282">(26)</span><span class="sxs-lookup"><span data-stu-id="bc53c-282">(26)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-283">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bc53c-283">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="bc53c-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="bc53c-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="bc53c-285">(27)</span><span class="sxs-lookup"><span data-stu-id="bc53c-285">(27)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-286">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="bc53c-286">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="bc53c-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="bc53c-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="bc53c-288">(28)</span><span class="sxs-lookup"><span data-stu-id="bc53c-288">(28)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-289">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="bc53c-289">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="bc53c-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="bc53c-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="bc53c-291">(29)</span><span class="sxs-lookup"><span data-stu-id="bc53c-291">(29)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-292">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="bc53c-292">Device is disabled.</span></span> <span data-ttu-id="bc53c-293">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="bc53c-293">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="bc53c-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="bc53c-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="bc53c-295">(30)</span><span class="sxs-lookup"><span data-stu-id="bc53c-295">(30)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-296">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bc53c-296">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="bc53c-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="bc53c-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="bc53c-298">31</span><span class="sxs-lookup"><span data-stu-id="bc53c-298">(31)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-299">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="bc53c-299">Device is not working properly.</span></span> <span data-ttu-id="bc53c-300">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="bc53c-300">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bc53c-301">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="bc53c-301">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-302">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bc53c-302">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-303">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-304">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="bc53c-304">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-305">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="bc53c-305">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="bc53c-306">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bc53c-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bc53c-307">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="bc53c-307">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-308">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bc53c-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-309">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-310">Qualificatori: [ **\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="bc53c-310">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-311">Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="bc53c-311">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="bc53c-312">Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="bc53c-312">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="bc53c-313">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bc53c-313">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bc53c-314">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="bc53c-314">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-315">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bc53c-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-316">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-317">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="bc53c-317">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-318">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bc53c-318">Description of the object.</span></span>

<span data-ttu-id="bc53c-319">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bc53c-319">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bc53c-320">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="bc53c-320">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-321">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bc53c-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-322">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-323">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| hardware \\ \\ DeviceMap \\ \\ SerialComm")</span><span class="sxs-lookup"><span data-stu-id="bc53c-323">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Hardware\\\\DeviceMap\\\\SerialComm")</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-324">Identificatore univoco della porta seriale con altri dispositivi nel sistema.</span><span class="sxs-lookup"><span data-stu-id="bc53c-324">Unique identifier of the serial port with other devices on the system.</span></span>

<span data-ttu-id="bc53c-325">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bc53c-325">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bc53c-326">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="bc53c-326">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-327">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bc53c-327">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-328">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-329">Se **true**, l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="bc53c-329">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="bc53c-330">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bc53c-330">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bc53c-331">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="bc53c-331">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-332">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bc53c-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-333">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-334">Stringa in formato libero che fornisce ulteriori informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="bc53c-334">Free-form string supplying more information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="bc53c-335">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bc53c-335">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bc53c-336">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="bc53c-336">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-337">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="bc53c-337">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-338">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-339">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="bc53c-339">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-340">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bc53c-340">Date and time the object was installed.</span></span> <span data-ttu-id="bc53c-341">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="bc53c-341">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="bc53c-342">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bc53c-342">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bc53c-343">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="bc53c-343">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-344">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bc53c-344">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-345">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-346">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="bc53c-346">Last error code reported by the logical device.</span></span>

<span data-ttu-id="bc53c-347">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bc53c-347">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bc53c-348">**MaxBaudRate**</span><span class="sxs-lookup"><span data-stu-id="bc53c-348">**MaxBaudRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-349">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bc53c-349">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-350">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-351">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| porte seriali \| 004,6 "), [**unità**](../wmisdk/standard-qualifiers.md) (" bit al secondo ")</span><span class="sxs-lookup"><span data-stu-id="bc53c-351">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Serial Ports\|004.6"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-352">Velocità in baud massima (in bit al secondo) supportata dal controller seriale.</span><span class="sxs-lookup"><span data-stu-id="bc53c-352">Maximum baud rate (in bits per second) supported by the serial controller.</span></span>

<span data-ttu-id="bc53c-353">Questa proprietà viene ereditata da [**CIM \_ controller seriale**](cim-serialcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="bc53c-353">This property is inherited from [**CIM\_SerialController**](cim-serialcontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="bc53c-354">**MaximumInputBufferSize**</span><span class="sxs-lookup"><span data-stu-id="bc53c-354">**MaximumInputBufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-355">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bc53c-355">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-356">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-357">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwMaxRxQueue"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="bc53c-357">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwMaxRxQueue"), [**units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-358">Dimensione massima del buffer di input interno del driver della porta seriale.</span><span class="sxs-lookup"><span data-stu-id="bc53c-358">Maximum size of the serial port driver's internal input buffer.</span></span> <span data-ttu-id="bc53c-359">Il valore 0 (zero) indica che non viene imposto alcun valore massimo dal provider seriale.</span><span class="sxs-lookup"><span data-stu-id="bc53c-359">A value of 0 (zero) indicates that no maximum value is imposed by the serial provider.</span></span>

</dd> <dt>

<span data-ttu-id="bc53c-360">**MaximumOutputBufferSize**</span><span class="sxs-lookup"><span data-stu-id="bc53c-360">**MaximumOutputBufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-361">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bc53c-361">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-362">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-363">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwMaxTxQueue"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="bc53c-363">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwMaxTxQueue"), [**units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-364">Dimensioni massime del buffer di output interno del driver della porta seriale.</span><span class="sxs-lookup"><span data-stu-id="bc53c-364">Maximum size of the serial port driver's internal output buffer.</span></span> <span data-ttu-id="bc53c-365">Il valore 0 (zero) indica che non viene imposto alcun valore massimo dal provider seriale.</span><span class="sxs-lookup"><span data-stu-id="bc53c-365">A value of 0 (zero) indicates that no maximum value is imposed by the serial provider.</span></span>

</dd> <dt>

<span data-ttu-id="bc53c-366">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="bc53c-366">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-367">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bc53c-367">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-368">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-369">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Porta bus DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="bc53c-369">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-370">Numero massimo di entità indirizzabili direttamente supportato da questo controller.</span><span class="sxs-lookup"><span data-stu-id="bc53c-370">Maximum number of directly addressable entities supportable by this controller.</span></span> <span data-ttu-id="bc53c-371">Se il numero è sconosciuto, è necessario usare un valore pari a 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="bc53c-371">A value of 0 (zero) should be used if the number is unknown.</span></span>

<span data-ttu-id="bc53c-372">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="bc53c-372">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="bc53c-373">**Nome**</span><span class="sxs-lookup"><span data-stu-id="bc53c-373">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-374">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bc53c-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-375">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-376">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="bc53c-376">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-377">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="bc53c-377">Label by which the object is known.</span></span> <span data-ttu-id="bc53c-378">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="bc53c-378">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="bc53c-379">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bc53c-379">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bc53c-380">**OSAutoDiscovered**</span><span class="sxs-lookup"><span data-stu-id="bc53c-380">**OSAutoDiscovered**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-381">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bc53c-381">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-382">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-383">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| hardware \\ \\ Description \\ \\ System \\ \\ MultifunctionAdapter")</span><span class="sxs-lookup"><span data-stu-id="bc53c-383">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HARDWARE\\\\DESCRIPTION\\\\SYSTEM\\\\MultifunctionAdapter")</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-384">Se **true**, le istanze di questa classe sono state individuate automaticamente dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="bc53c-384">If **TRUE**, the instances of this class were automatically discovered by the operating system.</span></span> <span data-ttu-id="bc53c-385">Se, ad esempio, l'hardware è stato aggiunto tramite il pannello di controllo, il sistema operativo trova le istanze di questa classe eseguendo una query sull'hardware dalle istanze di questa classe.</span><span class="sxs-lookup"><span data-stu-id="bc53c-385">If, for example, hardware was added through Control Panel, the operating system finds instances of this class by querying hardware from the instances of this class.</span></span>

</dd> <dt>

<span data-ttu-id="bc53c-386">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="bc53c-386">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-387">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bc53c-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-388">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-389">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="bc53c-389">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-390">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="bc53c-390">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="bc53c-391">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bc53c-391">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="bc53c-392">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="bc53c-392">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="bc53c-393">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="bc53c-393">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-394">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bc53c-394">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-395">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-396">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="bc53c-396">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="bc53c-397">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="bc53c-397">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bc53c-398"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="bc53c-398"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="bc53c-399"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="bc53c-399"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="bc53c-400"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="bc53c-400"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="bc53c-401"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="bc53c-401"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-402">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="bc53c-402">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="bc53c-403"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="bc53c-403"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-404">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="bc53c-404">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="bc53c-405"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="bc53c-405"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-406">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="bc53c-406">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="bc53c-407">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="bc53c-407">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="bc53c-408">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="bc53c-408">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="bc53c-409"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="bc53c-409"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-410">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="bc53c-410">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="bc53c-411"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="bc53c-411"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-412">Tempo Power-On supportato</span><span class="sxs-lookup"><span data-stu-id="bc53c-412">Timed Power-On Supported</span></span>

<span data-ttu-id="bc53c-413">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="bc53c-413">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bc53c-414">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="bc53c-414">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-415">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bc53c-415">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-416">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-417">Se **true**, il dispositivo può essere gestito dal risparmio di energia (può essere impostato in modalità di sospensione e così via).</span><span class="sxs-lookup"><span data-stu-id="bc53c-417">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="bc53c-418">La proprietà non indica che le funzionalità di risparmio energia sono attualmente abilitate, solo che il dispositivo logico è in grado di gestire il risparmio di energia.</span><span class="sxs-lookup"><span data-stu-id="bc53c-418">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="bc53c-419">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bc53c-419">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bc53c-420">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="bc53c-420">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-421">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bc53c-421">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-422">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-423">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Porta bus DMTF \| 001,2 "," MIF. \|Dischi DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="bc53c-423">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-424">Protocollo usato dal controller per accedere ai dispositivi "controllati".</span><span class="sxs-lookup"><span data-stu-id="bc53c-424">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="bc53c-425">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="bc53c-425">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="bc53c-426">Nell'elenco seguente sono riportati i valori possibili.</span><span class="sxs-lookup"><span data-stu-id="bc53c-426">The following list shows the possible values.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bc53c-427"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="bc53c-427"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bc53c-428"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="bc53c-428"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="bc53c-429"><span id="EISA"></span><span id="eisa"></span>**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="bc53c-429"><span id="EISA"></span><span id="eisa"></span>**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="bc53c-430"><span id="ISA"></span><span id="isa"></span>**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="bc53c-430"><span id="ISA"></span><span id="isa"></span>**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="bc53c-431"><span id="PCI"></span><span id="pci"></span>**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="bc53c-431"><span id="PCI"></span><span id="pci"></span>**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="bc53c-432"><span id="ATA_ATAPI"></span><span id="ata_atapi"></span>**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="bc53c-432"><span id="ATA_ATAPI"></span><span id="ata_atapi"></span>**ATA/ATAPI** (6)</span></span>


</dt> <dd>

<span data-ttu-id="bc53c-433">ATA o ATAPI</span><span class="sxs-lookup"><span data-stu-id="bc53c-433">ATA or ATAPI</span></span>

</dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="bc53c-434"><span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>**Dischetto flessibile** (7)</span><span class="sxs-lookup"><span data-stu-id="bc53c-434"><span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="bc53c-435"><span id="1496"></span>**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="bc53c-435"><span id="1496"></span>**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="bc53c-436"><span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>**Interfaccia parallela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="bc53c-436"><span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="bc53c-437"><span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>**Protocollo di Fibre Channel SCSI** (10)</span><span class="sxs-lookup"><span data-stu-id="bc53c-437"><span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="bc53c-438"><span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>**Protocollo bus seriale SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="bc53c-438"><span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="bc53c-439"><span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>**Protocollo bus seriale SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="bc53c-439"><span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="bc53c-440"><span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>**Architettura di archiviazione seriale SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="bc53c-440"><span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="bc53c-441"><span id="VESA"></span><span id="vesa"></span>**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="bc53c-441"><span id="VESA"></span><span id="vesa"></span>**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="bc53c-442"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="bc53c-442"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="bc53c-443"><span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>**Bus seriale universale** (16)</span><span class="sxs-lookup"><span data-stu-id="bc53c-443"><span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="bc53c-444"><span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>**Protocollo parallelo** (17)</span><span class="sxs-lookup"><span data-stu-id="bc53c-444"><span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="bc53c-445"><span id="ESCON"></span><span id="escon"></span>**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="bc53c-445"><span id="ESCON"></span><span id="escon"></span>**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="bc53c-446"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostica** (19)</span><span class="sxs-lookup"><span data-stu-id="bc53c-446"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="bc53c-447"><span id="I2C"></span><span id="i2c"></span>**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="bc53c-447"><span id="I2C"></span><span id="i2c"></span>**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="bc53c-448"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Potenza** (21)</span><span class="sxs-lookup"><span data-stu-id="bc53c-448"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="bc53c-449"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="bc53c-449"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="bc53c-450"><span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="bc53c-450"><span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="bc53c-451"><span id="VME"></span><span id="vme"></span>**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="bc53c-451"><span id="VME"></span><span id="vme"></span>**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="bc53c-452"><span id="IPI"></span><span id="ipi"></span>**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="bc53c-452"><span id="IPI"></span><span id="ipi"></span>**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="bc53c-453"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="bc53c-453"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="bc53c-454"><span id="RS232"></span><span id="rs232"></span>**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="bc53c-454"><span id="RS232"></span><span id="rs232"></span>**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="bc53c-455"><span id="ieee_802.3_10base5"></span>**IEEE 802,3 10Base5** (28)</span><span class="sxs-lookup"><span data-stu-id="bc53c-455"><span id="ieee_802.3_10base5"></span>**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="bc53c-456"><span id="ieee_802.3_10base2"></span>**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="bc53c-456"><span id="ieee_802.3_10base2"></span>**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="bc53c-457"><span id="ieee_802.3_1base5"></span>**IEEE 802,3 1Base5** (30)</span><span class="sxs-lookup"><span data-stu-id="bc53c-457"><span id="ieee_802.3_1base5"></span>**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="bc53c-458"><span id="ieee_802.3_10broad36"></span>**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="bc53c-458"><span id="ieee_802.3_10broad36"></span>**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="bc53c-459"><span id="ieee_802.3_100basevg"></span>**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="bc53c-459"><span id="ieee_802.3_100basevg"></span>**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="bc53c-460"><span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>**Token-ring IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="bc53c-460"><span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="bc53c-461"><span id="ansi_x3t9.5_fddi"></span>**ANSI X3T 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="bc53c-461"><span id="ansi_x3t9.5_fddi"></span>**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="bc53c-462"><span id="MCA"></span><span id="mca"></span>**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="bc53c-462"><span id="MCA"></span><span id="mca"></span>**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="bc53c-463"><span id="ESDI"></span><span id="esdi"></span>**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="bc53c-463"><span id="ESDI"></span><span id="esdi"></span>**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="bc53c-464"><span id="IDE"></span><span id="ide"></span>**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="bc53c-464"><span id="IDE"></span><span id="ide"></span>**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="bc53c-465"><span id="CMD"></span><span id="cmd"></span>**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="bc53c-465"><span id="CMD"></span><span id="cmd"></span>**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="bc53c-466"><span id="ST506"></span><span id="st506"></span>**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="bc53c-466"><span id="ST506"></span><span id="st506"></span>**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="bc53c-467"><span id="DSSI"></span><span id="dssi"></span>**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="bc53c-467"><span id="DSSI"></span><span id="dssi"></span>**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="bc53c-468"><span id="QIC2"></span><span id="qic2"></span>**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="bc53c-468"><span id="QIC2"></span><span id="qic2"></span>**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="bc53c-469"><span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>**ATA/IDE avanzato** (42)</span><span class="sxs-lookup"><span data-stu-id="bc53c-469"><span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="bc53c-470"><span id="AGP"></span><span id="agp"></span>**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="bc53c-470"><span id="AGP"></span><span id="agp"></span>**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="bc53c-471"><span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>**TWIRP (infrarossi bidirezionali)** (44)</span><span class="sxs-lookup"><span data-stu-id="bc53c-471"><span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="bc53c-472"><span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>**FIR (infrarossi veloci)** (45)</span><span class="sxs-lookup"><span data-stu-id="bc53c-472"><span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="bc53c-473"><span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>**Sir (Serial Infrared)** (46)</span><span class="sxs-lookup"><span data-stu-id="bc53c-473"><span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="bc53c-474"><span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="bc53c-474"><span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bc53c-475">**ProviderType**</span><span class="sxs-lookup"><span data-stu-id="bc53c-475">**ProviderType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-476">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bc53c-476">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-477">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-478">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvSubType")</span><span class="sxs-lookup"><span data-stu-id="bc53c-478">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvSubType")</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-479">Tipo di provider di comunicazioni.</span><span class="sxs-lookup"><span data-stu-id="bc53c-479">Communications provider type.</span></span>

<span data-ttu-id="bc53c-480">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="bc53c-480">The values are:</span></span>

<dl> <dd><span data-ttu-id="bc53c-481">"Dispositivo FAX"</span><span class="sxs-lookup"><span data-stu-id="bc53c-481">"FAX Device"</span></span></dd> <dd><span data-ttu-id="bc53c-482">"Protocollo LAT"</span><span class="sxs-lookup"><span data-stu-id="bc53c-482">"LAT Protocol"</span></span></dd> <dd><span data-ttu-id="bc53c-483">"Dispositivo modem"</span><span class="sxs-lookup"><span data-stu-id="bc53c-483">"Modem Device"</span></span></dd> <dd><span data-ttu-id="bc53c-484">"Bridge di rete"</span><span class="sxs-lookup"><span data-stu-id="bc53c-484">"Network Bridge"</span></span></dd> <dd><span data-ttu-id="bc53c-485">"Porta parallela"</span><span class="sxs-lookup"><span data-stu-id="bc53c-485">"Parallel Port"</span></span></dd> <dd><span data-ttu-id="bc53c-486">"Porta seriale RS232"</span><span class="sxs-lookup"><span data-stu-id="bc53c-486">"RS232 Serial Port"</span></span></dd> <dd><span data-ttu-id="bc53c-487">"Porta RS422"</span><span class="sxs-lookup"><span data-stu-id="bc53c-487">"RS422 Port"</span></span></dd> <dd><span data-ttu-id="bc53c-488">"Porta RS423"</span><span class="sxs-lookup"><span data-stu-id="bc53c-488">"RS423 Port"</span></span></dd> <dd><span data-ttu-id="bc53c-489">"Porta RS449"</span><span class="sxs-lookup"><span data-stu-id="bc53c-489">"RS449 Port"</span></span></dd> <dd><span data-ttu-id="bc53c-490">"Dispositivo scanner"</span><span class="sxs-lookup"><span data-stu-id="bc53c-490">"Scanner Device"</span></span></dd> <dd><span data-ttu-id="bc53c-491">"TCP/IP TelNet"</span><span class="sxs-lookup"><span data-stu-id="bc53c-491">"TCP/IP TelNet"</span></span></dd> <dd><span data-ttu-id="bc53c-492">"X. 25"</span><span class="sxs-lookup"><span data-stu-id="bc53c-492">"X.25"</span></span></dd> <dd><span data-ttu-id="bc53c-493">Unspecified</span><span class="sxs-lookup"><span data-stu-id="bc53c-493">"Unspecified"</span></span></dd> </dl>

<dt>

<span id="FAX_Device"></span><span id="fax_device"></span><span id="FAX_DEVICE"></span>

<span data-ttu-id="bc53c-494">**Dispositivo fax** ("dispositivo fax")</span><span class="sxs-lookup"><span data-stu-id="bc53c-494">**FAX Device** ("FAX Device")</span></span>


</dt> <dd></dd> <dt>

<span id="LAT_Protocol"></span><span id="lat_protocol"></span><span id="LAT_PROTOCOL"></span>

<span data-ttu-id="bc53c-495">**Protocollo Lat** ("protocollo LAT")</span><span class="sxs-lookup"><span data-stu-id="bc53c-495">**LAT Protocol** ("LAT Protocol")</span></span>


</dt> <dd></dd> <dt>

<span id="Modem_Device"></span><span id="modem_device"></span><span id="MODEM_DEVICE"></span>

<span data-ttu-id="bc53c-496">**Dispositivo modem** ("dispositivo modem")</span><span class="sxs-lookup"><span data-stu-id="bc53c-496">**Modem Device** ("Modem Device")</span></span>


</dt> <dd></dd> <dt>

<span id="Network_Bridge"></span><span id="network_bridge"></span><span id="NETWORK_BRIDGE"></span>

<span data-ttu-id="bc53c-497">**Bridge** di rete ("Bridge di rete")</span><span class="sxs-lookup"><span data-stu-id="bc53c-497">**Network Bridge** ("Network Bridge")</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

<span data-ttu-id="bc53c-498">**Porta parallela** ("porta parallela")</span><span class="sxs-lookup"><span data-stu-id="bc53c-498">**Parallel Port** ("Parallel Port")</span></span>


</dt> <dd></dd> <dt>

<span id="RS232_Serial_Port"></span><span id="rs232_serial_port"></span><span id="RS232_SERIAL_PORT"></span>

<span data-ttu-id="bc53c-499">**Porta seriale RS232** ("porta seriale RS232")</span><span class="sxs-lookup"><span data-stu-id="bc53c-499">**RS232 Serial Port** ("RS232 Serial Port")</span></span>


</dt> <dd></dd> <dt>

<span id="RS422_Port"></span><span id="rs422_port"></span><span id="RS422_PORT"></span>

<span data-ttu-id="bc53c-500">**Porta RS422** ("porta RS422")</span><span class="sxs-lookup"><span data-stu-id="bc53c-500">**RS422 Port** ("RS422 Port")</span></span>


</dt> <dd></dd> <dt>

<span id="RS423_Port"></span><span id="rs423_port"></span><span id="RS423_PORT"></span>

<span data-ttu-id="bc53c-501">**Porta RS423** ("porta RS423")</span><span class="sxs-lookup"><span data-stu-id="bc53c-501">**RS423 Port** ("RS423 Port")</span></span>


</dt> <dd></dd> <dt>

<span id="RS449_Port"></span><span id="rs449_port"></span><span id="RS449_PORT"></span>

<span data-ttu-id="bc53c-502">**Porta RS449** ("porta RS449")</span><span class="sxs-lookup"><span data-stu-id="bc53c-502">**RS449 Port** ("RS449 Port")</span></span>


</dt> <dd></dd> <dt>

<span id="Scanner_Device"></span><span id="scanner_device"></span><span id="SCANNER_DEVICE"></span>

<span data-ttu-id="bc53c-503">**Dispositivo scanner** ("dispositivo scanner")</span><span class="sxs-lookup"><span data-stu-id="bc53c-503">**Scanner Device** ("Scanner Device")</span></span>


</dt> <dd></dd> <dt>

<span id="TCP_IP_TelNet"></span><span id="tcp_ip_telnet"></span><span id="TCP_IP_TELNET"></span>

<span data-ttu-id="bc53c-504">**TCP/IP Telnet** ("TCP/IP Telnet")</span><span class="sxs-lookup"><span data-stu-id="bc53c-504">**TCP/IP TelNet** ("TCP/IP TelNet")</span></span>


</dt> <dd></dd> <dt>

<span id="X.25"></span><span id="x.25"></span>

<span data-ttu-id="bc53c-505">**X. 25** ("x. 25")</span><span class="sxs-lookup"><span data-stu-id="bc53c-505">**X.25** ("X.25")</span></span>


</dt> <dd></dd> <dt>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>

<span data-ttu-id="bc53c-506">Non **specificato** ("non specificato")</span><span class="sxs-lookup"><span data-stu-id="bc53c-506">**Unspecified** ("Unspecified")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bc53c-507">**SettableBaudRate**</span><span class="sxs-lookup"><span data-stu-id="bc53c-507">**SettableBaudRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-508">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bc53c-508">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-509">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-509">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-510">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| SP \_ baud")</span><span class="sxs-lookup"><span data-stu-id="bc53c-510">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_BAUD")</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-511">Se **true**, la velocità in baud può essere modificata per questa porta seriale.</span><span class="sxs-lookup"><span data-stu-id="bc53c-511">If **TRUE**, the baud rate can be changed for this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="bc53c-512">**SettableDataBits**</span><span class="sxs-lookup"><span data-stu-id="bc53c-512">**SettableDataBits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-513">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bc53c-513">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-514">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-514">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-515">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| SP \_ DataBits")</span><span class="sxs-lookup"><span data-stu-id="bc53c-515">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_DATABITS")</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-516">Se **true**, i bit di dati possono essere impostati per questa porta seriale.</span><span class="sxs-lookup"><span data-stu-id="bc53c-516">If **TRUE**, data bits can be set for this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="bc53c-517">**SettableFlowControl**</span><span class="sxs-lookup"><span data-stu-id="bc53c-517">**SettableFlowControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-518">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bc53c-518">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-519">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-519">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-520">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| SP \_ handshaking")</span><span class="sxs-lookup"><span data-stu-id="bc53c-520">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_HANDSHAKING")</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-521">Se **true**, il controllo di flusso può essere impostato per questa porta seriale.</span><span class="sxs-lookup"><span data-stu-id="bc53c-521">If **TRUE**, flow control can be set for this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="bc53c-522">**SettableParity**</span><span class="sxs-lookup"><span data-stu-id="bc53c-522">**SettableParity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-523">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bc53c-523">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-524">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-525">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| SP \_ parità")</span><span class="sxs-lookup"><span data-stu-id="bc53c-525">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_PARITY")</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-526">Se **true**, è possibile impostare la parità per questa porta seriale.</span><span class="sxs-lookup"><span data-stu-id="bc53c-526">If **TRUE**, parity can be set for this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="bc53c-527">**SettableParityCheck**</span><span class="sxs-lookup"><span data-stu-id="bc53c-527">**SettableParityCheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-528">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bc53c-528">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-529">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-529">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-530">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| SP \_ parità \_ Check")</span><span class="sxs-lookup"><span data-stu-id="bc53c-530">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_PARITY\_CHECK")</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-531">Se **true**, è possibile impostare il controllo della parità per questa porta seriale (se è supportata la verifica della parità).</span><span class="sxs-lookup"><span data-stu-id="bc53c-531">If **TRUE**, parity checking can be set for this serial port (if parity checking is supported).</span></span>

</dd> <dt>

<span data-ttu-id="bc53c-532">**SettableRLSD**</span><span class="sxs-lookup"><span data-stu-id="bc53c-532">**SettableRLSD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-533">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bc53c-533">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-534">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-534">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-535">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| SP \_ RISD")</span><span class="sxs-lookup"><span data-stu-id="bc53c-535">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_RLSD")</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-536">Se **true**, è possibile impostare il rilevamento del segnale di riga (RISD) ricevuto per questa porta seriale (se RISD è supportato).</span><span class="sxs-lookup"><span data-stu-id="bc53c-536">If **TRUE**, Received Line Signal Detect (RLSD) can be set for this serial port (if RLSD is supported).</span></span>

</dd> <dt>

<span data-ttu-id="bc53c-537">**SettableStopBits**</span><span class="sxs-lookup"><span data-stu-id="bc53c-537">**SettableStopBits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-538">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bc53c-538">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-539">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-539">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-540">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| SP \_ Stop")</span><span class="sxs-lookup"><span data-stu-id="bc53c-540">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_STOPBITS")</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-541">Se **true**, è possibile impostare bits stop per questa porta seriale.</span><span class="sxs-lookup"><span data-stu-id="bc53c-541">If **TRUE**, stop bits can be set for this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="bc53c-542">**Status**</span><span class="sxs-lookup"><span data-stu-id="bc53c-542">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-543">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bc53c-543">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-544">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-544">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-545">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="bc53c-545">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-546">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bc53c-546">Current status of the object.</span></span> <span data-ttu-id="bc53c-547">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="bc53c-547">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="bc53c-548">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="bc53c-548">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="bc53c-549">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="bc53c-549">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="bc53c-550">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="bc53c-550">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="bc53c-551">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="bc53c-551">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="bc53c-552">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bc53c-552">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="bc53c-553">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="bc53c-553">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="bc53c-554">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="bc53c-554">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="bc53c-555">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="bc53c-555">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="bc53c-556">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="bc53c-556">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bc53c-557">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="bc53c-557">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="bc53c-558">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="bc53c-558">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="bc53c-559">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="bc53c-559">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="bc53c-560">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="bc53c-560">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="bc53c-561">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="bc53c-561">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="bc53c-562">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="bc53c-562">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="bc53c-563">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="bc53c-563">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="bc53c-564">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="bc53c-564">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="bc53c-565">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="bc53c-565">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bc53c-566">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="bc53c-566">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-567">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bc53c-567">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-568">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-568">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-569">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="bc53c-569">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-570">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="bc53c-570">State of the logical device.</span></span> <span data-ttu-id="bc53c-571">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="bc53c-571">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="bc53c-572">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bc53c-572">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bc53c-573">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="bc53c-573">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bc53c-574">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="bc53c-574">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="bc53c-575">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="bc53c-575">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="bc53c-576">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="bc53c-576">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="bc53c-577">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="bc53c-577">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bc53c-578">**Supports16BitMode**</span><span class="sxs-lookup"><span data-stu-id="bc53c-578">**Supports16BitMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-579">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bc53c-579">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-580">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-580">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-581">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ 16BITMODE")</span><span class="sxs-lookup"><span data-stu-id="bc53c-581">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_16BITMODE")</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-582">Se **true**, la modalità a 16 bit è supportata su questa porta seriale.</span><span class="sxs-lookup"><span data-stu-id="bc53c-582">If **TRUE**, 16-bit mode is supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="bc53c-583">**SupportsDTRDSR**</span><span class="sxs-lookup"><span data-stu-id="bc53c-583">**SupportsDTRDSR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-584">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bc53c-584">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-585">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-585">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-586">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ DTRDSR")</span><span class="sxs-lookup"><span data-stu-id="bc53c-586">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_DTRDSR")</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-587">Se **true**, sulla porta seriale sono supportati i segnali di Data Terminal Ready (DTR) e di data Set Ready (DSR).</span><span class="sxs-lookup"><span data-stu-id="bc53c-587">If **TRUE**, data terminal ready (DTR) and data set ready (DSR) signals are supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="bc53c-588">**SupportsElapsedTimeouts**</span><span class="sxs-lookup"><span data-stu-id="bc53c-588">**SupportsElapsedTimeouts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-589">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bc53c-589">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-590">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-590">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-591">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ TOTALTIMEOUTS")</span><span class="sxs-lookup"><span data-stu-id="bc53c-591">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_TOTALTIMEOUTS")</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-592">Se **true**, i timeout scaduti sono supportati in questa porta seriale.</span><span class="sxs-lookup"><span data-stu-id="bc53c-592">If **TRUE**, elapsed time-outs are supported on this serial port.</span></span> <span data-ttu-id="bc53c-593">I timeout trascorsi tengono traccia della quantità totale di tempo tra trasmissioni di dati.</span><span class="sxs-lookup"><span data-stu-id="bc53c-593">Elapsed timeouts track the total amount of time between data transmissions.</span></span>

</dd> <dt>

<span data-ttu-id="bc53c-594">**SupportsIntTimeouts**</span><span class="sxs-lookup"><span data-stu-id="bc53c-594">**SupportsIntTimeouts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-595">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bc53c-595">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-596">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-596">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-597">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ INTTIMEOUTS")</span><span class="sxs-lookup"><span data-stu-id="bc53c-597">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_INTTIMEOUTS")</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-598">Se **true**, i timeout dell'intervallo sono supportati.</span><span class="sxs-lookup"><span data-stu-id="bc53c-598">If **TRUE**, interval time-outs are supported.</span></span> <span data-ttu-id="bc53c-599">Un timeout di intervallo è la quantità di tempo che può trascorrere tra l'arrivo di ogni dato.</span><span class="sxs-lookup"><span data-stu-id="bc53c-599">An interval timeout is the amount of time allowed to elapse between the arrival of each piece of data.</span></span>

</dd> <dt>

<span data-ttu-id="bc53c-600">**SupportsParityCheck**</span><span class="sxs-lookup"><span data-stu-id="bc53c-600">**SupportsParityCheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-601">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bc53c-601">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-602">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-602">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-603">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF di \_ parità \_ Check")</span><span class="sxs-lookup"><span data-stu-id="bc53c-603">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_PARITY\_CHECK")</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-604">Se **true**, il controllo della parità è supportato su questa porta seriale.</span><span class="sxs-lookup"><span data-stu-id="bc53c-604">If **TRUE**, parity checking is supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="bc53c-605">**SupportsRLSD**</span><span class="sxs-lookup"><span data-stu-id="bc53c-605">**SupportsRLSD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-606">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bc53c-606">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-607">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-607">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-608">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ RISD")</span><span class="sxs-lookup"><span data-stu-id="bc53c-608">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_RLSD")</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-609">Se **true**, la ricezione del segnale di riga (RISD) è supportata su questa porta seriale.</span><span class="sxs-lookup"><span data-stu-id="bc53c-609">If **TRUE**, Received Line Signal Detect (RLSD) is supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="bc53c-610">**SupportsRTSCTS**</span><span class="sxs-lookup"><span data-stu-id="bc53c-610">**SupportsRTSCTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-611">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bc53c-611">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-612">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-612">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-613">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ RTSCTS")</span><span class="sxs-lookup"><span data-stu-id="bc53c-613">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_RTSCTS")</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-614">Se **true**, i segnali RTS (Ready to Send) e CTS (Clear to Send) sono supportati in questa porta seriale.</span><span class="sxs-lookup"><span data-stu-id="bc53c-614">If **TRUE**, ready to send (RTS) and clear to send (CTS) signals are supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="bc53c-615">**SupportsSpecialCharacters**</span><span class="sxs-lookup"><span data-stu-id="bc53c-615">**SupportsSpecialCharacters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-616">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bc53c-616">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-617">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-617">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-618">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ SPECIALCHARS")</span><span class="sxs-lookup"><span data-stu-id="bc53c-618">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_SPECIALCHARS")</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-619">Se **true**, i caratteri di controllo della porta seriale sono supportati.</span><span class="sxs-lookup"><span data-stu-id="bc53c-619">If **TRUE**, serial port control characters are supported.</span></span> <span data-ttu-id="bc53c-620">Questi caratteri segnalano gli eventi anziché i dati.</span><span class="sxs-lookup"><span data-stu-id="bc53c-620">These characters signal events rather than data.</span></span> <span data-ttu-id="bc53c-621">Questi caratteri non sono visualizzabili e vengono impostati dal driver.</span><span class="sxs-lookup"><span data-stu-id="bc53c-621">These characters are not displayable and are set by the driver.</span></span> <span data-ttu-id="bc53c-622">Sono incluse EofChar, ErrorChar, BreakChar, EventChar, XonChar e XoffChar.</span><span class="sxs-lookup"><span data-stu-id="bc53c-622">They include EofChar, ErrorChar, BreakChar, EventChar, XonChar, and XoffChar.</span></span>

</dd> <dt>

<span data-ttu-id="bc53c-623">**SupportsXOnXOff**</span><span class="sxs-lookup"><span data-stu-id="bc53c-623">**SupportsXOnXOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-624">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bc53c-624">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-625">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-625">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-626">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ XONXOFF")</span><span class="sxs-lookup"><span data-stu-id="bc53c-626">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_XONXOFF")</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-627">Se **true**, il controllo di flusso XON o XOFF è supportato su questa porta seriale.</span><span class="sxs-lookup"><span data-stu-id="bc53c-627">If **TRUE**, XON or XOFF flow-control is supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="bc53c-628">**SupportsXOnXOffSet**</span><span class="sxs-lookup"><span data-stu-id="bc53c-628">**SupportsXOnXOffSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-629">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bc53c-629">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-630">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-630">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-631">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ SETXCHAR")</span><span class="sxs-lookup"><span data-stu-id="bc53c-631">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_SETXCHAR")</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-632">Se **true**, il provider di comunicazioni supporta la configurazione dell'impostazione del controllo di flusso XOFF di XONor.</span><span class="sxs-lookup"><span data-stu-id="bc53c-632">If **TRUE**, the communications provider supports configuration of the XONor XOFF flow-control setting.</span></span>

</dd> <dt>

<span data-ttu-id="bc53c-633">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="bc53c-633">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-634">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bc53c-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-635">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-635">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-636">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="bc53c-636">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-637">Valore della proprietà **CreationClassName** del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="bc53c-637">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="bc53c-638">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bc53c-638">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bc53c-639">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="bc53c-639">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-640">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bc53c-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-641">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-641">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-642">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="bc53c-642">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-643">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="bc53c-643">Name of the scoping system.</span></span>

<span data-ttu-id="bc53c-644">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bc53c-644">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bc53c-645">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="bc53c-645">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc53c-646">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="bc53c-646">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bc53c-647">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc53c-647">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc53c-648">Data e ora dell'ultima reimpostazione del controller.</span><span class="sxs-lookup"><span data-stu-id="bc53c-648">Date and time this controller was last reset.</span></span> <span data-ttu-id="bc53c-649">Questo potrebbe significare che il controller è stato spento o reinizializzato.</span><span class="sxs-lookup"><span data-stu-id="bc53c-649">This could mean the controller was powered down, or reinitialized.</span></span>

<span data-ttu-id="bc53c-650">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="bc53c-650">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bc53c-651">Commenti</span><span class="sxs-lookup"><span data-stu-id="bc53c-651">Remarks</span></span>

<span data-ttu-id="bc53c-652">La **classe \_ SerialPort Win32** è derivata da [**CIM \_ controller seriale**](cim-serialcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="bc53c-652">The **Win32\_SerialPort** class is derived from [**CIM\_SerialController**](cim-serialcontroller.md).</span></span>

## <a name="examples"></a><span data-ttu-id="bc53c-653">Esempio</span><span class="sxs-lookup"><span data-stu-id="bc53c-653">Examples</span></span>

<span data-ttu-id="bc53c-654">Per un metodo alternativo per il recupero delle informazioni sulla porta seriale (dal registro di sistema), vedere l'esempio [enumerate ports](https://Gallery.TechNet.Microsoft.Com/scriptcenter/087b4d73-4a5e-4746-b365-ad682911360e) Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="bc53c-654">For an alternate method of retrieving serial port information (from the registry), see the [Enumerate Ports](https://Gallery.TechNet.Microsoft.Com/scriptcenter/087b4d73-4a5e-4746-b365-ad682911360e) Visual Basic sample.</span></span>

<span data-ttu-id="bc53c-655">L'esempio di [elenco delle proprietà della porta seriale](https://Gallery.TechNet.Microsoft.Com/42ff8eab-7d2b-4549-b178-835daecf4f12) di PowerShell restituisce informazioni sulle porte seriali installate in un computer.</span><span class="sxs-lookup"><span data-stu-id="bc53c-655">The [List Serial Port Properties](https://Gallery.TechNet.Microsoft.Com/42ff8eab-7d2b-4549-b178-835daecf4f12) PowerShell example returns information about the serial ports installed on a computer.</span></span>

<span data-ttu-id="bc53c-656">Nell'esempio VBScript seguente vengono restituite informazioni sulle porte seriali installate in un computer.</span><span class="sxs-lookup"><span data-stu-id="bc53c-656">The following VBScript sample returns information about the serial ports installed on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_SerialPort") 
 
For Each objItem in colItems 
    Wscript.Echo "Binary: " & objItem.Binary 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Device ID: " & objItem.DeviceID 
    Wscript.Echo "Maximum Baud Rate: " & objItem.MaxBaudRate 
    Wscript.Echo "Maximum Input Buffer Size: " & objItem.MaximumInputBufferSize 
    Wscript.Echo "Maximum Output Buffer Size: " & _ 
        objItem.MaximumOutputBufferSize 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "OS Auto Discovered: " & objItem.OSAutoDiscovered 
    Wscript.Echo "PNP Device ID: " & objItem.PNPDeviceID 
    Wscript.Echo "Provider Type: " & objItem.ProviderType 
    Wscript.Echo "Settable Baud Rate: " & objItem.SettableBaudRate 
    Wscript.Echo "Settable Data Bits: " & objItem.SettableDataBits 
    Wscript.Echo "Settable Flow Control: " & objItem.SettableFlowControl 
    Wscript.Echo "Settable Parity: " & objItem.SettableParity 
    Wscript.Echo "Settable Parity Check: " & objItem.SettableParityCheck 
    Wscript.Echo "Settable RLSD: " & objItem.SettableRLSD 
    Wscript.Echo "Settable Stop Bits: " & objItem.SettableStopBits 
    Wscript.Echo "Supports 16-Bit Mode: " & objItem.Supports16BitMode 
    Wscript.Echo "Supports DTRDSR: " & objItem.SupportsDTRDSR 
    Wscript.Echo "Supports Elapsed Timeouts: " & _ 
        objItem.SupportsElapsedTimeouts 
    Wscript.Echo "Supports Int Timeouts: " & objItem.SupportsIntTimeouts 
    Wscript.Echo "Supports Parity Check: " & objItem.SupportsParityCheck 
    Wscript.Echo "Supports RLSD: " & objItem.SupportsRLSD 
    Wscript.Echo "Supports RTSCTS: " & objItem.SupportsRTSCTS 
    Wscript.Echo "Supports Special Characters: " & _ 
        objItem.SupportsSpecialCharacters 
    Wscript.Echo "Supports XOn XOff: " & objItem.SupportsXOnXOff 
    Wscript.Echo "Supports XOn XOff Setting: " & objItem.SupportsXOnXOffSet 
Next
```



## <a name="requirements"></a><span data-ttu-id="bc53c-657">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bc53c-657">Requirements</span></span>



| <span data-ttu-id="bc53c-658">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc53c-658">Requirement</span></span> | <span data-ttu-id="bc53c-659">Valore</span><span class="sxs-lookup"><span data-stu-id="bc53c-659">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc53c-660">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc53c-660">Minimum supported client</span></span><br/> | <span data-ttu-id="bc53c-661">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bc53c-661">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bc53c-662">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc53c-662">Minimum supported server</span></span><br/> | <span data-ttu-id="bc53c-663">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bc53c-663">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bc53c-664">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bc53c-664">Namespace</span></span><br/>                | <span data-ttu-id="bc53c-665">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="bc53c-665">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bc53c-666">MOF</span><span class="sxs-lookup"><span data-stu-id="bc53c-666">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bc53c-667"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bc53c-667"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bc53c-668">DLL</span><span class="sxs-lookup"><span data-stu-id="bc53c-668">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc53c-669"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc53c-669"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc53c-670">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bc53c-670">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc53c-671">**\_Controller seriale CIM**</span><span class="sxs-lookup"><span data-stu-id="bc53c-671">**CIM\_SerialController**</span></span>](cim-serialcontroller.md)
</dt> <dt>

[<span data-ttu-id="bc53c-672">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="bc53c-672">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 

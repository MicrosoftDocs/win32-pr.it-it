---
description: La \_ classe WMI POTSModem Win32 rappresenta i servizi e le caratteristiche di un modem del servizio telefonico (POTS) Plain Old in un computer che esegue Windows.
ms.assetid: 24589942-e2c3-477e-8179-59ae4a4aa85a
ms.tgt_platform: multiple
title: Classe Win32_POTSModem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_POTSModem
- Win32_POTSModem.Reset
- Win32_POTSModem.SetPowerState
- Win32_POTSModem.AnswerMode
- Win32_POTSModem.AttachedTo
- Win32_POTSModem.Availability
- Win32_POTSModem.BlindOff
- Win32_POTSModem.BlindOn
- Win32_POTSModem.Caption
- Win32_POTSModem.CompatibilityFlags
- Win32_POTSModem.CompressionInfo
- Win32_POTSModem.CompressionOff
- Win32_POTSModem.CompressionOn
- Win32_POTSModem.ConfigManagerErrorCode
- Win32_POTSModem.ConfigManagerUserConfig
- Win32_POTSModem.ConfigurationDialog
- Win32_POTSModem.CountriesSupported
- Win32_POTSModem.CountrySelected
- Win32_POTSModem.CreationClassName
- Win32_POTSModem.CurrentPasswords
- Win32_POTSModem.DCB
- Win32_POTSModem.Default
- Win32_POTSModem.Description
- Win32_POTSModem.DeviceID
- Win32_POTSModem.DeviceLoader
- Win32_POTSModem.DeviceType
- Win32_POTSModem.DialType
- Win32_POTSModem.DriverDate
- Win32_POTSModem.ErrorCleared
- Win32_POTSModem.ErrorControlForced
- Win32_POTSModem.ErrorControlInfo
- Win32_POTSModem.ErrorControlOff
- Win32_POTSModem.ErrorControlOn
- Win32_POTSModem.ErrorDescription
- Win32_POTSModem.FlowControlHard
- Win32_POTSModem.FlowControlOff
- Win32_POTSModem.FlowControlSoft
- Win32_POTSModem.InactivityScale
- Win32_POTSModem.InactivityTimeout
- Win32_POTSModem.Index
- Win32_POTSModem.IndexEx
- Win32_POTSModem.InstallDate
- Win32_POTSModem.LastErrorCode
- Win32_POTSModem.MaxBaudRateToPhone
- Win32_POTSModem.MaxBaudRateToSerialPort
- Win32_POTSModem.MaxNumberOfPasswords
- Win32_POTSModem.Model
- Win32_POTSModem.ModemInfPath
- Win32_POTSModem.ModemInfSection
- Win32_POTSModem.ModulationBell
- Win32_POTSModem.ModulationCCITT
- Win32_POTSModem.ModulationScheme
- Win32_POTSModem.Name
- Win32_POTSModem.PNPDeviceID
- Win32_POTSModem.PortSubClass
- Win32_POTSModem.PowerManagementCapabilities
- Win32_POTSModem.PowerManagementSupported
- Win32_POTSModem.Prefix
- Win32_POTSModem.Properties
- Win32_POTSModem.ProviderName
- Win32_POTSModem.Pulse
- Win32_POTSModem.Reset
- Win32_POTSModem.ResponsesKeyName
- Win32_POTSModem.RingsBeforeAnswer
- Win32_POTSModem.SpeakerModeDial
- Win32_POTSModem.SpeakerModeOff
- Win32_POTSModem.SpeakerModeOn
- Win32_POTSModem.SpeakerModeSetup
- Win32_POTSModem.SpeakerVolumeHigh
- Win32_POTSModem.SpeakerVolumeInfo
- Win32_POTSModem.SpeakerVolumeLow
- Win32_POTSModem.SpeakerVolumeMed
- Win32_POTSModem.Status
- Win32_POTSModem.StatusInfo
- Win32_POTSModem.StringFormat
- Win32_POTSModem.SupportsCallback
- Win32_POTSModem.SupportsSynchronousConnect
- Win32_POTSModem.SystemCreationClassName
- Win32_POTSModem.SystemName
- Win32_POTSModem.Terminator
- Win32_POTSModem.TimeOfLastReset
- Win32_POTSModem.Tone
- Win32_POTSModem.VoiceSwitchFeature
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6ec9634c5ee86d6819bf8f7a45dd521276565903
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877826"
---
# <a name="win32_potsmodem-class"></a><span data-ttu-id="18aa6-103">Win32 \_ POTSModem (classe)</span><span class="sxs-lookup"><span data-stu-id="18aa6-103">Win32\_POTSModem class</span></span>

<span data-ttu-id="18aa6-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ POTSModem Win32** rappresenta i servizi e le caratteristiche di un modem del servizio telefonico (POTS) Plain Old in un computer che esegue Windows.</span><span class="sxs-lookup"><span data-stu-id="18aa6-104">The **Win32\_POTSModem** [WMI class](../wmisdk/retrieving-a-class.md) represents the services and characteristics of a Plain Old Telephone Service (POTS) modem on a computer system running Windows.</span></span>

<span data-ttu-id="18aa6-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="18aa6-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="18aa6-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="18aa6-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="18aa6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="18aa6-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4BE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_POTSModem : CIM_PotsModem
{
  uint16   AnswerMode;
  string   AttachedTo;
  uint16   Availability;
  string   BlindOff;
  string   BlindOn;
  string   Caption;
  string   CompatibilityFlags;
  uint16   CompressionInfo;
  string   CompressionOff;
  string   CompressionOn;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   ConfigurationDialog;
  string   CountriesSupported[];
  string   CountrySelected;
  string   CreationClassName;
  string   CurrentPasswords[];
  uint8    DCB[];
  uint8    Default[];
  string   Description;
  string   DeviceID;
  string   DeviceLoader;
  string   DeviceType;
  uint16   DialType;
  datetime DriverDate;
  boolean  ErrorCleared;
  string   ErrorControlForced;
  uint16   ErrorControlInfo;
  string   ErrorControlOff;
  string   ErrorControlOn;
  string   ErrorDescription;
  string   FlowControlHard;
  string   FlowControlOff;
  string   FlowControlSoft;
  string   InactivityScale;
  uint32   InactivityTimeout;
  uint32   Index;
  string   IndexEx;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxBaudRateToPhone;
  uint32   MaxBaudRateToSerialPort;
  uint16   MaxNumberOfPasswords;
  string   Model;
  string   ModemInfPath;
  string   ModemInfSection;
  string   ModulationBell;
  string   ModulationCCITT;
  uint16   ModulationScheme;
  string   Name;
  string   PNPDeviceID;
  string   PortSubClass;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Prefix;
  uint8    Properties[];
  string   ProviderName;
  string   Pulse;
  string   Reset;
  string   ResponsesKeyName;
  uint8    RingsBeforeAnswer;
  string   SpeakerModeDial;
  string   SpeakerModeOff;
  string   SpeakerModeOn;
  string   SpeakerModeSetup;
  string   SpeakerVolumeHigh;
  uint16   SpeakerVolumeInfo;
  string   SpeakerVolumeLow;
  string   SpeakerVolumeMed;
  string   Status;
  uint16   StatusInfo;
  string   StringFormat;
  boolean  SupportsCallback;
  boolean  SupportsSynchronousConnect;
  string   SystemCreationClassName;
  string   SystemName;
  string   Terminator;
  datetime TimeOfLastReset;
  string   Tone;
  string   VoiceSwitchFeature;
};
```

## <a name="members"></a><span data-ttu-id="18aa6-108">Members</span><span class="sxs-lookup"><span data-stu-id="18aa6-108">Members</span></span>

<span data-ttu-id="18aa6-109">La classe **Win32 \_ POTSModem** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="18aa6-109">The **Win32\_POTSModem** class has these types of members:</span></span>

-   [<span data-ttu-id="18aa6-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="18aa6-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="18aa6-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="18aa6-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="18aa6-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="18aa6-112">Methods</span></span>

<span data-ttu-id="18aa6-113">La classe **Win32 \_ POTSModem** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="18aa6-113">The **Win32\_POTSModem** class has these methods.</span></span>



| <span data-ttu-id="18aa6-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="18aa6-114">Method</span></span>            | <span data-ttu-id="18aa6-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18aa6-115">Description</span></span>                                                                                                                                                                            |
|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18aa6-116">**Reimpostazione**</span><span class="sxs-lookup"><span data-stu-id="18aa6-116">**Reset**</span></span>         | <span data-ttu-id="18aa6-117">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="18aa6-117">Not implemented.</span></span> <span data-ttu-id="18aa6-118">Per implementare questo metodo, vedere il metodo [**Reset**](reset-method-in-class-cim-controller.md) in [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="18aa6-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_PotsModem**](cim-potsmodem.md).</span></span><br/>                 |
| <span data-ttu-id="18aa6-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="18aa6-119">**SetPowerState**</span></span> | <span data-ttu-id="18aa6-120">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="18aa6-120">Not implemented.</span></span> <span data-ttu-id="18aa6-121">Per implementare questo metodo, vedere il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) in [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="18aa6-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_PotsModem**](cim-potsmodem.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="18aa6-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="18aa6-122">Properties</span></span>

<span data-ttu-id="18aa6-123">La classe **Win32 \_ POTSModem** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="18aa6-123">The **Win32\_POTSModem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="18aa6-124">**AnswerMode**</span><span class="sxs-lookup"><span data-stu-id="18aa6-124">**AnswerMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-125">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18aa6-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-127">Impostazione della risposta automatica o di callback corrente per il modem.</span><span class="sxs-lookup"><span data-stu-id="18aa6-127">Current auto-answer or callback setting for the modem.</span></span>

<span data-ttu-id="18aa6-128">Questa proprietà viene ereditata da [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="18aa6-128">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18aa6-129">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="18aa6-129">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="18aa6-130">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="18aa6-130">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="18aa6-131">**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="18aa6-131">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Manual_Answer"></span><span id="manual_answer"></span><span id="MANUAL_ANSWER"></span>

<span data-ttu-id="18aa6-132">**Risposta manuale** (3)</span><span class="sxs-lookup"><span data-stu-id="18aa6-132">**Manual Answer** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto_Answer"></span><span id="auto_answer"></span><span id="AUTO_ANSWER"></span>

<span data-ttu-id="18aa6-133">**Risposta automatica** (4)</span><span class="sxs-lookup"><span data-stu-id="18aa6-133">**Auto Answer** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto_Answer_with_Call-Back"></span><span id="auto_answer_with_call-back"></span><span id="AUTO_ANSWER_WITH_CALL-BACK"></span>

<span data-ttu-id="18aa6-134">**Risposta automatica con Call-back** (5)</span><span class="sxs-lookup"><span data-stu-id="18aa6-134">**Auto Answer with Call-Back** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="18aa6-135">**AttachedTo**</span><span class="sxs-lookup"><span data-stu-id="18aa6-135">**AttachedTo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-136">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-138">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| legatiai")</span><span class="sxs-lookup"><span data-stu-id="18aa6-138">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|AttachedTo")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-139">Porta a cui è collegato il modem pot.</span><span class="sxs-lookup"><span data-stu-id="18aa6-139">Port to which the POTS modem is attached.</span></span>

<span data-ttu-id="18aa6-140">Esempio: "COM1"</span><span class="sxs-lookup"><span data-stu-id="18aa6-140">Example: "COM1"</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-141">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="18aa6-141">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-142">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18aa6-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-144">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="18aa6-144">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-145">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18aa6-145">Availability and status of the device.</span></span>

<span data-ttu-id="18aa6-146">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18aa6-146">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="18aa6-147"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="18aa6-147"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18aa6-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="18aa6-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="18aa6-149"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="18aa6-149"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-150">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="18aa6-150">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="18aa6-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="18aa6-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="18aa6-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="18aa6-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="18aa6-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="18aa6-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="18aa6-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="18aa6-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="18aa6-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="18aa6-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="18aa6-156"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="18aa6-156"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="18aa6-157"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="18aa6-157"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="18aa6-158"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="18aa6-158"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="18aa6-159"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="18aa6-159"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="18aa6-160"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="18aa6-160"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-161">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="18aa6-161">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="18aa6-162"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="18aa6-162"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-163">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="18aa6-163">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="18aa6-164"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="18aa6-164"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-165">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="18aa6-165">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="18aa6-166"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="18aa6-166"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="18aa6-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="18aa6-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-168">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="18aa6-168">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="18aa6-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="18aa6-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-170">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="18aa6-170">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="18aa6-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="18aa6-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-172">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="18aa6-172">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="18aa6-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="18aa6-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-174">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="18aa6-174">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="18aa6-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="18aa6-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-176">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="18aa6-176">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="18aa6-177">**BlindOff**</span><span class="sxs-lookup"><span data-stu-id="18aa6-177">**BlindOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-178">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-180">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| BlindOff")</span><span class="sxs-lookup"><span data-stu-id="18aa6-180">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|BlindOff")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-181">Stringa di comando utilizzata per rilevare un tono di connessione prima della connessione.</span><span class="sxs-lookup"><span data-stu-id="18aa6-181">Command string used to detect a dial tone before dialing.</span></span>

<span data-ttu-id="18aa6-182">Esempio: "x4"</span><span class="sxs-lookup"><span data-stu-id="18aa6-182">Example: "X4"</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-183">**BlindOn**</span><span class="sxs-lookup"><span data-stu-id="18aa6-183">**BlindOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-184">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-186">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| Blindon")</span><span class="sxs-lookup"><span data-stu-id="18aa6-186">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|BlindOn")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-187">Stringa di comando usata per comporre se è presente un tono di composizione.</span><span class="sxs-lookup"><span data-stu-id="18aa6-187">Command string used to dial whether or not there is a dial tone.</span></span>

<span data-ttu-id="18aa6-188">Esempio: "X3"</span><span class="sxs-lookup"><span data-stu-id="18aa6-188">Example: "X3"</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-189">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="18aa6-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-190">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-192">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="18aa6-192">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-193">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="18aa6-193">Short description of the object.</span></span>

<span data-ttu-id="18aa6-194">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="18aa6-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-195">**CompatibilityFlags**</span><span class="sxs-lookup"><span data-stu-id="18aa6-195">**CompatibilityFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-196">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-197">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-198">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| CompatibilityFlags")</span><span class="sxs-lookup"><span data-stu-id="18aa6-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|CompatibilityFlags")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-199">Tutti i protocolli di connessione modem con cui questo dispositivo modem è compatibile.</span><span class="sxs-lookup"><span data-stu-id="18aa6-199">All modem connection protocols with which this modem device is compatible.</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-200">**CompressionInfo**</span><span class="sxs-lookup"><span data-stu-id="18aa6-200">**CompressionInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-201">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18aa6-201">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-202">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-203">Caratteristiche di compressione dei dati del modem.</span><span class="sxs-lookup"><span data-stu-id="18aa6-203">Data compression characteristics of the modem.</span></span>

<span data-ttu-id="18aa6-204">Questa proprietà viene ereditata da [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="18aa6-204">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18aa6-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="18aa6-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="18aa6-206"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="18aa6-206"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-207">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="18aa6-207">Unknown</span></span>

</dd> <dt>

<span id="No_Compression"></span><span id="no_compression"></span><span id="NO_COMPRESSION"></span>

<span data-ttu-id="18aa6-208"><span id="No_Compression"></span><span id="no_compression"></span><span id="NO_COMPRESSION"></span>**Nessuna compressione** (2)</span><span class="sxs-lookup"><span data-stu-id="18aa6-208"><span id="No_Compression"></span><span id="no_compression"></span><span id="NO_COMPRESSION"></span>**No Compression** (2)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-209">Altro</span><span class="sxs-lookup"><span data-stu-id="18aa6-209">Other</span></span>

</dd> <dt>

<span id="MNP_5"></span><span id="mnp_5"></span>

<span data-ttu-id="18aa6-210"><span id="MNP_5"></span><span id="mnp_5"></span>**MNP 5** (3)</span><span class="sxs-lookup"><span data-stu-id="18aa6-210"><span id="MNP_5"></span><span id="mnp_5"></span>**MNP 5** (3)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-211">Nessuna compressione</span><span class="sxs-lookup"><span data-stu-id="18aa6-211">No Compression</span></span>

</dd> <dt>

<span id="V.42bis"></span><span id="v.42bis"></span><span id="V.42BIS"></span>

<span data-ttu-id="18aa6-212"><span id="v.42bis"></span><span id="V.42BIS"></span>**V. 42bis** (4)</span><span class="sxs-lookup"><span data-stu-id="18aa6-212"><span id="v.42bis"></span><span id="V.42BIS"></span>**V.42bis** (4)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-213">MNP 5</span><span class="sxs-lookup"><span data-stu-id="18aa6-213">MNP 5</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="18aa6-214"><span id="5"></span>**5**</span><span class="sxs-lookup"><span data-stu-id="18aa6-214"><span id="5"></span>**5**</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-215">V. 42bis</span><span class="sxs-lookup"><span data-stu-id="18aa6-215">V.42bis</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="18aa6-216">**CompressionOff**</span><span class="sxs-lookup"><span data-stu-id="18aa6-216">**CompressionOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-217">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-218">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-219">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| Compression \_ off")</span><span class="sxs-lookup"><span data-stu-id="18aa6-219">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Compression\_Off")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-220">Stringa di comando utilizzata per disabilitare la compressione dei dati hardware.</span><span class="sxs-lookup"><span data-stu-id="18aa6-220">Command string used to disable hardware data compression.</span></span>

<span data-ttu-id="18aa6-221">Esempio: "S46 = 136"</span><span class="sxs-lookup"><span data-stu-id="18aa6-221">Example: "S46=136"</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-222">**CompressionOn**</span><span class="sxs-lookup"><span data-stu-id="18aa6-222">**CompressionOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-223">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-224">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-225">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| Compression \_ on")</span><span class="sxs-lookup"><span data-stu-id="18aa6-225">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Compression\_On")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-226">Stringa di comando utilizzata per abilitare la compressione dei dati hardware.</span><span class="sxs-lookup"><span data-stu-id="18aa6-226">Command string used to enable hardware data compression.</span></span>

<span data-ttu-id="18aa6-227">Esempio: "S46 = 138"</span><span class="sxs-lookup"><span data-stu-id="18aa6-227">Example: "S46=138"</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-228">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="18aa6-228">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-229">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="18aa6-229">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-230">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-231">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="18aa6-231">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-232">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="18aa6-232">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="18aa6-233">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18aa6-233">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="18aa6-234"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="18aa6-234"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="18aa6-235"> (0)</span><span class="sxs-lookup"><span data-stu-id="18aa6-235">(0)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-236">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="18aa6-236">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="18aa6-237"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="18aa6-237"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="18aa6-238">(1)</span><span class="sxs-lookup"><span data-stu-id="18aa6-238">(1)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-239">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="18aa6-239">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="18aa6-240"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="18aa6-240"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="18aa6-241">(2)</span><span class="sxs-lookup"><span data-stu-id="18aa6-241">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="18aa6-242"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="18aa6-242"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="18aa6-243">(3)</span><span class="sxs-lookup"><span data-stu-id="18aa6-243">(3)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-244">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="18aa6-244">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="18aa6-245"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="18aa6-245"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="18aa6-246">(4)</span><span class="sxs-lookup"><span data-stu-id="18aa6-246">(4)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-247">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="18aa6-247">Device is not working properly.</span></span> <span data-ttu-id="18aa6-248">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="18aa6-248">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="18aa6-249"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="18aa6-249"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="18aa6-250">(5)</span><span class="sxs-lookup"><span data-stu-id="18aa6-250">(5)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-251">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="18aa6-251">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="18aa6-252"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="18aa6-252"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="18aa6-253"> (6)</span><span class="sxs-lookup"><span data-stu-id="18aa6-253">(6)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-254">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="18aa6-254">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="18aa6-255"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="18aa6-255"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="18aa6-256">(7)</span><span class="sxs-lookup"><span data-stu-id="18aa6-256">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="18aa6-257"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="18aa6-257"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="18aa6-258">(8)</span><span class="sxs-lookup"><span data-stu-id="18aa6-258">(8)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-259">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="18aa6-259">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="18aa6-260"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="18aa6-260"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="18aa6-261">(9)</span><span class="sxs-lookup"><span data-stu-id="18aa6-261">(9)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-262">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="18aa6-262">Device is not working properly.</span></span> <span data-ttu-id="18aa6-263">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18aa6-263">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="18aa6-264"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="18aa6-264"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="18aa6-265">(10)</span><span class="sxs-lookup"><span data-stu-id="18aa6-265">(10)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-266">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18aa6-266">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="18aa6-267"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="18aa6-267"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="18aa6-268">(11)</span><span class="sxs-lookup"><span data-stu-id="18aa6-268">(11)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-269">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18aa6-269">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="18aa6-270"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="18aa6-270"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="18aa6-271">12</span><span class="sxs-lookup"><span data-stu-id="18aa6-271">(12)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-272">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="18aa6-272">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="18aa6-273"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="18aa6-273"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="18aa6-274">(13)</span><span class="sxs-lookup"><span data-stu-id="18aa6-274">(13)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-275">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18aa6-275">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="18aa6-276"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="18aa6-276"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="18aa6-277">(14)</span><span class="sxs-lookup"><span data-stu-id="18aa6-277">(14)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-278">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="18aa6-278">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="18aa6-279"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="18aa6-279"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="18aa6-280">(15)</span><span class="sxs-lookup"><span data-stu-id="18aa6-280">(15)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-281">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="18aa6-281">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="18aa6-282"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="18aa6-282"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="18aa6-283">(16)</span><span class="sxs-lookup"><span data-stu-id="18aa6-283">(16)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-284">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18aa6-284">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="18aa6-285"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="18aa6-285"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="18aa6-286">(17)</span><span class="sxs-lookup"><span data-stu-id="18aa6-286">(17)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-287">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="18aa6-287">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="18aa6-288"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="18aa6-288"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="18aa6-289">(18)</span><span class="sxs-lookup"><span data-stu-id="18aa6-289">(18)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-290">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18aa6-290">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="18aa6-291"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="18aa6-291"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="18aa6-292">(19)</span><span class="sxs-lookup"><span data-stu-id="18aa6-292">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="18aa6-293"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="18aa6-293"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="18aa6-294">(20)</span><span class="sxs-lookup"><span data-stu-id="18aa6-294">(20)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-295">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="18aa6-295">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="18aa6-296"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="18aa6-296"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="18aa6-297">(21)</span><span class="sxs-lookup"><span data-stu-id="18aa6-297">(21)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-298">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="18aa6-298">System failure.</span></span> <span data-ttu-id="18aa6-299">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="18aa6-299">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="18aa6-300">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18aa6-300">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="18aa6-301"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="18aa6-301"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="18aa6-302">(22)</span><span class="sxs-lookup"><span data-stu-id="18aa6-302">(22)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-303">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="18aa6-303">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="18aa6-304"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="18aa6-304"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="18aa6-305">(23)</span><span class="sxs-lookup"><span data-stu-id="18aa6-305">(23)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-306">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="18aa6-306">System failure.</span></span> <span data-ttu-id="18aa6-307">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="18aa6-307">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="18aa6-308"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="18aa6-308"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="18aa6-309">(24)</span><span class="sxs-lookup"><span data-stu-id="18aa6-309">(24)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-310">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="18aa6-310">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="18aa6-311"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="18aa6-311"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="18aa6-312">(25)</span><span class="sxs-lookup"><span data-stu-id="18aa6-312">(25)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-313">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18aa6-313">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="18aa6-314"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="18aa6-314"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="18aa6-315">(26)</span><span class="sxs-lookup"><span data-stu-id="18aa6-315">(26)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-316">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18aa6-316">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="18aa6-317"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="18aa6-317"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="18aa6-318">(27)</span><span class="sxs-lookup"><span data-stu-id="18aa6-318">(27)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-319">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="18aa6-319">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="18aa6-320"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="18aa6-320"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="18aa6-321">(28)</span><span class="sxs-lookup"><span data-stu-id="18aa6-321">(28)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-322">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="18aa6-322">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="18aa6-323"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="18aa6-323"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="18aa6-324">(29)</span><span class="sxs-lookup"><span data-stu-id="18aa6-324">(29)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-325">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="18aa6-325">Device is disabled.</span></span> <span data-ttu-id="18aa6-326">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="18aa6-326">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="18aa6-327"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="18aa6-327"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="18aa6-328">(30)</span><span class="sxs-lookup"><span data-stu-id="18aa6-328">(30)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-329">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18aa6-329">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="18aa6-330"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="18aa6-330"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="18aa6-331">31</span><span class="sxs-lookup"><span data-stu-id="18aa6-331">(31)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-332">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="18aa6-332">Device is not working properly.</span></span> <span data-ttu-id="18aa6-333">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="18aa6-333">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="18aa6-334">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="18aa6-334">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-335">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="18aa6-335">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-336">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-337">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="18aa6-337">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-338">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="18aa6-338">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="18aa6-339">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18aa6-339">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-340">**ConfigurationDialog**</span><span class="sxs-lookup"><span data-stu-id="18aa6-340">**ConfigurationDialog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-341">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-342">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-343">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| ConfigDialog")</span><span class="sxs-lookup"><span data-stu-id="18aa6-343">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ConfigDialog")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-344">Stringa di inizializzazione del modem.</span><span class="sxs-lookup"><span data-stu-id="18aa6-344">Modem initialization string.</span></span> <span data-ttu-id="18aa6-345">Questa proprietà è costituita da stringhe di comando di altre proprietà di questa classe.</span><span class="sxs-lookup"><span data-stu-id="18aa6-345">This property is made up of command strings from other properties of this class.</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-346">**CountriesSupported**</span><span class="sxs-lookup"><span data-stu-id="18aa6-346">**CountriesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-347">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="18aa6-347">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-348">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-349">Matrice di paesi/aree geografiche in cui il modem può funzionare.</span><span class="sxs-lookup"><span data-stu-id="18aa6-349">Array of countries/regions in which the modem can operate.</span></span>

<span data-ttu-id="18aa6-350">Questa proprietà viene ereditata da [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="18aa6-350">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-351">**CountrySelected**</span><span class="sxs-lookup"><span data-stu-id="18aa6-351">**CountrySelected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-352">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-353">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-354">Paese/area geografica per cui il modem è attualmente programmato.</span><span class="sxs-lookup"><span data-stu-id="18aa6-354">Country/region for which the modem is currently programmed.</span></span> <span data-ttu-id="18aa6-355">Quando sono supportati più paesi o aree geografiche, questa proprietà definisce quello attualmente selezionato per l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="18aa6-355">When multiple countries/regions are supported, this property defines which one is currently selected for use.</span></span>

<span data-ttu-id="18aa6-356">Questa proprietà viene ereditata da [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="18aa6-356">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-357">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="18aa6-357">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-358">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-359">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-360">Qualificatori: [ **\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="18aa6-360">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-361">Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="18aa6-361">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="18aa6-362">Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="18aa6-362">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="18aa6-363">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="18aa6-363">This property is inherited from [**CIM\_LogicalDevice**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-364">**CurrentPasswords**</span><span class="sxs-lookup"><span data-stu-id="18aa6-364">**CurrentPasswords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-365">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="18aa6-365">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-366">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-367">Elenco delle password attualmente definite per il modem.</span><span class="sxs-lookup"><span data-stu-id="18aa6-367">List of currently defined passwords for the modem.</span></span> <span data-ttu-id="18aa6-368">Questa matrice può essere lasciata vuota per motivi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="18aa6-368">This array may be left blank for security reasons.</span></span>

<span data-ttu-id="18aa6-369">Questa proprietà viene ereditata da [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="18aa6-369">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-370">**DCB**</span><span class="sxs-lookup"><span data-stu-id="18aa6-370">**DCB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-371">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="18aa6-371">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-372">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-373">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)")</span><span class="sxs-lookup"><span data-stu-id="18aa6-373">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-374">Impostazioni di controllo per un dispositivo di comunicazione seriale, in questo caso il dispositivo modem.</span><span class="sxs-lookup"><span data-stu-id="18aa6-374">Control settings for a serial communications device, in this case, the modem device.</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-375">**Default**</span><span class="sxs-lookup"><span data-stu-id="18aa6-375">**Default**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-376">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="18aa6-376">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-377">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-378">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| default")</span><span class="sxs-lookup"><span data-stu-id="18aa6-378">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Default")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-379">Se **true**, questo modem di POT è il modem predefinito nel computer che esegue Windows.</span><span class="sxs-lookup"><span data-stu-id="18aa6-379">If **TRUE**, this POTS modem is the default modem on the computer system running Windows.</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-380">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="18aa6-380">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-381">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-382">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-383">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="18aa6-383">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-384">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="18aa6-384">Description of the object.</span></span>

<span data-ttu-id="18aa6-385">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="18aa6-385">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-386">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="18aa6-386">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-387">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-388">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-389">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="18aa6-389">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-390">Identificatore univoco di questo modem POT da altri dispositivi nel sistema.</span><span class="sxs-lookup"><span data-stu-id="18aa6-390">Unique identifier of this POTS modem from other devices on the system.</span></span>

<span data-ttu-id="18aa6-391">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18aa6-391">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-392">**DeviceLoader**</span><span class="sxs-lookup"><span data-stu-id="18aa6-392">**DeviceLoader**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-393">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-393">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-394">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-395">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| DevLoader")</span><span class="sxs-lookup"><span data-stu-id="18aa6-395">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|DevLoader")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-396">Nome del caricatore del dispositivo per il modem.</span><span class="sxs-lookup"><span data-stu-id="18aa6-396">Name of the device loader for the modem.</span></span> <span data-ttu-id="18aa6-397">Un caricatore del dispositivo carica e gestisce i driver e gli enumeratori di dispositivo per un determinato dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18aa6-397">A device loader loads and manages device drivers and enumerators for a given device.</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-398">**DeviceType**</span><span class="sxs-lookup"><span data-stu-id="18aa6-398">**DeviceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-399">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-400">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-401">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| DeviceType")</span><span class="sxs-lookup"><span data-stu-id="18aa6-401">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|DeviceType")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-402">Tipo fisico del modem.</span><span class="sxs-lookup"><span data-stu-id="18aa6-402">Physical type of the modem.</span></span>

<span data-ttu-id="18aa6-403">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="18aa6-403">The values are:</span></span>

<dl> <dd><span data-ttu-id="18aa6-404">"Modem null"</span><span class="sxs-lookup"><span data-stu-id="18aa6-404">"Null Modem"</span></span></dd> <dd><span data-ttu-id="18aa6-405">"Modem interno"</span><span class="sxs-lookup"><span data-stu-id="18aa6-405">"Internal Modem"</span></span></dd> <dd><span data-ttu-id="18aa6-406">"Modem esterno"</span><span class="sxs-lookup"><span data-stu-id="18aa6-406">"External Modem"</span></span></dd> <dd><span data-ttu-id="18aa6-407">"Modem PCMCIA"</span><span class="sxs-lookup"><span data-stu-id="18aa6-407">"PCMCIA Modem"</span></span></dd> <dd><span data-ttu-id="18aa6-408">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="18aa6-408">"Unknown"</span></span></dd> </dl>

<dt>

<span id="Null_Modem"></span><span id="null_modem"></span><span id="NULL_MODEM"></span>

<span data-ttu-id="18aa6-409">**Modem null** ("modem null")</span><span class="sxs-lookup"><span data-stu-id="18aa6-409">**Null Modem** ("Null Modem")</span></span>


</dt> <dd></dd> <dt>

<span id="Internal_Modem"></span><span id="internal_modem"></span><span id="INTERNAL_MODEM"></span>

<span data-ttu-id="18aa6-410">**Modem interno** ("modem interno")</span><span class="sxs-lookup"><span data-stu-id="18aa6-410">**Internal Modem** ("Internal Modem")</span></span>


</dt> <dd></dd> <dt>

<span id="External_Modem"></span><span id="external_modem"></span><span id="EXTERNAL_MODEM"></span>

<span data-ttu-id="18aa6-411">**Modem esterno** ("modem esterno")</span><span class="sxs-lookup"><span data-stu-id="18aa6-411">**External Modem** ("External Modem")</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Modem"></span><span id="pcmcia_modem"></span><span id="PCMCIA_MODEM"></span>

<span data-ttu-id="18aa6-412">**Modem PCMCIA** ("modem PCMCIA")</span><span class="sxs-lookup"><span data-stu-id="18aa6-412">**PCMCIA Modem** ("PCMCIA Modem")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18aa6-413">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="18aa6-413">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="18aa6-414">**DialType**</span><span class="sxs-lookup"><span data-stu-id="18aa6-414">**DialType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-415">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18aa6-415">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-416">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-417">Tipo di metodo di composizione utilizzato.</span><span class="sxs-lookup"><span data-stu-id="18aa6-417">Type of dialing method used.</span></span>

<span data-ttu-id="18aa6-418">Questa proprietà viene ereditata da [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="18aa6-418">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18aa6-419">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="18aa6-419">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Tone"></span><span id="tone"></span><span id="TONE"></span>

<span data-ttu-id="18aa6-420">**Tono** (1)</span><span class="sxs-lookup"><span data-stu-id="18aa6-420">**Tone** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Pulse"></span><span id="pulse"></span><span id="PULSE"></span>

<span data-ttu-id="18aa6-421">**Impulsi** (2)</span><span class="sxs-lookup"><span data-stu-id="18aa6-421">**Pulse** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="18aa6-422">**DriverDate**</span><span class="sxs-lookup"><span data-stu-id="18aa6-422">**DriverDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-423">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="18aa6-423">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-424">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-425">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| DriverDate")</span><span class="sxs-lookup"><span data-stu-id="18aa6-425">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|DriverDate")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-426">Data del driver del modem.</span><span class="sxs-lookup"><span data-stu-id="18aa6-426">Date of the modem driver.</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-427">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="18aa6-427">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-428">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="18aa6-428">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-429">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-430">Se **true**, l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="18aa6-430">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="18aa6-431">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18aa6-431">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-432">**ErrorControlForced**</span><span class="sxs-lookup"><span data-stu-id="18aa6-432">**ErrorControlForced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-433">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-434">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-434">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-435">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| ErrorControl \_ forced")</span><span class="sxs-lookup"><span data-stu-id="18aa6-435">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ErrorControl\_Forced")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-436">Stringa di comando utilizzata per abilitare il controllo della correzione degli errori quando si stabilisce una connessione.</span><span class="sxs-lookup"><span data-stu-id="18aa6-436">Command string used to enable error correction control when establishing a connection.</span></span> <span data-ttu-id="18aa6-437">Ciò aumenta l'affidabilità della connessione.</span><span class="sxs-lookup"><span data-stu-id="18aa6-437">This increases the reliability of the connection.</span></span>

<span data-ttu-id="18aa6-438">Esempio: "+ Q5S36 = 4S48 = 7"</span><span class="sxs-lookup"><span data-stu-id="18aa6-438">Example: "+Q5S36=4S48=7"</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-439">**ErrorControlInfo**</span><span class="sxs-lookup"><span data-stu-id="18aa6-439">**ErrorControlInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-440">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18aa6-440">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-441">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-442">Caratteristiche di correzione degli errori del modem.</span><span class="sxs-lookup"><span data-stu-id="18aa6-442">Error correction characteristics of the modem.</span></span>

<span data-ttu-id="18aa6-443">Questa proprietà viene ereditata da [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="18aa6-443">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18aa6-444">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="18aa6-444">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="18aa6-445">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="18aa6-445">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Error_Correction"></span><span id="no_error_correction"></span><span id="NO_ERROR_CORRECTION"></span>

<span data-ttu-id="18aa6-446">**Nessuna correzione errori** (2)</span><span class="sxs-lookup"><span data-stu-id="18aa6-446">**No Error Correction** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MNP_4"></span><span id="mnp_4"></span>

<span data-ttu-id="18aa6-447">**MNP 4** (3)</span><span class="sxs-lookup"><span data-stu-id="18aa6-447">**MNP 4** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="LAPM"></span><span id="lapm"></span>

<span data-ttu-id="18aa6-448">**LAPM** (4)</span><span class="sxs-lookup"><span data-stu-id="18aa6-448">**LAPM** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="18aa6-449">**ErrorControlOff**</span><span class="sxs-lookup"><span data-stu-id="18aa6-449">**ErrorControlOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-450">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-450">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-451">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-452">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| ErrorControl \_ off")</span><span class="sxs-lookup"><span data-stu-id="18aa6-452">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ErrorControl\_Off")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-453">Stringa di comando utilizzata per disabilitare il controllo degli errori.</span><span class="sxs-lookup"><span data-stu-id="18aa6-453">Command string used to disable error control.</span></span>

<span data-ttu-id="18aa6-454">Esempio: "+ Q6S36 = 3S48 = 128"</span><span class="sxs-lookup"><span data-stu-id="18aa6-454">Example: "+Q6S36=3S48=128"</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-455">**ErrorControlOn**</span><span class="sxs-lookup"><span data-stu-id="18aa6-455">**ErrorControlOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-456">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-456">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-457">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-458">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| ErrorControl \_ on")</span><span class="sxs-lookup"><span data-stu-id="18aa6-458">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ErrorControl\_On")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-459">Stringa di comando utilizzata per abilitare il controllo degli errori.</span><span class="sxs-lookup"><span data-stu-id="18aa6-459">Command string used to enable error control.</span></span>

<span data-ttu-id="18aa6-460">Esempio: "+ Q5S36 = 7S48 = 7"</span><span class="sxs-lookup"><span data-stu-id="18aa6-460">Example: "+Q5S36=7S48=7"</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-461">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="18aa6-461">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-462">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-462">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-463">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-463">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-464">Altre informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="18aa6-464">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="18aa6-465">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18aa6-465">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-466">**FlowControlHard**</span><span class="sxs-lookup"><span data-stu-id="18aa6-466">**FlowControlHard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-467">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-467">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-468">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-469">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| FlowControl \_ hard")</span><span class="sxs-lookup"><span data-stu-id="18aa6-469">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|FlowControl\_Hard")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-470">Stringa di comando usata per abilitare il controllo del flusso hardware.</span><span class="sxs-lookup"><span data-stu-id="18aa6-470">Command string used to enable hardware flow control.</span></span> <span data-ttu-id="18aa6-471">Il controllo di flusso è costituito da segnali inviati tra computer che verificano che entrambi i computer siano pronti per la trasmissione o la ricezione di dati.</span><span class="sxs-lookup"><span data-stu-id="18aa6-471">Flow control consists of signals sent between computers that verify that both computers are ready to transmit or receive data.</span></span>

<span data-ttu-id="18aa6-472">Esempio: "&K1"</span><span class="sxs-lookup"><span data-stu-id="18aa6-472">Example: "&K1"</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-473">**FlowControlOff**</span><span class="sxs-lookup"><span data-stu-id="18aa6-473">**FlowControlOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-474">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-475">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-476">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| FlowControl \_ off")</span><span class="sxs-lookup"><span data-stu-id="18aa6-476">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|FlowControl\_Off")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-477">Stringa di comando usata per disabilitare il controllo di flusso.</span><span class="sxs-lookup"><span data-stu-id="18aa6-477">Command string used to disable flow control.</span></span> <span data-ttu-id="18aa6-478">Il controllo di flusso è costituito da segnali inviati tra computer che verificano che entrambi i computer siano pronti per la trasmissione o la ricezione di dati.</span><span class="sxs-lookup"><span data-stu-id="18aa6-478">Flow control consists of signals sent between computers that verify that both computers are ready to transmit or receive data.</span></span>

<span data-ttu-id="18aa6-479">Esempio: "&K0"</span><span class="sxs-lookup"><span data-stu-id="18aa6-479">Example: "&K0"</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-480">**FlowControlSoft**</span><span class="sxs-lookup"><span data-stu-id="18aa6-480">**FlowControlSoft**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-481">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-482">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-483">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| FlowControl \_ soft")</span><span class="sxs-lookup"><span data-stu-id="18aa6-483">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|FlowControl\_Soft")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-484">Stringa di comando usata per abilitare il controllo del flusso software.</span><span class="sxs-lookup"><span data-stu-id="18aa6-484">Command string used to enable software flow control.</span></span> <span data-ttu-id="18aa6-485">Il controllo di flusso è costituito da segnali inviati tra computer che verificano che entrambi i computer siano pronti per la trasmissione o la ricezione di dati.</span><span class="sxs-lookup"><span data-stu-id="18aa6-485">Flow control consists of signals sent between computers that verify that both computers are ready to transmit or receive data.</span></span>

<span data-ttu-id="18aa6-486">Esempio: "&K2"</span><span class="sxs-lookup"><span data-stu-id="18aa6-486">Example: "&K2"</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-487">**InactivityScale**</span><span class="sxs-lookup"><span data-stu-id="18aa6-487">**InactivityScale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-488">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-488">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-489">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-489">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-490">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| InactivityScale")</span><span class="sxs-lookup"><span data-stu-id="18aa6-490">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|InactivityScale")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-491">Moltiplicatore utilizzato con la proprietà **InactivityTimeout** per calcolare il periodo di timeout di una connessione.</span><span class="sxs-lookup"><span data-stu-id="18aa6-491">Multiplier used with the **InactivityTimeout** property to calculate the timeout period of a connection.</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-492">**InactivityTimeout**</span><span class="sxs-lookup"><span data-stu-id="18aa6-492">**InactivityTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-493">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="18aa6-493">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-494">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-495">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("secondi")</span><span class="sxs-lookup"><span data-stu-id="18aa6-495">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-496">Limite di tempo (in secondi) per la disconnessione automatica della linea telefonica, se non vengono scambiati dati.</span><span class="sxs-lookup"><span data-stu-id="18aa6-496">Time limit (in seconds) for automatic disconnection of the phone line, if no data is exchanged.</span></span> <span data-ttu-id="18aa6-497">Il valore 0 (zero) indica che questa funzionalità è presente ma non abilitata.</span><span class="sxs-lookup"><span data-stu-id="18aa6-497">A value of 0 (zero) indicates that this feature is present but not enabled.</span></span>

<span data-ttu-id="18aa6-498">Questa proprietà viene ereditata da [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="18aa6-498">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-499">**Index**</span><span class="sxs-lookup"><span data-stu-id="18aa6-499">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-500">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="18aa6-500">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-501">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-501">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-502">Numero di indice per questo modem POTS.</span><span class="sxs-lookup"><span data-stu-id="18aa6-502">Index number for this POTS modem.</span></span>

<span data-ttu-id="18aa6-503">Esempio: 0</span><span class="sxs-lookup"><span data-stu-id="18aa6-503">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-504">**IndexEx**</span><span class="sxs-lookup"><span data-stu-id="18aa6-504">**IndexEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-505">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-506">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-506">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-507">ID dell'istanza del dispositivo per questo modem di pot.</span><span class="sxs-lookup"><span data-stu-id="18aa6-507">The device instance ID for this POTS modem.</span></span>

<span data-ttu-id="18aa6-508">Esempio: "1&08"</span><span class="sxs-lookup"><span data-stu-id="18aa6-508">Example: "1&08"</span></span>

<span data-ttu-id="18aa6-509">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Questa proprietà è disponibile a partire da Windows Server 2016 e Windows 10.</span><span class="sxs-lookup"><span data-stu-id="18aa6-509">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is available beginning with Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-510">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="18aa6-510">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-511">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="18aa6-511">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-512">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-513">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="18aa6-513">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-514">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="18aa6-514">Date and time the object was installed.</span></span> <span data-ttu-id="18aa6-515">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="18aa6-515">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="18aa6-516">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="18aa6-516">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-517">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="18aa6-517">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-518">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="18aa6-518">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-519">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-520">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="18aa6-520">Last error code reported by the logical device.</span></span>

<span data-ttu-id="18aa6-521">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18aa6-521">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-522">**MaxBaudRateToPhone**</span><span class="sxs-lookup"><span data-stu-id="18aa6-522">**MaxBaudRateToPhone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-523">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="18aa6-523">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-524">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-525">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("bit al secondo")</span><span class="sxs-lookup"><span data-stu-id="18aa6-525">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-526">Velocità di comunicazione massima impostabile per l'accesso al sistema telefonico.</span><span class="sxs-lookup"><span data-stu-id="18aa6-526">Maximum settable communication speed for accessing the phone system.</span></span>

<span data-ttu-id="18aa6-527">Questa proprietà viene ereditata da [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="18aa6-527">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-528">**MaxBaudRateToSerialPort**</span><span class="sxs-lookup"><span data-stu-id="18aa6-528">**MaxBaudRateToSerialPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-529">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="18aa6-529">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-530">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-530">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-531">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("bit al secondo")</span><span class="sxs-lookup"><span data-stu-id="18aa6-531">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-532">Velocità di comunicazione massima impostabile per la porta COM per un modem esterno.</span><span class="sxs-lookup"><span data-stu-id="18aa6-532">Maximum settable communication speed to the COM port for an external modem.</span></span> <span data-ttu-id="18aa6-533">Immettere 0 (zero) se non è applicabile.</span><span class="sxs-lookup"><span data-stu-id="18aa6-533">Enter 0 (zero) if not applicable.</span></span>

<span data-ttu-id="18aa6-534">Questa proprietà viene ereditata da [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="18aa6-534">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-535">**MaxNumberOfPasswords**</span><span class="sxs-lookup"><span data-stu-id="18aa6-535">**MaxNumberOfPasswords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-536">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18aa6-536">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-537">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-538">Numero di password definibili nel modem.</span><span class="sxs-lookup"><span data-stu-id="18aa6-538">Number of passwords definable in the modem itself.</span></span> <span data-ttu-id="18aa6-539">Se questa funzionalità non è supportata, immettere 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="18aa6-539">If this feature is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="18aa6-540">Questa proprietà viene ereditata da [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="18aa6-540">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-541">**Modello**</span><span class="sxs-lookup"><span data-stu-id="18aa6-541">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-542">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-542">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-543">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-543">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-544">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| Model")</span><span class="sxs-lookup"><span data-stu-id="18aa6-544">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Model")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-545">Modello di questo modem di pot.</span><span class="sxs-lookup"><span data-stu-id="18aa6-545">Model of this POTS modem.</span></span>

<span data-ttu-id="18aa6-546">Esempio: "Sportster 56K External"</span><span class="sxs-lookup"><span data-stu-id="18aa6-546">Example: "Sportster 56K External"</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-547">**ModemInfPath**</span><span class="sxs-lookup"><span data-stu-id="18aa6-547">**ModemInfPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-548">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-548">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-549">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-549">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-550">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| InfPath")</span><span class="sxs-lookup"><span data-stu-id="18aa6-550">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|InfPath")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-551">Percorso del file con estensione inf del modem.</span><span class="sxs-lookup"><span data-stu-id="18aa6-551">Path to this modem's .inf file.</span></span> <span data-ttu-id="18aa6-552">Questo file contiene le informazioni di inizializzazione per il modem e il relativo driver.</span><span class="sxs-lookup"><span data-stu-id="18aa6-552">This file contains initialization information for the modem and its driver.</span></span>

<span data-ttu-id="18aa6-553">Esempio: "C: \\ Windows \\ inf"</span><span class="sxs-lookup"><span data-stu-id="18aa6-553">Example: "C:\\Windows\\INF"</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-554">**ModemInfSection**</span><span class="sxs-lookup"><span data-stu-id="18aa6-554">**ModemInfSection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-555">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-555">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-556">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-556">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-557">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| InfSection")</span><span class="sxs-lookup"><span data-stu-id="18aa6-557">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|InfSection")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-558">Nome della sezione nel file inf del modem che contiene informazioni sul modem.</span><span class="sxs-lookup"><span data-stu-id="18aa6-558">Name of the section in the modem's .inf file that contains information about the modem.</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-559">**ModulationBell**</span><span class="sxs-lookup"><span data-stu-id="18aa6-559">**ModulationBell**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-560">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-560">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-561">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-561">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-562">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| Modulation \_ Bell")</span><span class="sxs-lookup"><span data-stu-id="18aa6-562">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Modulation\_Bell")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-563">Stringa di comando usata per indicare al modem di usare le modulazioni a campana per 300 e 1200 bps.</span><span class="sxs-lookup"><span data-stu-id="18aa6-563">Command string used to instruct the modem to use Bell modulations for 300 and 1200 bps.</span></span>

<span data-ttu-id="18aa6-564">Esempio: "B1"</span><span class="sxs-lookup"><span data-stu-id="18aa6-564">Example: "B1"</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-565">**ModulationCCITT**</span><span class="sxs-lookup"><span data-stu-id="18aa6-565">**ModulationCCITT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-566">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-566">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-567">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-567">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-568">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| Modulation \_ CCITT")</span><span class="sxs-lookup"><span data-stu-id="18aa6-568">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Modulation\_CCITT")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-569">Stringa di comando usata per indicare al modem di usare le modulazioni CCITT per 300 e 1200 bps.</span><span class="sxs-lookup"><span data-stu-id="18aa6-569">Command string used to instruct the modem to use CCITT modulations for 300 and 1200 bps.</span></span>

<span data-ttu-id="18aa6-570">Esempio: "B0"</span><span class="sxs-lookup"><span data-stu-id="18aa6-570">Example: "B0"</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-571">**ModulationScheme**</span><span class="sxs-lookup"><span data-stu-id="18aa6-571">**ModulationScheme**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-572">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18aa6-572">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-573">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-573">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-574">Schema di modulazione del modem.</span><span class="sxs-lookup"><span data-stu-id="18aa6-574">Modulation scheme of the modem.</span></span>

<span data-ttu-id="18aa6-575">Questa proprietà viene ereditata da [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="18aa6-575">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18aa6-576">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="18aa6-576">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="18aa6-577">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="18aa6-577">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="18aa6-578">**Non supportato** (2)</span><span class="sxs-lookup"><span data-stu-id="18aa6-578">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Bell_103"></span><span id="bell_103"></span><span id="BELL_103"></span>

<span data-ttu-id="18aa6-579">**Campana 103** (3)</span><span class="sxs-lookup"><span data-stu-id="18aa6-579">**Bell 103** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bell_212A"></span><span id="bell_212a"></span><span id="BELL_212A"></span>

<span data-ttu-id="18aa6-580">**Bell 212A** (4)</span><span class="sxs-lookup"><span data-stu-id="18aa6-580">**Bell 212A** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="V.22bis"></span><span id="v.22bis"></span><span id="V.22BIS"></span>

<span data-ttu-id="18aa6-581">**V. 22bis** (5)</span><span class="sxs-lookup"><span data-stu-id="18aa6-581">**V.22bis** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="V.32"></span><span id="v.32"></span>

<span data-ttu-id="18aa6-582">**V. 32** (6)</span><span class="sxs-lookup"><span data-stu-id="18aa6-582">**V.32** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="V.32bis"></span><span id="v.32bis"></span><span id="V.32BIS"></span>

<span data-ttu-id="18aa6-583">**V. 32bis** (7)</span><span class="sxs-lookup"><span data-stu-id="18aa6-583">**V.32bis** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="V.turbo"></span><span id="v.turbo"></span><span id="V.TURBO"></span>

<span data-ttu-id="18aa6-584">**V. Turbo** (8)</span><span class="sxs-lookup"><span data-stu-id="18aa6-584">**V.turbo** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="V.FC"></span><span id="v.fc"></span>

<span data-ttu-id="18aa6-585">**V. FC** (9)</span><span class="sxs-lookup"><span data-stu-id="18aa6-585">**V.FC** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="V.34"></span><span id="v.34"></span>

<span data-ttu-id="18aa6-586">**V. 34** (10)</span><span class="sxs-lookup"><span data-stu-id="18aa6-586">**V.34** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="V.34bis"></span><span id="v.34bis"></span><span id="V.34BIS"></span>

<span data-ttu-id="18aa6-587">**V. 34bis** (11)</span><span class="sxs-lookup"><span data-stu-id="18aa6-587">**V.34bis** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="18aa6-588">**Nome**</span><span class="sxs-lookup"><span data-stu-id="18aa6-588">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-589">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-590">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-590">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-591">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="18aa6-591">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-592">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="18aa6-592">Label by which the object is known.</span></span> <span data-ttu-id="18aa6-593">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="18aa6-593">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="18aa6-594">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="18aa6-594">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-595">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="18aa6-595">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-596">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-596">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-597">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-597">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-598">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="18aa6-598">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-599">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="18aa6-599">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="18aa6-600">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18aa6-600">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="18aa6-601">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="18aa6-601">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-602">**PortSubClass**</span><span class="sxs-lookup"><span data-stu-id="18aa6-602">**PortSubClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-603">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-603">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-604">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-604">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-605">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| PortSubClass"), **valore** ("porta parallela", "porta seriale", "modem")</span><span class="sxs-lookup"><span data-stu-id="18aa6-605">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|PortSubClass"), **Value** ("Parallel Port", "Serial Port", "Modem")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-606">Definizione della porta utilizzata per questo modem.</span><span class="sxs-lookup"><span data-stu-id="18aa6-606">Definition of the port used for this modem.</span></span>

<dt>



 <span data-ttu-id="18aa6-607">("00")</span><span class="sxs-lookup"><span data-stu-id="18aa6-607">("00")</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-608">Porta parallela</span><span class="sxs-lookup"><span data-stu-id="18aa6-608">Parallel Port</span></span>

</dd> <dt>



 <span data-ttu-id="18aa6-609">("01")</span><span class="sxs-lookup"><span data-stu-id="18aa6-609">("01")</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-610">Porta seriale</span><span class="sxs-lookup"><span data-stu-id="18aa6-610">Serial Port</span></span>

</dd> <dt>



 <span data-ttu-id="18aa6-611">("02")</span><span class="sxs-lookup"><span data-stu-id="18aa6-611">("02")</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-612">Modem</span><span class="sxs-lookup"><span data-stu-id="18aa6-612">Modem</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="18aa6-613">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="18aa6-613">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-614">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18aa6-614">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-615">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-615">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-616">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="18aa6-616">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="18aa6-617">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="18aa6-617">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18aa6-618"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="18aa6-618"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="18aa6-619"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="18aa6-619"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="18aa6-620"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="18aa6-620"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="18aa6-621"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="18aa6-621"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-622">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="18aa6-622">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="18aa6-623"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="18aa6-623"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-624">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="18aa6-624">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="18aa6-625"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="18aa6-625"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-626">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="18aa6-626">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="18aa6-627">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="18aa6-627">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="18aa6-628">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="18aa6-628">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="18aa6-629"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="18aa6-629"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-630">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="18aa6-630">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="18aa6-631"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="18aa6-631"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="18aa6-632">Tempo Power-On supportato</span><span class="sxs-lookup"><span data-stu-id="18aa6-632">Timed Power-On Supported</span></span>

<span data-ttu-id="18aa6-633">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="18aa6-633">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="18aa6-634">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="18aa6-634">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-635">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="18aa6-635">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-636">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-636">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-637">Se **true**, il dispositivo può essere gestito dal risparmio di energia (può essere impostato in modalità di sospensione e così via).</span><span class="sxs-lookup"><span data-stu-id="18aa6-637">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="18aa6-638">La proprietà non indica che le funzionalità di risparmio energia sono attualmente abilitate, solo che il dispositivo logico è in grado di gestire il risparmio di energia.</span><span class="sxs-lookup"><span data-stu-id="18aa6-638">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="18aa6-639">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18aa6-639">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-640">**Prefix**</span><span class="sxs-lookup"><span data-stu-id="18aa6-640">**Prefix**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-641">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-641">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-642">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-642">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-643">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| prefisso della classe di controllo CurrentControlSet di sistema Win32Registry \\ \\ \\ \\ \\ \\ \| ")</span><span class="sxs-lookup"><span data-stu-id="18aa6-643">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Prefix")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-644">Prefisso di composizione usato per accedere a una linea esterna.</span><span class="sxs-lookup"><span data-stu-id="18aa6-644">Dialing prefix used to access an outside line.</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-645">**Proprietà**</span><span class="sxs-lookup"><span data-stu-id="18aa6-645">**Properties**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-646">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="18aa6-646">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-647">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-647">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-648">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| proprietà della classe del controllo Win32Registry System \\ \\ CurrentControlSet \\ \\ \\ \\ \| ")</span><span class="sxs-lookup"><span data-stu-id="18aa6-648">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Properties")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-649">Elenco di tutte le proprietà (e i relativi valori) per questo modem.</span><span class="sxs-lookup"><span data-stu-id="18aa6-649">List of all the properties (and their values) for this modem.</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-650">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="18aa6-650">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-651">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-651">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-652">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-652">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-653">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| providerName")</span><span class="sxs-lookup"><span data-stu-id="18aa6-653">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ProviderName")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-654">Percorso di rete del computer che fornisce i servizi modem.</span><span class="sxs-lookup"><span data-stu-id="18aa6-654">Network path to the computer that provides the modem services.</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-655">**Impulso**</span><span class="sxs-lookup"><span data-stu-id="18aa6-655">**Pulse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-656">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-656">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-657">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-657">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-658">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| Pulse")</span><span class="sxs-lookup"><span data-stu-id="18aa6-658">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Pulse")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-659">Stringa di comando utilizzata per indicare al modem di utilizzare la modalità a impulsi per la composizione.</span><span class="sxs-lookup"><span data-stu-id="18aa6-659">Command string used to instruct the modem to use pulse mode for dialing.</span></span> <span data-ttu-id="18aa6-660">La composizione a impulsi è necessaria per le linee telefoniche che non sono in grado di gestire la composizione dei toni.</span><span class="sxs-lookup"><span data-stu-id="18aa6-660">Pulse dialing is necessary for phone lines that are unable to handle tone dialing.</span></span>

<span data-ttu-id="18aa6-661">Esempio: "P"</span><span class="sxs-lookup"><span data-stu-id="18aa6-661">Example: "P"</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-662">**Reimpostazione**</span><span class="sxs-lookup"><span data-stu-id="18aa6-662">**Reset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-663">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-663">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-664">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-664">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-665">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) (reset), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| Reset")</span><span class="sxs-lookup"><span data-stu-id="18aa6-665">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) (Reset), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Reset")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-666">Stringa di comando utilizzata per reimpostare il modem per la chiamata successiva.</span><span class="sxs-lookup"><span data-stu-id="18aa6-666">Command string used to reset the modem for the next call.</span></span>

<span data-ttu-id="18aa6-667">Esempio: "AT&F"</span><span class="sxs-lookup"><span data-stu-id="18aa6-667">Example: "AT&F"</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-668">**ResponsesKeyName**</span><span class="sxs-lookup"><span data-stu-id="18aa6-668">**ResponsesKeyName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-669">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-669">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-670">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-670">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-671">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| ResponsesKeyName")</span><span class="sxs-lookup"><span data-stu-id="18aa6-671">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ResponsesKeyName")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-672">Risposta che questo modem potrebbe segnalare al sistema operativo durante il processo di connessione.</span><span class="sxs-lookup"><span data-stu-id="18aa6-672">Response this modem might report to the operating system during the connection process.</span></span> <span data-ttu-id="18aa6-673">I primi due caratteri specificano il tipo di risposta.</span><span class="sxs-lookup"><span data-stu-id="18aa6-673">The first two characters specify the type of response.</span></span> <span data-ttu-id="18aa6-674">I secondi due caratteri specificano le informazioni sulla connessione in corso.</span><span class="sxs-lookup"><span data-stu-id="18aa6-674">The second two characters specify information about the connection being made.</span></span> <span data-ttu-id="18aa6-675">I due caratteri vengono usati solo per lo stato della negoziazione o per i codici di risposta di connessione.</span><span class="sxs-lookup"><span data-stu-id="18aa6-675">The second two characters are used only for Negotiation Progress or Connect response codes.</span></span> <span data-ttu-id="18aa6-676">Gli otto caratteri successivi specificano la velocità della linea da modem a modem negoziata in bit al secondo (BPS).</span><span class="sxs-lookup"><span data-stu-id="18aa6-676">The next eight characters specify the modem-to-modem line speed negotiated in bits per second (bps).</span></span> <span data-ttu-id="18aa6-677">I caratteri rappresentano un formato Long integer senza segno a 32 bit (byte e parola invertita).</span><span class="sxs-lookup"><span data-stu-id="18aa6-677">The characters represent a 32-bit unsigned long integer format (byte and word reversed).</span></span> <span data-ttu-id="18aa6-678">Gli ultimi otto caratteri indicano che il modem sta passando a una porta diversa o a una velocità del Data Terminal Equipment (DTE).</span><span class="sxs-lookup"><span data-stu-id="18aa6-678">The last eight characters indicate that the modem is changing to a different port or Data Terminal Equipment (DTE) speed.</span></span> <span data-ttu-id="18aa6-679">Questo campo non viene in genere usato perché i modem rendono le connessioni a una velocità di porta bloccata indipendentemente dalla velocità da modem a modem o DCE (Data Communications Equipment).</span><span class="sxs-lookup"><span data-stu-id="18aa6-679">Usually this field is not used because modems make connections at a locked port speed regardless of the modem-to-modem or Data Communications Equipment (DCE) speed.</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-680">**RingsBeforeAnswer**</span><span class="sxs-lookup"><span data-stu-id="18aa6-680">**RingsBeforeAnswer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-681">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="18aa6-681">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-682">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-682">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-683">Numero di anelli prima che il modem risponda a una chiamata in ingresso.</span><span class="sxs-lookup"><span data-stu-id="18aa6-683">Number of rings before the modem answers an incoming call.</span></span>

<span data-ttu-id="18aa6-684">Questa proprietà viene ereditata da [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="18aa6-684">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-685">**SpeakerModeDial**</span><span class="sxs-lookup"><span data-stu-id="18aa6-685">**SpeakerModeDial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-686">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-687">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-687">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-688">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| SpeakerModeDial")</span><span class="sxs-lookup"><span data-stu-id="18aa6-688">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerModeDial")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-689">Stringa di comando utilizzata per attivare l'altoparlante del modem dopo aver composto un numero e disattivarlo quando è stata stabilita una connessione.</span><span class="sxs-lookup"><span data-stu-id="18aa6-689">Command string used to turn the modem speaker on after dialing a number, and turning the speaker off when a connection has been established.</span></span>

<span data-ttu-id="18aa6-690">Esempio: "M1"</span><span class="sxs-lookup"><span data-stu-id="18aa6-690">Example: "M1"</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-691">**SpeakerModeOff**</span><span class="sxs-lookup"><span data-stu-id="18aa6-691">**SpeakerModeOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-692">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-692">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-693">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-693">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-694">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| SpeakerModeOff")</span><span class="sxs-lookup"><span data-stu-id="18aa6-694">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerModeOff")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-695">Stringa di comando utilizzata per disattivare l'altoparlante del modem.</span><span class="sxs-lookup"><span data-stu-id="18aa6-695">Command string used to turn the modem speaker off.</span></span>

<span data-ttu-id="18aa6-696">Esempio: "M0"</span><span class="sxs-lookup"><span data-stu-id="18aa6-696">Example: "M0"</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-697">**SpeakerModeOn**</span><span class="sxs-lookup"><span data-stu-id="18aa6-697">**SpeakerModeOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-698">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-698">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-699">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-699">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-700">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| SpeakerModeOn")</span><span class="sxs-lookup"><span data-stu-id="18aa6-700">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerModeOn")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-701">Stringa di comando utilizzata per attivare l'altoparlante del modem.</span><span class="sxs-lookup"><span data-stu-id="18aa6-701">Command string used to turn the modem speaker on.</span></span>

<span data-ttu-id="18aa6-702">Esempio: "m2"</span><span class="sxs-lookup"><span data-stu-id="18aa6-702">Example: "M2"</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-703">**SpeakerModeSetup**</span><span class="sxs-lookup"><span data-stu-id="18aa6-703">**SpeakerModeSetup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-704">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-704">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-705">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-705">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-706">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| SpeakerModeSetup")</span><span class="sxs-lookup"><span data-stu-id="18aa6-706">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerModeSetup")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-707">Stringa di comando utilizzata per indicare al modem di accendere l'altoparlante (fino a quando non viene stabilita una connessione).</span><span class="sxs-lookup"><span data-stu-id="18aa6-707">Command string used to instruct the modem to turn the speaker on (until a connection is established).</span></span>

<span data-ttu-id="18aa6-708">Esempio: "M3"</span><span class="sxs-lookup"><span data-stu-id="18aa6-708">Example: "M3"</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-709">**SpeakerVolumeHigh**</span><span class="sxs-lookup"><span data-stu-id="18aa6-709">**SpeakerVolumeHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-710">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-710">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-711">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-711">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-712">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| SpeakerVolume \_ High")</span><span class="sxs-lookup"><span data-stu-id="18aa6-712">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerVolume\_High")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-713">Stringa di comando utilizzata per impostare l'altoparlante del modem sul volume più alto.</span><span class="sxs-lookup"><span data-stu-id="18aa6-713">Command string used to set the modem speaker to the highest volume.</span></span>

<span data-ttu-id="18aa6-714">Esempio: "L3"</span><span class="sxs-lookup"><span data-stu-id="18aa6-714">Example: "L3"</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-715">**SpeakerVolumeInfo**</span><span class="sxs-lookup"><span data-stu-id="18aa6-715">**SpeakerVolumeInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-716">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18aa6-716">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-717">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-717">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-718">Descrive il livello di volume dei toni acustici dal modem.</span><span class="sxs-lookup"><span data-stu-id="18aa6-718">Describes the volume level of the audible tones from the modem.</span></span>

<span data-ttu-id="18aa6-719">Questa proprietà viene ereditata da [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="18aa6-719">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18aa6-720">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="18aa6-720">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="18aa6-721">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="18aa6-721">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="18aa6-722">**Non supportato** (2)</span><span class="sxs-lookup"><span data-stu-id="18aa6-722">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="18aa6-723">**Alta** (3)</span><span class="sxs-lookup"><span data-stu-id="18aa6-723">**High** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

<span data-ttu-id="18aa6-724">**Media** (4)</span><span class="sxs-lookup"><span data-stu-id="18aa6-724">**Medium** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="18aa6-725">**Bassa** (5)</span><span class="sxs-lookup"><span data-stu-id="18aa6-725">**Low** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span data-ttu-id="18aa6-726">**Disattivato** (6)</span><span class="sxs-lookup"><span data-stu-id="18aa6-726">**Off** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="18aa6-727">**Automatico** (7)</span><span class="sxs-lookup"><span data-stu-id="18aa6-727">**Auto** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="18aa6-728">**SpeakerVolumeLow**</span><span class="sxs-lookup"><span data-stu-id="18aa6-728">**SpeakerVolumeLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-729">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-729">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-730">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-730">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-731">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| SpeakerVolume \_ low")</span><span class="sxs-lookup"><span data-stu-id="18aa6-731">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerVolume\_Low")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-732">Stringa di comando utilizzata per impostare l'altoparlante del modem sul volume più basso.</span><span class="sxs-lookup"><span data-stu-id="18aa6-732">Command string used to set the modem speaker to the lowest volume.</span></span>

<span data-ttu-id="18aa6-733">Esempio: "L1"</span><span class="sxs-lookup"><span data-stu-id="18aa6-733">Example: "L1"</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-734">**SpeakerVolumeMed**</span><span class="sxs-lookup"><span data-stu-id="18aa6-734">**SpeakerVolumeMed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-735">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-735">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-736">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-736">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-737">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| SpeakerVolume \_ Med")</span><span class="sxs-lookup"><span data-stu-id="18aa6-737">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerVolume\_Med")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-738">Stringa di comando utilizzata per impostare l'altoparlante del modem su un volume medio.</span><span class="sxs-lookup"><span data-stu-id="18aa6-738">Command string used to set the modem speaker to a medium volume.</span></span>

<span data-ttu-id="18aa6-739">Esempio: "L2"</span><span class="sxs-lookup"><span data-stu-id="18aa6-739">Example: "L2"</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-740">**Status**</span><span class="sxs-lookup"><span data-stu-id="18aa6-740">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-741">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-741">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-742">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-742">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-743">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="18aa6-743">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-744">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="18aa6-744">Current status of the object.</span></span> <span data-ttu-id="18aa6-745">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="18aa6-745">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="18aa6-746">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="18aa6-746">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="18aa6-747">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="18aa6-747">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="18aa6-748">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="18aa6-748">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="18aa6-749">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="18aa6-749">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="18aa6-750">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="18aa6-750">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="18aa6-751">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="18aa6-751">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="18aa6-752">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="18aa6-752">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="18aa6-753">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="18aa6-753">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="18aa6-754">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="18aa6-754">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18aa6-755">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="18aa6-755">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="18aa6-756">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="18aa6-756">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="18aa6-757">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="18aa6-757">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="18aa6-758">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="18aa6-758">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="18aa6-759">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="18aa6-759">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="18aa6-760">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="18aa6-760">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="18aa6-761">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="18aa6-761">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="18aa6-762">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="18aa6-762">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="18aa6-763">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="18aa6-763">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="18aa6-764">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="18aa6-764">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-765">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18aa6-765">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-766">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-766">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-767">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="18aa6-767">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-768">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="18aa6-768">State of the logical device.</span></span> <span data-ttu-id="18aa6-769">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="18aa6-769">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="18aa6-770">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18aa6-770">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="18aa6-771">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="18aa6-771">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18aa6-772">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="18aa6-772">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="18aa6-773">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="18aa6-773">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="18aa6-774">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="18aa6-774">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="18aa6-775">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="18aa6-775">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="18aa6-776">**StringFormat**</span><span class="sxs-lookup"><span data-stu-id="18aa6-776">**StringFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-777">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-777">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-778">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-778">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-779">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \_ API \| line Device Structures \| LINEDEVCAPS \| dwStringFormat")</span><span class="sxs-lookup"><span data-stu-id="18aa6-779">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Line Device Structures\|LINEDEVCAPS\|dwStringFormat")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-780">Tipo di caratteri utilizzati per il testo passato attraverso il modem.</span><span class="sxs-lookup"><span data-stu-id="18aa6-780">Type of characters used for text passed through the modem.</span></span>

<span data-ttu-id="18aa6-781">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="18aa6-781">The values are:</span></span>

<dl> <dd><span data-ttu-id="18aa6-782">"Formato stringa ASCII"</span><span class="sxs-lookup"><span data-stu-id="18aa6-782">"ASCII string format"</span></span></dd> <dd><span data-ttu-id="18aa6-783">"Formato stringa DBCS"</span><span class="sxs-lookup"><span data-stu-id="18aa6-783">"DBCS string format"</span></span></dd> <dd><span data-ttu-id="18aa6-784">"Formato stringa UNICODE"</span><span class="sxs-lookup"><span data-stu-id="18aa6-784">"UNICODE string format"</span></span></dd> </dl>

<dt>

<span id="ASCII_string_format"></span><span id="ascii_string_format"></span><span id="ASCII_STRING_FORMAT"></span>

<span data-ttu-id="18aa6-785">**Formato stringa ASCII** ("formato stringa ASCII")</span><span class="sxs-lookup"><span data-stu-id="18aa6-785">**ASCII string format** ("ASCII string format")</span></span>


</dt> <dd></dd> <dt>

<span id="DBCS_string_format"></span><span id="dbcs_string_format"></span><span id="DBCS_STRING_FORMAT"></span>

<span data-ttu-id="18aa6-786">**Formato stringa DBCS** ("formato stringa DBCS")</span><span class="sxs-lookup"><span data-stu-id="18aa6-786">**DBCS string format** ("DBCS string format")</span></span>


</dt> <dd></dd> <dt>

<span id="UNICODE_string_format"></span><span id="unicode_string_format"></span><span id="UNICODE_STRING_FORMAT"></span>

<span data-ttu-id="18aa6-787">**Formato stringa Unicode** ("formato stringa Unicode")</span><span class="sxs-lookup"><span data-stu-id="18aa6-787">**UNICODE string format** ("UNICODE string format")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="18aa6-788">**SupportsCallback**</span><span class="sxs-lookup"><span data-stu-id="18aa6-788">**SupportsCallback**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-789">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="18aa6-789">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-790">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-790">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-791">Se **true**, il modem supporta il callback.</span><span class="sxs-lookup"><span data-stu-id="18aa6-791">If **TRUE**, the modem supports callback.</span></span>

<span data-ttu-id="18aa6-792">Questa proprietà viene ereditata da [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="18aa6-792">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-793">**SupportsSynchronousConnect**</span><span class="sxs-lookup"><span data-stu-id="18aa6-793">**SupportsSynchronousConnect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-794">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="18aa6-794">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-795">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-795">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-796">Se **true**, sincrona e asincrona, la comunicazione è supportata.</span><span class="sxs-lookup"><span data-stu-id="18aa6-796">If **TRUE**, synchronous, as well as asynchronous, communication is supported.</span></span>

<span data-ttu-id="18aa6-797">Questa proprietà viene ereditata da [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="18aa6-797">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-798">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="18aa6-798">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-799">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-799">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-800">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-800">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-801">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="18aa6-801">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-802">Valore della proprietà **CreationClassName** del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="18aa6-802">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="18aa6-803">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18aa6-803">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-804">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="18aa6-804">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-805">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-805">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-806">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-806">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-807">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="18aa6-807">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-808">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="18aa6-808">Name of the scoping system.</span></span>

<span data-ttu-id="18aa6-809">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18aa6-809">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-810">**Carattere di terminazione**</span><span class="sxs-lookup"><span data-stu-id="18aa6-810">**Terminator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-811">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-811">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-812">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-812">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-813">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| Terminator")</span><span class="sxs-lookup"><span data-stu-id="18aa6-813">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Terminator")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-814">Stringa che contrassegna la fine di una stringa di comando.</span><span class="sxs-lookup"><span data-stu-id="18aa6-814">String that marks the end of a command string.</span></span>

<span data-ttu-id="18aa6-815">Esempio: "<CR"</span><span class="sxs-lookup"><span data-stu-id="18aa6-815">Example: "<cr"</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-816">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="18aa6-816">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-817">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="18aa6-817">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-818">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-818">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-819">Data e ora dell'ultima reimpostazione del modem.</span><span class="sxs-lookup"><span data-stu-id="18aa6-819">Date and time the modem was last reset.</span></span>

<span data-ttu-id="18aa6-820">Questa proprietà viene ereditata da [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="18aa6-820">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-821">**Tono**</span><span class="sxs-lookup"><span data-stu-id="18aa6-821">**Tone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-822">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-822">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-823">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-823">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-824">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| Tone")</span><span class="sxs-lookup"><span data-stu-id="18aa6-824">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Tone")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-825">Stringa di comando che indica al modem di utilizzare la modalità Tone per la composizione.</span><span class="sxs-lookup"><span data-stu-id="18aa6-825">Command string that instructs the modem to use tone mode for dialing.</span></span> <span data-ttu-id="18aa6-826">La linea telefonica deve supportare la composizione dei toni.</span><span class="sxs-lookup"><span data-stu-id="18aa6-826">The phone line must support tone dialing.</span></span>

<span data-ttu-id="18aa6-827">Esempio: "T"</span><span class="sxs-lookup"><span data-stu-id="18aa6-827">Example: "T"</span></span>

</dd> <dt>

<span data-ttu-id="18aa6-828">**VoiceSwitchFeature**</span><span class="sxs-lookup"><span data-stu-id="18aa6-828">**VoiceSwitchFeature**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18aa6-829">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18aa6-829">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-830">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18aa6-830">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18aa6-831">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| VoiceSwitchFeature")</span><span class="sxs-lookup"><span data-stu-id="18aa6-831">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|VoiceSwitchFeature")</span></span>
</dt> </dl>

<span data-ttu-id="18aa6-832">Stringhe di comando utilizzate per attivare le funzionalità vocali di un modem vocale.</span><span class="sxs-lookup"><span data-stu-id="18aa6-832">Command strings used to activate the voice capabilities of a voice modem.</span></span>

<span data-ttu-id="18aa6-833">Esempio: "AT + V"</span><span class="sxs-lookup"><span data-stu-id="18aa6-833">Example: "AT+V"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="18aa6-834">Commenti</span><span class="sxs-lookup"><span data-stu-id="18aa6-834">Remarks</span></span>

<span data-ttu-id="18aa6-835">La classe **Win32 \_ POTSModem** è derivata da [**CIM \_ POTSModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="18aa6-835">The **Win32\_POTSModem** class is derived from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="18aa6-836">Requisiti</span><span class="sxs-lookup"><span data-stu-id="18aa6-836">Requirements</span></span>



| <span data-ttu-id="18aa6-837">Requisito</span><span class="sxs-lookup"><span data-stu-id="18aa6-837">Requirement</span></span> | <span data-ttu-id="18aa6-838">Valore</span><span class="sxs-lookup"><span data-stu-id="18aa6-838">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18aa6-839">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18aa6-839">Minimum supported client</span></span><br/> | <span data-ttu-id="18aa6-840">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="18aa6-840">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="18aa6-841">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18aa6-841">Minimum supported server</span></span><br/> | <span data-ttu-id="18aa6-842">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18aa6-842">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="18aa6-843">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="18aa6-843">Namespace</span></span><br/>                | <span data-ttu-id="18aa6-844">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="18aa6-844">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="18aa6-845">MOF</span><span class="sxs-lookup"><span data-stu-id="18aa6-845">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18aa6-846"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="18aa6-846"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="18aa6-847">DLL</span><span class="sxs-lookup"><span data-stu-id="18aa6-847">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18aa6-848"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18aa6-848"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18aa6-849">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="18aa6-849">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18aa6-850">**\_POTSMODEM CIM**</span><span class="sxs-lookup"><span data-stu-id="18aa6-850">**CIM\_PotsModem**</span></span>](cim-potsmodem.md)
</dt> <dt>

[<span data-ttu-id="18aa6-851">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="18aa6-851">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 

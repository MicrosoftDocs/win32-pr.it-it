---
description: La classe WMI WIN32 POTSModem rappresenta i servizi e le caratteristiche di un \_ modem PLAIN OLD Telephone Service (POTS) in un computer che esegue Windows.
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
ms.openlocfilehash: e79cb842acd2063522f901d050c3fab6db3251a39a212a234f062935cc30b87c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020109"
---
# <a name="win32_potsmodem-class"></a>Classe \_ POTSModem Win32

La classe [WMI](../wmisdk/retrieving-a-class.md) **WIN32 \_ POTSModem** rappresenta i servizi e le caratteristiche di un modem POTS (Plain Old Telephone Service) in un computer che esegue Windows.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

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

## <a name="members"></a>Members

La **classe \_ POTSModem Win32** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe WIN32 \_ POTSModem** include questi metodi.



| Metodo            | Descrizione                                                                                                                                                                            |
|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Reimpostazione**         | Non implementato. Per implementare questo metodo, vedere il [**metodo Reset**](reset-method-in-class-cim-controller.md) in [**CIM \_ PotsModem.**](cim-potsmodem.md)<br/>                 |
| **SetPowerState** | Non implementato. Per implementare questo metodo, vedere il [**metodo SetPowerState**](setpowerstate-method-in-class-cim-controller.md) in [**CIM \_ PotsModem.**](cim-potsmodem.md)<br/> |



 

### <a name="properties"></a>Proprietà

La **classe WIN32 \_ POTSModem** ha queste proprietà.

<dl> <dt>

**AnswerMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Impostazione corrente di risposta automatica o callback per il modem.

Questa proprietà viene ereditata da [**CIM \_ PotsModem.**](cim-potsmodem.md)

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Disabilitato** (2)


</dt> <dd></dd> <dt>

<span id="Manual_Answer"></span><span id="manual_answer"></span><span id="MANUAL_ANSWER"></span>

**Risposta manuale** (3)


</dt> <dd></dd> <dt>

<span id="Auto_Answer"></span><span id="auto_answer"></span><span id="AUTO_ANSWER"></span>

**Risposta automatica** (4)


</dt> <dd></dd> <dt>

<span id="Auto_Answer_with_Call-Back"></span><span id="auto_answer_with_call-back"></span><span id="AUTO_ANSWER_WITH_CALL-BACK"></span>

**Risposta automatica con call-back** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**AttachedTo**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \| AttachedTo")
</dt> </dl>

Porta a cui è collegato il modem POTS.

Esempio: "COM1"

</dd> <dt>

**Disponibilità**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| Operational State \| 003.5", "MIB. IETF \| HOST-RESOURCES-MIB.hrDeviceStatus")
</dt> </dl>

Disponibilità e stato del dispositivo.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)


</dt> <dd>

Esecuzione o alimentazione completa

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuori servizio** (9)


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia - Sconosciuto** (13)


</dt> <dd>

È noto che il dispositivo è in modalità di risparmio energia, ma lo stato esatto è sconosciuto.

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia - Modalità a basso consumo** (14)


</dt> <dd>

Il dispositivo è in stato di risparmio energia, ma continua a funzionare e può presentare prestazioni ridotte.

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia - Standby** (15)


</dt> <dd>

Il dispositivo non funziona, ma può essere alimentato rapidamente.

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia - Avviso** (17)


</dt> <dd>

Il dispositivo è in uno stato di avviso, anche se in modalità di risparmio energia.

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**In pausa** (18)


</dt> <dd>

Il dispositivo è in pausa.

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)


</dt> <dd>

Il dispositivo non è pronto.

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurato** (20)


</dt> <dd>

Il dispositivo non è configurato.

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattiva** (21)


</dt> <dd>

Il dispositivo è silenzioso.

</dd> </dl>

</dd> <dt>

**BlindOff**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \| BlindOff")
</dt> </dl>

Stringa di comando usata per rilevare un segnale di composizione prima della composizione.

Esempio: "X4"

</dd> <dt>

**BlindOn**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \| BlindOn")
</dt> </dl>

Stringa di comando usata per stabilire se è presente o meno un tono di composizione.

Esempio: "X3"

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Breve descrizione dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**CompatibilityFlags**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \| CompatibilityFlags")
</dt> </dl>

Tutti i protocolli di connessione modem con cui il dispositivo modem è compatibile.

</dd> <dt>

**CompressionInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Caratteristiche di compressione dei dati del modem.

Questa proprietà viene ereditata da [**CIM \_ PotsModem.**](cim-potsmodem.md)

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)


</dt> <dd>

Sconosciuto

</dd> <dt>

<span id="No_Compression"></span><span id="no_compression"></span><span id="NO_COMPRESSION"></span>

<span id="No_Compression"></span><span id="no_compression"></span><span id="NO_COMPRESSION"></span>**Nessuna compressione** (2)


</dt> <dd>

Altro

</dd> <dt>

<span id="MNP_5"></span><span id="mnp_5"></span>

<span id="MNP_5"></span><span id="mnp_5"></span>**MNP 5** (3)


</dt> <dd>

Nessuna compressione

</dd> <dt>

<span id="V.42bis"></span><span id="v.42bis"></span><span id="V.42BIS"></span>

<span id="v.42bis"></span><span id="V.42BIS"></span>**V.42bis** (4)


</dt> <dd>

MNP 5

</dd> <dt>

<span id="5"></span>

<span id="5"></span>**5**


</dt> <dd>

V.42bis

</dd> </dl>

</dd> <dt>

**CompressionOff**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \| Compression \_ Off")
</dt> </dl>

Stringa di comando usata per disabilitare la compressione dei dati hardware.

Esempio: "S46=136"

</dd> <dt>

**CompressionOn**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \| Compression \_ On")
</dt> </dl>

Stringa di comando usata per abilitare la compressione dei dati hardware.

Esempio: "S46=138"

</dd> <dt>

**ConfigManagerErrorCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")
</dt> </dl>

Codice di errore Gestione configurazione Win32.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Questo dispositivo funziona correttamente.**  (0)


</dt> <dd>

Il dispositivo funziona correttamente.

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.** (1)


</dt> <dd>

Il dispositivo non è configurato correttamente.

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows possibile caricare il driver per questo dispositivo.** (2)


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato o il sistema potrebbe avere memoria insufficiente o altre risorse.** (3)


</dt> <dd>

Il driver per questo dispositivo potrebbe essere danneggiato o il sistema potrebbe avere memoria insufficiente o altre risorse.

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Questo dispositivo non funziona correttamente. Uno dei relativi driver o il registro potrebbe essere danneggiato.** (4)


</dt> <dd>

Il dispositivo non funziona correttamente. Uno dei relativi driver o il Registro di sistema potrebbe essere danneggiato.

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che non Windows gestire.** (5)


</dt> <dd>

Il driver per il dispositivo richiede una risorsa che Windows non può gestire.

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**  (6)


</dt> <dd>

La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.** (7)


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore del driver per il dispositivo è mancante.** (8)


</dt> <dd>

Il caricatore del driver per il dispositivo è mancante.

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.** (9)


</dt> <dd>

Il dispositivo non funziona correttamente. Il firmware di controllo segnala erroneamente le risorse per il dispositivo.

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Questo dispositivo non può essere avviato.** (10)


</dt> <dd>

Impossibile avviare il dispositivo.

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Questo dispositivo non è riuscito.** (11)


</dt> <dd>

Dispositivo non riuscito.

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non riesce a trovare risorse gratuite sufficienti da usare.** (12)


</dt> <dd>

Il dispositivo non riesce a trovare risorse gratuite sufficienti da usare.

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows verificare le risorse del dispositivo.** (13)


</dt> <dd>

Windows possibile verificare le risorse del dispositivo.

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non può funzionare correttamente fino a quando non si riavvia il computer.** (14)


</dt> <dd>

Il dispositivo non può funzionare correttamente fino al riavvio del computer.

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Questo dispositivo non funziona correttamente perché è probabile che si sia verificato un problema di rienumere.** (15)


</dt> <dd>

Il dispositivo non funziona correttamente a causa di un possibile problema di enumerazione.

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows identificare tutte le risorse utilizzate dal dispositivo.** (16)


</dt> <dd>

Windows identificare tutte le risorse utilizzate dal dispositivo.

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Questo dispositivo richiede un tipo di risorsa sconosciuto.** (17)


</dt> <dd>

Il dispositivo richiede un tipo di risorsa sconosciuto.

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.** (18)


</dt> <dd>

I driver di dispositivo devono essere reinstallati.

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'uso del caricatore VxD.** (19)


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il Registro di sistema potrebbe essere danneggiato.** (20)


</dt> <dd>

Il Registro di sistema potrebbe essere danneggiato.

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.** (21)


</dt> <dd>

Errore di sistema. Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware. Windows sta rimuovendo il dispositivo.

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Questo dispositivo è disabilitato.** (22)


</dt> <dd>

Il dispositivo è disabilitato.

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware.** (23)


</dt> <dd>

Errore di sistema. Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non dispone di tutti i relativi driver installati.** (24)


</dt> <dd>

Il dispositivo non è presente, non funziona correttamente o non dispone di tutti i relativi driver installati.

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora configurando questo dispositivo.** (25)


</dt> <dd>

Windows sta ancora configurando il dispositivo.

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora configurando questo dispositivo.** (26)


</dt> <dd>

Windows sta ancora configurando il dispositivo.

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.** (27)


</dt> <dd>

Il dispositivo non ha una configurazione di log valida.

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.** (28)


</dt> <dd>

I driver di dispositivo non sono installati.

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha dato le risorse necessarie.** (29)


</dt> <dd>

Il dispositivo è disabilitato. Il firmware del dispositivo non ha fornito le risorse necessarie.

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa richiesta di interrupt (IRQ) in uso da un altro dispositivo.** (30)


</dt> <dd>

Il dispositivo usa una risorsa IRQ in uso da un altro dispositivo.

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché non Windows caricare i driver necessari per questo dispositivo.** (31)


</dt> <dd>

Il dispositivo non funziona correttamente. Windows non è possibile caricare i driver di dispositivo necessari.

</dd> </dl>

</dd> <dt>

**ConfigManagerUserConfig**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")
</dt> </dl>

Se **TRUE,** il dispositivo usa una configurazione definita dall'utente.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**Finestra di dialogo Configurazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \| ConfigDialog")
</dt> </dl>

Stringa di inizializzazione del modem. Questa proprietà è costituito da stringhe di comando di altre proprietà di questa classe.

</dd> <dt>

**Paesi Supportati**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di paesi/aree geografiche in cui il modem può operare.

Questa proprietà viene ereditata da [**CIM \_ PotsModem.**](cim-potsmodem.md)

</dd> <dt>

**CountrySelected**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Paese per cui è attualmente programmato il modem. Quando sono supportati più paesi/aree geografiche, questa proprietà definisce quale paese è attualmente selezionato per l'uso.

Questa proprietà viene ereditata da [**CIM \_ PotsModem.**](cim-potsmodem.md)

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave \_ CIM**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata nella creazione di un'istanza. Se usata con le altre proprietà chiave della classe , la proprietà consente l'identificazione univoca di tutte le istanze di questa classe e delle relative sottoclassi.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicalfile.md)

</dd> <dt>

**CurrentPasswords**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elenco delle password attualmente definite per il modem. Questa matrice può essere lasciata vuota per motivi di sicurezza.

Questa proprietà viene ereditata da [**CIM \_ PotsModem.**](cim-potsmodem.md)

</dd> <dt>

**DCB**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture di comunicazione Win32API \| \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)")
</dt> </dl>

Controllare le impostazioni per un dispositivo di comunicazione seriale, in questo caso il dispositivo modem.

</dd> <dt>

**Default**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \| Default")
</dt> </dl>

Se **TRUE,** questo modem POTS è il modem predefinito nel computer che esegue Windows.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Descrizione dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Deviceid**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key,**](../wmisdk/key-qualifier.md) [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Identificatore univoco di questo modem POTS da altri dispositivi nel sistema.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**DeviceLoader**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \| DevLoader")
</dt> </dl>

Nome del caricatore del dispositivo per il modem. Un caricatore di dispositivi carica e gestisce i driver di dispositivo e gli enumeratori per un determinato dispositivo.

</dd> <dt>

**DeviceType**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \| DeviceType")
</dt> </dl>

Tipo fisico del modem.

I valori possibili sono:

<dl> <dd>"Modem Null"</dd> <dd>"Modem interno"</dd> <dd>"Modem esterno"</dd> <dd>"PCMCIA Modem"</dd> <dd>"Sconosciuto"</dd> </dl>

<dt>

<span id="Null_Modem"></span><span id="null_modem"></span><span id="NULL_MODEM"></span>

**Modem Null** ("Modem Null")


</dt> <dd></dd> <dt>

<span id="Internal_Modem"></span><span id="internal_modem"></span><span id="INTERNAL_MODEM"></span>

**Modem interno** ("modem interno")


</dt> <dd></dd> <dt>

<span id="External_Modem"></span><span id="external_modem"></span><span id="EXTERNAL_MODEM"></span>

**Modem esterno** ("modem esterno")


</dt> <dd></dd> <dt>

<span id="PCMCIA_Modem"></span><span id="pcmcia_modem"></span><span id="PCMCIA_MODEM"></span>

**PcMCIA Modem** ("PCMCIA Modem")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** ("Sconosciuto")


</dt> <dd></dd> </dl>

</dd> <dt>

**Tipo di connessione**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di metodo di composizione utilizzato.

Questa proprietà viene ereditata da [**CIM \_ PotsModem.**](cim-potsmodem.md)

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Tone"></span><span id="tone"></span><span id="TONE"></span>

**Tono** (1)


</dt> <dd></dd> <dt>

<span id="Pulse"></span><span id="pulse"></span><span id="PULSE"></span>

**Pulse** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Data driver**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \| DriverDate")
</dt> </dl>

Data del driver del modem.

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **TRUE,** l'errore segnalato in **LastErrorCode** viene ora cancellato.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**ErrorControlForced**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \| ErrorControl \_ Forced")
</dt> </dl>

Stringa di comando usata per abilitare il controllo della correzione degli errori quando si stabilisce una connessione. In questo modo si aumenta l'affidabilità della connessione.

Esempio: "+Q5S36=4S48=7"

</dd> <dt>

**ErrorControlInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Caratteristiche di correzione degli errori del modem.

Questa proprietà viene ereditata da [**CIM \_ PotsModem.**](cim-potsmodem.md)

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="No_Error_Correction"></span><span id="no_error_correction"></span><span id="NO_ERROR_CORRECTION"></span>

**Nessuna correzione di errore** (2)


</dt> <dd></dd> <dt>

<span id="MNP_4"></span><span id="mnp_4"></span>

**MNP 4** (3)


</dt> <dd></dd> <dt>

<span id="LAPM"></span><span id="lapm"></span>

**LAPM** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**ErrorControlOff**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \| ErrorControl \_ Off")
</dt> </dl>

Stringa di comando utilizzata per disabilitare il controllo degli errori.

Esempio: "+Q6S36=3S48=128"

</dd> <dt>

**ErrorControlOn**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \| ErrorControl \_ On")
</dt> </dl>

Stringa di comando utilizzata per abilitare il controllo degli errori.

Esempio: "+Q5S36=7S48=7"

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Altre informazioni sull'errore registrato in **LastErrorCode** e informazioni su eventuali azioni correttive che possono essere eseguite.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**FlowControlHard**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \| FlowControl \_ Hard")
</dt> </dl>

Stringa di comando usata per abilitare il controllo di flusso hardware. Flow controllo è costituito da segnali inviati tra computer che verificano che entrambi i computer siano pronti per trasmettere o ricevere dati.

Esempio: "&K1"

</dd> <dt>

**FlowControlOff**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \| FlowControl \_ Off")
</dt> </dl>

Stringa di comando usata per disabilitare il controllo di flusso. Flow controllo è costituito da segnali inviati tra computer che verificano che entrambi i computer siano pronti per trasmettere o ricevere dati.

Esempio: "&K0"

</dd> <dt>

**FlowControlSoft**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \| FlowControl \_ Soft")
</dt> </dl>

Stringa di comando usata per abilitare il controllo di flusso software. Flow controllo è costituito da segnali inviati tra computer che verificano che entrambi i computer siano pronti per trasmettere o ricevere dati.

Esempio: "&K2"

</dd> <dt>

**InactivityScale**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \| InactivityScale")
</dt> </dl>

Moltiplicatore usato con la **proprietà InactivityTimeout** per calcolare il periodo di timeout di una connessione.

</dd> <dt>

**InactivityTimeout**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("secondi")
</dt> </dl>

Limite di tempo (in secondi) per la disconnessione automatica della linea telefonica, se non viene scambiato alcun dato. Il valore 0 (zero) indica che questa funzionalità è presente ma non abilitata.

Questa proprietà viene ereditata da [**CIM \_ PotsModem.**](cim-potsmodem.md)

</dd> <dt>

**Index**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di indice per questo modem POTS.

Esempio: 0

</dd> <dt>

**IndexEx**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

ID dell'istanza del dispositivo per questo modem POTS.

Esempio: "1&08"

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 e Windows Vista:** Questa proprietà è disponibile a partire da Windows Server 2016 e Windows 10.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")
</dt> </dl>

Data e ora di installazione dell'oggetto. Questa proprietà non richiede un valore per indicare che l'oggetto è installato.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ultimo codice di errore segnalato dal dispositivo logico.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**MaxBaudRateToPhone**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("bit al secondo")
</dt> </dl>

Velocità massima di comunicazione impostabile per l'accesso al sistema telefonico.

Questa proprietà viene ereditata da [**CIM \_ PotsModem.**](cim-potsmodem.md)

</dd> <dt>

**MaxBaudRateToSerialPort**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("bit al secondo")
</dt> </dl>

Velocità massima di comunicazione impostabile sulla porta COM per un modem esterno. Immettere 0 (zero) se non applicabile.

Questa proprietà viene ereditata da [**CIM \_ PotsModem.**](cim-potsmodem.md)

</dd> <dt>

**MaxNumberOfPasswords**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di password definibili nel modem stesso. Se questa funzionalità non è supportata, immettere 0 (zero).

Questa proprietà viene ereditata da [**CIM \_ PotsModem.**](cim-potsmodem.md)

</dd> <dt>

**Modello**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \| Model")
</dt> </dl>

Modello di questo modem POTS.

Esempio: "Sportster 56K External"

</dd> <dt>

**ModemInfPath**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \| InfPath")
</dt> </dl>

Percorso del file inf del modem. Questo file contiene informazioni di inizializzazione per il modem e il relativo driver.

Esempio: "C: \\ Windows \\ INF"

</dd> <dt>

**ModemInfSection**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \| InfSection")
</dt> </dl>

Nome della sezione nel file inf del modem che contiene informazioni sul modem.

</dd> <dt>

**ModulationBell**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \| Modulation \_ Bell")
</dt> </dl>

Stringa di comando usata per indicare al modem di usare le modulazioni Bell per 300 e 1200 bps.

Esempio: "B1"

</dd> <dt>

**ModulationCCITT**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \| Modulation \_ CCITT")
</dt> </dl>

Stringa di comando usata per indicare al modem di usare le modulazioni CCITT per 300 e 1200 bps.

Esempio: "B0"

</dd> <dt>

**ModulationScheme**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Schema di modulazione del modem.

Questa proprietà viene ereditata da [**CIM \_ PotsModem.**](cim-potsmodem.md)

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

**Non supportato** (2)


</dt> <dd></dd> <dt>

<span id="Bell_103"></span><span id="bell_103"></span><span id="BELL_103"></span>

**Bell 103** (3)


</dt> <dd></dd> <dt>

<span id="Bell_212A"></span><span id="bell_212a"></span><span id="BELL_212A"></span>

**Bell 212A** (4)


</dt> <dd></dd> <dt>

<span id="V.22bis"></span><span id="v.22bis"></span><span id="V.22BIS"></span>

**V.22bis** (5)


</dt> <dd></dd> <dt>

<span id="V.32"></span><span id="v.32"></span>

**V.32** (6)


</dt> <dd></dd> <dt>

<span id="V.32bis"></span><span id="v.32bis"></span><span id="V.32BIS"></span>

**V.32bis** (7)


</dt> <dd></dd> <dt>

<span id="V.turbo"></span><span id="v.turbo"></span><span id="V.TURBO"></span>

**V.turbo** (8)


</dt> <dd></dd> <dt>

<span id="V.FC"></span><span id="v.fc"></span>

**V.FC** (9)


</dt> <dd></dd> <dt>

<span id="V.34"></span><span id="v.34"></span>

**V.34** (10)


</dt> <dd></dd> <dt>

<span id="V.34bis"></span><span id="v.34bis"></span><span id="V.34BIS"></span>

**V.34bis** (11)


</dt> <dd></dd> </dl>

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")
</dt> </dl>

Etichetta con cui l'oggetto è noto. In caso di sottoclasse, la proprietà può essere sottoposta a override per essere una proprietà chiave.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**PNPDeviceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")
</dt> </dl>

Windows Plug and Play identificatore di dispositivo del dispositivo logico.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

Esempio: \* "PNP030b"

</dd> <dt>

**PortSubClass**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \| PortSubClass"), **Value** ("Parallel Port", "Serial Port", "Modem")
</dt> </dl>

Definizione della porta utilizzata per questo modem.

<dt>



 ("00")


</dt> <dd>

Porta parallela

</dd> <dt>



 ("01")


</dt> <dd>

Porta seriale

</dd> <dt>



 ("02")


</dt> <dd>

Modem

</dd> </dl>

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice delle funzionalità specifiche correlate all'alimentazione di un dispositivo logico.

Questa proprietà viene ereditata da **CIM \_ LogicalDevice.**

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)


</dt> <dd>

Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto o le informazioni non sono disponibili.

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità risparmio energia immesse automaticamente** (4)


</dt> <dd>

Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)


</dt> <dd>

Il [**metodo SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato. Questo metodo si trova nella classe **CIM \_ LogicalDevice** padre e può essere implementato. Per altre informazioni, vedere [Progettazione di Managed Object Format (MOF).](../wmisdk/designing-managed-object-format--mof--classes.md)

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Alimentazione supportata** (6)


</dt> <dd>

Il [**metodo SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il *parametro PowerState* impostato su 5 (Ciclo di alimentazione).

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Accensione a tempo supportata** (7)


</dt> <dd>

Tempor Power-On supportato

Il [**metodo SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (Power Cycle) e *Time* impostato su una data e un'ora o un intervallo specifici per l'accensione.

</dd> </dl>

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **TRUE,** il dispositivo può essere gestito dall'alimentazione (può essere messo in modalità di sospensione e così via). La proprietà non indica che le funzionalità di risparmio energia sono attualmente abilitate, ma solo che il dispositivo logico è in grado di eseguire il risparmio energia.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**Prefix**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \| Prefix")
</dt> </dl>

Prefisso di composizione usato per accedere a una linea esterna.

</dd> <dt>

**Proprietà**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \| Properties")
</dt> </dl>

Elenco di tutte le proprietà (e dei relativi valori) per il modem.

</dd> <dt>

**ProviderName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \| ProviderName")
</dt> </dl>

Percorso di rete del computer che fornisce i servizi modem.

</dd> <dt>

**Impulso**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \| Pulse")
</dt> </dl>

Stringa di comando utilizzata per indicare al modem di usare la modalità pulse per la composizione. La composizione a pulsazione è necessaria per le linee telefoniche che non sono in grado di gestire la composizione a tono.

Esempio: "P"

</dd> <dt>

**Reimpostazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](../wmisdk/standard-qualifiers.md) (reset), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet Control Class \\ \\ \\ \\ \| Reset")
</dt> </dl>

Stringa di comando usata per reimpostare il modem per la chiamata successiva.

Esempio: "AT&F"

</dd> <dt>

**ResponsesKeyName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \| ResponsesKeyName")
</dt> </dl>

Risposta che il modem potrebbe segnalare al sistema operativo durante il processo di connessione. I primi due caratteri specificano il tipo di risposta. I secondi due caratteri specificano informazioni sulla connessione effettuata. I secondi due caratteri vengono usati solo per lo stato di avanzamento della negoziazione o Connessione di risposta. Gli otto caratteri successivi specificano la velocità della linea da modem a modem negoziata in bit al secondo (bps). I caratteri rappresentano un formato long integer senza segno a 32 bit (byte e parola invertito). Gli ultimi otto caratteri indicano che il modem sta cambiando a una porta diversa o a una velocità DTE (Data Terminal Equipment). In genere questo campo non viene utilizzato perché i modem esecutori effettuano connessioni a una velocità della porta bloccata indipendentemente dalla velocità da modem a modem o DCE (Data Communications Equipment).

</dd> <dt>

**RingsBeforeAnswer**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di anelli prima che il modem rileva una chiamata in ingresso.

Questa proprietà viene ereditata da [**CIM \_ PotsModem.**](cim-potsmodem.md)

</dd> <dt>

**SpeakerModeDial**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \| SpeakerModeDial")
</dt> </dl>

Stringa di comando usata per attivare l'altoparlante del modem dopo la composizione di un numero e la disattivazione della voce quando è stata stabilita una connessione.

Esempio: "M1"

</dd> <dt>

**SpeakerModeOff**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \| SpeakerModeOff")
</dt> </dl>

Stringa di comando utilizzata per disattivare l'altoparlante del modem.

Esempio: "M0"

</dd> <dt>

**SpeakerModeOn**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \| SpeakerModeOn")
</dt> </dl>

Stringa di comando utilizzata per attivare l'altoparlante del modem.

Esempio: "M2"

</dd> <dt>

**SpeakerModeSetup**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \| SpeakerModeSetup")
</dt> </dl>

Stringa di comando usata per indicare al modem di accendere l'altoparlante (fino a quando non viene stabilita una connessione).

Esempio: "M3"

</dd> <dt>

**SpeakerVolumeHigh**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \| SpeakerVolume \_ High")
</dt> </dl>

Stringa di comando utilizzata per impostare l'altoparlante del modem sul volume più elevato.

Esempio: "L3"

</dd> <dt>

**SpeakerVolumeInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrive il livello di volume dei toni udibili del modem.

Questa proprietà viene ereditata da [**CIM \_ PotsModem.**](cim-potsmodem.md)

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

**Non supportato** (2)


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

**Alto** (3)


</dt> <dd></dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

**Media** (4)


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

**Basso** (5)


</dt> <dd></dd> <dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

**Disattivato** (6)


</dt> <dd></dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

**Auto** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**SpeakerVolumeLow**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \| SpeakerVolume \_ Low")
</dt> </dl>

Stringa di comando utilizzata per impostare l'altoparlante del modem sul volume più basso.

Esempio: "L1"

</dd> <dt>

**SpeakerVolumeMed**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \| SpeakerVolume \_ Med")
</dt> </dl>

Stringa di comando utilizzata per impostare l'altoparlante del modem su un volume medio.

Esempio: "L2"

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Stato corrente dell'oggetto. È possibile definire vari stati operativi e non operativi. Gli stati operativi includono: "OK", "Degraded" e "Pred Fail" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente ma prevedere un errore nel prossimo futuro). Gli stati nonoperational includono: "Error", "Starting", "Stopping" e "Service". Quest'ultimo, "Servizio", può essere applicato durante il ridimensionamento del mirror di un disco, il ricaricamento di un elenco di autorizzazioni utente o altro lavoro amministrativo. Non tutte queste operazioni sono online, ma l'elemento gestito non è "OK" né in uno degli altri stati.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

Sono inclusi i valori seguenti:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Errore** ("Error")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degraded** ("Degraded")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** ("Sconosciuto")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred Fail** ("Pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Starting** ("Starting")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Arresto** ("Arresto")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Servizio** ("Servizio")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Stressed** ("Stressed")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ("NonRecover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Nessun contatto** ("Nessun contatto")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Lost Comm** ("Lost Comm")


</dt> <dd></dd> </dl>

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| Operational State \| 003.3")
</dt> </dl>

Stato del dispositivo logico. Se questa proprietà non si applica al dispositivo logico, è necessario usare il valore 5 (Non applicabile).

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (2)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Abilitato** (3)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Disabilitato** (4)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Non applicabile** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**Stringformat**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \_ API Line Device \| Structures \| LINEDEVCAPS \| dwStringFormat")
</dt> </dl>

Tipo di caratteri utilizzati per il testo passato attraverso il modem.

I valori possibili sono:

<dl> <dd>"Formato stringa ASCII"</dd> <dd>"Formato stringa DBCS"</dd> <dd>"Formato stringa UNICODE"</dd> </dl>

<dt>

<span id="ASCII_string_format"></span><span id="ascii_string_format"></span><span id="ASCII_STRING_FORMAT"></span>

**Formato stringa ASCII** ("formato stringa ASCII")


</dt> <dd></dd> <dt>

<span id="DBCS_string_format"></span><span id="dbcs_string_format"></span><span id="DBCS_STRING_FORMAT"></span>

**Formato stringa DBCS** ("formato stringa DBCS")


</dt> <dd></dd> <dt>

<span id="UNICODE_string_format"></span><span id="unicode_string_format"></span><span id="UNICODE_STRING_FORMAT"></span>

**Formato stringa UNICODE** ("formato stringa UNICODE")


</dt> <dd></dd> </dl>

</dd> <dt>

**SupportsCallback**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **TRUE,** il modem supporta il callback.

Questa proprietà viene ereditata da [**CIM \_ PotsModem.**](cim-potsmodem.md)

</dd> <dt>

**SupportsSynchronousConnect**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **TRUE,** la comunicazione sincrona e asincrona è supportata.

Questa proprietà viene ereditata da [**CIM \_ PotsModem.**](cim-potsmodem.md)

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagati**](../wmisdk/standard-qualifiers.md) ("[**Sistema CIM \_**](cim-system.md).**CreationClassName**"), [**CHIAVE \_ CIM**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Valore della proprietà **CreationClassName** del computer di ambito.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagati**](../wmisdk/standard-qualifiers.md) ("[**Sistema CIM \_**](cim-system.md).**Name**"), [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Nome del sistema di ambito.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**Carattere di terminazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \| Terminator")
</dt> </dl>

Stringa che contrassegna la fine di una stringa di comando.

Esempio: "<cr"

</dd> <dt>

**TimeOfLastReset**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora dell'ultima reimpostazione del modem.

Questa proprietà viene ereditata da [**CIM \_ PotsModem.**](cim-potsmodem.md)

</dd> <dt>

**Tono**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \| Tone")
</dt> </dl>

Stringa di comando che indica al modem di utilizzare la modalità tono per la composizione. La linea telefonica deve supportare la composizione a tono.

Esempio: "T"

</dd> <dt>

**Funzionalità voiceSwitchFeature**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \| VoiceSwitchFeature")
</dt> </dl>

Stringhe di comando usate per attivare le funzionalità vocali di un voice modem.

Esempio: "AT+V"

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe WIN32 \_ POTSModem** è derivata da [**CIM \_ PotsModem.**](cim-potsmodem.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ PotsModem**](cim-potsmodem.md)
</dt> <dt>

[Classi hardware del sistema computer](computer-system-hardware-classes.md)
</dt> </dl>

 

 

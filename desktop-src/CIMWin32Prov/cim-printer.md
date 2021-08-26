---
description: La classe CIM \_ Printer rappresenta le funzionalità e la gestione del dispositivo logico della stampante.
ms.assetid: e41ff580-0202-4d3f-8d78-4705d5fb41b3
ms.tgt_platform: multiple
title: CIM_Printer classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Printer
- CIM_Printer.Availability
- CIM_Printer.AvailableJobSheets
- CIM_Printer.Capabilities
- CIM_Printer.CapabilityDescriptions
- CIM_Printer.Caption
- CIM_Printer.CharSetsSupported
- CIM_Printer.ConfigManagerErrorCode
- CIM_Printer.ConfigManagerUserConfig
- CIM_Printer.CreationClassName
- CIM_Printer.CurrentCapabilities
- CIM_Printer.CurrentCharSet
- CIM_Printer.CurrentLanguage
- CIM_Printer.CurrentMimeType
- CIM_Printer.CurrentNaturalLanguage
- CIM_Printer.CurrentPaperType
- CIM_Printer.DefaultCapabilities
- CIM_Printer.DefaultCopies
- CIM_Printer.DefaultLanguage
- CIM_Printer.DefaultMimeType
- CIM_Printer.DefaultNumberUp
- CIM_Printer.DefaultPaperType
- CIM_Printer.Description
- CIM_Printer.DetectedErrorState
- CIM_Printer.DeviceID
- CIM_Printer.ErrorCleared
- CIM_Printer.ErrorDescription
- CIM_Printer.ErrorInformation
- CIM_Printer.HorizontalResolution
- CIM_Printer.InstallDate
- CIM_Printer.JobCountSinceLastReset
- CIM_Printer.LanguagesSupported
- CIM_Printer.LastErrorCode
- CIM_Printer.MarkingTechnology
- CIM_Printer.MaxCopies
- CIM_Printer.MaxNumberUp
- CIM_Printer.MaxSizeSupported
- CIM_Printer.MimeTypesSupported
- CIM_Printer.Name
- CIM_Printer.NaturalLanguagesSupported
- CIM_Printer.PaperSizesSupported
- CIM_Printer.PaperTypesAvailable
- CIM_Printer.PNPDeviceID
- CIM_Printer.PowerManagementCapabilities
- CIM_Printer.PowerManagementSupported
- CIM_Printer.PrinterStatus
- CIM_Printer.Status
- CIM_Printer.StatusInfo
- CIM_Printer.SystemCreationClassName
- CIM_Printer.SystemName
- CIM_Printer.TimeOfLastReset
- CIM_Printer.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 001e0fce9645ddc2487a934fcbfa5986771f3dad841f58ea60dd4772e9120d7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921231"
---
# <a name="cim_printer-class"></a>Classe CiM \_ Printer

La **classe CIM \_ Printer** rappresenta le funzionalità e la gestione del dispositivo logico della stampante.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Common Information Model Distributed Management Task Force) sono le classi padre su cui vengono compilate le classi WMI. WMI attualmente supporta solo gli schemi [della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal Managed Object Format (MOF) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{8502C54A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Printer : CIM_LogicalDevice
{
  uint16   Availability;
  string   AvailableJobSheets[];
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  string   CharSetsSupported[];
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint16   CurrentCapabilities[];
  string   CurrentCharSet;
  uint16   CurrentLanguage;
  string   CurrentMimeType;
  string   CurrentNaturalLanguage;
  string   CurrentPaperType;
  uint16   DefaultCapabilities[];
  uint32   DefaultCopies;
  uint16   DefaultLanguage;
  string   DefaultMimeType;
  uint32   DefaultNumberUp;
  string   DefaultPaperType;
  string   Description;
  uint16   DetectedErrorState;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorInformation[];
  uint32   HorizontalResolution;
  datetime InstallDate;
  uint32   JobCountSinceLastReset;
  uint16   LanguagesSupported[];
  uint32   LastErrorCode;
  uint16   MarkingTechnology;
  uint32   MaxCopies;
  uint32   MaxNumberUp;
  uint32   MaxSizeSupported;
  string   MimeTypesSupported[];
  string   Name;
  string   NaturalLanguagesSupported[];
  uint16   PaperSizesSupported[];
  string   PaperTypesAvailable[];
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   PrinterStatus;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
  uint32   VerticalResolution;
};
```

## <a name="members"></a>Members

La **classe CIM \_ Printer** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe CIM \_ Printer** include questi metodi.



| Metodo                                                             | Descrizione                                                                                                                              |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [**Reset**](reset-method-in-class-cim-printer.md)                 | Richiede una reimpostazione del dispositivo logico. Non implementato da WMI.<br/>                                                               |
| [**SetPowerState**](setpowerstate-method-in-class-cim-printer.md) | Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato. Non implementato da WMI.<br/> |



 

### <a name="properties"></a>Proprietà

La **classe CIM \_ Printer** ha queste proprietà.

<dl> <dt>

**Disponibilità**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Operational State \| 003.5", "MIB. IETF \| HOST-RESOURCES-MIB.hrDeviceStatus")
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

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/alimentazione completa** (3)


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

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)


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

Il dispositivo è noto per essere in modalità risparmio energia, ma lo stato esatto è sconosciuto.

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia - Modalità a basso consumo** (14)


</dt> <dd>

Il dispositivo è in stato di risparmio energia, ma funziona ancora e può presentare prestazioni ridotte.

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia - Standby** (15)


</dt> <dd>

Il dispositivo non funziona, ma può essere portato a piena potenza rapidamente.

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia - Avviso** (17)


</dt> <dd>

Il dispositivo è in uno stato di avviso, anche se in modalità risparmio energia.

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**In pausa** (18)


</dt> <dd>

Il dispositivo è sospeso.

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

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)


</dt> <dd>

Il dispositivo è silenzioso.

</dd> </dl>

</dd> <dt>

**AvailableJobSheets**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob.RequiredJobSheets")
</dt> </dl>

Descrive tutti i fogli di lavoro disponibili nella stampante. Può essere usato anche per descrivere il banner che una stampante può fornire all'inizio di ogni processo o può descrivere altre opzioni specificate dall'utente.

</dd> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indicizzato"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Printer**. CapabilityDescriptions", "CIM \_ PrintJob.Finishing", "CIM \_ PrintService.Capabilities")
</dt> </dl>

Funzionalità della stampante.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Stampa a colori** (2)


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Stampa duplex** (3)


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copie** (4)


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Regole di confronto** (5)


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Graffatura** (6)


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Stampa con trasparenza** (7)


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punzone** (8)


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Copertura** (9)


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Stampa in bianco e nero** (11)


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)


</dt> <dd>

Lato uno

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Long Edge a due lati** (13)


</dt> <dd>

Bordo lungo a due lati

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Short Edge a due lati** (14)


</dt> <dd>

Bordo corto a due lati

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Verticale** (15)


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Orizzontale** (16)


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Verticale inverso** (17)


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Orizzontale inverso** (18)


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)


</dt> <dd>

Qualità elevata

</dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Qualità normale** (20)


</dt> <dd>

Normale di qualità

</dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Qualità bassa** (21)


</dt> <dd>

Qualità bassa

</dd> </dl>

</dd> <dt>

**CapabilityDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Printer**.**Funzionalità di**")
</dt> </dl>

Stringhe in formato libero che forniscono spiegazioni dettagliate per una delle funzionalità della stampante indicate nella **matrice Capabilities.**

> [!Note]  
> Ogni voce di questa matrice è correlata alla voce nella matrice **Capabilities** che si trova nello stesso indice.

 

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Breve descrizione testuale dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**CharSetsSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob.CharSet"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Printer-MIB.prtLocalizationCharacterSet")
</dt> </dl>

Set di caratteri disponibili per l'output del testo correlato alla gestione della stampante. Le stringhe fornite in questa proprietà devono essere conformi alla semantica e alla sintassi specificate nella sezione 4.1.2 ("Parametro Charset") in RFC 2046 (PARTE 2 MIME) e contenute nel Registro di sistema dei set di caratteri IANA. Ad esempio, "utf-8", "us-ascii" e "iso-8859-1".

</dd> <dt>

**ConfigManagerErrorCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")
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

Il driver per questo dispositivo potrebbe essere danneggiato o la memoria del sistema potrebbe essere insufficiente o altre risorse.

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei relativi driver o il Registro di sistema potrebbe essere danneggiato.** (4)


</dt> <dd>

Il dispositivo non funziona correttamente. Uno dei relativi driver o il Registro di sistema potrebbe essere danneggiato.

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che non Windows gestire.** (5)


</dt> <dd>

Il driver per il dispositivo richiede una risorsa che non Windows gestire.

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

<span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.** (10)


</dt> <dd>

Impossibile avviare il dispositivo.

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Il dispositivo non è riuscito.** (11)


</dt> <dd>

Dispositivo non riuscito.

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non riesce a trovare risorse gratuite sufficienti da usare.** (12)


</dt> <dd>

Il dispositivo non riesce a trovare risorse gratuite sufficienti da usare.

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows possibile verificare le risorse del dispositivo.** (13)


</dt> <dd>

Windows possibile verificare le risorse del dispositivo.

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente fino a quando non si riavvia il computer.** (14)


</dt> <dd>

Il dispositivo non funziona correttamente finché il computer non viene riavviato.

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Questo dispositivo non funziona correttamente perché è probabile che si sia verificato un problema di enumerazione.** (15)


</dt> <dd>

Il dispositivo non funziona correttamente a causa di un possibile problema di enumerazione.

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.** (16)


</dt> <dd>

Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.

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

<span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro potrebbe essere danneggiato.** (20)


</dt> <dd>

Il Registro di sistema potrebbe essere danneggiato.

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo il dispositivo.** (21)


</dt> <dd>

Errore di sistema. Se la modifica del driver di dispositivo è inefficace, vedere la documentazione dell'hardware. Windows sta rimuovendo il dispositivo.

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Questo dispositivo è disabilitato.** (22)


</dt> <dd>

Il dispositivo è disabilitato.

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware.** (23)


</dt> <dd>

Errore di sistema. Se la modifica del driver di dispositivo è inefficace, vedere la documentazione dell'hardware.

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Il dispositivo non è presente, non funziona correttamente o non dispone di tutti i relativi driver installati.** (24)


</dt> <dd>

Il dispositivo non è presente, non funziona correttamente o non dispone di tutti i relativi driver installati.

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora configurando il dispositivo.** (25)


</dt> <dd>

Windows sta ancora configurando il dispositivo.

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora configurando il dispositivo.** (26)


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

<span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa richiesta di interrupt (IRQ) che un altro dispositivo sta usando.** (30)


</dt> <dd>

Il dispositivo usa una risorsa IRQ in uso da un altro dispositivo.

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché non Windows caricare i driver necessari per il dispositivo.** (31)


</dt> <dd>

Il dispositivo non funziona correttamente. Windows possibile caricare i driver di dispositivo necessari.

</dd> </dl>

</dd> <dt>

**ConfigManagerUserConfig**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")
</dt> </dl>

Se **TRUE,** il dispositivo usa una configurazione definita dall'utente.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave \_ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Nome della classe o sottoclasse utilizzata nella creazione di un'istanza di . Se usata con altre proprietà chiave della classe , questa proprietà consente l'identificazione univoca di tutte le istanze della classe e delle relative sottoclassi.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**CurrentCapabilities**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Printer**.**Funzionalità di**")
</dt> </dl>

Completamenti e altre funzionalità della stampante attualmente in uso. Ogni voce di questa proprietà deve essere elencata anche nella **matrice Capabilities.**

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Stampa a colori** (2)


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Stampa duplex** (3)


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copie** (4)


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Regole di confronto** (5)


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Graffatura** (6)


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Stampa con trasparenza** (7)


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Avaio** (8)


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Stampa in bianco e nero** (11)


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)


</dt> <dd>

Lato uno

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Bordo lungo a due lati** (13)


</dt> <dd>

Bordo lungo a due lati

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Bordo breve a due lati** (14)


</dt> <dd>

Bordo breve a due lati

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Verticale** (15)


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Orizzontale** (16)


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Verticale inverso** (17)


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Orizzontale** inverso (18)


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)


</dt> <dd>

Qualità elevata

</dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)


</dt> <dd>

Qualità normale

</dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Qualità bassa** (21)


</dt> <dd>

Qualità bassa

</dd> </dl>

</dd> <dt>

**CurrentCharSet**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Printer**.**CharSetsSupported**")
</dt> </dl>

Set di caratteri corrente utilizzato per l'output del testo relativo alla gestione della stampante. Il set di caratteri descritto da questa proprietà deve essere elencato anche nella **proprietà CharsetsSupported.** La stringa specificata da questa proprietà deve essere conforme alla semantica e alla sintassi specificate nella sezione 4.1.2 ("parametro Charset") in RFC 2046 (MIME parte 2) e contenuta nel Registro di sistema dei set di caratteri IANA. Ad esempio, "utf-8", "us-ascii" e "iso-8859-1".

</dd> <dt>

**CurrentLanguage**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Printer**. LanguagesSupported", "CIM \_ Printer.CurrentMimeType")
</dt> </dl>

Lingua della stampante corrente in uso; la lingua deve essere elencata anche nella **proprietà LanguagesSupported.**

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (2)


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

**PCL** (3)


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

**HPGL** (4)


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

**PJL** (5)


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

**PS** (6)


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

**PSPrinter** (7)


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

**IPDS** (8)


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

**PPDS** (9)


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

**EscapeP** (10)


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

**Epson** (11)


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

**DDIF** (12)


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

**Interpress** (13)


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

**ISO6429** (14)


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

**Dati riga** (15)


</dt> <dd></dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

**MODCA** (16)


</dt> <dd></dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

**REGIS** (17)


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

**SCS** (18)


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

**SPDL** (19)


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

**TEK4014** (20)


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

**PDS** (21)


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

**IGP** (22)


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

**CodeV** (23)


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

**DSCDSE** (24)


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

**WPS** (25)


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

**LN03** (26)


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

**CCITT** (27)


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

**QUIC** (28)


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

**CPAP** (29)


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

**DecPPL** (30)


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

**Testo semplice** (31)


</dt> <dd></dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

**NPAP** (32)


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

**DOC** (33)


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

**imPress** (34)


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

**Pinwriter** (35)


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

**NPDL** (36)


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

**NEC201PL** (37)


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

**Automatico** (38)


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

**Pagine** (39)


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

**ROSSETTO** (40)


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

**TIFF** (41)


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

**Diagnostica** (42)


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

**CaPSL** (43)


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

**EXCL** (44)


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

**LCDS** (45)


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

**XES** (46)


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

**MIME** (47)


</dt> <dd></dd> </dl>

</dd> <dt>

**CurrentMimeType**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Printer**.**CurrentLanguage**")
</dt> </dl>

Tipo Mime attualmente in uso dalla stampante quando la **proprietà CurrentLanguage** è impostata per indicare che è in uso un tipo mime.

</dd> <dt>

**CurrentNaturalLanguage**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Printer**.**NaturalLanguagesSupported**")
</dt> </dl>

Lingua corrente utilizzata dalla stampante per la gestione. La lingua elencata qui deve essere elencata anche in **NaturalLanguagesSupported**.

</dd> <dt>

**CurrentPaperType**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Printer**.**PaperTypesAvailable**")
</dt> </dl>

Tipo di carta attualmente in uso dalla stampante. La stringa deve essere espressa nel formato specificato da ISO/IEC 10175 Document Printing Application (DPA), riepilogato anche nell'appendice C di RFC 1759 (Printer MIB).

</dd> <dt>

**DefaultCapabilities**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Printer**.**Funzionalità**")
</dt> </dl>

Finiture predefinite e altre funzionalità della stampante. Ogni voce di questa proprietà deve essere elencata anche nella matrice **Capabilities.**

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Stampa a colori** (2)


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Stampa duplex** (3)


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copie** (4)


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Regole di confronto** (5)


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Graffatura** (6)


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Stampa con trasparenza** (7)


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punzone** (8)


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Copertura** (9)


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Stampa in bianco e nero** (11)


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)


</dt> <dd>

Lato uno

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Long Edge a due** lati (13)


</dt> <dd>

Bordo lungo a due lati

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Short Edge a due lati** (14)


</dt> <dd>

Bordo corto a due lati

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Verticale** (15)


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Orizzontale** (16)


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Verticale inverso** (17)


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Orizzontale inverso** (18)


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Qualità elevata** (19)


</dt> <dd>

Qualità elevata

</dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Qualità normale** (20)


</dt> <dd>

Qualità normale

</dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Qualità bassa** (21)


</dt> <dd>

Qualità bassa

</dd> </dl>

</dd> <dt>

**DefaultCopies**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di copie che verranno prodotti da un singolo processo, se non diversamente specificato.

</dd> <dt>

**DefaultLanguage**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Printer**. LanguagesSupported", "CIM \_ Printer.DefaultMimeType")
</dt> </dl>

Lingua predefinita della stampante. La lingua deve essere elencata anche nella **proprietà LanguagesSupported.**

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (2)


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

**PCL** (3)


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

**HPGL** (4)


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

**PJL** (5)


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

**PS** (6)


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

**PSPrinter** (7)


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

**IPDS** (8)


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

**PPDS** (9)


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

**EscapeP** (10)


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

**Epson** (11)


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

**DDIF** (12)


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

**Interpress** (13)


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

**ISO6429** (14)


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

**Dati riga** (15)


</dt> <dd></dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

**MODCA** (16)


</dt> <dd></dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

**REGIS** (17)


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

**SCS** (18)


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

**SPDL** (19)


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

**TEK4014** (20)


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

**PDS** (21)


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

**IGP** (22)


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

**CodeV** (23)


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

**DSCDSE** (24)


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

**WPS** (25)


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

**LN03** (26)


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

**CCITT** (27)


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

**QUIC** (28)


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

**CPAP** (29)


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

**DecPPL** (30)


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

**Testo semplice** (31)


</dt> <dd></dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

**NPAP** (32)


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

**DOC** (33)


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

**imPress** (34)


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

**Pinwriter** (35)


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

**NPDL** (36)


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

**NEC201PL** (37)


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

**Automatico** (38)


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

**Pagine** (39)


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

**ROSSETTO** (40)


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

**TIFF** (41)


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

**Diagnostica** (42)


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

**CaPSL** (43)


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

**EXCL** (44)


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

**LCDS** (45)


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

**XES** (46)


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

**MIME** (47)


</dt> <dd></dd> </dl>

</dd> <dt>

**DefaultMimeType**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Printer**.**DefaultLanguage**")
</dt> </dl>

Tipo mime predefinito utilizzato dalla stampante quando la **proprietà DefaultLanguage** è impostata per indicare che è in uso un tipo mime.

</dd> <dt>

**DefaultNumberUp**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di pagine del flusso di stampa di cui la stampante eseguirà il rendering su un singolo foglio multimediale, a meno che un processo non specifichi diversamente.

</dd> <dt>

**DefaultPaperType**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Printer**.**PaperTypesAvailable**")
</dt> </dl>

Tipo di carta che verrà utilizzato dalla stampante se PrintJob non specifica un tipo specifico. La stringa deve essere espressa nel formato specificato da ISO/IEC 10175 Document Printing Application (DPA), riepilogato anche nell'appendice C di RFC 1759 (Printer MIB).

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Descrizione testuale dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**DetectedErrorState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Printer**.**ErrorInformation**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Printer-MIB.hrPrinterDetectedErrorState")
</dt> </dl>

Informazioni sull'errore della stampante.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="No_Error"></span><span id="no_error"></span><span id="NO_ERROR"></span>

**Nessun errore** (2)


</dt> <dd></dd> <dt>

<span id="Low_Paper"></span><span id="low_paper"></span><span id="LOW_PAPER"></span>

**Carta bassa** (3)


</dt> <dd></dd> <dt>

<span id="No_Paper"></span><span id="no_paper"></span><span id="NO_PAPER"></span>

**Nessun documento** (4)


</dt> <dd></dd> <dt>

<span id="Low_Toner"></span><span id="low_toner"></span><span id="LOW_TONER"></span>

**Toner basso** (5)


</dt> <dd></dd> <dt>

<span id="No_Toner"></span><span id="no_toner"></span><span id="NO_TONER"></span>

**Nessun toner** (6)


</dt> <dd></dd> <dt>

<span id="Door_Open"></span><span id="door_open"></span><span id="DOOR_OPEN"></span>

**Porta aperta** (7)


</dt> <dd></dd> <dt>

<span id="Jammed"></span><span id="jammed"></span><span id="JAMMED"></span>

**Inceppato** (8)


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

**Offline** (9)


</dt> <dd></dd> <dt>

<span id="Service_Requested"></span><span id="service_requested"></span><span id="SERVICE_REQUESTED"></span>

**Servizio richiesto** (10)


</dt> <dd></dd> <dt>

<span id="Output_Bin_Full"></span><span id="output_bin_full"></span><span id="OUTPUT_BIN_FULL"></span>

**Bin di output pieno** (11)


</dt> <dd></dd> </dl>

</dd> <dt>

**Deviceid**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave \_ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **TRUE,** l'errore segnalato nella **proprietà LastErrorCode** viene ora cancellato.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**ErrorInformation**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Printer**.**DetectedErrorState**")
</dt> </dl>

Matrice che fornisce informazioni supplementari per lo stato di errore corrente, indicato nella **proprietà DetectedErrorState.**

</dd> <dt>

**HorizontalResolution**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob.HorizontalResolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixel per pollice")
</dt> </dl>

Risoluzione orizzontale in pixel per pollice.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")
</dt> </dl>

Data e ora di installazione dell'oggetto. Questa proprietà non richiede un valore per indicare che l'oggetto è installato.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**JobCountSinceLastReset**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Contatore**
</dt> </dl>

Processi della stampante elaborati dopo l'ultima reimpostazione. Questi processi possono essere elaborati da una o più code di stampa.

</dd> <dt>

**LanguagesSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Printer-MIB.prtInterpreterLangFamily"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Printer**. MimeTypesSupported", "CIM \_ PrintJob.Language", "CIM \_ PrintService.LanguagesSupported")
</dt> </dl>

Lingue di stampa supportate in modo nativo.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (2)


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

**PCL** (3)


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

**HPGL** (4)


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

**PJL** (5)


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

**PS** (6)


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

**PSPrinter** (7)


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

**IPDS** (8)


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

**PPDS** (9)


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

**EscapeP** (10)


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

**Epson** (11)


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

**DDIF** (12)


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

**Interpress** (13)


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

**ISO6429** (14)


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

**Dati riga** (15)


</dt> <dd></dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

**MODCA** (16)


</dt> <dd></dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

**REGIS** (17)


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

**SCS** (18)


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

**SPDL** (19)


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

**TEK4014** (20)


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

**PDS** (21)


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

**IGP** (22)


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

**CodeV** (23)


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

**DSCDSE** (24)


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

**WPS** (25)


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

**LN03** (26)


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

**CCITT** (27)


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

**QUIC** (28)


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

**CPAP** (29)


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

**DecPPL** (30)


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

**Testo semplice** (31)


</dt> <dd></dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

**NPAP** (32)


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

**DOC** (33)


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

**imPress** (34)


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

**Pinwriter** (35)


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

**NPDL** (36)


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

**NEC201PL** (37)


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

**Automatico** (38)


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

**Pagine** (39)


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

**ROSSETTO** (40)


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

**TIFF** (41)


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

**Diagnostica** (42)


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

**CaPSL** (43)


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

**EXCL** (44)


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

**LCDS** (45)


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

**XES** (46)


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

**MIME** (47)


</dt> <dd></dd> <dt>

<span id="XPS"></span><span id="xps"></span>

**XPS** (48)


</dt> <dd></dd> <dt>

<span id="HPGL2"></span><span id="hpgl2"></span>

**HPGL2** (49)


</dt> <dd></dd> <dt>

<span id="PCLXL"></span><span id="pclxl"></span>

**PCLXL** (50)


</dt> <dd></dd> </dl>

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

**MarkingTechnology**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Printer-MIB.prtMarkerMarkerMarkTech")
</dt> </dl>

Tecnologia di contrassegno usata dalla stampante.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (2)


</dt> <dd></dd> <dt>

<span id="Electrophotographic_LED"></span><span id="electrophotographic_led"></span><span id="ELECTROPHOTOGRAPHIC_LED"></span>

**LED elettrofotografico** (3)


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Laser"></span><span id="electrophotographic_laser"></span><span id="ELECTROPHOTOGRAPHIC_LASER"></span>

**Laser elettrofotografico** (4)


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Other"></span><span id="electrophotographic_other"></span><span id="ELECTROPHOTOGRAPHIC_OTHER"></span>

**Altro elettrofotografico** (5)


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_9pin"></span><span id="impact_moving_head_dot_matrix_9pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_9PIN"></span>

**Impatto Spostamento della matrice dei punti della testa 9 punti** (6)


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_24pin"></span><span id="impact_moving_head_dot_matrix_24pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_24PIN"></span>

**Impatto Spostamento della matrice dei punti della testa a 24 puntini** (7)


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_Other"></span><span id="impact_moving_head_dot_matrix_other"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_OTHER"></span>

**Impatto Spostamento della matrice dei punti della testa altro** (8)


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Fully_Formed"></span><span id="impact_moving_head_fully_formed"></span><span id="IMPACT_MOVING_HEAD_FULLY_FORMED"></span>

**Impatto Spostamento della testa completamente formato** (9)


</dt> <dd></dd> <dt>

<span id="Impact_Band"></span><span id="impact_band"></span><span id="IMPACT_BAND"></span>

**Banda di impatto** (10)


</dt> <dd></dd> <dt>

<span id="Impact_Other"></span><span id="impact_other"></span><span id="IMPACT_OTHER"></span>

**Impatto altro** (11)


</dt> <dd></dd> <dt>

<span id="Inkjet_Aqueous"></span><span id="inkjet_aqueous"></span><span id="INKJET_AQUEOUS"></span>

**Inkjet Aqueous** (12)


</dt> <dd></dd> <dt>

<span id="Inkjet_Solid"></span><span id="inkjet_solid"></span><span id="INKJET_SOLID"></span>

**Inkjet Solid** (13)


</dt> <dd></dd> <dt>

<span id="Inkjet_Other"></span><span id="inkjet_other"></span><span id="INKJET_OTHER"></span>

**Inkjet Other** (14)


</dt> <dd></dd> <dt>

<span id="Pen"></span><span id="pen"></span><span id="PEN"></span>

**Penna** (15)


</dt> <dd></dd> <dt>

<span id="Thermal_Transfer"></span><span id="thermal_transfer"></span><span id="THERMAL_TRANSFER"></span>

**Trasferimento termico** (16)


</dt> <dd></dd> <dt>

<span id="Thermal_Sensitive"></span><span id="thermal_sensitive"></span><span id="THERMAL_SENSITIVE"></span>

**Sensibile termico** (17)


</dt> <dd></dd> <dt>

<span id="Thermal_Diffusion"></span><span id="thermal_diffusion"></span><span id="THERMAL_DIFFUSION"></span>

**Diffusione termica** (18)


</dt> <dd></dd> <dt>

<span id="Thermal_Other"></span><span id="thermal_other"></span><span id="THERMAL_OTHER"></span>

**Altro termico** (19)


</dt> <dd></dd> <dt>

<span id="Electroerosion"></span><span id="electroerosion"></span><span id="ELECTROEROSION"></span>

**Recisorezione** (20)


</dt> <dd></dd> <dt>

<span id="Electrostatic"></span><span id="electrostatic"></span><span id="ELECTROSTATIC"></span>

**Estatico** (21)


</dt> <dd></dd> <dt>

<span id="Photographic_Microfiche"></span><span id="photographic_microfiche"></span><span id="PHOTOGRAPHIC_MICROFICHE"></span>

**Microfiche per la fotografia** (22)


</dt> <dd></dd> <dt>

<span id="Photographic_Imagesetter"></span><span id="photographic_imagesetter"></span><span id="PHOTOGRAPHIC_IMAGESETTER"></span>

**Imagesetter** (23)


</dt> <dd></dd> <dt>

<span id="Photographic_Other"></span><span id="photographic_other"></span><span id="PHOTOGRAPHIC_OTHER"></span>

**Altro** (24)


</dt> <dd></dd> <dt>

<span id="Ion_Deposition"></span><span id="ion_deposition"></span><span id="ION_DEPOSITION"></span>

**Deposizione ione** (25)


</dt> <dd></dd> <dt>

<span id="eBeam"></span><span id="ebeam"></span><span id="EBEAM"></span>

**eBeam** (26)


</dt> <dd></dd> <dt>

<span id="Typesetter"></span><span id="typesetter"></span><span id="TYPESETTER"></span>

**Typesetter** (27)


</dt> <dd></dd> </dl>

</dd> <dt>

**MaxCopies**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob.Copies")
</dt> </dl>

Numero massimo di copie che possono essere prodotte dalla stampante da un singolo processo.

</dd> <dt>

**MaxNumberUp**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob.NumberUp")
</dt> </dl>

Numero massimo di pagine del flusso di stampa di cui la stampante può eseguire il rendering su un singolo foglio multimediale.

</dd> <dt>

**MaxSizeSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob.JobSize"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")
</dt> </dl>

Processo più grande (come flusso di byte) che la stampante accetterà in unità di kilobyte. Il valore 0 (zero) indica che non è stato impostato alcun limite.

</dd> <dt>

**MimeTypesSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Printer**. LanguagesSupported", "CIM \_ PrintJob.MimeTypes", "CIM \_ PrintService.MimeTypesSupported")
</dt> </dl>

Stringhe in formato libero che forniscono spiegazioni dettagliate dei tipi MIME supportati dalla stampante. Se per questa proprietà vengono forniti dati, il valore 47 ("Mime") deve essere incluso nella **proprietà LanguagesSupported.**

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")
</dt> </dl>

Etichetta con cui l'oggetto è noto. Quando è sottoclassata, questa proprietà può essere sottoposta a override come proprietà chiave.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**NaturalLanguagesSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Printer-MIB.prtLocalizationLanguage"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob.NaturalLanguage")
</dt> </dl>

Lingue disponibili per le stringhe utilizzate dalla stampante per l'output delle informazioni di gestione. Le stringhe devono essere conformi a RFC 1766. Ad esempio, "en" viene usato per l'inglese.

</dd> <dt>

**PaperSizesSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipi di carta supportati.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="A"></span><span id="a"></span>

**A** (2)


</dt> <dd></dd> <dt>

<span id="B"></span><span id="b"></span>

**B** (3)


</dt> <dd></dd> <dt>

<span id="C"></span><span id="c"></span>

**C** (4)


</dt> <dd></dd> <dt>

<span id="D"></span><span id="d"></span>

**D** (5)


</dt> <dd></dd> <dt>

<span id="E"></span><span id="e"></span>

**E** (6)


</dt> <dd></dd> <dt>

<span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>

**Lettera** (7)


</dt> <dd></dd> <dt>

<span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>

**Note legali** (8)


</dt> <dd></dd> <dt>

<span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>

**Busta NA-10x13** (9)


</dt> <dd></dd> <dt>

<span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>

**Busta NA-9x12** (10)


</dt> <dd></dd> <dt>

<span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>

**Na-Number-10-Envelope** (11)


</dt> <dd></dd> <dt>

<span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>

**Busta NA-7x9** (12)


</dt> <dd></dd> <dt>

<span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>

**Busta NA-9x11** (13)


</dt> <dd></dd> <dt>

<span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>

**Busta NA-10x14** (14)


</dt> <dd></dd> <dt>

<span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>

**Na-Number-9-Envelope** (15)


</dt> <dd></dd> <dt>

<span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>

**Busta NA-6x9** (16)


</dt> <dd></dd> <dt>

<span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>

**Busta NA-10x15** (17)


</dt> <dd></dd> <dt>

<span id="A0"></span><span id="a0"></span>

**A0** (18)


</dt> <dd></dd> <dt>

<span id="A1"></span><span id="a1"></span>

**A1** (19)


</dt> <dd></dd> <dt>

<span id="A2"></span><span id="a2"></span>

**A2** (20)


</dt> <dd></dd> <dt>

<span id="A3"></span><span id="a3"></span>

**A3** (21)


</dt> <dd></dd> <dt>

<span id="A4"></span><span id="a4"></span>

**A4** (22)


</dt> <dd></dd> <dt>

<span id="A5"></span><span id="a5"></span>

**A5** (23)


</dt> <dd></dd> <dt>

<span id="A6"></span><span id="a6"></span>

**A6** (24)


</dt> <dd></dd> <dt>

<span id="A7"></span><span id="a7"></span>

**A7** (25)


</dt> <dd></dd> <dt>

<span id="A8"></span><span id="a8"></span>

**A8** (26)


</dt> <dd></dd> <dt>

<span id="A9A10"></span><span id="a9a10"></span>

**A9A10** (27)


</dt> <dd></dd> <dt>

<span id="B0"></span><span id="b0"></span>

**B0** (28)


</dt> <dd></dd> <dt>

<span id="B1"></span><span id="b1"></span>

**B1** (29)


</dt> <dd></dd> <dt>

<span id="B2"></span><span id="b2"></span>

**B2** (30)


</dt> <dd></dd> <dt>

<span id="B3"></span><span id="b3"></span>

**B3** (31)


</dt> <dd></dd> <dt>

<span id="B4"></span><span id="b4"></span>

**B4** (32)


</dt> <dd></dd> <dt>

<span id="B5"></span><span id="b5"></span>

**B5** (33)


</dt> <dd></dd> <dt>

<span id="B6"></span><span id="b6"></span>

**B6** (34)


</dt> <dd></dd> <dt>

<span id="B7"></span><span id="b7"></span>

**B7** (35)


</dt> <dd></dd> <dt>

<span id="B8"></span><span id="b8"></span>

**B8** (36)


</dt> <dd></dd> <dt>

<span id="B9"></span><span id="b9"></span>

**B9** (37)


</dt> <dd></dd> <dt>

<span id="B10"></span><span id="b10"></span>

**B10** (38)


</dt> <dd></dd> <dt>

<span id="C0"></span><span id="c0"></span>

**C0** (39)


</dt> <dd></dd> <dt>

<span id="C1"></span><span id="c1"></span>

**C1** (40)


</dt> <dd></dd> <dt>

<span id="C2C3"></span><span id="c2c3"></span>

**C2C3** (41)


</dt> <dd></dd> <dt>

<span id="C4"></span><span id="c4"></span>

**C4** (42)


</dt> <dd></dd> <dt>

<span id="C5"></span><span id="c5"></span>

**C5** (43)


</dt> <dd></dd> <dt>

<span id="C6"></span><span id="c6"></span>

**C6** (44)


</dt> <dd></dd> <dt>

<span id="C7"></span><span id="c7"></span>

**C7** (45)


</dt> <dd></dd> <dt>

<span id="C8"></span><span id="c8"></span>

**C8** (46)


</dt> <dd></dd> <dt>

<span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>

**DESIGNATO ISO** (47)


</dt> <dd></dd> <dt>

<span id="JIS_B0"></span><span id="jis_b0"></span>

**JIS B0** (48)


</dt> <dd></dd> <dt>

<span id="JIS_B1"></span><span id="jis_b1"></span>

**JIS B1** (49)


</dt> <dd></dd> <dt>

<span id="JIS_B2"></span><span id="jis_b2"></span>

**JIS B2** (50)


</dt> <dd></dd> <dt>

<span id="JIS_B3"></span><span id="jis_b3"></span>

**JIS B3** (51)


</dt> <dd></dd> <dt>

<span id="JIS_B4"></span><span id="jis_b4"></span>

**JIS B4** (52)


</dt> <dd></dd> <dt>

<span id="JIS_B5"></span><span id="jis_b5"></span>

**JIS B5** (53)


</dt> <dd></dd> <dt>

<span id="JIS_B6"></span><span id="jis_b6"></span>

**JIS B6** (54)


</dt> <dd></dd> <dt>

<span id="JIS_B7"></span><span id="jis_b7"></span>

**JIS B7** (55)


</dt> <dd></dd> <dt>

<span id="JIS_B8"></span><span id="jis_b8"></span>

**JIS B8** (56)


</dt> <dd></dd> <dt>

<span id="JIS_B9"></span><span id="jis_b9"></span>

**JIS B9** (57)


</dt> <dd></dd> <dt>

<span id="JIS_B10"></span><span id="jis_b10"></span>

**JIS B10** (58)


</dt> <dd></dd> <dt>

<span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>

**Na-Letter** (59)


</dt> <dd></dd> <dt>

<span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>

**NA-Legal** (60)


</dt> <dd></dd> <dt>

<span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>

**Busta B4** (61)


</dt> <dd></dd> <dt>

<span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>

**Busta B5** (62)


</dt> <dd></dd> <dt>

<span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>

**Busta C3** (63)


</dt> <dd></dd> <dt>

<span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>

**Busta C4** (64)


</dt> <dd></dd> <dt>

<span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>

**Busta C5** (65)


</dt> <dd></dd> <dt>

<span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>

**Busta C6** (66)


</dt> <dd></dd> <dt>

<span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>

**Designated-Long-Envelope** (67)


</dt> <dd></dd> <dt>

<span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>

**Busta-Monarca** (68)


</dt> <dd></dd> <dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

**Executive** (69)


</dt> <dd></dd> <dt>

<span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span>

**Folio** (70)


</dt> <dd></dd> <dt>

<span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>

**Fattura** (71)


</dt> <dd></dd> <dt>

<span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>

**Libro** mastro (72)


</dt> <dd></dd> <dt>

<span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>

**Quarto** (73)


</dt> <dd></dd> </dl>

</dd> <dt>

**PaperTypesAvailable**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob.RequiredPaperType", "CIM \_ PrintService.PaperTypesAvailable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Printer-MIB.prtInputMediaName")
</dt> </dl>

Stringhe in formato libero che specificano i tipi di carta attualmente disponibili per la stampante. Ogni stringa deve essere espressa nel formato specificato da ISO/IEC 10175 Document Printing Application (DPA), riepilogato anche nell'appendice C di RFC 1759 (Printer MIB). Esempi di stringhe valide sono "iso-a4-colored" e "na-10x14-envelope". Per definizione, un formato carta disponibile ed elencato nella **proprietà PaperTypesAvailable** dovrebbe essere visualizzato anche nella **proprietà PaperSizesSupported.**

</dd> <dt>

**PNPDeviceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")
</dt> </dl>

Win32 Plug and Play identificatore di dispositivo del dispositivo logico. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

Esempio: \* "PNP030b"

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

Il [**metodo SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato. Questo metodo si trova nella classe **CIM \_ LogicalDevice** padre e può essere implementato. Per altre informazioni, vedere [Progettazione di Managed Object Format (MOF).](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Alimentazione supportata** (6)


</dt> <dd>

Il [**metodo SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il *parametro PowerState* impostato su 5 (Ciclo di alimentazione).

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Accensione a tempo supportata** (7)


</dt> <dd>

Il [**metodo SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (Power Cycle) e *Time* impostato su una data e un'ora o un intervallo specifici per l'accensione.

</dd> </dl>

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **TRUE,** il dispositivo può essere gestito dall'alimentazione, vale a dire inserito in uno stato di risparmio energia. Se **FALSE,** il valore intero 1 ("Non supportato") deve essere l'unica voce nella matrice **PowerManagementCapabilities.**

Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o, se abilitate, quali funzionalità sono supportate. Per altre informazioni, vedere la matrice **PowerManagementCapabilities.** Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**PrinterStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Printer-MIB.hrPrinterStatus")
</dt> </dl>

Informazioni sullo stato, oltre a quella specificata nella **proprietà Availability,** per una stampante.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (2)


</dt> <dd></dd> <dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

**Inattivo** (3)


</dt> <dd></dd> <dt>

<span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>

**Stampa** (4)


</dt> <dd></dd> <dt>

<span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>

**Warmup** (5)


</dt> <dd></dd> <dt>

<span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>

**Stampa arrestata** (6)


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

**Offline** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Stato corrente dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

Sono inclusi i valori seguenti:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Errore** ("Errore")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degradato** ("Degraded")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** ("Sconosciuto")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred Fail** ("Pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Avvio** ("Avvio")


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

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Operational State \| 003.3")
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

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Sistema CIM \_**](cim-system.md).**CreationClassName**"), [**CHIAVE \_ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Nome della classe di creazione del sistema di definizione dell'ambito.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Sistema CIM \_**](cim-system.md).**Name**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Nome del sistema di definizione dell'ambito.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**TimeOfLastReset**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ora dell'ultima reimpostazione della stampante.

</dd> <dt>

**VerticalResolution**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob.HorizontalResolution"), [**Unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixel per pollice")
</dt> </dl>

Risoluzione verticale in pixel per pollice.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe CIM \_ Printer** è derivata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

WMI non implementa questa classe. Per la classe WMI derivata dalla **stampante CIM, \_** vedere [Classi Win32.](win32-provider.md)

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe aver apportato modifiche per correggere errori secondari, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.

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

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> </dl>

 


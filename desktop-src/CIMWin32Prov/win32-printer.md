---
description: Rappresenta un dispositivo connesso a un computer in esecuzione in un sistema operativo Microsoft Windows in grado di produrre un'immagine o un testo stampato su carta o altro supporto.
ms.assetid: 58090e6a-8f13-4859-adb8-a7c6299d3efd
ms.tgt_platform: multiple
title: Classe Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer
- Win32_Printer.Reset
- Win32_Printer.SetPowerState
- Win32_Printer.Attributes
- Win32_Printer.Availability
- Win32_Printer.AvailableJobSheets
- Win32_Printer.AveragePagesPerMinute
- Win32_Printer.Capabilities
- Win32_Printer.CapabilityDescriptions
- Win32_Printer.Caption
- Win32_Printer.CharSetsSupported
- Win32_Printer.Comment
- Win32_Printer.ConfigManagerErrorCode
- Win32_Printer.ConfigManagerUserConfig
- Win32_Printer.CreationClassName
- Win32_Printer.CurrentCapabilities
- Win32_Printer.CurrentCharSet
- Win32_Printer.CurrentLanguage
- Win32_Printer.CurrentMimeType
- Win32_Printer.CurrentNaturalLanguage
- Win32_Printer.CurrentPaperType
- Win32_Printer.Default
- Win32_Printer.DefaultCapabilities
- Win32_Printer.DefaultCopies
- Win32_Printer.DefaultLanguage
- Win32_Printer.DefaultMimeType
- Win32_Printer.DefaultNumberUp
- Win32_Printer.DefaultPaperType
- Win32_Printer.DefaultPriority
- Win32_Printer.Description
- Win32_Printer.DetectedErrorState
- Win32_Printer.DeviceID
- Win32_Printer.Direct
- Win32_Printer.DoCompleteFirst
- Win32_Printer.DriverName
- Win32_Printer.EnableBIDI
- Win32_Printer.EnableDevQueryPrint
- Win32_Printer.ErrorCleared
- Win32_Printer.ErrorDescription
- Win32_Printer.ErrorInformation
- Win32_Printer.ExtendedDetectedErrorState
- Win32_Printer.ExtendedPrinterStatus
- Win32_Printer.Hidden
- Win32_Printer.HorizontalResolution
- Win32_Printer.InstallDate
- Win32_Printer.JobCountSinceLastReset
- Win32_Printer.KeepPrintedJobs
- Win32_Printer.LanguagesSupported
- Win32_Printer.LastErrorCode
- Win32_Printer.Local
- Win32_Printer.Location
- Win32_Printer.MarkingTechnology
- Win32_Printer.MaxCopies
- Win32_Printer.MaxNumberUp
- Win32_Printer.MaxSizeSupported
- Win32_Printer.MimeTypesSupported
- Win32_Printer.Name
- Win32_Printer.NaturalLanguagesSupported
- Win32_Printer.Network
- Win32_Printer.PaperSizesSupported
- Win32_Printer.PaperTypesAvailable
- Win32_Printer.Parameters
- Win32_Printer.PNPDeviceID
- Win32_Printer.PortName
- Win32_Printer.PowerManagementCapabilities
- Win32_Printer.PowerManagementSupported
- Win32_Printer.PrinterPaperNames
- Win32_Printer.PrinterState
- Win32_Printer.PrinterStatus
- Win32_Printer.PrintJobDataType
- Win32_Printer.PrintProcessor
- Win32_Printer.Priority
- Win32_Printer.Published
- Win32_Printer.Queued
- Win32_Printer.RawOnly
- Win32_Printer.SeparatorFile
- Win32_Printer.ServerName
- Win32_Printer.Shared
- Win32_Printer.ShareName
- Win32_Printer.SpoolEnabled
- Win32_Printer.StartTime
- Win32_Printer.Status
- Win32_Printer.StatusInfo
- Win32_Printer.SystemCreationClassName
- Win32_Printer.SystemName
- Win32_Printer.TimeOfLastReset
- Win32_Printer.UntilTime
- Win32_Printer.VerticalResolution
- Win32_Printer.WorkOffline
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5f1a91ac90560343a38e546590005e8b984d13843eba8195381daa204e2d22cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077311"
---
# <a name="win32_printer-class"></a>Classe Printer Win32 \_

La classe [WMI](../wmisdk/retrieving-a-class.md) stampante **Win32 \_** rappresenta un dispositivo connesso a un computer in esecuzione in un sistema operativo Microsoft Windows in grado di produrre un'immagine stampata o un testo su carta o altro supporto.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
class Win32_Printer : CIM_Printer
{
  uint32   Attributes;
  uint16   Availability;
  string   AvailableJobSheets[];
  uint32   AveragePagesPerMinute;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  string   CharSetsSupported[];
  string   Comment;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint16   CurrentCapabilities[];
  string   CurrentCharSet;
  uint16   CurrentLanguage;
  string   CurrentMimeType;
  string   CurrentNaturalLanguage;
  string   CurrentPaperType;
  boolean  Default;
  uint16   DefaultCapabilities[];
  uint32   DefaultCopies;
  uint16   DefaultLanguage;
  string   DefaultMimeType;
  uint32   DefaultNumberUp;
  string   DefaultPaperType;
  uint32   DefaultPriority;
  string   Description;
  uint16   DetectedErrorState;
  string   DeviceID;
  boolean  Direct;
  boolean  DoCompleteFirst;
  string   DriverName;
  boolean  EnableBIDI;
  boolean  EnableDevQueryPrint;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorInformation[];
  uint16   ExtendedDetectedErrorState;
  uint16   ExtendedPrinterStatus;
  boolean  Hidden;
  uint32   HorizontalResolution;
  datetime InstallDate;
  uint32   JobCountSinceLastReset;
  boolean  KeepPrintedJobs;
  uint16   LanguagesSupported[];
  uint32   LastErrorCode;
  boolean  Local;
  string   Location;
  uint16   MarkingTechnology;
  uint32   MaxCopies;
  uint32   MaxNumberUp;
  uint32   MaxSizeSupported;
  string   MimeTypesSupported[];
  string   Name;
  string   NaturalLanguagesSupported[];
  boolean  Network;
  uint16   PaperSizesSupported[];
  string   PaperTypesAvailable[];
  string   Parameters;
  string   PNPDeviceID;
  string   PortName;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   PrinterPaperNames[];
  uint32   PrinterState;
  uint16   PrinterStatus;
  string   PrintJobDataType;
  string   PrintProcessor;
  uint32   Priority;
  boolean  Published;
  boolean  Queued;
  boolean  RawOnly;
  string   SeparatorFile;
  string   ServerName;
  boolean  Shared;
  string   ShareName;
  boolean  SpoolEnabled;
  datetime StartTime;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
  datetime UntilTime;
  uint32   VerticalResolution;
  boolean  WorkOffline;
};
```

## <a name="members"></a>Members

La **classe Win32 \_ Printer** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ Printer Win32** include questi metodi.



| Metodo                                                                               | Descrizione                                                                                                                                                                                                       |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddPrinterConnection**](addprinterconnection-method-in-class-win32-printer.md)   | Aggiunge una connessione alla stampante.<br/>                                                                                                                                                                      |
| [**CancelAllJobs**](cancelalljobs-method-in-class-win32-printer.md)                 | Annulla tutti i processi.<br/>                                                                                                                                                                                      |
| [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class-win32-printer.md) | Restituisce il descrittore di sicurezza che controlla l'accesso alla stampante.<br/>                                                                                                                                   |
| [**Sospendi**](pause-method-in-class-win32-printer.md)                                 | Mette in pausa la coda di stampa.<br/>                                                                                                                                                                                |
| [**PrintTestPage**](printtestpage-method-in-class-win32-printer.md)                 | Stampa una pagina di test.<br/>                                                                                                                                                                                    |
| [**RenamePrinter**](renameprinter-method-in-class-win32-printer.md)                 | Rinomina una stampante.<br/>                                                                                                                                                                                     |
| **Reimpostazione**                                                                            | Non implementato. Per altre informazioni su come implementare questo metodo, vedere il [**metodo Reset**](reset-method-in-class-cim-controller.md) nella [**stampante \_ CIM.**](cim-printer.md)<br/>                 |
| [**Riprendi**](resume-method-in-class-win32-printer.md)                               | Riprende la coda di stampa sospesa.<br/>                                                                                                                                                                            |
| [**SetDefaultPrinter**](setdefaultprinter-method-in-class-win32-printer.md)         | Imposta la stampante predefinita.<br/>                                                                                                                                                                              |
| **SetPowerState**                                                                    | Non implementato. Per altre informazioni su come implementare questo metodo, vedere il [**metodo SetPowerState**](setpowerstate-method-in-class-cim-controller.md) nella [**stampante \_ CIM.**](cim-printer.md)<br/> |
| [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class-win32-printer.md) | Scrive una versione aggiornata del descrittore di sicurezza che controlla l'accesso alla stampante.<br/>                                                                                                              |



 

### <a name="properties"></a>Proprietà

La **classe \_ Printer Win32** dispone di queste proprietà.

<dl> <dt>

**Attributes (Attributi)**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Mappa di bit degli attributi per Windows stampa basata su un dispositivo di stampa.

<dt>

<span id="PRINTER_ATTRIBUTE_QUEUED"></span><span id="printer_attribute_queued"></span>

<span id="PRINTER_ATTRIBUTE_QUEUED"></span><span id="printer_attribute_queued"></span>**STAMPANTE \_ ATTRIBUTE \_ QUEUED** (1 (0x1))


</dt> <dd>

Queued

I processi di stampa vengono memorizzati nel buffer e accodati.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_DIRECT"></span><span id="printer_attribute_direct"></span>

<span id="PRINTER_ATTRIBUTE_DIRECT"></span><span id="printer_attribute_direct"></span>**PRINTER \_ ATTRIBUTE \_ DIRECT** (2 (0x2))


</dt> <dd>

Connessione diretta

Documento da inviare direttamente alla stampante. Questo valore viene utilizzato se i processi di stampa non vengono accodati correttamente.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_DEFAULT"></span><span id="printer_attribute_default"></span>

<span id="PRINTER_ATTRIBUTE_DEFAULT"></span><span id="printer_attribute_default"></span>**PRINTER \_ ATTRIBUTE \_ DEFAULT** (4 (0x4))


</dt> <dd>

Predefinito

Stampante predefinita in un computer.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_SHARED"></span><span id="printer_attribute_shared"></span>

<span id="PRINTER_ATTRIBUTE_SHARED"></span><span id="printer_attribute_shared"></span>**PRINTER \_ ATTRIBUTE \_ SHARED** (8 (0x8))


</dt> <dd>

Condiviso

Disponibile come risorsa di rete condivisa.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_NETWORK"></span><span id="printer_attribute_network"></span>

<span id="PRINTER_ATTRIBUTE_NETWORK"></span><span id="printer_attribute_network"></span>**PRINTER \_ RETE \_ ATTRIBUTI** (16 (0x10))


</dt> <dd>

Rete

Collegato a una rete. Se sono impostati sia bit locali che di rete, ciò indica una stampante di rete.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_HIDDEN"></span><span id="printer_attribute_hidden"></span>

<span id="PRINTER_ATTRIBUTE_HIDDEN"></span><span id="printer_attribute_hidden"></span>**STAMPANTE \_ ATTRIBUTE \_ HIDDEN** (32 (0x20))


</dt> <dd>

Nascosto

Nascosto ad alcuni utenti della rete.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_LOCAL"></span><span id="printer_attribute_local"></span>

<span id="PRINTER_ATTRIBUTE_LOCAL"></span><span id="printer_attribute_local"></span>**PRINTER \_ ATTRIBUTE \_ LOCAL** (64 (0x40))


</dt> <dd>

Locale

Connessione diretta a un computer. Se sono impostati sia bit locali che di rete, ciò indica una stampante di rete.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_ENABLEDEVQ"></span><span id="printer_attribute_enabledevq"></span>

<span id="PRINTER_ATTRIBUTE_ENABLEDEVQ"></span><span id="printer_attribute_enabledevq"></span>**PRINTER \_ ATTRIBUTE \_ ENABLEDEVQ** (128 (0x80))


</dt> <dd>

EnableDevQ

Abilitare la coda sulla stampante, se disponibile.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_KEEPPRINTEDJOBS"></span><span id="printer_attribute_keepprintedjobs"></span>

<span id="PRINTER_ATTRIBUTE_KEEPPRINTEDJOBS"></span><span id="printer_attribute_keepprintedjobs"></span>**PRINTER \_ ATTRIBUTO \_ KEEPPRINTEDJOBS** (256 (0x100))


</dt> <dd>

KeepPrintedJobs

Lo spooler non deve eliminare i documenti dopo che sono stati stampati.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_DO_COMPLETE_FIRST"></span><span id="printer_attribute_do_complete_first"></span>

<span id="PRINTER_ATTRIBUTE_DO_COMPLETE_FIRST"></span><span id="printer_attribute_do_complete_first"></span>**PRINTER \_ ATTRIBUTE \_ DO \_ COMPLETE \_ FIRST** (512 (0x200))


</dt> <dd>

DoCompleteFirst

Avviare i processi che hanno terminato per primi lo spooling.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_WORK_OFFLINE"></span><span id="printer_attribute_work_offline"></span>

<span id="PRINTER_ATTRIBUTE_WORK_OFFLINE"></span><span id="printer_attribute_work_offline"></span>**PRINTER \_ ATTRIBUTE \_ WORK \_ OFFLINE** (1024 (0x400))


</dt> <dd>

WorkOffline

Accoda i processi di stampa quando una stampante non è disponibile.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_ENABLE_BIDI"></span><span id="printer_attribute_enable_bidi"></span>

<span id="PRINTER_ATTRIBUTE_ENABLE_BIDI"></span><span id="printer_attribute_enable_bidi"></span>**PRINTER \_ ATTRIBUTE \_ ENABLE \_ OFFERI** (2048 (0x800))


</dt> <dd>

EnableBIDI

Abilitare la stampa bidirezionale.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_RAW_ONLY"></span><span id="printer_attribute_raw_only"></span>

<span id="PRINTER_ATTRIBUTE_RAW_ONLY"></span><span id="printer_attribute_raw_only"></span>**PRINTER \_ SOLO \_ ATTRIBUTO \_ NON** ELABORATO (4096 (0x1000))


</dt> <dd>

Consente solo lo spooling dei processi con tipo di dati non elaborati.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_PUBLISHED"></span><span id="printer_attribute_published"></span>

<span id="PRINTER_ATTRIBUTE_PUBLISHED"></span><span id="printer_attribute_published"></span>**PRINTER \_ ATTRIBUTE \_ PUBLISHED** (8192 (0x2000))


</dt> <dd>

Pubblicato

Pubblicato nel servizio directory di rete.

</dd> </dl>

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

Il dispositivo è in stato di risparmio energia, ma è ancora funzionante e può presentare prestazioni ridotte.

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

**AvailableJobSheets**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob.RequiredJobSheets")
</dt> </dl>

Matrice di tutti i fogli di lavoro disponibili su una stampante. Può essere usato anche per descrivere il banner che una stampante può fornire all'inizio di ogni processo o altre opzioni specificate dall'utente.

Questa proprietà viene ereditata da [**CIM \_ Printer.**](cim-printer.md)

</dd> <dt>

**AveragePagesPerMinute**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Velocità di stampa, in numero medio di pagine al minuto, che una stampante può generare output.

</dd> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Printer**](cim-printer.md). CapabilityDescriptions", "CIM \_ PrintJob.Finishing", "CIM \_ PrintService.Capabilities")
</dt> </dl>

Matrice di funzionalità della stampante.

Questa proprietà viene ereditata da [**CIM \_ Printer.**](cim-printer.md)

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

One-Sided

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Bordo lungo a due lati** (13)


</dt> <dd>

Two-Sided Long Edge

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Bordo breve a due lati** (14)


</dt> <dd>

Two-Sided Short Edge

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


</dt> <dd></dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)


</dt> <dd></dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Qualità bassa** (21)


</dt> <dd></dd> </dl>

</dd> <dt>

**CapabilityDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Printer**](cim-printer.md).**Funzionalità di**")
</dt> </dl>

Matrice di stringhe in formato libero che forniscono spiegazioni dettagliate per le funzionalità della stampante indicate nella **matrice Capabilities.** Ogni voce di questa matrice è correlata a una voce nella matrice **Capabilities** che si trova nello stesso indice.

Questa proprietà viene ereditata da [**CIM \_ Printer.**](cim-printer.md)

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Breve descrizione di un oggetto, ovvero una stringa di una riga.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**CharSetsSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob.CharSet"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Printer-MIB.prtLocalizationCharacterSet")
</dt> </dl>

Matrice di set di caratteri disponibili per l'output. Le stringhe fornite in questa proprietà devono essere conformi alla semantica e alla sintassi specificate nella sezione 4.1.2 ("Parametri charset") in RFC 2046 (MIME parte 2) e contenute nel Registro di sistema dei set di caratteri IANA. Ad esempio, "UTF-8", "us-ASCII" e "iso-8859-1".

Questa proprietà viene ereditata da [**CIM \_ Printer.**](cim-printer.md)

</dd> <dt>

**Commento**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Commento per una coda di stampa.

Esempio: Stampante a colori

</dd> <dt>

**ConfigManagerErrorCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")
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

Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")
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

Qualificatori: [ **chiave \_ CIM**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata per creare un'istanza di . Se usata con altre proprietà chiave della classe , la proprietà consente l'identificazione univoca di tutte le istanze di questa classe e delle relative sottoclassi.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**CurrentCapabilities**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Printer**](cim-printer.md).**Funzionalità di**")
</dt> </dl>

Matrice di funzionalità della stampante attualmente in uso. Una voce in questa proprietà deve essere elencata anche nella **matrice Capabilities.**

Questa proprietà viene ereditata da [**CIM \_ Printer.**](cim-printer.md)

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

One-Sided

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Bordo lungo a due lati** (13)


</dt> <dd>

Two-Sided Long Edge

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Bordo breve a due lati** (14)


</dt> <dd>

Two-Sided short edge

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


</dt> <dd></dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)


</dt> <dd></dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Qualità bassa** (21)


</dt> <dd></dd> </dl>

</dd> <dt>

**CurrentCharSet**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Printer**](cim-printer.md).**CharSetsSupported**")
</dt> </dl>

Set di caratteri attualmente utilizzato per l'output. Le stringhe fornite in questa proprietà devono essere conformi alla semantica e alla sintassi specificate nella sezione 4.1.2 ("Parametri charset") in RFC 2046 (MIME parte 2) e contenute nel Registro di sistema dei set di caratteri IANA. Ad esempio, "utf-8", "us-ASCII" e iso-8859-1.

Questa proprietà viene ereditata da [**CIM \_ Printer.**](cim-printer.md)

</dd> <dt>

**CurrentLanguage**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Printer**](cim-printer.md). LanguagesSupported", "**CIM \_ Printer**.**CurrentMimeType**")
</dt> </dl>

Lingua della stampante attualmente utilizzata. La lingua usata deve essere elencata nella **proprietà LanguagesSupported.**

Questa proprietà viene ereditata da [**CIM \_ Printer.**](cim-printer.md)

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span id="PCL"></span><span id="pcl"></span>**PCL** (3)


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span id="PJL"></span><span id="pjl"></span>**PJL** (5)


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span id="PS"></span><span id="ps"></span>**PS** (6)


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span id="IPDS"></span><span id="ipds"></span>**IPDS** (8)


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpress** (13)


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Dati riga** (15)


</dt> <dd>

Dati riga

</dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span id="MODCA"></span><span id="modca"></span>**MODCA** (16)


</dt> <dd>

DODCA

</dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span id="REGIS"></span><span id="regis"></span>**REGIS** (17)


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span id="SCS"></span><span id="scs"></span>**SCS** (18)


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span id="PDS"></span><span id="pds"></span>**PDS** (21)


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span id="IGP"></span><span id="igp"></span>**IGP** (22)


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span id="WPS"></span><span id="wps"></span>**WPS** (25)


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span id="LN03"></span><span id="ln03"></span>**LN03** (26)


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span id="QUIC"></span><span id="quic"></span>**QUIC** (28)


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Testo semplice** (31)


</dt> <dd>

Simpletext

</dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span id="NPAP"></span><span id="npap"></span>**NPAP** (32)


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span id="DOC"></span><span id="doc"></span>**DOC** (33)


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**imPress** (34)


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatico** (38)


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Pagine** (39)


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span id="LIPS"></span><span id="lips"></span>**ROSSETTO** (40)


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostica** (42)


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**CaPSL** (43)


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span id="EXCL"></span><span id="excl"></span>**EXCL** (44)


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span id="LCDS"></span><span id="lcds"></span>**LCDS** (45)


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span id="XES"></span><span id="xes"></span>**XES** (46)


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span id="MIME"></span><span id="mime"></span>**MIME** (47)


</dt> <dd></dd> <dt>

48
</dt> <dd>

XPS

</dd> <dt>

49
</dt> <dd>

HPGL2

</dd> <dt>

50
</dt> <dd>

PCLXL

</dd> </dl>

</dd> <dt>

**CurrentMimeType**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Printer**](cim-printer.md).**CurrentLanguage**")
</dt> </dl>

Tipo MIME attualmente in uso se **CurrentLanguage** è un tipo MIME (valore = 47).

Questa proprietà viene ereditata dalla [**stampante CIM. \_**](cim-printer.md)

</dd> <dt>

**CurrentNaturalLanguage**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Printer**](cim-printer.md).**NaturalLanguagesSupported**")
</dt> </dl>

Lingua attualmente utilizzata dalla stampante per la gestione. La lingua elencata qui deve essere elencata anche nella **proprietà NaturalLanguagesSupported.**

Questa proprietà viene ereditata dalla [**stampante CIM. \_**](cim-printer.md)

</dd> <dt>

**CurrentPaperType**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Printer**](cim-printer.md).**PaperTypesAvailable**")
</dt> </dl>

Tipo di carta utilizzato dalla stampante. Deve essere espresso nel formato specificato da ISO/IEC 10175 Document Printing Application (DPA), riepilogato nell'appendice C di RFC 1759 (Printer MIB).

Questa proprietà viene ereditata dalla [**stampante CIM. \_**](cim-printer.md)

</dd> <dt>

**Default**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **TRUE,** la stampante è la stampante predefinita.

</dd> <dt>

**DefaultCapabilities**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Printer**](cim-printer.md).**Funzionalità**")
</dt> </dl>

Matrice delle funzionalità della stampante usate per impostazione predefinita. Ogni voce nella **matrice DefaultCapabilities** deve essere elencata anche nella matrice **Capabilities.**

Questa proprietà viene ereditata dalla [**stampante CIM. \_**](cim-printer.md)

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

One-Sided

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Long Edge a due** lati (13)


</dt> <dd>

Two-Sided Long Edge

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Short Edge a due lati** (14)


</dt> <dd>

Two-Sided Short Edge

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


</dt> <dd></dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Qualità normale** (20)


</dt> <dd></dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Qualità bassa** (21)


</dt> <dd></dd> </dl>

</dd> <dt>

**DefaultCopies**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di copie prodotte per un processo, se non diversamente specificato.

Questa proprietà viene ereditata dalla [**stampante CIM. \_**](cim-printer.md)

</dd> <dt>

**DefaultLanguage**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Printer**](cim-printer.md). LanguagesSupported", "**CIM \_ Printer**.**DefaultMimeType**")
</dt> </dl>

Lingua predefinita della stampante. La lingua elencata qui deve essere elencata anche nella **proprietà LanguagesSupported.**

Questa proprietà viene ereditata dalla [**stampante CIM. \_**](cim-printer.md)

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span id="PCL"></span><span id="pcl"></span>**PCL** (3)


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span id="PJL"></span><span id="pjl"></span>**PJL** (5)


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span id="PS"></span><span id="ps"></span>**PS** (6)


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span id="IPDS"></span><span id="ipds"></span>**IPDS** (8)


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpress** (13)


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Dati riga** (15)


</dt> <dd>

LineData

</dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span id="MODCA"></span><span id="modca"></span>**MODCA** (16)


</dt> <dd>

DODCA

</dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span id="REGIS"></span><span id="regis"></span>**REGIS** (17)


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span id="SCS"></span><span id="scs"></span>**SCS** (18)


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span id="PDS"></span><span id="pds"></span>**PDS** (21)


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span id="IGP"></span><span id="igp"></span>**IGP** (22)


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span id="WPS"></span><span id="wps"></span>**WPS** (25)


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span id="LN03"></span><span id="ln03"></span>**LN03** (26)


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span id="QUIC"></span><span id="quic"></span>**QUIC** (28)


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Testo semplice** (31)


</dt> <dd>

Simpletext

</dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span id="NPAP"></span><span id="npap"></span>**NPAP** (32)


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span id="DOC"></span><span id="doc"></span>**DOC** (33)


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**imPress** (34)


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatico** (38)


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Pagine** (39)


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span id="LIPS"></span><span id="lips"></span>**ROSSETTO** (40)


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostica** (42)


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**CaPSL** (43)


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span id="EXCL"></span><span id="excl"></span>**EXCL** (44)


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span id="LCDS"></span><span id="lcds"></span>**LCDS** (45)


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span id="XES"></span><span id="xes"></span>**XES** (46)


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span id="MIME"></span><span id="mime"></span>**MIME** (47)


</dt> <dd></dd> <dt>

48
</dt> <dd>

XPS

</dd> <dt>

49
</dt> <dd>

HPGL2

</dd> <dt>

50
</dt> <dd>

PCLXL

</dd> </dl>

</dd> <dt>

**DefaultMimeType**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Printer**](cim-printer.md).**DefaultLanguage**")
</dt> </dl>

Tipo MIME attualmente in uso, se il **valore DefaultLanguage** è un tipo MIME (valore = 47).

Questa proprietà viene ereditata dalla [**stampante CIM. \_**](cim-printer.md)

</dd> <dt>

**DefaultNumberUp**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di pagine del flusso di stampa di cui la stampante esegue il rendering su un foglio multimediale, a meno che un processo non specifichi diversamente.

Questa proprietà viene ereditata dalla [**stampante CIM. \_**](cim-printer.md)

</dd> <dt>

**DefaultPaperType**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Printer**](cim-printer.md).**PaperTypesAvailable**")
</dt> </dl>

Tipo di carta utilizzato dalla stampante, a meno che un processo di stampa non specifichi un tipo di carta diverso. La stringa deve essere espressa nel formato specificato da ISO/IEC 1017 Document Printing Application (DPA), riepilogato nell'appendice C di [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (Printer MIB).

Questa proprietà viene ereditata dalla [**stampante CIM. \_**](cim-printer.md)

</dd> <dt>

**DefaultPriority**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Valore di priorità predefinito assegnato a ogni processo di stampa.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Descrizione di un oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**DetectedErrorState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Printer**](cim-printer.md).**ErrorInformation**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Printer-MIB.hrPrinterDetectedErrorState")
</dt> </dl>

Informazioni sull'errore della stampante.

Questa proprietà viene ereditata dalla [**stampante CIM. \_**](cim-printer.md)

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

Qualificatori: [ **chiave \_ CIM**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Identificatore univoco della stampante in un sistema.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**Diretta**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Se **TRUE,** il processo di stampa viene inviato direttamente alla stampante. Se **FALSE,** il processo di stampa viene spoolato.

</dd> <dt>

**DoCompleteFirst**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Se **TRUE,** la stampante avvia i processi che hanno terminato lo spooling. Se **FALSE,** la stampante avvia i processi nell'ordine in cui vengono ricevuti.

</dd> <dt>

**DriverName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Nome del driver Windows stampante.

Esempio: Windows driver fax

</dd> <dt>

**EnableBIDI**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Se **TRUE,** la stampante può stampare in modo bidirezionale.

</dd> <dt>

**EnableDevQueryPrint**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Se **TRUE,** la stampante contiene i documenti nella coda quando le impostazioni di documenti e stampanti non corrispondono.

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **TRUE,** l'errore segnalato in **LastErrorCode** è stato cancellato.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che è possibile eseguire.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**ErrorInformation**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Printer**](cim-printer.md).**DetectedErrorState**")
</dt> </dl>

Matrice di informazioni supplementari per lo stato di errore corrente indicato in **DetectedErrorState.**

Questa proprietà viene ereditata dalla [**stampante CIM. \_**](cim-printer.md)

</dd> <dt>

**ExtendedDetectedErrorState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Segnala informazioni sugli errori standard. Informazioni aggiuntive devono essere registrate in **DetectedErrorState.**

I valori possibili sono:

<dt>

0 (0x0)
</dt> <dd>

Sconosciuto

</dd> <dt>

1 (0x1)
</dt> <dd>

Altro

</dd> <dt>

2 (0x2)
</dt> <dd>

Nessun errore

</dd> <dt>

3 (0x3)
</dt> <dd>

Carta in esaurimento

</dd> <dt>

4 (0x4)
</dt> <dd>

Carta esaurita

</dd> <dt>

5 (0x5)
</dt> <dd>

Toner insufficiente

</dd> <dt>

6 (0x6)
</dt> <dd>

Toner esaurito

</dd> <dt>

7 (0x7)
</dt> <dd>

Sportello aperto

</dd> <dt>

8 (0x8)
</dt> <dd>

Fogli bloccati

</dd> <dt>

9 (0x9)
</dt> <dd>

Necessaria manutenzione

</dd> <dt>

10 (0xA)
</dt> <dd>

Raccoglitore pieno

</dd> <dt>

11 (0xB)
</dt> <dd>

Problema relativo alla carta

</dd> <dt>

12 (0xC)
</dt> <dd>

Impossibile stampare la pagina

</dd> <dt>

13 (0xD)
</dt> <dd>

Intervento dell'utente obbligatorio

</dd> <dt>

14 (0xE)
</dt> <dd>

Memoria insufficiente

</dd> <dt>

15 (0xF)
</dt> <dd>

Server sconosciuto

</dd> </dl>

</dd> <dt>

**ExtendedPrinterStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Informazioni sullo stato per una stampante diverse dalle informazioni specificate nella **proprietà** Availability.

<dt>

1 (0x1)
</dt> <dd>

Altro

</dd> <dt>

2 (0x2)
</dt> <dd>

Sconosciuto

</dd> <dt>

3 (0x3)
</dt> <dd>

Idle

</dd> <dt>

4 (0x4)
</dt> <dd>

Stampa

</dd> <dt>

5 (0x5)
</dt> <dd>

Riscaldamento

</dd> <dt>

6 (0x6)
</dt> <dd>

Stampa arrestata

</dd> <dt>

7
</dt> <dd>

Offline

</dd> <dt>

8 (0x8)
</dt> <dd>

Paused

</dd> <dt>

9 (0x9)
</dt> <dd>

Errore

</dd> <dt>

10 (0xA)
</dt> <dd>

Busy

</dd> <dt>

11 (0xB)
</dt> <dd>

Non disponibile

</dd> <dt>

12 (0xC)
</dt> <dd>

Attesa

</dd> <dt>

13 (0xD)
</dt> <dd>

Elaborazione in corso

</dd> <dt>

14 (0xE)
</dt> <dd>

Inizializzazione

</dd> <dt>

15
</dt> <dd>

Risparmio energia

</dd> <dt>

16 (0x10)
</dt> <dd>

Eliminazione in sospeso

</dd> <dt>

17 (0x11)
</dt> <dd>

I/O attivo

</dd> <dt>

18 (0x12)
</dt> <dd>

Feed manuale

</dd> </dl>

</dd> <dt>

**Hidden**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Se **TRUE,** la stampante è nascosta agli utenti di rete.

</dd> <dt>

**HorizontalResolution**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob.HorizontalResolution"), [**Unità**](../wmisdk/standard-qualifiers.md) ("pixel per pollice")
</dt> </dl>

Risoluzione orizzontale della stampante, in pixel per pollice.

Questa proprietà viene ereditata da [**CIM \_ Printer.**](cim-printer.md)

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")
</dt> </dl>

Data e ora di installazione di un oggetto. L'oggetto può essere installato senza che venga scritto un valore in questa proprietà. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**JobCountSinceLastReset**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Counter**
</dt> </dl>

Numero di processi di stampa dall'ultima reimpostazione della stampante.

Questa proprietà viene ereditata da [**CIM \_ Printer.**](cim-printer.md)

</dd> <dt>

**KeepPrintedJobs**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Se **TRUE,** lo spooler di stampa non elimina i processi completati.

</dd> <dt>

**LanguagesSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Printer-MIB.prtInterpreterLangFamily"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Printer**](cim-printer.md). MimeTypesSupported", "CIM \_ PrintJob.Language", "CIM \_ PrintService.LanguagesSupported")
</dt> </dl>

Matrice delle lingue di stampa supportate in modo nativo.

Questa proprietà viene ereditata da [**CIM \_ Printer.**](cim-printer.md)

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span id="PCL"></span><span id="pcl"></span>**PCL** (3)


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span id="PJL"></span><span id="pjl"></span>**PJL** (5)


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span id="PS"></span><span id="ps"></span>**PS** (6)


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span id="IPDS"></span><span id="ipds"></span>**IPDS** (8)


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpress** (13)


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Dati riga** (15)


</dt> <dd>

Dati riga

</dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span id="MODCA"></span><span id="modca"></span>**MODCA** (16)


</dt> <dd>

DODCA

</dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span id="REGIS"></span><span id="regis"></span>**REGIS** (17)


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span id="SCS"></span><span id="scs"></span>**SCS** (18)


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span id="PDS"></span><span id="pds"></span>**PDS** (21)


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span id="IGP"></span><span id="igp"></span>**IGP** (22)


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span id="WPS"></span><span id="wps"></span>**WPS** (25)


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span id="LN03"></span><span id="ln03"></span>**LN03** (26)


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span id="QUIC"></span><span id="quic"></span>**QUIC** (28)


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Testo semplice** (31)


</dt> <dd>

Simpletext

</dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span id="NPAP"></span><span id="npap"></span>**NPAP** (32)


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span id="DOC"></span><span id="doc"></span>**DOC** (33)


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**imPress** (34)


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatico** (38)


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Pagine** (39)


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span id="LIPS"></span><span id="lips"></span>**EVASO** (40)


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostica** (42)


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**CaPSL** (43)


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span id="EXCL"></span><span id="excl"></span>**EXCL** (44)


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span id="LCDS"></span><span id="lcds"></span>**LCDS** (45)


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span id="XES"></span><span id="xes"></span>**XES** (46)


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span id="MIME"></span><span id="mime"></span>**MIME** (47)


</dt> <dd></dd> <dt>

<span id="XPS"></span><span id="xps"></span>

<span id="XPS"></span><span id="xps"></span>**XPS** (48)


</dt> <dd></dd> <dt>

<span id="HPGL2"></span><span id="hpgl2"></span>

<span id="HPGL2"></span><span id="hpgl2"></span>**HPGL2** (49)


</dt> <dd></dd> <dt>

<span id="PCLXL"></span><span id="pclxl"></span>

<span id="PCLXL"></span><span id="pclxl"></span>**PCLXL** (50)


</dt> <dd></dd> </dl>

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ultimo codice di errore riportato dal dispositivo logico.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**Locale**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Se **TRUE,** la stampante non è collegata a una rete. Se entrambe **le proprietà Local** e **Network** sono impostate su **TRUE,** la stampante è una stampante di rete.

</dd> <dt>

**Posizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Posizione fisica della stampante.

Esempio: Bldg. 38, Stanza 1164

</dd> <dt>

**MarkingTechnology**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Printer-MIB.prtMarkerMarkerMarkTech")
</dt> </dl>

Tecnologia di contrassegno utilizzata dalla stampante.

Questa proprietà viene ereditata dalla [**stampante CIM. \_**](cim-printer.md)

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

**Impatto Spostamento della matrice dei punti della testa a 9 punti** (6)


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

**Elettroerosione** (20)


</dt> <dd></dd> <dt>

<span id="Electrostatic"></span><span id="electrostatic"></span><span id="ELECTROSTATIC"></span>

**Elettrostatico** (21)


</dt> <dd></dd> <dt>

<span id="Photographic_Microfiche"></span><span id="photographic_microfiche"></span><span id="PHOTOGRAPHIC_MICROFICHE"></span>

**Microfiche fotografiche** (22)


</dt> <dd></dd> <dt>

<span id="Photographic_Imagesetter"></span><span id="photographic_imagesetter"></span><span id="PHOTOGRAPHIC_IMAGESETTER"></span>

**Imagesetter** (23)


</dt> <dd></dd> <dt>

<span id="Photographic_Other"></span><span id="photographic_other"></span><span id="PHOTOGRAPHIC_OTHER"></span>

**Altro fotografico** (24)


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

Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob.Copies")
</dt> </dl>

Numero massimo di copie che la stampante può produrre per un processo.

Questa proprietà viene ereditata dalla [**stampante CIM. \_**](cim-printer.md)

</dd> <dt>

**MaxNumberUp**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob.NumberUp")
</dt> </dl>

Numero massimo di pagine del flusso di stampa di cui la stampante può eseguire il rendering su un foglio multimediale, ad esempio la carta.

Questa proprietà viene ereditata dalla [**stampante CIM. \_**](cim-printer.md)

</dd> <dt>

**MaxSizeSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob.JobSize"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobyte")
</dt> </dl>

Processo più grande come flusso di byte, in kilobyte, che la stampante può accettare. Il valore 0 (zero) indica che non è impostato alcun limite.

Questa proprietà viene ereditata dalla [**stampante CIM. \_**](cim-printer.md)

</dd> <dt>

**MimeTypesSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Printer**](cim-printer.md). LanguagesSupported", "CIM \_ PrintJob.MimeTypes", "CIM \_ PrintService.MimeTypesSupported")
</dt> </dl>

Matrice di spiegazioni dettagliate di tipo MIME supportate dalla stampante. Se vengono forniti dati, il valore 47 ("MIME") deve essere incluso nella **proprietà LanguagesSupported.**

Questa proprietà viene ereditata dalla [**stampante CIM. \_**](cim-printer.md)

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")
</dt> </dl>

Nome della stampante.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**NaturalLanguagesSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indicizzato"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Printer-MIB.prtLocalizationLanguage"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob.NaturalLanguage")
</dt> </dl>

Matrice di linguaggi supportati per le stringhe utilizzate dalla stampante per l'output delle informazioni di gestione. Deve essere conforme [a RFC 1766](https://www.ietf.org/rfc/rfc1766.txt). Ad esempio, "en" viene usato per l'inglese.

Questa proprietà viene ereditata dalla [**stampante CIM. \_**](cim-printer.md)

</dd> <dt>

**Network**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Se **TRUE,** la stampante è una stampante di rete. Se entrambe **le proprietà Local** e **Network** sono impostate su **TRUE,** la stampante è una stampante di rete.

</dd> <dt>

**PaperSizesSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice dei tipi di carta supportati dalla stampante.

Questa proprietà viene ereditata dalla [**stampante CIM. \_**](cim-printer.md)

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)


</dt> <dd></dd> <dt>

<span id="A"></span><span id="a"></span>

<span id="A"></span><span id="a"></span>**A** (2)


</dt> <dd></dd> <dt>

<span id="B"></span><span id="b"></span>

<span id="B"></span><span id="b"></span>**B** (3)


</dt> <dd></dd> <dt>

<span id="C"></span><span id="c"></span>

<span id="C"></span><span id="c"></span>**C** (4)


</dt> <dd></dd> <dt>

<span id="D"></span><span id="d"></span>

<span id="D"></span><span id="d"></span>**D** (5)


</dt> <dd></dd> <dt>

<span id="E"></span><span id="e"></span>

<span id="E"></span><span id="e"></span>**E** (6)


</dt> <dd></dd> <dt>

<span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>

<span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>**Lettera** (7)


</dt> <dd></dd> <dt>

<span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>

<span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>**Legale** (8)


</dt> <dd></dd> <dt>

<span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>

<span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>**NA-10x13-Envelope** (9)


</dt> <dd></dd> <dt>

<span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>

<span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>**Na-9x12-Envelope** (10)


</dt> <dd></dd> <dt>

<span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>

<span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>**NA-Number-10-Envelope** (11)


</dt> <dd></dd> <dt>

<span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>

<span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>**NA-7x9-Envelope** (12)


</dt> <dd></dd> <dt>

<span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>

<span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>**NA-9x11-Envelope** (13)


</dt> <dd></dd> <dt>

<span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>

<span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>**Na-10x14-Envelope** (14)


</dt> <dd></dd> <dt>

<span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>

<span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>**NA-Number-9-Envelope** (15)


</dt> <dd></dd> <dt>

<span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>

<span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>**NA-6x9-Envelope** (16)


</dt> <dd></dd> <dt>

<span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>

<span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>**Na-10x15-Envelope** (17)


</dt> <dd></dd> <dt>

<span id="A0"></span><span id="a0"></span>

<span id="A0"></span><span id="a0"></span>**A0** (18)


</dt> <dd></dd> <dt>

<span id="A1"></span><span id="a1"></span>

<span id="A1"></span><span id="a1"></span>**A1** (19)


</dt> <dd></dd> <dt>

<span id="A2"></span><span id="a2"></span>

<span id="A2"></span><span id="a2"></span>**A2** (20)


</dt> <dd></dd> <dt>

<span id="A3"></span><span id="a3"></span>

<span id="A3"></span><span id="a3"></span>**A3** (21)


</dt> <dd></dd> <dt>

<span id="A4"></span><span id="a4"></span>

<span id="A4"></span><span id="a4"></span>**A4** (22)


</dt> <dd></dd> <dt>

<span id="A5"></span><span id="a5"></span>

<span id="A5"></span><span id="a5"></span>**A5** (23)


</dt> <dd></dd> <dt>

<span id="A6"></span><span id="a6"></span>

<span id="A6"></span><span id="a6"></span>**A6** (24)


</dt> <dd></dd> <dt>

<span id="A7"></span><span id="a7"></span>

<span id="A7"></span><span id="a7"></span>**A7** (25)


</dt> <dd></dd> <dt>

<span id="A8"></span><span id="a8"></span>

<span id="A8"></span><span id="a8"></span>**A8** (26)


</dt> <dd></dd> <dt>

<span id="A9A10"></span><span id="a9a10"></span>

<span id="A9A10"></span><span id="a9a10"></span>**A9A10** (27)


</dt> <dd></dd> <dt>

<span id="B0"></span><span id="b0"></span>

<span id="B0"></span><span id="b0"></span>**B0** (28)


</dt> <dd></dd> <dt>

<span id="B1"></span><span id="b1"></span>

<span id="B1"></span><span id="b1"></span>**B1** (29)


</dt> <dd></dd> <dt>

<span id="B2"></span><span id="b2"></span>

<span id="B2"></span><span id="b2"></span>**B2** (30)


</dt> <dd></dd> <dt>

<span id="B3"></span><span id="b3"></span>

<span id="B3"></span><span id="b3"></span>**B3** (31)


</dt> <dd></dd> <dt>

<span id="B4"></span><span id="b4"></span>

<span id="B4"></span><span id="b4"></span>**B4** (32)


</dt> <dd></dd> <dt>

<span id="B5"></span><span id="b5"></span>

<span id="B5"></span><span id="b5"></span>**B5** (33)


</dt> <dd></dd> <dt>

<span id="B6"></span><span id="b6"></span>

<span id="B6"></span><span id="b6"></span>**B6** (34)


</dt> <dd></dd> <dt>

<span id="B7"></span><span id="b7"></span>

<span id="B7"></span><span id="b7"></span>**B7** (35)


</dt> <dd></dd> <dt>

<span id="B8"></span><span id="b8"></span>

<span id="B8"></span><span id="b8"></span>**B8** (36)


</dt> <dd></dd> <dt>

<span id="B9"></span><span id="b9"></span>

<span id="B9"></span><span id="b9"></span>**B9** (37)


</dt> <dd></dd> <dt>

<span id="B10"></span><span id="b10"></span>

<span id="B10"></span><span id="b10"></span>**B10** (38)


</dt> <dd></dd> <dt>

<span id="C0"></span><span id="c0"></span>

<span id="C0"></span><span id="c0"></span>**C0** (39)


</dt> <dd></dd> <dt>

<span id="C1"></span><span id="c1"></span>

<span id="C1"></span><span id="c1"></span>**C1** (40)


</dt> <dd></dd> <dt>

<span id="C2C3"></span><span id="c2c3"></span>

<span id="C2C3"></span><span id="c2c3"></span>**C2C3** (41)


</dt> <dd>

C2

</dd> <dt>

<span id="C4"></span><span id="c4"></span>

<span id="C4"></span><span id="c4"></span>**C4** (42)


</dt> <dd>

C3

</dd> <dt>

<span id="C5"></span><span id="c5"></span>

<span id="C5"></span><span id="c5"></span>**C5** (43)


</dt> <dd>

C4

</dd> <dt>

<span id="C6"></span><span id="c6"></span>

<span id="C6"></span><span id="c6"></span>**C6** (44)


</dt> <dd>

C5

</dd> <dt>

<span id="C7"></span><span id="c7"></span>

<span id="C7"></span><span id="c7"></span>**C7** (45)


</dt> <dd>

C6

</dd> <dt>

<span id="C8"></span><span id="c8"></span>

<span id="C8"></span><span id="c8"></span>**C8** (46)


</dt> <dd>

C7

</dd> <dt>

<span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>

<span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>**Designato da ISO** (47)


</dt> <dd>

C8

</dd> <dt>

<span id="JIS_B0"></span><span id="jis_b0"></span>

<span id="JIS_B0"></span><span id="jis_b0"></span>**JIS B0** (48)


</dt> <dd>

ISO-Designated

</dd> <dt>

<span id="JIS_B1"></span><span id="jis_b1"></span>

<span id="JIS_B1"></span><span id="jis_b1"></span>**JIS B1** (49)


</dt> <dd>

JIS B0

</dd> <dt>

<span id="JIS_B2"></span><span id="jis_b2"></span>

<span id="JIS_B2"></span><span id="jis_b2"></span>**JIS B2** (50)


</dt> <dd>

JIS B1

</dd> <dt>

<span id="JIS_B3"></span><span id="jis_b3"></span>

<span id="JIS_B3"></span><span id="jis_b3"></span>**JIS B3** (51)


</dt> <dd>

JIS B2

</dd> <dt>

<span id="JIS_B4"></span><span id="jis_b4"></span>

<span id="JIS_B4"></span><span id="jis_b4"></span>**JIS B4** (52)


</dt> <dd>

JIS B3

</dd> <dt>

<span id="JIS_B5"></span><span id="jis_b5"></span>

<span id="JIS_B5"></span><span id="jis_b5"></span>**JIS B5** (53)


</dt> <dd>

JIS B4

</dd> <dt>

<span id="JIS_B6"></span><span id="jis_b6"></span>

<span id="JIS_B6"></span><span id="jis_b6"></span>**JIS B6** (54)


</dt> <dd>

JIS B5

</dd> <dt>

<span id="JIS_B7"></span><span id="jis_b7"></span>

<span id="JIS_B7"></span><span id="jis_b7"></span>**JIS B7** (55)


</dt> <dd>

JIS B6

</dd> <dt>

<span id="JIS_B8"></span><span id="jis_b8"></span>

<span id="JIS_B8"></span><span id="jis_b8"></span>**JIS B8** (56)


</dt> <dd>

JIS B7

</dd> <dt>

<span id="JIS_B9"></span><span id="jis_b9"></span>

<span id="JIS_B9"></span><span id="jis_b9"></span>**JIS B9** (57)


</dt> <dd>

JIS B8

</dd> <dt>

<span id="JIS_B10"></span><span id="jis_b10"></span>

<span id="JIS_B10"></span><span id="jis_b10"></span>**JIS B10** (58)


</dt> <dd>

JIS B9

</dd> <dt>

<span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>

<span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>**Na-Letter** (59)


</dt> <dd>

JIS B10

</dd> <dt>

<span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>

<span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>**NA-Legal** (60)


</dt> <dd></dd> <dt>

<span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>

<span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>**Busta B4** (61)


</dt> <dd></dd> <dt>

<span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>

<span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>**Busta B5** (62)


</dt> <dd></dd> <dt>

<span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>

<span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>**Busta C3** (63)


</dt> <dd></dd> <dt>

<span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>

<span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>**Busta C4** (64)


</dt> <dd></dd> <dt>

<span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>

<span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>**Busta C5** (65)


</dt> <dd></dd> <dt>

<span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>

<span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>**Busta C6** (66)


</dt> <dd></dd> <dt>

<span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>

<span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>**Designated-Long-Envelope** (67)


</dt> <dd></dd> <dt>

<span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>

<span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>**Busta-Monarca** (68)


</dt> <dd></dd> <dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executive** (69)


</dt> <dd></dd> <dt>

<span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span>

<span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span>**Folio** (70)


</dt> <dd></dd> <dt>

<span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>

<span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>**Fattura** (71)


</dt> <dd></dd> <dt>

<span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>

<span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>**Libro** mastro (72)


</dt> <dd></dd> <dt>

<span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>

<span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>**Quarto** (73)


</dt> <dd></dd> </dl>

</dd> <dt>

**PaperTypesAvailable**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob.RequiredPaperType", "CIM \_ PrintService.PaperTypesAvailable"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Printer-MIB.prtInputMediaName")
</dt> </dl>

Matrice di tipi di carta attualmente disponibili nella stampante. Ogni stringa deve essere espressa nel formato specificato da ISO/IEC 10175 Document Printing Application (DPA), riepilogato nell'appendice C di [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (Printer MIB). Qualsiasi formato di carta identificato in questa proprietà deve essere visualizzato anche nella **proprietà PaperSizesSupported.**

Questa proprietà viene ereditata dalla [**stampante CIM. \_**](cim-printer.md)

Esempio: iso-a4-colored

</dd> <dt>

**Parametri**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Parametri facoltativi per il processore di stampa.

Esempio: "Copies=2"

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

Esempio: \* PNP030b

</dd> <dt>

**PortName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Porta utilizzata per trasmettere dati a una stampante. Se una stampante è connessa a più porte, i nomi di ogni porta sono separati da virgole.

Esempio: LPT1:, LPT2:, LPT3:

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

Se **TRUE,** la potenza del dispositivo può essere gestita, ovvero può essere attivata la modalità di sospensione. La proprietà non indica che le funzionalità di risparmio energia sono abilitate, ma solo che il dispositivo logico è in grado di eseguire il risparmio energia.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**PrinterPaperNames**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di formati di carta supportati dalla stampante. I nomi specificati dalla stampante vengono usati per rappresentare i formati di carta supportati.

Esempio: B5 (JIS)

</dd> <dt>

**PrinterState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **deprecati**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Uno dei possibili stati relativi a questa stampante. Questa proprietà è obsoleta. Al posto di questa proprietà, usare **PrinterStatus**.

<dt>

0
</dt> <dd>

Inattivo: per altre informazioni, vedere la sezione Osservazioni riportata di seguito.

</dd> <dt>

1
</dt> <dd>

Paused

</dd> <dt>

2
</dt> <dd>

Errore

</dd> <dt>

3
</dt> <dd>

Eliminazione in sospeso

</dd> <dt>

4
</dt> <dd>

Inceppamento

</dd> <dt>

5
</dt> <dd>

Paper Out

</dd> <dt>

6
</dt> <dd>

Feed manuale

</dd> <dt>

7
</dt> <dd>

Problema di carta

</dd> <dt>

8
</dt> <dd>

Offline

</dd> <dt>

9
</dt> <dd>

I/O attivo

</dd> <dt>

10
</dt> <dd>

Busy

</dd> <dt>

11
</dt> <dd>

Stampa

</dd> <dt>

12
</dt> <dd>

Raccoglitore pieno

</dd> <dt>

13
</dt> <dd>

Non disponibile

</dd> <dt>

14
</dt> <dd>

Attesa

</dd> <dt>

15
</dt> <dd>

Elaborazione in corso

</dd> <dt>

16
</dt> <dd>

Inizializzazione

</dd> <dt>

17
</dt> <dd>

Riscaldamento

</dd> <dt>

18
</dt> <dd>

Toner basso

</dd> <dt>

19
</dt> <dd>

Toner esaurito

</dd> <dt>

20
</dt> <dd>

Pagina Punt

</dd> <dt>

21
</dt> <dd>

Intervento dell'utente obbligatorio

</dd> <dt>

22
</dt> <dd>

Memoria insufficiente

</dd> <dt>

23
</dt> <dd>

Sportello aperto

</dd> <dt>

24
</dt> <dd>

Server \_ sconosciuto

</dd> <dt>

25
</dt> <dd>

Risparmio energia

</dd> </dl>

</dd> <dt>

**Stato stampante**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Printer-MIB.hrPrinterStatus")
</dt> </dl>

Informazioni sullo stato per una stampante diverse dalle informazioni specificate nella proprietà Availability del **dispositivo** logico.

Questa proprietà viene ereditata da [**CIM \_ Printer.**](cim-printer.md)

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)


</dt> <dd></dd> <dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Inattivo** (3)


</dt> <dd>

Inattivo: per altre informazioni, vedere la sezione Osservazioni più avanti.

</dd> <dt>

<span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>

<span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>**Stampa** (4)


</dt> <dd></dd> <dt>

<span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>

<span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>**Riscaldamento** (5)


</dt> <dd>

Riscaldamento

</dd> <dt>

<span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>

<span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>**Stampa arrestata** (6)


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**PrintJobDataType**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Tipo di dati di un processo di stampa in attesa del Windows di stampa basato sul dispositivo.

</dd> <dt>

**Printprocessor**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Nome dello spooler di stampa che gestisce i processi di stampa.

Esempio: SPOOLSS.DLL

</dd> <dt>

**Priorità**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Priorità della stampante. I processi con una stampante con priorità più alta vengono pianificati per primi.

</dd> <dt>

**Pubblicato**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Se **TRUE,** la stampante viene pubblicata nel servizio directory di rete.

</dd> <dt>

**Queued**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Se **TRUE,** la stampante accoda e accoda i processi di stampa.

</dd> <dt>

**RawOnly**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Se **TRUE,** la stampante accetta solo dati non elaborati di cui eseguire lo spooling.

</dd> <dt>

**SeparatorFile**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Nome del file utilizzato per creare una pagina separatore. Questa pagina viene utilizzata per separare i processi di stampa inviati alla stampante.

</dd> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del server che controlla la stampante. Se questa stringa è **NULL,** la stampante viene controllata in locale.

</dd> <dt>

**Condivisa**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Se **TRUE,** la stampante è disponibile come risorsa di rete condivisa.

</dd> <dt>

**ShareName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Nome della condivisione del Windows di stampa basato sul dispositivo.

Esempio: " \\ \\ PRINTSERVER1 \\ PRINTER2"

</dd> <dt>

**SpoolEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **deprecati**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Questa proprietà è obsoleta. non utilizzare . Se **TRUE,** lo spooling è abilitato per la stampante.

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Data e ora in cui una stampante può iniziare a stampare un processo, se la stampa è limitata a orari specifici. Questo valore è espresso come tempo trascorso dalle 12:00 GMT (Ora di Greenwich).

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Stato corrente dell'oggetto. È possibile definire vari stati operativi e non operativi. Gli stati operativi includono: **OK,** **Degraded** e **Pred Fail** (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente ma prevedere un errore nel prossimo futuro). Gli stati nonoperational includono: **Error,** **Starting,** **Stopping** e **Service.** Quest'ultimo, **Il servizio**, può essere applicato durante il ridimensionamento del mirror di un disco, il ricaricamento di un elenco di autorizzazioni utente o altro lavoro amministrativo. Non tutte queste operazioni sono online, ma l'elemento gestito non è **ok** né in uno degli altri stati.

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

Stato del dispositivo logico. Se questa proprietà non è applicabile al dispositivo logico, è necessario usare il valore 5 (**Non** applicabile ).

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

**TimeOfLastReset**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora dell'ultima reimpostazione della stampante.

Questa proprietà viene ereditata da [**CIM \_ Printer.**](cim-printer.md)

</dd> <dt>

**UntilTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Data e ora in cui una stampante può stampare l'ultimo processo, se la stampa è limitata a orari specifici. Questo valore è espresso come tempo trascorso dalle 12:00 GMT (Ora di Greenwich).

</dd> <dt>

**VerticalResolution**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob.HorizontalResolution"), [**Unità**](../wmisdk/standard-qualifiers.md) ("pixel per pollice")
</dt> </dl>

Risoluzione verticale, in pixel per pollice, della stampante.

Questa proprietà viene ereditata da [**CIM \_ Printer.**](cim-printer.md)

</dd> <dt>

**WorkOffline**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Se **TRUE,** è possibile accoda i processi di stampa nel computer quando la stampante è offline.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ Printer Win32** è derivata da [**CIM \_ Printer.**](cim-printer.md) Prima di chiamare [**SWbemObject.Put \_**](../wmisdk/swbemobject-put-.md) o [**IWbemServices::P utInstance**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-putinstance) per un'istanza di **stampante Win32, \_** è necessario che sia abilitato il privilegio **SeLoadDriverPrivilege** (**wbemPrivilegeLoadDriver** per Visual Basic e LoadDriver per i moniker di scripting). Per altre informazioni, vedere [**Costanti di privilegi ed**](../wmisdk/privilege-constants.md) Esecuzione di operazioni con [privilegi.](../wmisdk/executing-privileged-operations.md) L'esempio di codice VBScript seguente illustra come abilitare il **privilegio SetLoadDriverPrivilege** nello script.

Per l'utilizzo dei cluster della stampante MSCS, usare l'assembly prnadmin.dll oppure lo spazio dei nomi [.NET Framework System.Printing.](/dotnet/api/system.printing)


```VB
Set objPrinter = GetObject("winmgmts:{impersonationLevel=Impersonate,(LoadDriver)}!//./Root/CIMv2:Win32_Printer")
```



Windows usa le credenziali dell'utente che esegue lo script per determinare quali sono le stampanti disponibili. Pertanto, se si esegue uno script in modalità remota, potrebbe essere possibile accedere solo a qualsiasi stampante disponibile per l'account utente in tale sistema remoto.

Non è possibile usare la **classe \_ Printer Win32** per le stampanti in un cluster di stampa MSCS. Potrebbe invece essere necessario usare lo strumento PrinterAdmin (PrnAdmin.dll) o lo .NET Framework [system.Printing.](/dotnet/api/system.printing)

> [!Note]  
> Se si recupera **PrinterStatus** = 3 o **PrinterState** = 0, il driver della stampante potrebbe non fornire informazioni accurate in WMI. WMI recupera le informazioni della stampante dal spoolsv.exe processo. È possibile che il driver della stampante non ne segnala lo stato allo spooler. In questo caso, **la stampante Win32 \_** segnala la stampante come **inattiva.**

 

## <a name="examples"></a>Esempio

L'esempio ps create [a Computer Configuration Drawing using Visio](https://Gallery.TechNet.Microsoft.Com/84e2c31a-e644-4f79-83cd-e2b1a0ef8557) PowerShell nella raccolta TechNet usa la stampante **Win32 \_** per interagire con il modello di automazione di Visio per creare un disegno Visio.

PowerShell [Remote PC Info Script](https://Gallery.TechNet.Microsoft.Com/2a8a008c-ee30-4b50-a81a-1b7545ef3436) usa diverse classi, tra cui **Win32 \_ Printer,** per recuperare informazioni su un computer remoto.

L'esempio di codice di PowerShell seguente illustra come determinare la stampante predefinita del computer locale.


```PowerShell
Get-WmiObject win32_printer | %{if ($_.default) {$_}}
```



Nell'esempio di codice VBScript seguente viene descritto come recuperare le statistiche della stampante dalle istanze di **Win32 \_ Printer.**


```VB
Set PrinterSet = GetObject("winmgmts:").InstancesOf ("Win32_Printer")
If (PrinterSet.Count = 0 ) Then WScript.Echo "No Printers Installed!"
for each Printer in PrinterSet
   if Printer.PrinterStatus = 3 then WScript.Echo Printer.Name & Chr(13) & "Status:  Idle"
   if Printer.PrinterStatus = 4 then WScript.Echo Printer.Name & Chr(13) & "Status:  Printing"
   
next
```



L'esempio di codice Perl seguente descrive come recuperare le statistiche della stampante dalle istanze di **Win32 \_ Printer.**


```
use strict;
use Win32::OLE;

my $PrinterSet;

eval { $PrinterSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
   InstancesOf ("Win32_Printer"); };
unless($@)
{
   if ($PrinterSet->{Count} == 0) 
   {
      print "No Printers Installed!\n";
   }

   foreach my $PrinterInst (in $PrinterSet)
   {
      if ($PrinterInst->{PrinterStatus} == 3) 
      {
         print "\n$PrinterInst->{Name}\nStatus:  Idle\n";
      }
      if ($PrinterInst->{PrinterStatus} == 4) 
      {
         print "\n$PrinterInst->{Name}\nStatus:  Printing\n";
      }
   }
}
else
{
   print STDERR Win32::OLE->LastError, "\n";
}
```



Nell'esempio di codice VBScript seguente viene illustrato come ottenere il nome della stampante predefinita per un computer.


```VB
strComputer = "."
Set objWMIService = GetObject( "winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colInstalledPrinters =  objWMIService.ExecQuery ("Select * from Win32_Printer")
For Each objPrinter in colInstalledPrinters

    If objPrinter.Default = "True" Then 
      Wscript.Echo "Name: " & objPrinter.Name
    End If
Next
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                      |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Stampante \_ CIM**](cim-printer.md)
</dt> <dt>

[Classi hardware del sistema computer](computer-system-hardware-classes.md)
</dt> <dt>

[Attività WMI: Stampanti e stampa](../wmisdk/wmi-tasks--printers-and-printing.md)
</dt> </dl>

 

 

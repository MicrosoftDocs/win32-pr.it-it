---
title: Classe Win32_TerminalService
description: Sottoclasse della classe del servizio \_ Win32. TerminalService Win32 \_ rappresenta la proprietà Element dell'associazione \_ TerminalServiceToSetting Win32.
ms.assetid: 06c69d71-4e6f-48af-b13d-e593b8fcf376
ms.tgt_platform: multiple
keywords:
- Win32_TerminalService classe Servizi Desktop remoto
- Win32_TerminalService classe Servizi Desktop remoto , descritta
topic_type:
- apiref
api_name:
- Win32_TerminalService
- Win32_TerminalService.AcceptPause
- Win32_TerminalService.AcceptStop
- Win32_TerminalService.Caption
- Win32_TerminalService.CheckPoint
- Win32_TerminalService.CreationClassName
- Win32_TerminalService.DelayedAutoStart
- Win32_TerminalService.Description
- Win32_TerminalService.DesktopInteract
- Win32_TerminalService.DisplayName
- Win32_TerminalService.ErrorControl
- Win32_TerminalService.ExitCode
- Win32_TerminalService.InstallDate
- Win32_TerminalService.Name
- Win32_TerminalService.PathName
- Win32_TerminalService.ProcessId
- Win32_TerminalService.ServiceSpecificExitCode
- Win32_TerminalService.ServiceType
- Win32_TerminalService.Started
- Win32_TerminalService.StartMode
- Win32_TerminalService.StartName
- Win32_TerminalService.State
- Win32_TerminalService.Status
- Win32_TerminalService.SystemCreationClassName
- Win32_TerminalService.SystemName
- Win32_TerminalService.TagId
- Win32_TerminalService.WaitHint
- Win32_TerminalService.DisconnectedSessions
- Win32_TerminalService.TotalSessions
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 735b033017958816e8e9a40caea935847104fdcbe3e9acf3128890d88685d09e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867851"
---
# <a name="win32_terminalservice-class"></a>Classe TerminalService Win32 \_

La classe WMI **\_ TerminalService Win32** è una sottoclasse della [**classe Del \_ servizio Win32.**](/windows/desktop/CIMWin32Prov/win32-service) **Win32 \_ TerminalService rappresenta** la **proprietà Element** dell'associazione [**\_ TerminalServiceToSetting Win32.**](win32-terminalservicetosetting.md)

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà definite ed ereditate, in ordine alfabetico.

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("Win32_WIN32_TERMINALSERVICE_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TerminalService : Win32_Service
{
  boolean  AcceptPause;
  boolean  AcceptStop;
  string   Caption;
  uint32   CheckPoint;
  string   CreationClassName;
  boolean  DelayedAutoStart;
  string   Description;
  boolean  DesktopInteract;
  string   DisplayName;
  string   ErrorControl;
  uint32   ExitCode;
  datetime InstallDate;
  string   Name;
  string   PathName;
  uint32   ProcessId;
  uint32   ServiceSpecificExitCode;
  string   ServiceType;
  boolean  Started;
  string   StartMode;
  string   StartName;
  string   State;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   TagId;
  uint32   WaitHint;
  uint32   DisconnectedSessions;
  uint32   TotalSessions;
};
```

## <a name="members"></a>Members

La **classe \_ TerminalService Win32** include questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ TerminalService Win32** include questi metodi.



| Metodo                                                                       | Descrizione                                                                                          |
|:-----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**Cambiare**](win32-terminalservice-change.md)                               | Modifica un servizio.<br/>                                                                       |
| [**ChangeStartMode**](win32-terminalservice-changestartmode.md)             | Modifica la modalità di avvio di un servizio.<br/>                                                     |
| [**Crea**](win32-terminalservice-create.md)                               | Crea un nuovo servizio.<br/>                                                                    |
| [**Elimina**](win32-terminalservice-delete.md)                               | Elimina un servizio esistente.<br/>                                                              |
| [**GetSecurityDescriptor**](win32-terminalservice-getsecuritydescriptor.md) | Restituisce il descrittore di sicurezza che controlla l'accesso al servizio.<br/>                      |
| [**InterrogaeService**](win32-terminalservice-interrogateservice.md)       | Richiede che un servizio aggiornerne lo stato a Service Manager.<br/>                          |
| [**PauseService**](win32-terminalservice-pauseservice.md)                   | Tenta di mettere un servizio nello stato sospeso.<br/>                                          |
| [**ResumeService**](win32-terminalservice-resumeservice.md)                 | Tenta di impostare un servizio nello stato ripreso.<br/>                                         |
| [**SetSecurityDescriptor**](win32-terminalservice-setsecuritydescriptor.md) | Scrive una versione aggiornata del descrittore di sicurezza che controlla l'accesso al servizio.<br/> |
| [**Startservice**](win32-terminalservice-startservice.md)                   | Tenta di impostare un servizio sullo stato di avvio.<br/>                                       |
| [**StopService**](win32-terminalservice-stopservice.md)                     | Inserisce un servizio nello stato arrestato.<br/>                                                    |
| [**UserControlService**](win32-terminalservice-usercontrolservice.md)       | Tenta di inviare un codice di controllo definito dall'utente a un servizio.<br/>                                |



 

### <a name="properties"></a>Proprietà

La **classe \_ TerminalService Win32** ha queste proprietà.

<dl> <dt>

**AcceptPause**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Strutture del servizio Win32API \| SERVICE \| [**\_ STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| SERVICE ACCEPT PAUSE \_ \_ \_ CONTINUE"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accepts Pause")
</dt> </dl>

Indica se il servizio può essere sospeso.

Questa proprietà viene ereditata da [**Win32 \_ BaseService.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**AcceptStop**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Strutture del servizio Win32API \| SERVICE \| [**\_ STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| SERVICE ACCEPT \_ \_ STOP"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accepts Stop")
</dt> </dl>

Indica se il servizio può essere arrestato.

Questa proprietà viene ereditata da [**Win32 \_ BaseService.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Breve descrizione del servizio, una stringa di una riga.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**Checkpoint**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Strutture del servizio Win32API \| SERVICE \| [**\_ STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwCheckPoint"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Check Point Count")
</dt> </dl>

Valore incrementato periodicamente dal servizio per segnalare lo stato di avanzamento durante un'operazione di avvio, arresto, sospensione o continuazione di lunga durata. Ad esempio, il servizio incrementa questo valore durante il completamento di ogni passaggio dell'inizializzazione all'avvio. Il programma dell'interfaccia utente che richiama l'operazione sul servizio utilizza questo valore per tenere traccia dello stato di avanzamento del servizio durante un'operazione di lunga durata. Questo valore non è valido e deve essere zero quando il servizio non ha un'operazione di avvio, arresto, sospensione o continuazione in sospeso.

Questa proprietà viene ereditata dal [**servizio Win32. \_**](/windows/desktop/CIMWin32Prov/win32-service)

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**CIM \_ Key,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")
</dt> </dl>

Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata nella creazione di un'istanza di . Se usata con le altre proprietà chiave della classe , questa proprietà consente l'identificazione univoca di tutte le istanze di questa classe e delle relative sottoclassi.

Questa proprietà viene ereditata dal [**servizio CIM \_**](/windows/desktop/CIMWin32Prov/cim-service).

</dd> <dt>

**DelayedAutoStart**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Strutture del servizio Win32API \| SERVICE \| [**\_ DELAYED AUTO START \_ \_ \_ INFO**](/windows/desktop/api/winsvc/ns-winsvc-service_delayed_auto_start_info) \| fDelayedAutostart"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Avvio automatico ritardato")
</dt> </dl>

Se **True,** il servizio viene avviato dopo l'avvio di altri servizi di avvio automatico più un breve ritardo.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 e Windows Vista:** Questa proprietà non è supportata prima di Windows Server 2016 e Windows 10.

Questa proprietà viene ereditata dal [**servizio Win32. \_**](/windows/desktop/CIMWin32Prov/win32-service)

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Descrizione dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**DesktopInteract**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Strutture del servizio Win32API \| QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType \| SERVICE INTERACTIVE \_ \_ PROCESS"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Interagisce con desktop")
</dt> </dl>

Indica se il servizio può creare o comunicare con le finestre sul desktop e quindi interagire in qualche modo con un utente. I servizi interattivi devono essere eseguiti con l'account di sistema locale. La maggior parte dei servizi non è interattiva. ciò significa che non comunicano in alcun modo con l'utente.

Questa proprietà viene ereditata da [**Win32 \_ BaseService.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**Sessioni disconnesse**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di sessioni disconnesse nel server corrente. Queste sessioni possono ancora utilizzare attivamente le risorse del server, ma attualmente non hanno alcuna connessione di rete con un client.

</dd> <dt>

**DisplayName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Strutture del servizio Win32API \| QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpDisplayName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nome visualizzato")
</dt> </dl>

Nome del servizio visualizzato nello snap-in Servizi. La lunghezza massima della stringa è di 256 caratteri. Si noti che il nome visualizzato e il nome del servizio (archiviato nel Registro di sistema) non sono sempre uguali. Ad esempio, il servizio Client DHCP ha il nome del servizio Dhcp, ma il nome visualizzato Dhcp Client. Il nome viene mantenuto senza distinzione tra maiuscole e minuscole in Gestione controllo servizi. Tuttavia, [**i confronti di DisplayName**](/windows/desktop/CIMWin32Prov/win32-service) non sono sempre distinzione tra maiuscole e minuscole.

Constraint: accetta lo stesso valore della [**proprietà Name.**](/windows/desktop/CIMWin32Prov/win32-service)

Esempio: "Atdisk"

Questa proprietà viene ereditata da [**Win32 \_ BaseService.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**ErrorControl**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Strutture del servizio Win32API \| QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwErrorControl"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Gravità dell'errore di avvio")
</dt> </dl>

Gravità dell'errore se il servizio non viene avviato durante l'avvio. Il valore indica l'azione eseguita dal programma di avvio in caso di errore. Tutti gli errori vengono registrati dal computer.

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignora** ("Ignora")


</dt> <dd>

L'utente non viene notificato.

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normale** ("Normale")


</dt> <dd>

L'utente viene notificato. In genere si tratta di una finestra di messaggio che informa l'utente del problema.

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** ("Grave")


</dt> <dd>

Il sistema viene riavviato con l'ultima configurazione valida nota.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critico** ("Critico")


</dt> <dd>

Il sistema tenta un riavvio con una configurazione valida. Se il servizio non viene avviato una seconda volta, l'avvio ha esito negativo.

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** ("Sconosciuto")


</dt> <dd>

La gravità dell'errore è sconosciuta.

</dd> </dl>

Questa proprietà viene ereditata da [**Win32 \_ BaseService.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**ExitCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Strutture del servizio Win32API \| SERVICE \| [**\_ STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Codice di uscita")
</dt> </dl>

Windows codice di errore che definisce gli errori rilevati durante l'avvio o l'arresto del servizio. Questa proprietà è impostata su **ERROR \_ SERVICE SPECIFIC \_ \_ ERROR** (1066) quando l'errore è univoco per il servizio rappresentato da questa classe e le informazioni sull'errore sono disponibili nella [**proprietà ServiceSpecificExitCode.**](/windows/desktop/CIMWin32Prov/win32-service) Il servizio imposta questo valore su **NO \_ ERROR durante** l'esecuzione e di nuovo al termine normale.

Questa proprietà viene ereditata da [**Win32 \_ BaseService.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")
</dt> </dl>

L'oggetto Date è installato. Questa proprietà non richiede un valore per indicare che l'oggetto è installato.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identificatore univoco del servizio che fornisce un'indicazione della funzionalità gestita. Questa funzionalità è descritta nella [**proprietà Description**](/windows/desktop/CIMWin32Prov/win32-service) dell'oggetto .

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**PathName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Strutture del servizio Win32API \| QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpBinaryPathName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nome percorso file")
</dt> </dl>

Percorso completo del file binario del servizio che implementa il servizio.

Esempio: \\ "SystemRoot \\ System32 \\ drivers \\afd.sys"

Questa proprietà viene ereditata da [**Win32 \_ BaseService.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**Processid**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Strutture del servizio Win32API \| SERVICE STATUS \| [**\_ \_ PROCESS**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process) \| dwProcessId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("ID processo")
</dt> </dl>

Identificatore di processo del servizio.

Esempio: 324

Questa proprietà viene ereditata dal [**servizio Win32. \_**](/windows/desktop/CIMWin32Prov/win32-service)

</dd> <dt>

**ServiceSpecificExitCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Strutture del servizio Win32API \| SERVICE \| [**\_ STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwServiceSpecificExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Codice di uscita specifico del server")
</dt> </dl>

Codice di errore specifico del servizio per gli errori che si verificano durante l'avvio o l'arresto del servizio. I codici di uscita sono definiti dal servizio rappresentato da questa classe. Questo valore viene impostato solo quando il [**valore della proprietà ExitCode**](/windows/desktop/CIMWin32Prov/win32-service) è **ERROR SERVICE SPECIFIC \_ \_ \_ ERROR** (1066).

Questa proprietà viene ereditata da [**Win32 \_ BaseService.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**ServiceType**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Strutture del servizio Win32API \| QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tipo di servizio")
</dt> </dl>

Tipo di servizio fornito ai processi chiamanti.

I valori possibili sono:

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

**Driver kernel** ("Driver kernel")


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

**Driver del file system** ("Driver del file system")


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

**Adapter** ("Adapter")


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

**Recognizer Driver** ("Recognizer Driver")


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

**Processo personalizzato** ("Processo proprio")


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

**Processo di condivisione** ("Processo di condivisione")


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

**Processo interattivo** ("Processo interattivo")


</dt> <dd></dd> </dl>

Questa proprietà viene ereditata da [**Win32 \_ BaseService.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**Avviato**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")
</dt> </dl>

Indica se il servizio è stato avviato o meno.

Questa proprietà viene ereditata dal [**servizio CIM \_**](/windows/desktop/CIMWin32Prov/cim-service).

</dd> <dt>

**Modalità avvio**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Modalità di avvio")
</dt> </dl>

Modalità di avvio del Windows di base.

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Avvio** ("Avvio")


</dt> <dd>

Driver di dispositivo avviato dal caricatore del sistema operativo (valido solo per i servizi driver).

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema** ("Sistema")


</dt> <dd>

Driver di dispositivo avviato dal processo di inizializzazione del sistema operativo. Questo valore è valido solo per i servizi del driver.

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("Auto")


</dt> <dd>

Servizio da avviare automaticamente da Gestione controllo servizi durante l'avvio del sistema. I servizi automatici vengono avviati anche se un utente non esegue l'accesso.

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuale** ("Manuale")


</dt> <dd>

Servizio che deve essere avviato da Gestione controllo servizi quando un processo chiama il [**metodo StartService.**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) Questi servizi non vengono avviati a meno che un utente non eserviti l'accesso e li avvia.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")


</dt> <dd>

Servizio che non può essere avviato fino a quando startMode non viene modificato in Auto o Manual.

</dd> </dl>

Questa proprietà viene ereditata dal [**servizio CIM \_**](/windows/desktop/CIMWin32Prov/cim-service).

</dd> <dt>

**StartName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Strutture del servizio Win32API \| QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpServiceStartName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nome account iniziale")
</dt> </dl>

Nome dell'account con cui viene eseguito un servizio. A seconda del tipo di servizio, il nome dell'account può essere nel formato "NomeDominioNomeUtente" o \\ nel formato UPN (" *Username@DomainName* "). Il processo del servizio viene registrato usando uno di questi due formati durante l'esecuzione. Se l'account appartiene al dominio predefinito, ". \\ Username" può essere specificato. Per i driver a livello di kernel o di sistema, [**StartName**](/windows/desktop/CIMWin32Prov/win32-service) contiene il nome dell'oggetto driver ,ovvero \\ "FileSystem \\ Rdr" o \\ "Driver Xns", che il sistema di I/O usa per caricare il driver di \\ dispositivo. Inoltre, se viene **specificato NULL,** il driver viene eseguito con un nome di oggetto predefinito creato dal sistema di I/O in base al nome del servizio.

Esempio: "Amministratore \\ DWDOM"

Questa proprietà viene ereditata da [**Win32 \_ BaseService.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**State**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Strutture del servizio Win32API \| SERVICE \| [**\_ STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwCurrentState "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("State")
</dt> </dl>

Stato corrente del servizio di base.

I valori possibili sono:

<dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

**Arrestato** ("Arrestato")


</dt> <dd></dd> <dt>

<span id="Start_Pending"></span><span id="start_pending"></span><span id="START_PENDING"></span>

**Avvio in sospeso** ("Avvio in sospeso")


</dt> <dd></dd> <dt>

<span id="Stop_Pending"></span><span id="stop_pending"></span><span id="STOP_PENDING"></span>

**Arresta in sospeso** ("Arresta in sospeso")


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

**In** esecuzione ("In esecuzione")


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

**Continua in sospeso** ("Continua in sospeso")


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

**Sospendi in** sospeso ("Sospendi in sospeso")


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

**Paused** ("Paused")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** ("Sconosciuto")


</dt> <dd></dd> </dl>

**Windows Server 2008 e Windows Vista:** Questa proprietà è di sola lettura prima Windows 7 e Windows Server 2008 R2.

Questa proprietà viene ereditata da [**Win32 \_ BaseService.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Stato corrente dell'oggetto. È possibile definire vari stati operativi e non operativi. Gli stati operativi includono: "OK", "Degraded" e "Pred Fail" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente ma prevedere un errore nel prossimo futuro). Gli stati nonoperational includono: "Error", "Starting", "Stopping" e "Service". Quest'ultimo, "Servizio", può essere applicato durante il ridimensionamento del mirror di un disco, il ricaricamento di un elenco di autorizzazioni utente o altro lavoro amministrativo. Non tutte queste operazioni sono online, ma l'elemento gestito non è "OK" né in uno degli altri stati.

I valori possibili sono:

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

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Sistema CIM \_**](/windows/desktop/CIMWin32Prov/cim-system). CreationClassName"), [**CIM \_ Key,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Class Name")
</dt> </dl>

Nome del sistema che ospita il servizio.

Questa proprietà viene ereditata dal [**servizio CIM \_**](/windows/desktop/CIMWin32Prov/cim-service).

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Sistema CIM \_**](/windows/desktop/CIMWin32Prov/cim-system). Name"), [**CIM \_ Key,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Name")
</dt> </dl>

Nome del sistema che ospita il servizio.

Questa proprietà viene ereditata dal [**servizio CIM \_**](/windows/desktop/CIMWin32Prov/cim-service).

</dd> <dt>

**TagId**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Strutture del servizio Win32API \| QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwTagId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tag Id")
</dt> </dl>

Valore di tag univoco per questo servizio nel gruppo. Il valore 0 (zero) indica che il servizio non dispone di un tag . È possibile usare un tag per ordinare l'avvio del servizio all'interno di un gruppo di ordini di caricamento specificando un vettore di ordine dei tag nel registro che si trova in:

**HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **GroupOrderList**    

I tag vengono valutati solo per i servizi del tipo di avvio del driver del kernel e del driver del file system con modalità di avvio o di avvio del sistema.

Questa proprietà viene ereditata da [**Win32 \_ BaseService.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**TotalSessions**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero totale di sessioni nel server corrente. Sono incluse sia le sessioni connesse che le sessioni disconnesse.

</dd> <dt>

**WaitHint**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Strutture del servizio Win32API \| SERVICE \| [**\_ STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwWaitHint"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tempo di attesa stimato")
</dt> </dl>

Tempo stimato necessario, in millisecondi, per un'operazione di avvio, arresto, sospensione o continuazione in sospeso. Dopo che è trascorso il tempo specificato, il servizio effettua la chiamata successiva al **metodo SetServiceStatus** con un valore [**CheckPoint**](/windows/desktop/CIMWin32Prov/win32-service) incrementato o una modifica in **CurrentState**. Se la quantità di tempo specificata da **WaitHint** viene superata e **CheckPoint** non è stato incrementato o **CurrentState** non è stato modificato, il gestore di controllo del servizio o il programma di controllo del servizio presuppone che si sia verificato un errore.

Questa proprietà viene ereditata dal [**servizio Win32. \_**](/windows/desktop/CIMWin32Prov/win32-service)

</dd> </dl>

## <a name="remarks"></a>Commenti

Poiché la **classe \_ TerminalService Win32** è una sottoclasse della classe del servizio [**Win32, \_**](/windows/desktop/CIMWin32Prov/win32-service) la classe eredita tutte le proprietà e i metodi **del servizio Win32. \_**

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md) è associato a **\_ TerminalService Win32** come proprietà **Setting** dell'associazione [**\_ TerminalServiceToSetting Win32.**](win32-terminalservicetosetting.md)

[**Win32 \_ TSSessionDirectory è**](win32-tssessiondirectory.md) associato a **\_ TerminalService Win32** come proprietà **Setting** dell'associazione [**\_ Win32 TSSessionDirectorySetting.**](win32-tssessiondirectorysetting.md)

Managed Object Format file MOF contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Root\\CIMv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Servizio \_ Win32**](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[**Win32 \_ TerminalServiceToSetting**](win32-terminalservicetosetting.md)
</dt> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> <dt>

[**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)
</dt> <dt>

[**Servizio \_ CIM**](/windows/desktop/CIMWin32Prov/cim-service)
</dt> </dl>

 


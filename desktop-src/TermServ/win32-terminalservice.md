---
title: Classe Win32_TerminalService
description: Sottoclasse della classe del \_ servizio Win32. Win32 \_ TerminalService rappresenta la proprietà dell'elemento dell' \_ associazione TerminalServiceToSetting Win32.
ms.assetid: 06c69d71-4e6f-48af-b13d-e593b8fcf376
ms.tgt_platform: multiple
keywords:
- Classe Win32_TerminalService Servizi Desktop remoto
- Classe Win32_TerminalService Servizi Desktop remoto, descritta
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
ms.openlocfilehash: ba5646c6ac9abf41fddc023ad39884e611681a71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478844"
---
# <a name="win32_terminalservice-class"></a>Win32 \_ TerminalService (classe)

La classe WMI **\_ TerminalService Win32** è una sottoclasse della classe del [**\_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service) . **Win32 \_ TerminalService** rappresenta la proprietà dell' **elemento** dell' [**associazione \_ TerminalServiceToSetting Win32**](win32-terminalservicetosetting.md) .

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

La classe **Win32 \_ TerminalService** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **Win32 \_ TerminalService** presenta questi metodi.



| Metodo                                                                       | Descrizione                                                                                          |
|:-----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**Modificare**](win32-terminalservice-change.md)                               | Modifica un servizio.<br/>                                                                       |
| [**ChangeStartMode**](win32-terminalservice-changestartmode.md)             | Modifica la modalità di avvio di un servizio.<br/>                                                     |
| [**Creare**](win32-terminalservice-create.md)                               | Crea un nuovo servizio.<br/>                                                                    |
| [**Delete**](win32-terminalservice-delete.md)                               | Elimina un servizio esistente.<br/>                                                              |
| [**GetSecurityDescriptor**](win32-terminalservice-getsecuritydescriptor.md) | Restituisce il descrittore di sicurezza che controlla l'accesso al servizio.<br/>                      |
| [**InterrogateService**](win32-terminalservice-interrogateservice.md)       | Richiede che un servizio aggiorni lo stato a Service Manager.<br/>                          |
| [**PauseService**](win32-terminalservice-pauseservice.md)                   | Tenta di collocare un servizio in stato di sospensione.<br/>                                          |
| [**ResumeService**](win32-terminalservice-resumeservice.md)                 | Tenta di inserire un servizio nello stato ripresa.<br/>                                         |
| [**SetSecurityDescriptor**](win32-terminalservice-setsecuritydescriptor.md) | Scrive una versione aggiornata del descrittore di sicurezza che controlla l'accesso al servizio.<br/> |
| [**StartService**](win32-terminalservice-startservice.md)                   | Tenta di inserire un servizio nello stato di avvio.<br/>                                       |
| [**StopService**](win32-terminalservice-stopservice.md)                     | Inserisce un servizio nello stato interrotto.<br/>                                                    |
| [**UserControlService**](win32-terminalservice-usercontrolservice.md)       | Tenta di inviare un codice di controllo definito dall'utente a un servizio.<br/>                                |



 

### <a name="properties"></a>Proprietà

La classe **Win32 \_ TerminalService** dispone di queste proprietà.

<dl> <dt>

**AcceptPause**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API Service \| Structures Service \| [**\_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| DwControlsAccepted servizio \| \_ accettazione \_ pausa \_ continua"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("servizio accetta pausa")
</dt> </dl>

Indica se il servizio può essere sospeso.

Questa proprietà viene ereditata da [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**AcceptStop**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures Service \| [**\_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted servizio \| \_ Accept \_ Stop"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service accepts stop")
</dt> </dl>

Indica se il servizio può essere arrestato.

Questa proprietà viene ereditata da [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Breve descrizione del servizio una stringa a una riga.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**CheckPoint**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Service \_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| DwCheckPoint"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Check Point count")
</dt> </dl>

Valore che il servizio incrementa periodicamente per segnalare lo stato di avanzamento durante un'operazione di avvio, arresto, sospensione o continuazione Prolong. Il servizio, ad esempio, incrementa questo valore poiché completa ogni passaggio dell'inizializzazione all'avvio. Il programma dell'interfaccia utente che richiama l'operazione sul servizio utilizza questo valore per tenere traccia dello stato di avanzamento del servizio durante un'operazione di lunga durata. Questo valore non è valido e deve essere zero quando il servizio non dispone di un'operazione di avvio, arresto, pausa o continuazione in sospeso.

Questa proprietà viene ereditata [**dal \_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome classe")
</dt> </dl>

Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata per la creazione di un'istanza. Se utilizzata con le altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.

Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).

</dd> <dt>

**DelayedAutoStart**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Service \_ Retarded \_ auto \_ Start \_ info**](/windows/desktop/api/winsvc/ns-winsvc-service_delayed_auto_start_info) \| fDelayedAutostart"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("avvio automatico ritardato")
</dt> </dl>

Se **true**, il servizio viene avviato dopo l'avvio di altri servizi di avvio automatico più un breve ritardo.

**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Questa proprietà non è supportata prima di Windows Server 2016 e Windows 10.

Questa proprietà viene ereditata [**dal \_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service).

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Descrizione dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**DesktopInteract**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**query \_ Services \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType \| Service \_ Interactive \_ processo"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("interagisce con il desktop")
</dt> </dl>

Indica se il servizio è in grado di creare o comunicare con Windows sul desktop e quindi interagire in qualche modo con un utente. I servizi interattivi devono essere eseguiti con l'account di sistema locale. La maggior parte dei servizi non è interattiva; ovvero non comunicano con l'utente in alcun modo.

Questa proprietà viene ereditata da [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**DisconnectedSessions**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di sessioni disconnesse nel server corrente. Queste sessioni possono continuare a usare attivamente le risorse del server, ma attualmente non hanno una connessione di rete con un client.

</dd> <dt>

**DisplayName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**query \_ Service \_ Configuration**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpDisplayName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Display Name")
</dt> </dl>

Nome del servizio visualizzato nello snap-in servizi. La lunghezza massima della stringa è di 256 caratteri. Si noti che il nome visualizzato e il nome del servizio (archiviati nel registro di sistema) non sono sempre gli stessi. Il servizio client DHCP, ad esempio, ha il nome del servizio DHCP ma il nome visualizzato client DHCP. Il nome viene mantenuto con la distinzione tra maiuscole e minuscole in Gestione controllo servizi. Tuttavia, i confronti [**DisplayName**](/windows/desktop/CIMWin32Prov/win32-service) sono sempre senza distinzione tra maiuscole e minuscole.

Constraint: accetta lo stesso valore della proprietà [**Name**](/windows/desktop/CIMWin32Prov/win32-service) .

Esempio: "ATDISK"

Questa proprietà viene ereditata da [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**ErrorControl**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| DwErrorControl"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("gravità dell'avvio non riuscito")
</dt> </dl>

Gravità dell'errore se il servizio non viene avviato durante l'avvio. Il valore indica l'azione eseguita dal programma di avvio in caso di errore. Tutti gli errori vengono registrati dal computer.

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignora** ("Ignora")


</dt> <dd>

L'utente non viene notificato.

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normale** ("normale")


</dt> <dd>

L'utente viene notificato. In genere si tratta di una finestra di messaggio che informa l'utente del problema.

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** ("grave")


</dt> <dd>

Il sistema viene riavviato con l'ultima configurazione valida nota.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critico** ("critico")


</dt> <dd>

Il sistema tenta un riavvio con una configurazione valida. Se il servizio non viene avviato una seconda volta, l'avvio ha esito negativo.

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** ("sconosciuto")


</dt> <dd>

La gravità dell'errore è sconosciuta.

</dd> </dl>

Questa proprietà viene ereditata da [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**ExitCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Service \_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("codice di uscita")
</dt> </dl>

Codice di errore di Windows che definisce gli errori riscontrati durante l'avvio o l'arresto del servizio. Questa proprietà è impostata sull' **\_ \_ \_ errore specifico del servizio di errore** (1066) quando l'errore è univoco per il servizio rappresentato da questa classe e le informazioni sull'errore sono disponibili nella proprietà [**ServiceSpecificExitCode**](/windows/desktop/CIMWin32Prov/win32-service) . Il servizio imposta questo valore su **nessun \_ errore** durante l'esecuzione e di nuovo alla chiusura normale.

Questa proprietà viene ereditata da [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")
</dt> </dl>

L'oggetto data è installato. Questa proprietà non richiede un valore per indicare che l'oggetto è installato.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identificatore univoco del servizio che fornisce un'indicazione della funzionalità gestita. Questa funzionalità è descritta nella proprietà [**Description**](/windows/desktop/CIMWin32Prov/win32-service) dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**PathName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| LpBinaryPathName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome percorso file")
</dt> </dl>

Percorso completo del file binario del servizio che implementa il servizio.

Esempio: " \\ systemroot \\ system32 \\ drivers \\afd.sys"

Questa proprietà viene ereditata da [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**ProcessId**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Service \_ status \_ Process**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process) \| dwProcessId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("ID processo")
</dt> </dl>

Identificatore del processo del servizio.

Esempio: 324

Questa proprietà viene ereditata [**dal \_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service).

</dd> <dt>

**ServiceSpecificExitCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Service \_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwServiceSpecificExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("codice di uscita specifico del server")
</dt> </dl>

Codice di errore specifico del servizio per gli errori che si verificano durante l'avvio o l'arresto del servizio. I codici di uscita sono definiti dal servizio rappresentato da questa classe. Questo valore viene impostato solo quando il valore della proprietà [**ExitCode**](/windows/desktop/CIMWin32Prov/win32-service) è **\_ \_ \_ errore specifico del servizio di errore** (1066).

Questa proprietà viene ereditata da [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**ServiceType**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| DwServiceType"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo di servizio")
</dt> </dl>

Tipo di servizio fornito ai processi chiamanti.

I valori possibili sono:

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

**Driver del kernel** ("driver del kernel")


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

**Driver del file System** ("driver del file System")


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

**Adapter** ("adapter")


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

**Driver di riconoscimento** ("driver di riconoscimento")


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

**Processo personale** ("processo personalizzato")


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

**Processo di condivisione** ("processo di condivisione")


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

**Processo interattivo** ("processo interattivo")


</dt> <dd></dd> </dl>

Questa proprietà viene ereditata da [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**Avviato**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")
</dt> </dl>

Indica se il servizio è stato avviato o meno.

Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).

</dd> <dt>

**Modalità avvio**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("modalità di avvio")
</dt> </dl>

Modalità di avvio del servizio di base di Windows.

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Avvio** ("avvio")


</dt> <dd>

Driver di dispositivo avviato dal caricatore del sistema operativo (valido solo per i servizi driver).

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema** ("sistema")


</dt> <dd>

Driver di dispositivo avviato dal processo di inizializzazione del sistema operativo. Questo valore è valido solo per i servizi del driver.

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Automatico** ("auto")


</dt> <dd>

Servizio da avviare automaticamente da Gestione controllo servizi durante l'avvio del sistema. I servizi automatici vengono avviati anche se un utente non esegue l'accesso.

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuale** ("manuale")


</dt> <dd>

Servizio che deve essere avviato da Gestione controllo servizi quando un processo chiama il metodo [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) . Questi servizi non vengono avviati, a meno che un utente non esegua l'accesso e li avvii.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** ("disabilitato")


</dt> <dd>

Servizio che non può essere avviato finché il relativo StartMode non viene modificato in auto o manuale.

</dd> </dl>

Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).

</dd> <dt>

**StartName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| LpServiceStartName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome account iniziale")
</dt> </dl>

Nome dell'account con cui viene eseguito un servizio. A seconda del tipo di servizio, il nome dell'account può avere la forma di "DomainName \\ username" o del formato UPN (" *Username@DomainName* "). Il processo del servizio viene registrato utilizzando una di queste due forme durante l'esecuzione. Se l'account appartiene al dominio predefinito, ". \\ Nome utente "può essere specificato. Per i driver a livello di sistema o del kernel, [**StartName**](/windows/desktop/CIMWin32Prov/win32-service) contiene il nome dell'oggetto driver, ovvero " \\ filesystem \\ RDR" o " \\ driver \\ XNS", utilizzato dal sistema i/O per caricare il driver di dispositivo. Inoltre, se si specifica **null** , il driver viene eseguito con un nome di oggetto predefinito creato dal sistema i/O in base al nome del servizio.

Esempio: "DWDOM \\ admin"

Questa proprietà viene ereditata da [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**State**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Service \_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwCurrentState"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("state")
</dt> </dl>

Stato corrente del servizio di base.

I valori possibili sono:

<dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

**Arrestato** ("arrestato")


</dt> <dd></dd> <dt>

<span id="Start_Pending"></span><span id="start_pending"></span><span id="START_PENDING"></span>

**Avvio in sospeso** ("avvio in sospeso")


</dt> <dd></dd> <dt>

<span id="Stop_Pending"></span><span id="stop_pending"></span><span id="STOP_PENDING"></span>

**Arresta in sospeso** ("arresta in sospeso")


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

**In esecuzione** ("Running")


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

**Continua in sospeso** ("continua in sospeso")


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

**Sospensione in sospeso** ("pausa in sospeso")


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

**Sospesa** ("sospesa")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** ("sconosciuto")


</dt> <dd></dd> </dl>

**Windows Server 2008 e Windows Vista:** Questa proprietà è di sola lettura prima di Windows 7 e Windows Server 2008 R2.

Questa proprietà viene ereditata da [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")
</dt> </dl>

Stato corrente dell'oggetto. È possibile definire diversi stati operativi e non operativi. Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro). Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service". Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative. Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.

I valori possibili sono:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Errore** ("errore")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

Ridotto **("danneggiato"** )


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** ("sconosciuto")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Errore di predazione** ("Predator fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Avvio** di ("avvio")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Arresto** in corso ("arresto")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Servizio** ("servizio")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Sottolineato** (sottolineato)


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**Noncover** ("noncover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Nessun contatto** ("nessun contatto")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Comunicazione persa** ("comunicazione persa")


</dt> <dd></dd> </dl>

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system). CreationClassName "), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome classe di sistema ")
</dt> </dl>

Nome del tipo di sistema che ospita il servizio.

Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system). Nome "), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome sistema ")
</dt> </dl>

Nome del sistema che ospita il servizio.

Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).

</dd> <dt>

**TagId**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwTagId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("ID tag")
</dt> </dl>

Valore di tag univoco per il servizio nel gruppo. Il valore 0 (zero) indica che il servizio non dispone di un tag. Un tag può essere usato per ordinare l'avvio del servizio all'interno di un gruppo di ordini di caricamento specificando un vettore di ordine dei tag nel registro di sistema che si trova in:

**HKEY \_ Controllo CurrentControlSet del sistema del \_ computer locale** \\  \\  \\  \\ **GroupOrderList**    

I tag vengono valutati solo per i servizi del tipo di avvio del driver del kernel e del driver del file System con modalità avvio o sistema.

Questa proprietà viene ereditata da [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**TotalSessions**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero totale di sessioni nel server corrente. Sono incluse sessioni connesse e disconnesse.

</dd> <dt>

**WaitHint**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Service \_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwWaitHint"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tempo di attesa stimato")
</dt> </dl>

Tempo stimato necessario, in millisecondi, per un'operazione di avvio, arresto, sospensione o continuazione in sospeso. Dopo che è trascorso il tempo specificato, il servizio effettua la chiamata successiva al metodo **SetServiceStatus** con un valore di [**Checkpoint**](/windows/desktop/CIMWin32Prov/win32-service) incrementato o una modifica in **CurrentState**. Se la quantità di tempo specificata da **WaitHint** passa e il **Checkpoint** non è stato incrementato oppure **CurrentState** non è stato modificato, gestione controllo servizi o il programma di controllo del servizio presuppone che si sia verificato un errore.

Questa proprietà viene ereditata [**dal \_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service).

</dd> </dl>

## <a name="remarks"></a>Commenti

Poiché la classe **Win32 \_ TerminalService** è una sottoclasse della classe del [**\_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service) , la classe eredita tutte le proprietà e i metodi del **\_ servizio Win32**.

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md) è associato a **Win32 \_ TerminalService** come proprietà **Setting** dell'associazione [**\_ TerminalServiceToSetting di Win32**](win32-terminalservicetosetting.md) .

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md) è associato a **Win32 \_ TerminalService** come proprietà **Setting** dell'associazione [**\_ TSSessionDirectorySetting di Win32**](win32-tssessiondirectorysetting.md) .

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Root\\CIMv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[**\_TerminalServiceToSetting Win32**](win32-terminalservicetosetting.md)
</dt> <dt>

[**\_TSSessionDirectory Win32**](win32-tssessiondirectory.md)
</dt> <dt>

[**\_BaseService Win32**](/windows/desktop/CIMWin32Prov/win32-baseservice)
</dt> <dt>

[**\_Servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)
</dt> </dl>

 


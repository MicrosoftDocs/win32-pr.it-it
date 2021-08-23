---
description: Rappresenta un servizio in un computer che esegue Windows.
ms.assetid: 713402d3-ee73-4a6c-afb9-ad8033a4c580
ms.tgt_platform: multiple
title: Win32_Service classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service
- Win32_Service.AcceptPause
- Win32_Service.AcceptStop
- Win32_Service.Caption
- Win32_Service.CheckPoint
- Win32_Service.CreationClassName
- Win32_Service.DelayedAutoStart
- Win32_Service.Description
- Win32_Service.DesktopInteract
- Win32_Service.DisplayName
- Win32_Service.ErrorControl
- Win32_Service.ExitCode
- Win32_Service.InstallDate
- Win32_Service.Name
- Win32_Service.PathName
- Win32_Service.ProcessId
- Win32_Service.ServiceSpecificExitCode
- Win32_Service.ServiceType
- Win32_Service.Started
- Win32_Service.StartMode
- Win32_Service.StartName
- Win32_Service.State
- Win32_Service.Status
- Win32_Service.SystemCreationClassName
- Win32_Service.SystemName
- Win32_Service.TagId
- Win32_Service.WaitHint
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a33265b3dfc3b114d55b381a229b717e291bbd258716e8305d9995282d29b3f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759261"
---
# <a name="win32_service-class"></a>Classe del servizio Win32 \_

La classe [WMI](../wmisdk/retrieving-a-class.md) **\_ del servizio Win32** rappresenta un servizio in un computer che esegue Windows.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4D9-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Services"), AMENDMENT]
class Win32_Service : Win32_BaseService
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
};
```

## <a name="members"></a>Members

La **classe \_ del servizio Win32** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ del servizio Win32** include questi metodi.



| Metodo                                                                               | Descrizione                                                                                          |
|:-------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**Cambiare**](change-method-in-class-win32-service.md)                               | Modifica un servizio.<br/>                                                                       |
| [**ChangeStartMode**](changestartmode-method-in-class-win32-service.md)             | Modifica la modalità di avvio di un servizio.<br/>                                                     |
| [**Crea**](create-method-in-class-win32-service.md)                               | Crea un nuovo servizio.<br/>                                                                    |
| [**Elimina**](delete-method-in-class-win32-service.md)                               | Elimina un servizio esistente.<br/>                                                              |
| [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class-win32-service.md) | Restituisce il descrittore di sicurezza che controlla l'accesso al servizio.<br/>                      |
| [**InterrogaeService**](interrogateservice-method-in-class-win32-service.md)       | Richiede che un servizio aggiornerne lo stato a Service Manager.<br/>                          |
| [**PauseService**](pauseservice-method-in-class-win32-service.md)                   | Tenta di mettere un servizio nello stato sospeso.<br/>                                          |
| [**ResumeService**](resumeservice-method-in-class-win32-service.md)                 | Tenta di impostare un servizio nello stato ripreso.<br/>                                         |
| [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class-win32-service.md) | Scrive una versione aggiornata del descrittore di sicurezza che controlla l'accesso al servizio.<br/> |
| [**Startservice**](startservice-method-in-class-win32-service.md)                   | Tenta di impostare un servizio sullo stato di avvio.<br/>                                       |
| [**StopService**](stopservice-method-in-class-win32-service.md)                     | Inserisce un servizio nello stato arrestato.<br/>                                                    |
| [**UserControlService**](usercontrolservice-method-in-class-win32-service.md)       | Tenta di inviare un codice di controllo definito dall'utente a un servizio.<br/>                                |



 

### <a name="properties"></a>Proprietà

La **classe \_ del servizio Win32** dispone di queste proprietà.

<dl> <dt>

**AcceptPause**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture del servizio Win32API \| SERVICE \| [**\_ STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| SERVICE ACCEPT PAUSE \_ \_ \_ CONTINUE"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Accepts Pause")
</dt> </dl>

Indica se il servizio può essere sospeso.

Questa proprietà viene ereditata da [**Win32 \_ BaseService.**](win32-baseservice.md)

</dd> <dt>

**AcceptStop**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture del servizio Win32API \| SERVICE \| [**\_ STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| SERVICE ACCEPT \_ \_ STOP"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Accepts Stop")
</dt> </dl>

Indica se il servizio può essere arrestato.

Questa proprietà viene ereditata da [**Win32 \_ BaseService.**](win32-baseservice.md)

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Breve descrizione del servizio, ovvero una stringa di una riga.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Checkpoint**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture del servizio Win32API \| SERVICE \| [**\_ STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwCheckPoint"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Check Point Count")
</dt> </dl>

Valore incrementato periodicamente dal servizio per segnalare lo stato di avanzamento durante un'operazione di avvio, arresto, sospensione o continuazione di lunga durata. Ad esempio, il servizio incrementa questo valore durante il completamento di ogni passaggio dell'inizializzazione all'avvio. Il programma dell'interfaccia utente che richiama l'operazione sul servizio utilizza questo valore per tenere traccia dello stato di avanzamento del servizio durante un'operazione di lunga durata. Questo valore non è valido e deve essere zero quando il servizio non ha un'operazione di avvio, arresto, sospensione o continuazione in sospeso.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**CIM \_ Key,**](../wmisdk/standard-wmi-qualifiers.md) [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")
</dt> </dl>

Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata nella creazione di un'istanza di . Se usata con le altre proprietà chiave della classe , questa proprietà consente l'identificazione univoca di tutte le istanze di questa classe e delle relative sottoclassi.

Questa proprietà viene ereditata dal [**servizio CIM \_**](cim-service.md).

</dd> <dt>

**DelayedAutoStart**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture del servizio Win32API \| SERVICE \| [**\_ DELAYED AUTO START \_ \_ \_ INFO**](/windows/win32/api/winsvc/ns-winsvc-service_delayed_auto_start_info) \| fDelayedAutostart"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Avvio automatico ritardato")
</dt> </dl>

Se **True,** il servizio viene avviato dopo l'avvio di altri servizi di avvio automatico più un breve ritardo.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 e Windows Vista:** Questa proprietà non è supportata prima di Windows Server 2016 e Windows 10.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Descrizione dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**DesktopInteract**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture del servizio Win32API \| QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType \| SERVICE INTERACTIVE \_ \_ PROCESS"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Interagisce con desktop")
</dt> </dl>

Indica se il servizio può creare o comunicare con le finestre sul desktop e quindi interagire in qualche modo con un utente. I servizi interattivi devono essere eseguiti con l'account di sistema locale. La maggior parte dei servizi non è interattiva. ciò significa che non comunicano in alcun modo con l'utente.

Questa proprietà viene ereditata da [**Win32 \_ BaseService.**](win32-baseservice.md)

</dd> <dt>

**DisplayName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture del servizio Win32API \| QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| lpDisplayName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Nome visualizzato")
</dt> </dl>

Nome del servizio visualizzato nello snap-in Servizi. La lunghezza massima della stringa è di 256 caratteri. Si noti che il nome visualizzato e il nome del servizio (archiviato nel Registro di sistema) non sono sempre gli stessi. Ad esempio, il servizio Client DHCP ha il nome del servizio Dhcp, ma il nome visualizzato Client DHCP. Il nome viene mantenuto senza distinzione tra maiuscole e minuscole in Gestione controllo servizi. Tuttavia, per **i confronti displayName** non viene sempre fatto distinzione tra maiuscole e minuscole.

Vincolo: accetta lo stesso valore della **proprietà** Name.

Esempio: "Atdisk"

Questa proprietà viene ereditata da [**Win32 \_ BaseService.**](win32-baseservice.md)

</dd> <dt>

**ErrorControl**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture del servizio Win32API \| QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwErrorControl"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Gravità dell'errore di avvio")
</dt> </dl>

Gravità dell'errore se il servizio non viene avviato durante l'avvio. Il valore indica l'azione eseguita dal programma di avvio in caso di errore. Tutti gli errori vengono registrati dal computer.

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignora** ("Ignora")


</dt> <dd>

L'utente non viene notificato.

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")


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

Il sistema tenta un riavvio con una configurazione valida. Se il servizio non viene avviato una seconda volta, l'avvio non riesce.

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** ("Sconosciuto")


</dt> <dd>

La gravità dell'errore è sconosciuta.

</dd> </dl>

Questa proprietà viene ereditata da [**Win32 \_ BaseService.**](win32-baseservice.md)

</dd> <dt>

**Codice di uscita**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture del servizio Win32API \| SERVICE \| [**\_ STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Exit Code")
</dt> </dl>

Windows codice di errore che definisce gli errori rilevati durante l'avvio o l'arresto del servizio. Questa proprietà è impostata su **ERROR \_ SERVICE SPECIFIC \_ \_ ERROR** (1066) quando l'errore è univoco per il servizio rappresentato da questa classe e le informazioni sull'errore sono disponibili nella **proprietà ServiceSpecificExitCode.** Il servizio imposta questo valore su **NO \_ ERROR durante** l'esecuzione e di nuovo al termine normale.

Questa proprietà viene ereditata da [**Win32 \_ BaseService.**](win32-baseservice.md)

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")
</dt> </dl>

L'oggetto Data è installato. Questa proprietà non richiede un valore per indicare che l'oggetto è installato.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **Chiave**](../wmisdk/key-qualifier.md)
</dt> </dl>

Identificatore univoco del servizio che fornisce un'indicazione della funzionalità gestita. Questa funzionalità è descritta nella **proprietà Description** dell'oggetto .

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**PathName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture del servizio Win32API \| QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| lpBinaryPathName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Nome percorso file")
</dt> </dl>

Percorso completo del file binario del servizio che implementa il servizio.

Esempio: \\ "SystemRoot \\ System32 \\ drivers \\afd.sys"

Questa proprietà viene ereditata da [**Win32 \_ BaseService.**](win32-baseservice.md)

</dd> <dt>

**Processid**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures SERVICE STATUS \| [**\_ \_ PROCESS**](/windows/win32/api/winsvc/ns-winsvc-service_status_process) \| dwProcessId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Process Id")
</dt> </dl>

Identificatore del processo del servizio.

Esempio: 324

</dd> <dt>

**ServiceSpecificExitCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture del servizio Win32API \| SERVICE \| [**\_ STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwServiceSpecificExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Codice di uscita specifico del server")
</dt> </dl>

Codice di errore specifico del servizio per gli errori che si verificano durante l'avvio o l'arresto del servizio. I codici di uscita sono definiti dal servizio rappresentato da questa classe. Questo valore viene impostato solo quando il **valore della proprietà ExitCode** è **ERROR SERVICE SPECIFIC \_ \_ \_ ERROR** (1066).

Questa proprietà viene ereditata da [**Win32 \_ BaseService.**](win32-baseservice.md)

</dd> <dt>

**ServiceType**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture del servizio Win32API \| QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Tipo di servizio")
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

**Driver di riconoscimento** ("driver di riconoscimento")


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

**Own Process** ("Own Process")


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

**Processo di condivisione** ("Processo di condivisione")


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

**Processo interattivo** ("Processo interattivo")


</dt> <dd></dd> </dl>

Questa proprietà viene ereditata da [**Win32 \_ BaseService.**](win32-baseservice.md)

</dd> <dt>

**Avviato**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Started")
</dt> </dl>

Indica se il servizio è stato avviato o meno.

Questa proprietà viene ereditata dal [**servizio CIM \_**](cim-service.md).

</dd> <dt>

**Modalità avvio**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Modalità di avvio")
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

Servizio che deve essere avviato da Gestione controllo servizi quando un processo chiama il [**metodo StartService.**](startservice-method-in-class-win32-service.md) Questi servizi non vengono avviati a meno che un utente non eserviti l'accesso e li avvia.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")


</dt> <dd>

Servizio che non può essere avviato fino a quando startMode non viene modificato in Auto o Manual.

</dd> </dl>

Questa proprietà viene ereditata dal [**servizio CIM \_**](cim-service.md).

</dd> <dt>

**StartName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture del servizio Win32API \| QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| lpServiceStartName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Nome account iniziale")
</dt> </dl>

Nome dell'account con cui viene eseguito un servizio. A seconda del tipo di servizio, il nome dell'account può essere nel formato "NomeDominioNomeUtente" o \\ nel formato UPN (" *Username@DomainName* "). Il processo del servizio viene registrato usando uno di questi due formati durante l'esecuzione. Se l'account appartiene al dominio predefinito, ". \\ Username" può essere specificato. Per i driver a livello di kernel o di sistema, **StartName** contiene il nome dell'oggetto driver ,ovvero \\ "FileSystem \\ Rdr" o \\ "Driver Xns", che il sistema di I/O usa per caricare il driver di \\ dispositivo. Inoltre, se viene **specificato NULL,** il driver viene eseguito con un nome di oggetto predefinito creato dal sistema di I/O in base al nome del servizio.

Esempio: "Amministratore \\ DWDOM"

Questa proprietà viene ereditata da [**Win32 \_ BaseService.**](win32-baseservice.md)

</dd> <dt>

**State**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture del servizio Win32API \| SERVICE \| [**\_ STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwCurrentState "), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("State")
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

Questa proprietà viene ereditata da [**Win32 \_ BaseService.**](win32-baseservice.md)

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

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagati**](../wmisdk/standard-qualifiers.md) ("[**Sistema CIM \_**](cim-system.md).**CreationClassName**"), [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Class Name")
</dt> </dl>

Nome del sistema che ospita il servizio.

Questa proprietà viene ereditata dal [**servizio CIM \_**](cim-service.md).

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagati**](../wmisdk/standard-qualifiers.md) ("[**Sistema CIM \_**](cim-system.md).**Name**"), [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Name")
</dt> </dl>

Nome del sistema che ospita il servizio.

Questa proprietà viene ereditata dal [**servizio CIM \_**](cim-service.md).

</dd> <dt>

**TagId**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture del servizio Win32API \| QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwTagId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Tag Id")
</dt> </dl>

Valore di tag univoco per questo servizio nel gruppo. Il valore 0 (zero) indica che il servizio non dispone di un tag . È possibile usare un tag per ordinare l'avvio del servizio all'interno di un gruppo di ordini di caricamento specificando un vettore di ordine dei tag nel registro che si trova in:

**HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **GroupOrderList**    

I tag vengono valutati solo per i servizi del tipo di avvio del driver del kernel e del driver del file system con modalità di avvio o di avvio del sistema.

Questa proprietà viene ereditata da [**Win32 \_ BaseService.**](win32-baseservice.md)

</dd> <dt>

**WaitHint**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture del servizio Win32API \| SERVICE \| [**\_ STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwWaitHint"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Tempo di attesa stimato")
</dt> </dl>

Tempo stimato necessario, in millisecondi, per un'operazione di avvio, arresto, sospensione o continuazione in sospeso. Dopo che è trascorso il tempo specificato, il servizio effettua la chiamata successiva al metodo **SetServiceStatus** con un valore **CheckPoint** incrementato o una modifica in **CurrentState.** Se il tempo specificato da **WaitHint** passa e **CheckPoint** non è stato incrementato o **CurrentState** non è stato modificato, gestione controllo servizi o programma di controllo del servizio presuppone che si sia verificato un errore.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ del servizio Win32** è derivata da [**Win32 \_ BaseService.**](win32-baseservice.md)

Il modo in cui si gestisce un computer specifico dipende notevolmente dal ruolo del computer. Ad esempio, in genere si monitorano aspetti diversi di un server DNS rispetto a un server DHCP. Anche se nessuna singola proprietà può indicare se un computer specifico è un server di database, un server di posta elettronica o un server multimediale, è spesso possibile identificare il ruolo di un computer identificando i servizi installati.

Nelle organizzazioni di grandi dimensioni è probabile che in un singolo computer sia installato solo uno dei servizi principali, ad esempio la posta elettronica. Sarebbe insolito che un server di posta elettronica funzioni anche come server per i file del lettore microsoft® Windows Media® Technologies. Per questo scopo, l'identificazione di un servizio installato in un computer consente di identificare il ruolo del computer nella rete. Se il servizio Microsoft® Exchange Server è installato e in esecuzione in un computer, è in genere possibile presupporre che il computer funzioni come server di posta elettronica.

È possibile utilizzare la classe **Wmi Win32 \_ Service** per enumerare i servizi installati in un computer. Inoltre, è possibile utilizzare questa classe per determinare se tali servizi sono attualmente in esecuzione e per restituire eventuali altre informazioni necessarie su tale servizio e su come è stato configurato.

Un'applicazione di servizio è conforme alle regole di interfaccia di Gestione controllo servizi e può essere avviata automaticamente da un utente all'avvio del sistema tramite l'utilità del Pannello di controllo Servizi o da un'applicazione che usa le funzioni del servizio incluse nell'API Windows. I servizi possono essere avviati quando non sono presenti utenti connessi al computer.

Per poter enumerare questa classe, un utente che si connette da un computer remoto deve avere il privilegio **SC \_ MANAGER \_ CONNECT** abilitato. Per altre informazioni, vedere Sicurezza [del servizio e diritti di accesso.](../services/service-security-and-access-rights.md)

## <a name="examples"></a>Esempio

La query [WMI ps-che](https://Gallery.TechNet.Microsoft.Com/0f1ab629-d463-4406-be54-ec2c4c23bc1f) restituisce il servizio 'State' in un gruppo di dispositivi di esempio di PowerShell nella raccolta TechNet usa il servizio **\_ Win32** per creare un elenco di dispositivi da Active Directory e quindi eseguire una query su ogni dispositivo che risponde con ping per un servizio specifico in esecuzione.

[L'esempio di](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) PowerShell server report nella raccolta TechNet usa il servizio **Win32 \_** per raccogliere informazioni sul server e pubblicare nel documento di Word.

Nell'esempio di codice VBScript seguente vengono visualizzati tutti i servizi attualmente installati.


```VB
for each Service in _ 
    GetObject("winmgmts:").InstancesOf ("Win32_Service")
 WScript.Echo ""
 WScript.Echo Service.Name

 description = Service.Description 
 if IsNull(description) then description = "<No description>"

 pathName = Service.PathName
 if IsNull(pathName) then pathName = "<No path>"

 startName = Service.StartName
 if IsNull(startName) then startName = "<None>"

 WScript.Echo "  Description:  ", description
 WScript.Echo "  Executable:   ", pathName
 WScript.Echo "  Status:       ", Service.Status
 WScript.Echo "  State:        ", Service.State
 WScript.Echo "  Start Mode:   ", Service.StartMode
 Wscript.Echo "  Start Name:   ", startName
next
```



Nell'esempio di codice VBScript seguente vengono descritti i servizi sospesi, in esecuzione e arrestati nel computer specificato.


```VB
On Error Resume Next
 StateString = "Paused,Running,Stopped"
 StateArray = Split(StateString, ",", -1, 1) 
 ComputerName = InputBox("Enter the computer name", "List Service", "localhost")

 For x = 0 to Ubound (StateArray)
 Set Services = GetObject("winmgmts:\\" & ComputerName & "\Root\CIMv2").ExecQuery("SELECT * FROM Win32_Service where State='" & StateArray(x) & "'")
 
 For Each Service in Services
  SList = SList & Service.Name & VBlf 
 Next

 WScript.Echo StateArray(x) & " Services: " & VBlf & SList
 SList = ""

Next
```



Lo script Perl seguente illustra come recuperare un elenco di servizi in esecuzione dalle istanze del **servizio Win32. \_**


```
use strict;
use Win32::OLE;

my ( $ServiceSet, $Service );

eval { $ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\Root\\CIMv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE State=\"Running\""); };
unless ($@)
{
 print "\n";
 foreach $Service (in $ServiceSet) 
 {
  print $Service->{Name}, "\n";
  if( $Service->{Description} ) 
   {
    print "  $Service->{Description}\n";
   }
  else
   {
    print "  <No description>\n";
   }
  print "  Process ID: ", $Service->{ProcessId}, "\n";
  print "  Start Mode: ", $Service->{StartMode}, "\n";
  print "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



L'esempio c \# seguente [usa Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) per recuperare tutti i servizi in esecuzione nel computer locale.


```CSharp
static void QueryInstanceFunc()
        {
 
            CimSession session = CimSession.Create("localHost");
            IEnumerable<CimInstance> queryInstance = session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_Service");

            foreach (CimInstance cimObj in queryInstance)
            {
                Console.WriteLine(cimObj.CimInstanceProperties["Name"].ToString());
                Console.WriteLine(cimObj.CimInstanceProperties["State"].ToString());
                Console.WriteLine(cimObj.CimInstanceProperties["Status"].ToString());
                
                //Console.WriteLine(cimObj.CimInstanceProperties["NetworkAddress"].ToString());
                Console.WriteLine();

            }

            Console.ReadLine();
        }
    
```



Nell'esempio di codice C \# seguente viene utilizzato lo spazio dei nomi [System.Management](/dotnet/api/system.management) per recuperare tutti i servizi in esecuzione nel computer locale.

> [!Note]  
> [System.Management contiene](/dotnet/api/system.management) le classi originali usate per accedere a WMI. Tuttavia, sono considerati più lenti e in genere non vengono ridimensionati come le controparti [di Microsoft.Management.Infrastructure.](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85))

 


```CSharp
using System.Management;
...
        static void oldSchoolQueryInstanceFunc()
        {

            ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_Service");
            ManagementObjectSearcher searcher = new ManagementObjectSearcher(query);


            ManagementObjectCollection queryCollection = searcher.Get();
            foreach (ManagementObject m in queryCollection)
            {
                Console.WriteLine("ServiceName : {0}", m["Name"]);
                Console.WriteLine("State : {0}", m["State"]);
                Console.WriteLine("Status : {0}", m["Status"]);
                Console.WriteLine();
            }

            Console.ReadLine();


        }
```



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

[**Win32 \_ BaseService**](win32-baseservice.md)
</dt> <dt>

[Classi del sistema operativo](./operating-system-classes.md)
</dt> <dt>

[Attività WMI: Servizi](../wmisdk/wmi-tasks--services.md)
</dt> </dl>

 

 

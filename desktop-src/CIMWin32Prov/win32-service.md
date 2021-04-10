---
description: Rappresenta un servizio in un sistema di computer che esegue Windows.
ms.assetid: 713402d3-ee73-4a6c-afb9-ad8033a4c580
ms.tgt_platform: multiple
title: Classe Win32_Service
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
ms.openlocfilehash: b342282bfa3b49fe72e62cf79377a0ead11276eb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049109"
---
# <a name="win32_service-class"></a>\_Classe del servizio Win32

La [classe WMI](../wmisdk/retrieving-a-class.md) del **\_ servizio Win32** rappresenta un servizio in un computer in cui è in esecuzione Windows.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.

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

La classe del **\_ servizio Win32** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe del **\_ servizio Win32** presenta questi metodi.



| Metodo                                                                               | Descrizione                                                                                          |
|:-------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**Modificare**](change-method-in-class-win32-service.md)                               | Modifica un servizio.<br/>                                                                       |
| [**ChangeStartMode**](changestartmode-method-in-class-win32-service.md)             | Modifica la modalità di avvio di un servizio.<br/>                                                     |
| [**Creare**](create-method-in-class-win32-service.md)                               | Crea un nuovo servizio.<br/>                                                                    |
| [**Delete**](delete-method-in-class-win32-service.md)                               | Elimina un servizio esistente.<br/>                                                              |
| [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class-win32-service.md) | Restituisce il descrittore di sicurezza che controlla l'accesso al servizio.<br/>                      |
| [**InterrogateService**](interrogateservice-method-in-class-win32-service.md)       | Richiede che un servizio aggiorni lo stato a Service Manager.<br/>                          |
| [**PauseService**](pauseservice-method-in-class-win32-service.md)                   | Tenta di collocare un servizio in stato di sospensione.<br/>                                          |
| [**ResumeService**](resumeservice-method-in-class-win32-service.md)                 | Tenta di inserire un servizio nello stato ripresa.<br/>                                         |
| [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class-win32-service.md) | Scrive una versione aggiornata del descrittore di sicurezza che controlla l'accesso al servizio.<br/> |
| [**StartService**](startservice-method-in-class-win32-service.md)                   | Tenta di inserire un servizio nello stato di avvio.<br/>                                       |
| [**StopService**](stopservice-method-in-class-win32-service.md)                     | Inserisce un servizio nello stato interrotto.<br/>                                                    |
| [**UserControlService**](usercontrolservice-method-in-class-win32-service.md)       | Tenta di inviare un codice di controllo definito dall'utente a un servizio.<br/>                                |



 

### <a name="properties"></a>Proprietà

La classe del **\_ servizio Win32** dispone di queste proprietà.

<dl> <dt>

**AcceptPause**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API Service \| Structures Service \| [**\_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| DwControlsAccepted servizio \| \_ accettazione \_ pausa \_ continua"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("servizio accetta pausa")
</dt> </dl>

Indica se il servizio può essere sospeso.

Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**AcceptStop**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures Service \| [**\_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted servizio \| \_ Accept \_ Stop"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service accepts stop")
</dt> </dl>

Indica se il servizio può essere arrestato.

Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Breve descrizione del servizio, ovvero una stringa a una riga.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**CheckPoint**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| DwCheckPoint"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Check Point count")
</dt> </dl>

Valore che il servizio incrementa periodicamente per segnalare lo stato di avanzamento durante un'operazione di avvio, arresto, sospensione o continuazione Prolong. Il servizio, ad esempio, incrementa questo valore poiché completa ogni passaggio dell'inizializzazione all'avvio. Il programma dell'interfaccia utente che richiama l'operazione sul servizio utilizza questo valore per tenere traccia dello stato di avanzamento del servizio durante un'operazione di lunga durata. Questo valore non è valido e deve essere zero quando il servizio non dispone di un'operazione di avvio, arresto, pausa o continuazione in sospeso.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nome classe")
</dt> </dl>

Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata per la creazione di un'istanza. Se utilizzata con le altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.

Questa proprietà viene ereditata [**dal \_ servizio CIM**](cim-service.md).

</dd> <dt>

**DelayedAutoStart**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Service \_ Retarded \_ auto \_ Start \_ info**](/windows/win32/api/winsvc/ns-winsvc-service_delayed_auto_start_info) \| fDelayedAutostart"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("avvio automatico ritardato")
</dt> </dl>

Se **true**, il servizio viene avviato dopo l'avvio di altri servizi di avvio automatico più un breve ritardo.

**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Questa proprietà non è supportata prima di Windows Server 2016 e Windows 10.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Descrizione dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**DesktopInteract**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**query \_ Services \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType \| Service \_ Interactive \_ processo"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("interagisce con il desktop")
</dt> </dl>

Indica se il servizio è in grado di creare o comunicare con Windows sul desktop e quindi interagire in qualche modo con un utente. I servizi interattivi devono essere eseguiti con l'account di sistema locale. La maggior parte dei servizi non è interattiva; ovvero non comunicano con l'utente in alcun modo.

Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**DisplayName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**query \_ Service \_ Configuration**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| lpDisplayName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Display Name")
</dt> </dl>

Nome del servizio visualizzato nello snap-in servizi. La lunghezza massima della stringa è di 256 caratteri. Si noti che il nome visualizzato e il nome del servizio (archiviati nel registro di sistema) non sono sempre gli stessi. Il servizio client DHCP, ad esempio, ha il nome del servizio DHCP ma il nome visualizzato client DHCP. Il nome viene mantenuto con la distinzione tra maiuscole e minuscole in Gestione controllo servizi. Tuttavia, i confronti **DisplayName** sono sempre senza distinzione tra maiuscole e minuscole.

Constraint: accetta lo stesso valore della proprietà **Name** .

Esempio: "ATDISK"

Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**ErrorControl**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| DwErrorControl"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("gravità dell'avvio non riuscito")
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

Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**ExitCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("codice di uscita")
</dt> </dl>

Codice di errore di Windows che definisce gli errori riscontrati durante l'avvio o l'arresto del servizio. Questa proprietà è impostata sull' **\_ \_ \_ errore specifico del servizio di errore** (1066) quando l'errore è univoco per il servizio rappresentato da questa classe e le informazioni sull'errore sono disponibili nella proprietà **ServiceSpecificExitCode** . Il servizio imposta questo valore su **nessun \_ errore** durante l'esecuzione e di nuovo alla chiusura normale.

Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")
</dt> </dl>

L'oggetto data è installato. Questa proprietà non richiede un valore per indicare che l'oggetto è installato.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](../wmisdk/key-qualifier.md)
</dt> </dl>

Identificatore univoco del servizio che fornisce un'indicazione della funzionalità gestita. Questa funzionalità è descritta nella proprietà **Description** dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**PathName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| LpBinaryPathName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nome percorso file")
</dt> </dl>

Percorso completo del file binario del servizio che implementa il servizio.

Esempio: " \\ systemroot \\ system32 \\ drivers \\afd.sys"

Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**ProcessId**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Service \_ status \_ Process**](/windows/win32/api/winsvc/ns-winsvc-service_status_process) \| dwProcessId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("ID processo")
</dt> </dl>

Identificatore del processo del servizio.

Esempio: 324

</dd> <dt>

**ServiceSpecificExitCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwServiceSpecificExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("codice di uscita specifico del server")
</dt> </dl>

Codice di errore specifico del servizio per gli errori che si verificano durante l'avvio o l'arresto del servizio. I codici di uscita sono definiti dal servizio rappresentato da questa classe. Questo valore viene impostato solo quando il valore della proprietà **ExitCode** è **\_ \_ \_ errore specifico del servizio di errore** (1066).

Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**ServiceType**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| DwServiceType"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("tipo di servizio")
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

Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**Avviato**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Started")
</dt> </dl>

Indica se il servizio è stato avviato o meno.

Questa proprietà viene ereditata [**dal \_ servizio CIM**](cim-service.md).

</dd> <dt>

**Modalità avvio**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("modalità di avvio")
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

Servizio che deve essere avviato da Gestione controllo servizi quando un processo chiama il metodo [**StartService**](startservice-method-in-class-win32-service.md) . Questi servizi non vengono avviati, a meno che un utente non esegua l'accesso e li avvii.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** ("disabilitato")


</dt> <dd>

Servizio che non può essere avviato finché il relativo StartMode non viene modificato in auto o manuale.

</dd> </dl>

Questa proprietà viene ereditata [**dal \_ servizio CIM**](cim-service.md).

</dd> <dt>

**StartName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| LpServiceStartName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nome account iniziale")
</dt> </dl>

Nome dell'account con cui viene eseguito un servizio. A seconda del tipo di servizio, il nome dell'account può avere la forma di "DomainName \\ username" o del formato UPN (" *Username@DomainName* "). Il processo del servizio viene registrato utilizzando una di queste due forme durante l'esecuzione. Se l'account appartiene al dominio predefinito, ". \\ Nome utente "può essere specificato. Per i driver a livello di sistema o del kernel, **StartName** contiene il nome dell'oggetto driver, ovvero " \\ filesystem \\ RDR" o " \\ driver \\ XNS", utilizzato dal sistema i/O per caricare il driver di dispositivo. Inoltre, se si specifica **null** , il driver viene eseguito con un nome di oggetto predefinito creato dal sistema i/O in base al nome del servizio.

Esempio: "DWDOM \\ admin"

Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**State**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwCurrentState"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("state")
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

Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")
</dt> </dl>

Stato corrente dell'oggetto. È possibile definire diversi stati operativi e non operativi. Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro). Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service". Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative. Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

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

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome classe di sistema ")
</dt> </dl>

Nome del tipo di sistema che ospita il servizio.

Questa proprietà viene ereditata [**dal \_ servizio CIM**](cim-service.md).

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome sistema ")
</dt> </dl>

Nome del sistema che ospita il servizio.

Questa proprietà viene ereditata [**dal \_ servizio CIM**](cim-service.md).

</dd> <dt>

**TagId**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwTagId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("ID tag")
</dt> </dl>

Valore di tag univoco per il servizio nel gruppo. Il valore 0 (zero) indica che il servizio non dispone di un tag. Un tag può essere usato per ordinare l'avvio del servizio all'interno di un gruppo di ordini di caricamento specificando un vettore di ordine dei tag nel registro di sistema che si trova in:

**HKEY \_ Controllo CurrentControlSet del sistema del \_ computer locale** \\  \\  \\  \\ **GroupOrderList**    

I tag vengono valutati solo per i servizi del tipo di avvio del driver del kernel e del driver del file System con modalità avvio o sistema.

Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**WaitHint**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwWaitHint"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("tempo di attesa stimato")
</dt> </dl>

Tempo stimato necessario, in millisecondi, per un'operazione di avvio, arresto, sospensione o continuazione in sospeso. Dopo che è trascorso il tempo specificato, il servizio effettua la chiamata successiva al metodo **SetServiceStatus** con un valore di **Checkpoint** incrementato o una modifica in **CurrentState**. Se la quantità di tempo specificata da **WaitHint** passa e il **Checkpoint** non è stato incrementato oppure **CurrentState** non è stato modificato, gestione controllo servizi o il programma di controllo del servizio presuppone che si sia verificato un errore.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe del **\_ servizio Win32** è derivata da [**Win32 \_ BaseService**](win32-baseservice.md).

La modalità di gestione di un computer specifico dipende in larga misura dal ruolo svolto dal computer. Ad esempio, in genere si monitorano diversi aspetti di un server DNS rispetto a un server DHCP. Sebbene nessuna singola proprietà possa indicare se un determinato computer è un server di database, un server di posta elettronica o un server multimediale, è spesso possibile identificare il ruolo riprodotto da un computer identificando i servizi installati.

Nelle organizzazioni di grandi dimensioni è probabile che sia installato solo uno dei principali servizi, ad esempio la posta elettronica, in un singolo computer. Sarebbe insolito che un server di posta venga eseguito anche come server per i file di Microsoft® Windows Media® Technologies Player. Per questo motivo, l'identificazione di un servizio installato in un computer può consentire di identificare il ruolo del computer nella rete. Se il servizio Microsoft® Exchange Server è installato e in esecuzione in un computer, è in genere preferibile che questo computer funzioni come server di posta elettronica.

È possibile utilizzare la classe **del \_ servizio WMI Win32** per enumerare i servizi installati in un computer. Inoltre, è possibile usare questa classe per determinare se i servizi sono attualmente in esecuzione e per restituire qualsiasi altra informazione necessaria su tale servizio e su come è stato configurato.

Un'applicazione di servizio è conforme alle regole di interfaccia di gestione controllo servizi e può essere avviata automaticamente da un utente all'avvio del sistema tramite l'utilità pannello di controllo dei servizi o da un'applicazione che usa le funzioni del servizio incluse nell'API Windows. I servizi possono essere avviati quando nessun utente è connesso al computer.

Per poter enumerare questa classe, è necessario che un utente che si connette da un computer remoto disponga del privilegio **\_ \_ Gestione SC** . Per ulteriori informazioni, vedere [sicurezza del servizio e diritti di accesso](../services/service-security-and-access-rights.md).

## <a name="examples"></a>Esempio

La [query PS-WMI che restituisce il servizio "stato" in un gruppo di dispositivi esempio di](https://Gallery.TechNet.Microsoft.Com/0f1ab629-d463-4406-be54-ec2c4c23bc1f) PowerShell nella raccolta TechNet usa il **\_ servizio Win32** per creare un elenco di dispositivi da Active Directory, quindi esegue una query su ogni dispositivo che risponde con pingfor a un servizio specifico in esecuzione.

L'esempio di PowerShell per il [report del server](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) nella raccolta TechNet usa il **\_ servizio Win32** per raccogliere le informazioni sul server e pubblicarle nel documento di Word.

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



Nell'esempio di codice VBScript seguente vengono descritti i servizi sospesi, in esecuzione e interrotti nel computer specificato.


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



Nello script Perl seguente viene illustrato come recuperare un elenco di servizi in esecuzione da istanze **del \_ servizio Win32**.


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



Nell'esempio c seguente \# viene usato [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) per recuperare tutti i servizi in esecuzione nel computer locale.


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



Nell' \# esempio di codice C seguente viene usato lo spazio dei nomi [System. Management](/dotnet/api/system.management) per recuperare tutti i servizi in esecuzione nel computer locale.

> [!Note]  
> [System. Management](/dotnet/api/system.management) contiene le classi originali utilizzate per accedere a WMI. Tuttavia, sono considerate più lente e in genere non vengono ridimensionate, nonché le controparti [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) .

 


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
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_BaseService Win32**](win32-baseservice.md)
</dt> <dt>

[Classi del sistema operativo](./operating-system-classes.md)
</dt> <dt>

[Attività WMI: Servizi](../wmisdk/wmi-tasks--services.md)
</dt> </dl>

 

 

---
description: Rappresenta il driver di sistema per un servizio di base.
ms.assetid: 67dc6e14-c8c1-4168-8f99-b04c6ecd4ad2
ms.tgt_platform: multiple
title: Classe Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver
- Win32_SystemDriver.AcceptPause
- Win32_SystemDriver.AcceptStop
- Win32_SystemDriver.Caption
- Win32_SystemDriver.CreationClassName
- Win32_SystemDriver.Description
- Win32_SystemDriver.DesktopInteract
- Win32_SystemDriver.DisplayName
- Win32_SystemDriver.ErrorControl
- Win32_SystemDriver.ExitCode
- Win32_SystemDriver.InstallDate
- Win32_SystemDriver.Name
- Win32_SystemDriver.PathName
- Win32_SystemDriver.ServiceSpecificExitCode
- Win32_SystemDriver.ServiceType
- Win32_SystemDriver.Started
- Win32_SystemDriver.StartMode
- Win32_SystemDriver.StartName
- Win32_SystemDriver.State
- Win32_SystemDriver.Status
- Win32_SystemDriver.SystemCreationClassName
- Win32_SystemDriver.SystemName
- Win32_SystemDriver.TagId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15be9b176680e8abb259d3d011da9d6cec0c2fa8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748402"
---
# <a name="win32_systemdriver-class"></a>Win32 \_ SystemDriver (classe)

La  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ SystemDriver Win32** rappresenta il driver di sistema per un servizio di base.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4C5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemDriver : Win32_BaseService
{
  boolean  AcceptPause;
  boolean  AcceptStop;
  string   Caption;
  string   CreationClassName;
  string   Description;
  boolean  DesktopInteract;
  string   DisplayName;
  string   ErrorControl;
  uint32   ExitCode;
  datetime InstallDate;
  string   Name;
  string   PathName;
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
};
```

## <a name="members"></a>Members

La classe **Win32 \_ SystemDriver** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **Win32 \_ SystemDriver** presenta questi metodi.



| Metodo                                                                              | Descrizione                                                                                     |
|:------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**Modificare**](change-method-in-class-win32-systemdriver.md)                         | Metodo della classe che modifica un servizio.<br/>                                                |
| [**ChangeStartMode**](changestartmode-method-in-class-win32-systemdriver.md)       | Metodo della classe che modifica la modalità di avvio di un servizio.<br/>                              |
| [**Creare**](create-method-in-class-win32-systemdriver.md)                         | Metodo della classe che crea un nuovo servizio.<br/>                                             |
| [**Delete**](delete-method-in-class-win32-systemdriver.md)                         | Metodo della classe che elimina un servizio esistente.<br/>                                       |
| [**InterrogateService**](interrogateservice-method-in-class-win32-systemdriver.md) | Metodo della classe che richiede che il servizio aggiorni lo stato a Service Manager.<br/> |
| [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md)             | Metodo della classe che tenta di collocare il servizio nello stato sospeso.<br/>                 |
| [**ResumeService**](resumeservice-method-in-class-win32-systemdriver.md)           | Metodo della classe che tenta di collocare il servizio nello stato ripreso.<br/>                |
| [**StartService**](startservice-method-in-class-win32-systemdriver.md)             | Metodo della classe che tenta di collocare il servizio nello stato di avvio.<br/>              |
| [**StopService**](stopservice-method-in-class-win32-systemdriver.md)               | Metodo della classe che inserisce il servizio nello stato interrotto.<br/>                           |
| [**UserControlService**](usercontrolservice-method-in-class-win32-systemdriver.md) | Metodo della classe che tenta di inviare un codice di controllo definito dall'utente a un servizio.<br/>         |



 

### <a name="properties"></a>Proprietà

La classe **Win32 \_ SystemDriver** dispone di queste proprietà.

<dl> <dt>

**AcceptPause**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API Service \| Structures Service \| [**\_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| DwControlsAccepted servizio \| \_ accettazione \_ pausa \_ continua"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("servizio accetta pausa")
</dt> </dl>

Il servizio può essere sospeso.

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

Il servizio può essere arrestato.

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

Breve descrizione dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

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

Questo servizio può creare o comunicare con Windows sul desktop.

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

Nome visualizzato del servizio. La lunghezza massima della stringa è di 256 caratteri. Il nome viene mantenuto con la distinzione tra maiuscole e minuscole in Gestione controllo servizi. I confronti **DisplayName** sono sempre senza distinzione tra maiuscole e minuscole.

Constraints: accetta lo stesso valore della proprietà **Name** .

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

Gravità dell'errore se il servizio non viene avviato durante l'avvio. Questo valore indica l'azione eseguita dal programma di avvio in caso di errore. Tutti gli errori vengono registrati dal computer.

Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignora** ("Ignora")


</dt> <dd>

L'utente non viene notificato.

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normale** ("normale")


</dt> <dd>

L'utente viene notificato.

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** ("grave")


</dt> <dd>

Il sistema viene riavviato con l'ultima configurazione valida nota.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critico** ("critico")


</dt> <dd>

Il sistema tenta un riavvio con una configurazione valida.

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** ("sconosciuto")


</dt> <dd>

La cause dell'errore è sconosciuta.

</dd> </dl>

</dd> <dt>

**ExitCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("codice di uscita")
</dt> </dl>

Codice di errore di Windows che definisce eventuali problemi riscontrati durante l'avvio o l'arresto del servizio. Questa proprietà è impostata sull' **\_ \_ \_ errore specifico del servizio di errore** (1066) quando l'errore è univoco per il servizio rappresentato da questa classe e le informazioni sull'errore sono disponibili nella proprietà **ServiceSpecificExitCode** . Il servizio imposta questo valore su **nessun \_ errore** durante l'esecuzione e di nuovo alla chiusura normale.

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

L'oggetto è stato installato. Questa proprietà non richiede un valore per indicare che l'oggetto è installato.

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

Identificatore univoco per il servizio che fornisce un'indicazione della funzionalità gestita. Questa funzionalità è descritta più dettagliatamente nella proprietà **Description** dell'oggetto.

Questa proprietà viene ereditata [**dal \_ servizio CIM**](cim-service.md).

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

Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).

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

</dd> <dt>

**Avviato**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Started")
</dt> </dl>

Il servizio è stato avviato.

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

Modalità di avvio del driver di sistema.

Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).

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

Servizio da avviare automaticamente da Gestione controllo servizi durante l'avvio del sistema.

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuale** ("manuale")


</dt> <dd>

Servizio che deve essere avviato da Gestione controllo servizi quando un processo chiama il metodo [**StartService**](startservice-method-in-class-win32-systemdriver.md) .

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** ("disabilitato")


</dt> <dd>

Servizio che non può più essere avviato.

</dd> </dl>

</dd> <dt>

**StartName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| LpServiceStartName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nome account iniziale")
</dt> </dl>

Nome dell'account con cui viene eseguito il servizio. A seconda del tipo di servizio, il nome dell'account può essere nel formato DomainName \\ username. Il processo del servizio verrà registrato utilizzando una di queste due forme durante l'esecuzione. Se l'account appartiene al dominio predefinito,. \\ È possibile specificare il nome utente. Se viene specificato **null** , il servizio verrà connesso come account LocalSystem. Per i driver a livello di kernel o di sistema, **StartName** contiene il nome dell'oggetto driver, ovvero \\ filesystem \\ RDR o \\ driver \\ XNS, usato dal sistema di input e output (i/O) per caricare il driver di dispositivo. Inoltre, se si specifica **null** , il driver viene eseguito con un nome di oggetto predefinito creato dal sistema i/O in base al nome del servizio.

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

Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).

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

Valore di tag univoco per il servizio nel gruppo. Il valore 0 (zero) indica che al servizio non è stato assegnato un tag. Un tag può essere usato per ordinare l'avvio del servizio all'interno di un gruppo di ordini di caricamento specificando un vettore di ordine dei tag nel registro di sistema che si trova in:

Questa proprietà viene ereditata da [**Win32 \_ BaseService**](win32-baseservice.md).

**HKEY \_ \_GroupOrderList del \\ \\ \\ \\ controllo del sistema CurrentControlSet del computer locale**.

I tag vengono valutati solo per i servizi del driver del kernel e del driver del file System di avvio con modalità di avvio o di avvio del sistema.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ SystemDriver** è derivata da [**Win32 \_ BaseService**](win32-baseservice.md).

## <a name="examples"></a>Esempio

Nell'esempio [elenco driver di sistema](https://Gallery.TechNet.Microsoft.Com/5629cc13-cefc-4e51-a24f-aac6db23d141) VBScript vengono visualizzati i driver di sistema installati in un file HTML.

Nell'esempio di PowerShell seguente vengono recuperate alcune proprietà dai driver di sistema in esecuzione in un computer.


```PowerShell
Get-WmiObject -Class Win32_SystemDriver | Where-Object -FilterScript {$_.State -eq "Running"} | Where-Object -FilterScript {$_.StartMode -eq "Manual"} | Format-Table -Property Name,DisplayName
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
</dt> </dl>

 

 

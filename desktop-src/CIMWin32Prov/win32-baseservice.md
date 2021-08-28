---
description: La classe WMI astratta Win32 BaseService rappresenta gli oggetti eseguibili installati in un database del Registro di sistema \_ gestito da Gestione controllo servizi.
ms.assetid: 63673df9-3e41-4668-98fe-dc0e048328c1
ms.tgt_platform: multiple
title: Win32_BaseService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService
- Win32_BaseService.AcceptPause
- Win32_BaseService.AcceptStop
- Win32_BaseService.Caption
- Win32_BaseService.CreationClassName
- Win32_BaseService.Description
- Win32_BaseService.DesktopInteract
- Win32_BaseService.DisplayName
- Win32_BaseService.ErrorControl
- Win32_BaseService.ExitCode
- Win32_BaseService.InstallDate
- Win32_BaseService.Name
- Win32_BaseService.PathName
- Win32_BaseService.ServiceSpecificExitCode
- Win32_BaseService.ServiceType
- Win32_BaseService.Started
- Win32_BaseService.StartMode
- Win32_BaseService.StartName
- Win32_BaseService.State
- Win32_BaseService.Status
- Win32_BaseService.SystemCreationClassName
- Win32_BaseService.SystemName
- Win32_BaseService.TagId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b2ce4673b6739639475264f79a60a7fd1b1c7bc5a0f16153d22305a77812759a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119504371"
---
# <a name="win32_baseservice-class"></a>Classe BaseService Win32 \_

La classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **astratta \_ Win32 BaseService** rappresenta gli oggetti eseguibili installati in un database del Registro di sistema gestito da Gestione controllo servizi. Il file eseguibile associato a un servizio può essere avviato in fase di avvio da un programma di avvio o dal sistema. Può anche essere avviato su richiesta da Gestione controllo servizi. Qualsiasi servizio o processo che non appartiene a un utente specifico e che fornisce un'interfaccia per alcune funzionalità supportate dal sistema informatico, è un discendente (o membro) di questa classe.

Esempio: servizio client DHCP (Dynamic Host Configuration Protocol) in un computer che esegue Windows Server.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), Abstract, Provider("CIMWin32"), UUID("{8502C4C4-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("System Drivers and Services"), AMENDMENT]
class Win32_BaseService : CIM_Service
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

La **classe \_ BaseService Win32** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ BaseService Win32** include questi metodi.



| Metodo                                                                             | Descrizione                                                                   |
|:-----------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**Cambiare**](change-method-in-class-win32-baseservice.md)                         | Modifica un servizio.<br/>                                                |
| [**ChangeStartMode**](changestartmode-method-in-class-win32-baseservice.md)       | Modifica la modalità di avvio di un servizio.<br/>                              |
| [**Crea**](create-method-in-class-win32-baseservice.md)                         | Crea un nuovo servizio.<br/>                                             |
| [**Elimina**](delete-method-in-class-win32-baseservice.md)                         | Elimina un servizio esistente.<br/>                                       |
| [**InterrogateService**](interrogateservice-method-in-class-win32-baseservice.md) | Richiede che il servizio aggiornerne lo stato a Service Manager.<br/> |
| [**PauseService**](pauseservice-method-in-class-win32-baseservice.md)             | Esegue un tentativo di sospensione del servizio.<br/>                 |
| [**ResumeService**](resumeservice-method-in-class-win32-baseservice.md)           | Esegue un tentativo di ripresa del servizio.<br/>                |
| [**Startservice**](startservice-method-in-class-win32-baseservice.md)             | Tenta di inserire il servizio nello stato di avvio.<br/>              |
| [**StopService**](stopservice-method-in-class-win32-baseservice.md)               | Metodo della classe che posiziona il servizio nello stato arrestato.<br/>         |
| [**UserControlService**](usercontrolservice-method-in-class-win32-baseservice.md) | Tenta di inviare un codice di controllo definito dall'utente a un servizio.<br/>         |



 

### <a name="properties"></a>Proprietà

La **classe \_ BaseService Win32** ha queste proprietà.

<dl> <dt>

**AcceptPause**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Strutture del servizio Win32API \| SERVICE \| [**\_ STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| SERVICE ACCEPT PAUSE \_ \_ \_ CONTINUE"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accepts Pause")
</dt> </dl>

Il servizio può essere sospeso.

</dd> <dt>

**AcceptStop**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Strutture del servizio Win32API \| SERVICE \| [**\_ STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| SERVICE ACCEPT \_ \_ STOP"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accepts Stop")
</dt> </dl>

Il servizio può essere arrestato.

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Breve descrizione dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**CIM \_ Key,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")
</dt> </dl>

Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata nella creazione di un'istanza. Se usata con le altre proprietà chiave della classe , la proprietà consente l'identificazione univoca di tutte le istanze di questa classe e delle relative sottoclassi.

Questa proprietà viene ereditata dal [**servizio CIM. \_**](cim-service.md)

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
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

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Strutture del servizio Win32API \| QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType \| SERVICE INTERACTIVE \_ \_ PROCESS"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Interagisce con desktop")
</dt> </dl>

Il servizio può creare o comunicare con le finestre sul desktop.

</dd> <dt>

**DisplayName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Strutture del servizio Win32API \| QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpDisplayName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nome visualizzato")
</dt> </dl>

Nome visualizzato del servizio. La lunghezza massima della stringa è di 256 caratteri. Il nome viene mantenuto senza distinzione tra maiuscole e minuscole in Gestione controllo servizi. Nei confronti di **DisplayName non** viene sempre fatto distinzione tra maiuscole e minuscole.

Vincoli: accetta lo stesso valore della **proprietà** Name.

Esempio: "Atdisk"

</dd> <dt>

**ErrorControl**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Strutture del servizio Win32API \| QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwErrorControl"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Gravità dell'errore di avvio")
</dt> </dl>

Gravità dell'errore. Non è possibile avviare il servizio. Il valore indica l'azione eseguita dal programma di avvio in caso di errore. Tutti gli errori vengono registrati dal computer.

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignora** ("Ignora")


</dt> <dd>

L'utente non viene notificato.

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normale** ("Normale")


</dt> <dd>

L'utente viene notificato.

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** ("Grave")


</dt> <dd>

Il sistema è stato riavviato con l'ultima configurazione valida nota.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critico** ("Critico")


</dt> <dd>

Il sistema tenta un riavvio con una configurazione valida.

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** ("Sconosciuto")


</dt> <dd>

L'azione eseguita non è specificata.

</dd> </dl>

</dd> <dt>

**Codice di uscita**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Strutture del servizio Win32API \| SERVICE \| [**\_ STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Exit Code")
</dt> </dl>

Definizione di eventuali problemi riscontrati durante l'avvio o l'arresto del servizio. Questa proprietà è impostata su **ERROR \_ SERVICE SPECIFIC \_ \_ ERROR** (1066) quando l'errore è univoco per il servizio rappresentato da questa classe e le informazioni sull'errore sono disponibili nella **proprietà ServiceSpecificExitCode.** Il servizio imposta questo valore su **NO \_ ERROR durante** l'esecuzione e di nuovo al termine normale.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")
</dt> </dl>

L'oggetto è stato installato. Questa proprietà non richiede un valore per indicare che l'oggetto è installato.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **Chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identificatore univoco del servizio, che fornisce un'indicazione della funzionalità gestita. Questa funzionalità è descritta in modo più dettagliato nella proprietà **Description dell'oggetto.**

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**PathName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Strutture del servizio Win32API \| QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpBinaryPathName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nome percorso file")
</dt> </dl>

Percorso completo del file binario del servizio che implementa il servizio.

Esempio: \\ "SystemRoot \\ System32 \\ drivers \\afd.sys"

</dd> <dt>

**ServiceSpecificExitCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Strutture del servizio Win32API \| SERVICE \| [**\_ STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwServiceSpecificExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Codice di uscita specifico del server")
</dt> </dl>

Codice di errore specifico del servizio per gli errori che si verificano durante l'avvio o l'arresto del servizio. I codici di uscita sono definiti dal servizio rappresentato da questa classe. Questo valore viene impostato solo quando il **valore della proprietà ExitCode è** ERROR SERVICE SPECIFIC **\_ \_ \_ ERROR** (1066).

</dd> <dt>

**ServiceType**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Strutture del servizio Win32API \| QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tipo di servizio")
</dt> </dl>

Servizio fornito ai processi chiamanti.

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

</dd> <dt>

**Avviato**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")
</dt> </dl>

Il servizio è stato avviato.

Questa proprietà viene ereditata dal [**servizio CIM \_**](cim-service.md).

</dd> <dt>

**Modalità avvio**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("StartMode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Modalità di avvio")
</dt> </dl>

Modalità di avvio del Windows di base.

Questa proprietà viene ereditata dal [**servizio CIM \_**](cim-service.md).

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

Servizio che deve essere avviato automaticamente da Gestione controllo servizi durante l'avvio del sistema.

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuale** ("Manuale")


</dt> <dd>

Servizio che deve essere avviato da Gestione controllo servizi quando un processo chiama il [**metodo StartService.**](startservice-method-in-class-win32-baseservice.md)

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")


</dt> <dd>

Servizio che non può più essere avviato.

</dd> </dl>

</dd> <dt>

**StartName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Strutture del servizio Win32API \| QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpServiceStartName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nome account iniziale")
</dt> </dl>

Nome dell'account con cui viene eseguito il servizio. A seconda del tipo di servizio, il nome dell'account può essere nel formato "NomeDominioNomeUtente" o \\ nel formato UPN ( Username@DomainName ). Il processo del servizio verrà registrato usando uno di questi due formati durante l'esecuzione. Se l'account appartiene al dominio predefinito, ". \\ Username" può essere specificato. Se viene specificato **NULL,** il servizio verrà connesso come account LocalSystem. Per i driver a livello di kernel o di sistema, **StartName** contiene il nome dell'oggetto driver (ovvero FileSystem Rdr o Driver Xns) che il sistema di input e \\ output \\ \\ (I/O) usa per caricare il driver di \\ dispositivo. Inoltre, se viene **specificato NULL,** il driver viene eseguito con un nome di oggetto predefinito creato dal sistema di I/O in base al nome del servizio. Esempio: "DWDOM \\ Admin".

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

**Windows Server 2008 e Windows Vista:** Questa proprietà è di sola lettura.

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

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Sistema CIM \_**](cim-system.md).**CreationClassName**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Class Name")
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

Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Sistema CIM \_**](cim-system.md).**Name**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Name")
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

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Strutture del servizio Win32API \| QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwTagId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tag Id")
</dt> </dl>

Valore di tag univoco per questo servizio nel gruppo. Il valore 0 (zero) indica che al servizio non è stato assegnato un tag. È possibile usare un tag per ordinare la stella del servizio all'interno di un gruppo di ordini di caricamento specificando un vettore di ordine dei tag nel Registro di sistema disponibile in: HKEY \_ LOCAL \_ MACHINE System \\ \\ CurrentControlSet \\ Control \\ GroupOrderList. I tag vengono valutati solo per i servizi di tipo avvio driver kernel e driver del file system con modalità di avvio o di avvio del sistema.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ Win32 BaseService** è derivata dal [**servizio CIM \_**](cim-service.md).

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

[**Servizio \_ CIM**](cim-service.md)
</dt> <dt>

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 


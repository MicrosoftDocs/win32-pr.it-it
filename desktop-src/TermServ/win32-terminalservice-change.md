---
title: Modificare il metodo della Win32_Service classe (Mbnapi.h) (TerminalService)
description: Modifica un \_ terminalService Win32.
ms.assetid: 19E43A80-47C9-4C5A-8E73-723F206AA7C0
ms.tgt_platform: multiple
keywords:
- Modificare il metodo Servizi Desktop remoto
- Modificare il metodo Servizi Desktop remoto , Win32_Service classe
- Win32_Service classe Servizi Desktop remoto , metodo Change
topic_type:
- apiref
api_name:
- Win32_Service.Change
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c10e8c7b0a26ce2ca1e602478a64a888a1ad6b299f8ab7965303832bba7a3fc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118604433"
---
# <a name="change-method-of-the-win32_service-class-mbnapih---terminalservice"></a>Modificare il metodo della Win32_Service classe (Mbnapi.h) - TerminalService

Il **metodo Change** WMI [class](/windows/desktop/WmiSdk/retrieving-a-class) modifica un oggetto [**\_ TerminalService Win32.**](win32-terminalservice.md)

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 Change(
  [in] string  DisplayName,
  [in] string  PathName,
  [in] uint32  ServiceType,
  [in] uint32  ErrorControl,
  [in] string  StartMode,
  [in] boolean DesktopInteract,
  [in] string  StartName,
  [in] string  StartPassword,
  [in] string  LoadOrderGroup,
  [in] string  LoadOrderGroupDependencies,
  [in] string  ServiceDependencies
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DisplayName* \[ Pollici\]
</dt> <dd>

Nome visualizzato del servizio. La lunghezza massima della stringa è di 256 caratteri. Il nome viene mantenuto senza distinzione tra maiuscole e minuscole in Gestione controllo servizi. *Per i confronti displayName* non viene sempre fatto distinzione tra maiuscole e minuscole.

Vincoli: accetta lo stesso valore della **proprietà** Name.

Ad esempio, "Atdisk".

</dd> <dt>

*PathName* \[ Pollici\]
</dt> <dd>

Percorso completo del file eseguibile che implementa il servizio, ad esempio " \\ SystemRoot \\ System32 \\ drivers \\afd.sys".

</dd> <dt>

*ServiceType* \[ Pollici\]
</dt> <dd>

Tipo di servizi forniti ai processi che li chiamano.

<dt>

1 (0x1)
</dt> <dd>

Kernel Driver

</dd> <dt>

2 (0x2)
</dt> <dd>

File System Driver

</dd> <dt>

4 (0x4)
</dt> <dd>

Adattatore

</dd> <dt>

8 (0x8)
</dt> <dd>

Driver di riconoscimento

</dd> <dt>

16 (0x10)
</dt> <dd>

Processo personalizzato

</dd> <dt>

32 (0x20)
</dt> <dd>

Processo di condivisione

</dd> <dt>

256 (0x100)
</dt> <dd>

Processo interattivo

</dd> </dl> </dd> <dt>

*ErrorControl* \[ Pollici\]
</dt> <dd>

Gravità dell'errore se il servizio non viene avviato durante l'avvio. Il valore indica l'azione eseguita dal programma di avvio in caso di errore. Tutti gli errori vengono registrati dal sistema.

<dt>

0
</dt> <dd>

**Ignore**. L'avvio continua. All'utente non viene inviata alcuna notifica che indica che il servizio non è riuscito.

</dd> <dt>

1
</dt> <dd>

**Normale.** L'avvio continua. Prima dell'accesso dell'utente, l'utente riceve la notifica "Almeno un servizio o dispositivo ha avuto esito negativo durante l'avvio".

</dd> <dt>

2
</dt> <dd>

**Severa.** Il computer tenta di riavviare con l'ultima configurazione valida nota. Se il servizio non riesce di nuovo, l'avvio continua e viene inviata una notifica all'utente.

</dd> <dt>

3
</dt> <dd>

**Critico.** Il computer tenta di riavviare con l'ultima configurazione valida nota. Se il servizio ha nuovamente esito negativo, l'avvio si arresta.

</dd> </dl> </dd> <dt>

*StartMode* \[ Pollici\]
</dt> <dd>

Modalità di avvio del Windows di base. Per altre informazioni, vedere la sezione Osservazioni.

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Avvio**


</dt> <dd>

Driver di dispositivo avviato dal caricatore del sistema operativo.

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema**


</dt> <dd>

Driver di dispositivo avviato dal processo di inizializzazione del sistema operativo. Questo valore è valido solo per i servizi del driver.

</dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatico**


</dt> <dd>

Il servizio viene avviato automaticamente da Gestione controllo servizi durante l'avvio del sistema. I servizi di avvio automatico vengono avviati prima che un utente ese venga eseguito anche se nessun utente accede al computer.

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuale**


</dt> <dd>

Servizio che deve essere avviato da Gestione controllo servizi quando un processo chiama il [**metodo StartService.**](win32-terminalservice-startservice.md) Anche se i servizi manuali devono essere avviati in modo specifico da un utente (o da uno script), continuano a essere eseguiti anche se l'utente si disconnette. I servizi manuali vengono spesso definiti servizi su richiesta.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabili**


</dt> <dd>

Servizio che non può più essere avviato. Per avviare un servizio disabilitato, è prima necessario modificare l'opzione di avvio in Automatico o Manuale.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ Pollici\]
</dt> <dd>

Se **True,** il servizio può creare o comunicare con una finestra sul desktop.

</dd> <dt>

*StartName* \[ Pollici\]
</dt> <dd>

Nome dell'account con cui viene eseguito il servizio. A seconda del tipo di servizio, il nome dell'account può essere nel formato \\ NomeDominioNomeUtente o . \\ Nome utente. Il processo del servizio verrà registrato usando uno di questi due formati durante l'esecuzione. Se l'account appartiene al dominio predefinito, . \\ È possibile specificare il nome utente. Se viene specificato **NULL,** il servizio verrà connesso come account LocalSystem. Per i driver a livello di kernel o di sistema, *StartName* contiene il nome dell'oggetto driver (ovvero FileSystem Rdr o Driver Xns) che il sistema di input e \\ output \\ \\ (I/O) usa per caricare il driver di \\ dispositivo. Se viene specificato **NULL,** il driver viene eseguito con un nome di oggetto predefinito creato dal sistema di I/O in base al nome del servizio, ad esempio "DWDOM \\ Admin".

È anche possibile usare il formato nome dell'entità utente (UPN) per specificare **startName,** ad esempio *Username@DomainName* .

</dd> <dt>

*StartPassword* \[ Pollici\]
</dt> <dd>

Password per il nome dell'account specificato dal *parametro StartName.* Specificare **NULL** se la password non viene cambiata. Specificare una stringa vuota se il servizio non dispone di password.

> [!Note]  
> Quando si modifica un servizio da un sistema locale a una rete o da una rete a un sistema locale, *StartPassword* deve essere una stringa vuota ("") e non **NULL.**

 

</dd> <dt>

*LoadOrderGroup* \[ Pollici\]
</dt> <dd>

Nome del gruppo a cui è associato. I gruppi degli ordini di carico sono contenuti nel Registro di sistema e determinano la sequenza in cui i servizi vengono caricati nel sistema operativo. Se il puntatore **è NULL** o se punta a una stringa vuota, il servizio non appartiene a un gruppo. Per altre informazioni, vedere la sezione Osservazioni.

Le dipendenze tra gruppi devono essere elencate nel *parametro LoadOrderGroupDependencies.* I servizi nell'elenco dei gruppi di ordinamento del carico vengono avviati per primi, seguiti dai servizi in gruppi non presenti nell'elenco di gruppi di ordinamento del carico, seguiti dai servizi che non appartengono a un gruppo. Il Registro di sistema include un elenco di gruppi di ordinamento del carico disponibili in:

**HKEY \_ Local \_ MACHINE System** \\  \\ **CurrentControlSet** \\ **Control** \\ **ServiceGroupOrder**

</dd> <dt>

*Dipendenze di LoadOrderGroupDependencies* \[ Pollici\]
</dt> <dd>

Elenco di gruppi di ordinamento del carico che devono essere avviati prima dell'avvio del servizio. La matrice è doppiamente **null**-terminated. Se il puntatore **è NULL** o punta a una stringa vuota, il servizio non ha dipendenze. I nomi dei gruppi devono essere preceduti dal carattere **SC \_ GROUP \_ IDENTIFIER** (definito nel file Winsvc.h) per differenziarli dai nomi dei servizi perché i servizi e i gruppi di servizi condividono lo stesso spazio dei nomi. La dipendenza da un gruppo indica che questo servizio può essere eseguito se almeno un membro del gruppo è in esecuzione dopo un tentativo di avviare tutti i membri del gruppo.

</dd> <dt>

*Dipendenze dei servizi* \[ Pollici\]
</dt> <dd>

Elenco contenente i nomi dei servizi che devono essere avviati prima dell'avvio del servizio. La matrice è doppiamente **NULL**-terminated. Se il puntatore **è NULL** o punta a una stringa vuota, il servizio non ha dipendenze. La dipendenza da un servizio indica che questo servizio può essere eseguito solo se il servizio da cui dipende è in esecuzione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore. Per altri codici di errore, vedere [**Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [Codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**0**
</dt> <dd>

La richiesta è stata accettata.

</dd> <dt>

**1**
</dt> <dd>

La richiesta non è supportata.

</dd> <dt>

**2**
</dt> <dd>

L'utente non dispone dell'accesso necessario.

</dd> <dt>

**3**
</dt> <dd>

Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.

</dd> <dt>

**4**
</dt> <dd>

Il codice di controllo richiesto non è valido o non è accettabile per il servizio.

</dd> <dt>

**5**
</dt> <dd>

Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** ) è uguale a 0, 1 o 2.

</dd> <dt>

**6**
</dt> <dd>

Il servizio non è stato avviato.

</dd> <dt>

**7**
</dt> <dd>

Il servizio non ha risposto in tempo utile alla richiesta di avvio.

</dd> <dt>

**8**
</dt> <dd>

Errore sconosciuto durante l'avvio del servizio.

</dd> <dt>

**9**
</dt> <dd>

Impossibile trovare il percorso della directory del file eseguibile del servizio.

</dd> <dt>

**10**
</dt> <dd>

Il servizio è già in esecuzione.

</dd> <dt>

**11**
</dt> <dd>

Il database a cui aggiungere il nuovo servizio è bloccato.

</dd> <dt>

**12**
</dt> <dd>

Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.

</dd> <dt>

**13**
</dt> <dd>

Impossibile trovare un servizio dipendente necessario.

</dd> <dt>

**14**
</dt> <dd>

Il servizio è stato disabilitato dal sistema.

</dd> <dt>

**15**
</dt> <dd>

Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.

</dd> <dt>

**16**
</dt> <dd>

Questo servizio viene rimosso dal sistema.

</dd> <dt>

**17**
</dt> <dd>

Il servizio non ha thread di esecuzione.

</dd> <dt>

**18**
</dt> <dd>

Il servizio ha dipendenze circolari all'avvio.

</dd> <dt>

**19**
</dt> <dd>

Un servizio è in esecuzione con lo stesso nome.

</dd> <dt>

**20**
</dt> <dd>

Il nome del servizio contiene caratteri non validi.

</dd> <dt>

**21**
</dt> <dd>

Al servizio sono stati passati parametri non validi.

</dd> <dt>

**22**
</dt> <dd>

L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni per eseguire il servizio.

</dd> <dt>

**23**
</dt> <dd>

Il servizio esiste già nel database dei servizi disponibili dal sistema.

</dd> <dt>

**24**
</dt> <dd>

Il servizio è attualmente sospeso nel sistema.

</dd> </dl>

## <a name="remarks"></a>Commenti

All'avvio di un computer vengono avviati anche tutti i servizi di avvio automatico. In alcuni casi, uno di questi servizi potrebbe non essere avviato insieme al computer. Quando un servizio ha esito negativo durante l'avvio del sistema, il computer esegue un'azione in base al valore del codice di controllo degli errori del servizio.

la maggior parte dei servizi viene installata usando il codice di controllo degli errori normale. Alcune delle eccezioni, che vengono installate usando il codice di errore Ignora, includono:

-   Servizio Replica file
-   Smart card
-   Accesso secondario
-   WMI

Per i servizi installati usando il codice di errore Ignora, non viene inviata alcuna notifica all'utente che il servizio ha avuto esito negativo. Se si preferisce la notifica su schermo che non è stato possibile avviare un servizio, è possibile usare WMI per modificare il codice di controllo degli errori. I codici di controllo degli errori si applicano solo all'avvio del computer. I codici di controllo degli errori non vengono usati se si arresta e quindi si tenta di riavviare un servizio dopo l'esecuzione del computer.

In alcuni casi potrebbe essere necessario modificare l'account con cui viene eseguito un determinato servizio. Ad esempio, è possibile eseguire un servizio con un account amministrativo. Poiché ciò può creare una vulnerabilità di sicurezza, è possibile passare il servizio a un account con meno privilegi. In alternativa, è possibile che i servizi siano in esecuzione con un account che sta per essere eliminato oppure che si voglia assicurarsi che, in tutti i server, determinati servizi siano eseguiti con determinati account. È possibile usare il **metodo Change** della [**classe \_ TerminalService Win32**](win32-terminalservice.md) per configurare i servizi per l'esecuzione con un account utente specificato. Quando si seleziona un account, tenere presente quanto segue:

-   L'account usato come account del servizio deve avere il diritto di accedere come servizio. Questo diritto può essere concesso usando Criteri di gruppo.
-   L'account usato come account del servizio non deve essere membro di un gruppo administrators locale, di dominio o dell'organizzazione.
-   Ogni istanza di un servizio deve essere eseguita con un account utente univoco. Ciò offre sicurezza aggiuntiva e consente il controllo delle singole istanze del servizio.
-   Se il servizio è interattivo, il servizio deve essere eseguito con l'account LocalSystem.

    LocalSystem è obbligatorio perché solo una stazione finestra (WinSta0) può essere visibile e interattiva alla volta. Se un servizio viene eseguito con un account diverso da LocalSystem, viene eseguito nella stazione della finestra predefinita service-0x03e7$, che è \\ una finestra invisibile. I servizi in esecuzione in questa stazione finestra non possono ricevere input o visualizzare l'output.

Quando si assegna un account a un servizio, SCM richiede la password corretta per tale account prima di eseguire l'assegnazione. Se si specifica una password non corretta, Gestione controllo servizi rifiuta l'account. Se si configura un account del servizio usando l'account LocalSystem, LocalService o NetworkService, non è necessario specificare una password dell'account perché questi account non dispongono di password.

Gestione controllo servizi archivia la password dell'account nel database dei servizi. Dopo l'assegnazione della password, tuttavia, Gestione controllo servizi non garantisce che la password archiviata nel database dei servizi e la password assegnata all'account utente in Active Directory continuino a corrispondere. Di conseguenza, potrebbe verificarsi una situazione simile alla seguente:

-   . Configurare un servizio per l'esecuzione con un account utente specifico.
-   Il servizio viene avviato con tale account usando la password dell'account corrente.
-   Modificare la password per l'account utente.
-   L'esecuzione del servizio continua. Tuttavia, se il servizio si arresta, non è possibile riavviarlo perché Gestione controllo servizi continua a usare la vecchia password non valida. La modifica della password in Active Directory non modifica la password archiviata nel database dei servizi.

Se si eseguono servizi con account utente normali, è necessario aggiornare le password del servizio ogni volta che la password dell'account utente viene modificata. Questa operazione può richiedere molto tempo se non si è certi di quali servizi vengono eseguiti con tale account o di quali computer dispongono di servizi in esecuzione con tale account. Fortunatamente, è possibile usare WMI per controllare gli account del servizio in tutti i computer e, se necessario, modificare la password dell'account del servizio.

Il [**parametro \_ LoadOrderGroup Win32**](/windows/desktop/CIMWin32Prov/win32-loadordergroup) rappresenta un gruppo di servizi di sistema che definiscono le dipendenze di esecuzione. I servizi devono essere avviati nell'ordine specificato dal gruppo dell'ordine di caricamento perché i servizi dipendono l'uno dall'altro. Per il corretto funzionamento di questi servizi dipendenti è necessaria la presenza dei servizi antecenti.

Per modificare un servizio da un servizio di rete a un sistema locale, i parametri *StartName* e *StartPassword* devono avere i valori seguenti:


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



Per modificare un servizio da un servizio di sistema locale a una rete, i parametri *StartName* e *StartPassword* devono avere i valori seguenti:


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="examples"></a>Esempio

Il codice VBScript seguente modifica l'account del servizio per i servizi dall'esecuzione con un account utente specificato a LocalSystem.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colServiceList = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objService in colServices
 errServiceChange = objService.Change _
 ( , , , , , , ".\LocalSystem" , "")
Next
```



Il codice VBScript seguente modifica la password dell'account del servizio per tutti gli script in esecuzione in Netsvc


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colServiceList = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objservice in colServiceList
 errReturn = objService.Change( , , , , , , , "password")
Next
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>Mbnapi.h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Servizio \_ Win32**](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[Classi del sistema operativo](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[**Win32 \_ TerminalService**](win32-terminalservice.md)
</dt> <dt>

[Attività WMI: Servizi](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 


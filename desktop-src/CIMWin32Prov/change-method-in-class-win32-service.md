---
description: Modifica un servizio \_ Win32.
ms.assetid: b32753c5-8fcf-44ee-a95f-e4f6076e0f28
ms.tgt_platform: multiple
title: Modificare il metodo della Win32_Service classe (Mbnapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.Change
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ca513a31eded5202639da13b8e9f2e817c9df336b227ba93d903e44068b98898
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119440191"
---
# <a name="change-method-of-the-win32_service-class-mbnapih"></a>Modificare il metodo della Win32_Service classe (Mbnapi.h)

Il **metodo Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) modifica un servizio [**Win32. \_**](win32-service.md)

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
  [in] string  LoadOrderGroupDependencies[],
  [in] string  ServiceDependencies[]
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

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignora** (0)


</dt> <dd>

L'utente non viene notificato.

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normale** (1)


</dt> <dd>

Normale. L'utente viene notificato.

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** (2)


</dt> <dd>

Il sistema viene riavviato con l'ultima configurazione valida.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critico** (3)


</dt> <dd>

Il sistema tenta un riavvio con una configurazione valida.

</dd> </dl> </dd> <dt>

*StartMode* \[ Pollici\]
</dt> <dd>

Modalità di avvio del Windows di base. Per altre informazioni, vedere la sezione Osservazioni.

<dt>

Avvio
</dt> <dd>

Driver di dispositivo avviato dal caricatore del sistema operativo. Questo valore è valido solo per i servizi del driver.

</dd> <dt>

Sistema
</dt> <dd>

Driver di dispositivo avviato dal processo di inizializzazione del sistema operativo. Questo valore è valido solo per i servizi del driver.

</dd> <dt>

Automatico
</dt> <dd>

Servizio che deve essere avviato automaticamente da Gestione controllo servizi durante l'avvio del sistema.

</dd> <dt>

Manuale
</dt> <dd>

Servizio che deve essere avviato da Gestione controllo servizi quando un processo chiama il [**metodo StartService.**](startservice-method-in-class-win32-service.md)

</dd> <dt>

Disabled
</dt> <dd>

Servizio che non può più essere avviato.

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

Elenco di gruppi di ordinamento del carico che devono essere avviati prima dell'avvio del servizio. La matrice è doppiamente **null** con terminazione. Se il puntatore **è NULL** o se punta a una stringa vuota, il servizio non ha dipendenze. I nomi dei gruppi devono essere preceduti dal carattere **SC \_ GROUP \_ IDENTIFIER** (definito nel file Winsvc.h) per distinguerli dai nomi dei servizi perché i servizi e i gruppi di servizi condividono lo stesso spazio dei nomi. La dipendenza da un gruppo significa che il servizio può essere eseguito se almeno un membro del gruppo è in esecuzione dopo un tentativo di avviare tutti i membri del gruppo.

</dd> <dt>

*Dipendenze dei servizi* \[ Pollici\]
</dt> <dd>

Elenco contenente i nomi dei servizi che devono essere avviati prima dell'avvio del servizio. La matrice è doppiamente **NULL** con terminazione. Se il puntatore **è NULL** o se punta a una stringa vuota, il servizio non ha dipendenze. La dipendenza da un servizio indica che il servizio può essere eseguito solo se il servizio da cui dipende è in esecuzione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore. Per altri codici di errore, [**vedere Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum.**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum) Per i valori **HRESULT** generali, vedere [Codici di errore di sistema.](/windows/desktop/Debug/system-error-codes)

<dl> <dt>

**Success**
</dt> <dd>

0

La richiesta è stata accettata.

</dd> <dt>

**Non supportato**
</dt> <dd>

1

La richiesta non è supportata.

</dd> <dt>

**Accesso negato**
</dt> <dd>

2

L'utente non aveva l'accesso necessario.

</dd> <dt>

**Servizi dipendenti in esecuzione**
</dt> <dd>

3

Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.

</dd> <dt>

**Controllo del servizio non valido**
</dt> <dd>

4

Il codice di controllo richiesto non è valido o non è accettabile per il servizio.

</dd> <dt>

**Il servizio non può accettare il controllo**
</dt> <dd>

5

Il codice di controllo richiesto non può essere inviato al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](win32-baseservice.md).**State)** è uguale a 0, 1 o 2.

</dd> <dt>

**Servizio non attivo**
</dt> <dd>

6

Il servizio non è stato avviato.

</dd> <dt>

**Timeout richiesta di servizio**
</dt> <dd>

7

Il servizio non ha risposto in tempo utile alla richiesta di avvio.

</dd> <dt>

**Errore sconosciuto**
</dt> <dd>

8

Errore sconosciuto durante l'avvio del servizio.

</dd> <dt>

**Percorso non trovato**
</dt> <dd>

9

Impossibile trovare il percorso della directory del file eseguibile del servizio.

</dd> <dt>

**Servizio già in esecuzione**
</dt> <dd>

10

Il servizio è già in esecuzione.

</dd> <dt>

**Database del servizio bloccato**
</dt> <dd>

11

Il database a cui aggiungere il nuovo servizio è bloccato.

</dd> <dt>

**Dipendenza del servizio eliminata**
</dt> <dd>

12

Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.

</dd> <dt>

**Errore di dipendenza del servizio**
</dt> <dd>

13

Impossibile trovare un servizio dipendente necessario.

</dd> <dt>

**Servizio disabilitato**
</dt> <dd>

14

Il servizio è stato disabilitato dal sistema.

</dd> <dt>

**Accesso al servizio non riuscito**
</dt> <dd>

15

Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.

</dd> <dt>

**Servizio contrassegnato per l'eliminazione**
</dt> <dd>

16

Questo servizio viene rimosso dal sistema.

</dd> <dt>

**Nessun thread del servizio**
</dt> <dd>

17

Il servizio non ha thread di esecuzione.

</dd> <dt>

**Dipendenza circolare dello stato**
</dt> <dd>

18

Il servizio presenta dipendenze circolari all'avvio.

</dd> <dt>

**Nome duplicato stato**
</dt> <dd>

19

Un servizio viene eseguito con lo stesso nome.

</dd> <dt>

**Nome dello stato non valido**
</dt> <dd>

20

Il nome del servizio contiene caratteri non validi.

</dd> <dt>

**Parametro stato non valido**
</dt> <dd>

21

Al servizio sono stati passati parametri non validi.

</dd> <dt>

**Stato Account del servizio non valido**
</dt> <dd>

22

L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni per eseguire il servizio.

</dd> <dt>

**Servizio di stato esistente**
</dt> <dd>

23

Il servizio esiste già nel database dei servizi disponibili dal sistema.

</dd> <dt>

**Servizio già sospeso**
</dt> <dd>

24

Il servizio è attualmente sospeso nel sistema.

</dd> <dt>

**Altri**
</dt> <dd>

25 4294967295

</dd> </dl>

## <a name="remarks"></a>Commenti

All'avvio di un computer vengono avviati anche tutti i servizi di avvio automatico. In alcuni casi, uno di questi servizi potrebbe non essere avviato insieme al computer. Quando si verifica un errore di un servizio durante l'avvio del sistema, il computer esegue un'azione in base al valore del codice di controllo degli errori del servizio.

la maggior parte dei servizi viene installata usando il codice di controllo degli errori normale. Alcune delle eccezioni, che vengono installate usando il codice di errore Ignora, includono:

-   Servizio Replica file
-   Smart card
-   Accesso secondario
-   WMI

Per i servizi installati utilizzando il codice di errore Ignora, all'utente non viene inviata alcuna notifica che indica che il servizio non è riuscito. Se si preferisce una notifica sullo schermo che indica che non è stato possibile avviare un servizio, è possibile usare WMI per modificare il codice di controllo degli errori. I codici di controllo degli errori si applicano solo all'avvio del computer. I codici di controllo degli errori non vengono usati se si arresta e quindi si tenta di riavviare un servizio dopo l'esecuzione del computer.

In alcuni casi potrebbe essere necessario modificare l'account con cui viene eseguito un determinato servizio. Ad esempio, è possibile eseguire un servizio con un account amministrativo. Poiché ciò può creare una vulnerabilità di sicurezza, è possibile passare il servizio a un account con meno privilegi. In alternativa, è possibile che i servizi siano in esecuzione con un account che sta per essere eliminato o che si voglia assicurarsi che, in tutti i server, alcuni servizi siano eseguiti con determinati account. È possibile usare il **metodo Change** della classe Del servizio [**\_ Win32**](win32-service.md) per configurare i servizi per l'esecuzione con un account utente specificato. Quando si seleziona un account, tenere presente quanto segue:

-   L'account usato come account del servizio deve avere il diritto di accedere come servizio. Questo diritto può essere concesso usando Criteri di gruppo.
-   L'account usato come account del servizio non deve essere membro di un gruppo Administrators locale, di dominio o dell'organizzazione.
-   Ogni istanza di un servizio deve essere eseguita con un account utente univoco. Ciò offre sicurezza aggiuntiva e consente il controllo delle singole istanze del servizio.
-   Se il servizio è interattivo, il servizio deve essere eseguito con l'account LocalSystem.

    LocalSystem è obbligatorio perché solo una stazione finestra (WinSta0) può essere visibile e interattiva alla volta. Se un servizio viene eseguito con un account diverso da LocalSystem, viene eseguito nella stazione della finestra predefinita service-0x03e7$, che è \\ una finestra invisibile. I servizi in esecuzione in questa stazione finestra non possono ricevere input o visualizzare l'output.

Quando si assegna un account a un servizio, SCM richiede la password corretta per tale account prima di eseguire l'assegnazione. Se si specifica una password non corretta, Gestione controllo servizi rifiuta l'account. Se si configura un account del servizio usando l'account LocalSystem, LocalService o NetworkService, non è necessario specificare una password dell'account perché questi account non dispongono di password.

Gestione controllo servizi archivia la password dell'account nel database dei servizi. Dopo l'assegnazione della password, tuttavia, Gestione controllo servizi non garantisce che la password archiviata nel database dei servizi e la password assegnata all'account utente in Active Directory continuino a corrispondere. Di conseguenza, potrebbe verificarsi una situazione simile alla seguente:

-   Configurare un servizio per l'esecuzione con un account utente specifico.
-   Il servizio viene avviato con tale account usando la password dell'account corrente.
-   Modificare la password per l'account utente.
-   L'esecuzione del servizio continua. Tuttavia, se il servizio viene arrestato, non è possibile riavviarlo perché SCM continua a usare la vecchia password non valida. La modifica della password in Active Directory non modifica la password archiviata nel database dei servizi.

Se si eseguono servizi con account utente normali, è necessario aggiornare le password del servizio ogni volta che cambia la password dell'account utente. Ciò può richiedere molto tempo se non si è certi di quali servizi vengono eseguiti con tale account o quali computer dispongono di servizi in esecuzione con tale account. Fortunatamente, è possibile usare WMI per controllare gli account del servizio in tutti i computer e, se necessario, modificare la password dell'account del servizio.

Il [**parametro Win32 \_ LoadOrderGroup**](win32-loadordergroup.md) rappresenta un gruppo di servizi di sistema che definiscono le dipendenze di esecuzione. I servizi devono essere avviati nell'ordine specificato dal gruppo di ordini di caricamento perché i servizi dipendono l'uno dall'altro. Questi servizi dipendenti richiedono la presenza dei servizi di riferimento per il corretto funzionamento.

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
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colServiceList = objWMIService.ExecQuery("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objService in colServices
 errServiceChange = objService.Change( , , , , , , ".\LocalSystem" , "")
Next
```



Il codice VBScript seguente modifica la password dell'account del servizio per tutti gli script in esecuzione in Netsvc


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colServiceList = objWMIService.ExecQuery("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objservice in colServiceList
 errReturn = objService.Change( , , , , , , , "password")
Next
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| Intestazione<br/>                   | <dl> <dt>Mbnapi.h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Servizio \_ Win32**](win32-service.md)
</dt> <dt>

[Attività WMI: Servizi](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 


---
description: La classe CommandLineEventConsumer avvia un processo arbitrario nel sistema locale quando viene recapitato un evento.
ms.assetid: 0dcae783-1722-45a4-b5d4-3fcf455dacf8
ms.tgt_platform: multiple
title: Classe CommandLineEventConsumer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CommandLineEventConsumer
- CommandLineEventConsumer.CreatorSID
- CommandLineEventConsumer.MachineName
- CommandLineEventConsumer.MaximumQueueSize
- CommandLineEventConsumer.CommandLineTemplate
- CommandLineEventConsumer.CreateNewConsole
- CommandLineEventConsumer.CreateNewProcessGroup
- CommandLineEventConsumer.CreateSeparateWowVdm
- CommandLineEventConsumer.CreateSharedWowVdm
- CommandLineEventConsumer.DesktopName
- CommandLineEventConsumer.ExecutablePath
- CommandLineEventConsumer.FillAttributes
- CommandLineEventConsumer.ForceOffFeedback
- CommandLineEventConsumer.ForceOnFeedback
- CommandLineEventConsumer.KillTimeout
- CommandLineEventConsumer.Name
- CommandLineEventConsumer.Priority
- CommandLineEventConsumer.RunInteractively
- CommandLineEventConsumer.ShowWindowCommand
- CommandLineEventConsumer.UseDefaultErrorMode
- CommandLineEventConsumer.WindowTitle
- CommandLineEventConsumer.WorkingDirectory
- CommandLineEventConsumer.XCoordinate
- CommandLineEventConsumer.XNumCharacters
- CommandLineEventConsumer.XSize
- CommandLineEventConsumer.YCoordinate
- CommandLineEventConsumer.YNumCharacters
- CommandLineEventConsumer.YSize
- CommandLineEventConsumer.FillAttribute
api_type:
- DllExport
api_location:
- Wbemcons.dll
ms.openlocfilehash: 1784ba116417f6ed94aed2249a797cf8de4b3527
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334364"
---
# <a name="commandlineeventconsumer-class"></a>Classe CommandLineEventConsumer

La classe **CommandLineEventConsumer** avvia un processo arbitrario nel sistema locale quando viene recapitato un evento. Questa classe è uno dei consumer di eventi standard forniti da WMI. Per altre informazioni, vedere [monitoraggio e risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md).

> [!Note]  
> Quando si usa la classe **CommandLineEventConsumer** , proteggere il file eseguibile che si vuole avviare. Se il file eseguibile non si trova in un percorso sicuro o protetto con un elenco di controllo di accesso (ACL) sicuro, un utente non autorizzato può sostituire l'eseguibile con un eseguibile dannoso. Per ulteriori informazioni sugli ACL, visitare la sezione relativa alla sicurezza di Microsoft Windows Software Development Kit (SDK) e vedere [creazione di un descrittore di sicurezza per un nuovo oggetto](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).

 

## <a name="syntax"></a>Sintassi

``` syntax
[AMENDMENT]
class CommandLineEventConsumer : __EventConsumer
{
  uint8   CreatorSID[];
  string  MachineName;
  uint32  MaximumQueueSize;
  string  CommandLineTemplate;
  boolean CreateNewConsole = False;
  boolean CreateNewProcessGroup = True;
  boolean CreateSeparateWowVdm = False;
  boolean CreateSharedWowVdm = False;
  string  DesktopName;
  string  ExecutablePath;
  uint32  FillAttributes;
  boolean ForceOffFeedback = False;
  boolean ForceOnFeedback = False;
  uint32  KillTimeout = 0;
  string  Name;
  sint32  Priority = 0x20;
  boolean RunInteractively = False;
  uint32  ShowWindowCommand;
  boolean UseDefaultErrorMode = False;
  string  WindowTitle;
  string  WorkingDirectory;
  uint32  XCoordinate;
  uint32  XNumCharacters;
  uint32  XSize;
  uint32  YCoordinate;
  uint32  YNumCharacters;
  uint32  YSize;
  uint32  FillAttribute;
};
```

## <a name="members"></a>Members

La classe **CommandLineEventConsumer** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CommandLineEventConsumer** dispone di queste proprietà.

<dl> <dt>

**CommandLineTemplate**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Modello di stringa standard che specifica il processo da avviare. Questa proprietà può essere **null** e la proprietà **ExecutablePath** viene utilizzata come riga di comando.

</dd> <dt>

**CreateNewConsole**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Non usato. Se a questa proprietà viene assegnato un valore, viene generato un messaggio di traccia. Per ulteriori informazioni, vedere [traccia dell'attività WMI](tracing-wmi-activity.md).

</dd> <dt>

**CreateNewProcessGroup**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **true**, il nuovo processo è il processo radice di un nuovo gruppo di processi. Il gruppo di processi include tutti i processi discendenti di questo processo radice. L'identificatore di processo del nuovo gruppo di processi è uguale a questo identificatore di processo. I gruppi di processi vengono usati dal metodo [**GenerateConsoleCtrlEvent**](/windows/console/generateconsolectrlevent) per consentire l'invio di un segnale CTRL + C o Ctrl + Break a un gruppo di processi della console.

</dd> <dt>

**CreateSeparateWowVdm**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **true**, il nuovo processo viene eseguito in una macchina virtuale DOS privata (VDM). Questa operazione è valida solo quando si avvia un'applicazione in esecuzione in un sistema operativo Windows a 16 bit. Se è impostato su **false**, tutte le applicazioni in esecuzione su un sistema operativo Windows a 16 bit vengono eseguite come thread in un'unica VDM condivisa. Per ulteriori informazioni, vedere la sezione Osservazioni di questo argomento.

</dd> <dt>

**CreateSharedWowVdm**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **true**, il metodo [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) esegue il nuovo processo nella macchina virtuale DOS condivisa (VDM). Questa proprietà può eseguire l'override dell'opzione DefaultSeparateVDM nella sezione Windows di Win.ini se impostata su **true**. Per ulteriori informazioni, vedere la sezione Osservazioni di questo argomento.

</dd> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

ID di sicurezza (SID) che identifica in modo univoco l'utente che crea un filtro. WMI archivia il SID dell'utente che crea un'istanza di [**\_ \_ EventConsumer**](--eventconsumer.md) o il SID Administrator, a seconda del sistema operativo. Per ulteriori informazioni, vedere [associazione di un filtro eventi a un consumer logico](binding-an-event-filter-with-a-logical-consumer.md) e [monitoraggio e risposta agli eventi con](monitoring-and-responding-to-events-with-standard-consumers.md)consumer standard.

Questa proprietà viene ereditata da [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**Desktopname**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Non usato. Se a questa proprietà viene assegnato un valore, viene generato un messaggio di traccia. Per ulteriori informazioni, vedere [traccia dell'attività WMI](tracing-wmi-activity.md).

</dd> <dt>

**ExecutablePath**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Modulo da eseguire. La stringa può specificare il percorso completo e il nome file del modulo da eseguire oppure può specificare un nome parziale. Se viene specificato un nome parziale, si presuppone l'unità corrente e la directory corrente.

La proprietà **ExecutablePath** può essere **null**. In tal caso, il nome del modulo deve essere il primo token delimitato da spazi vuoti nel valore della proprietà **CommandLineTemplate** . Se si utilizza un nome di file lungo che contiene uno spazio, utilizzare stringhe tra virgolette per indicare dove termina il nome file e gli argomenti iniziano a chiarire il nome del file.

> [!Note]  
> Poiché la proprietà **CommandLineTemplate** può essere un modello in cui il modulo da eseguire viene fornito da una variabile, una proprietà **ExecutablePath** **null** consente il modulo specificato nel parametro da eseguire e quindi è fuori dal controllo. Impostare sempre la proprietà **ExecutablePath** nella registrazione **CommandLineEventConsumer** per includere l'eseguibile richiesto, evitando la sovrascrittura da parte dei parametri degli eventi. Se è necessario usare un modello e una variabile per specificare il modulo da eseguire, prestare attenzione agli utenti a cui vengono concessi i privilegi di scrittura completi nello spazio dei nomi.

 

</dd> <dt>

**FillAttribute**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica il testo iniziale e i colori di sfondo se viene creata una nuova finestra della console in un'applicazione console

</dd> <dt>

**FillAttributes**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Testo iniziale e colori di sfondo, se viene creata una nuova finestra della console in un'applicazione console. Questa proprietà viene ignorata in un'applicazione GUI. Il valore può essere una qualsiasi combinazione dei valori seguenti.

<dt>

1 (0x1)
</dt> <dd>

primo piano blu

</dd> <dt>

2 (0x2)
</dt> <dd>

primo piano verde

</dd> <dt>

4 (0x4)
</dt> <dd>

primo piano rosso

</dd> <dt>

8 (0x8)
</dt> <dd>

intensità in primo piano

</dd> <dt>

16 (0x10)
</dt> <dd>

sfondo blu

</dd> <dt>

32 (0x20)
</dt> <dd>

sfondo verde

</dd> <dt>

64 (0x40)
</dt> <dd>

sfondo rosso

</dd> <dt>

128 (0x80)
</dt> <dd>

intensità di sfondo

</dd> </dl>

Ad esempio, le combinazioni seguenti producono testo rosso su sfondo bianco:


```mof
0x4 | 0x40 | 0x20 | 0x10
```



  oppure  


```mof
0x74
```



</dd> <dt>

**ForceOffFeedback**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **true**, il cursore del feedback viene forzato all'avvio del processo. Viene visualizzato il cursore normale.

</dd> <dt>

**ForceOnFeedback**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **true**, il cursore è in modalità di feedback per due secondi dopo la chiamata a [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) . Durante questi due secondi, se il processo effettua la prima chiamata a GUI, il sistema fornisce cinque secondi per il processo. Durante questi cinque secondi, se il processo Mostra una finestra, il sistema concede altri cinque secondi al processo per completare il disegno della finestra.

</dd> <dt>

**KillTimeout**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero, in secondi, di attesa del servizio WMI prima di terminare un processo 0 (zero) indica che non è stato possibile terminare un processo. L'arresto di un processo impedisce l'esecuzione illimitata di un processo.

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del computer a cui Strumentazione gestione Windows (WMI) Invia gli eventi.

Questa proprietà viene ereditata da [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**MaximumQueueSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero massimo di code per un consumer specifico, in byte.

Questa proprietà viene ereditata da [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](key-qualifier.md)
</dt> </dl>

Nome univoco di un consumer.

</dd> <dt>

**Priorità**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Pianificazione del livello di priorità dei thread di processo. Nell'elenco seguente sono elencati i livelli di priorità disponibili.

<dt>

32 (0x20)
</dt> <dd>

Indica un processo normale senza necessità di pianificazione.

</dd> <dt>

64 (0x40)
</dt> <dd>

Indica un processo i cui thread vengono eseguiti solo quando il sistema è inattivo e vengono interrotti dai thread di qualsiasi processo in esecuzione in una classe di priorità superiore. Un esempio è un screen saver. La classe di priorità inattiva viene ereditata dai processi figlio.

</dd> <dt>

128 (0x80)
</dt> <dd>

Indica un processo che esegue attività critiche in termini di priorità elevata. I thread di un processo di classe ad alta priorità hanno la precedenza sui thread dei processi di classe di priorità normale o di priorità di inattività. Un esempio è il Elenco attività, che deve rispondere rapidamente quando viene chiamato dall'utente indipendentemente dal carico del sistema. Prestare particolare attenzione quando si usa la classe con priorità alta, perché un'applicazione associata alla CPU con una classe con priorità alta può usare quasi tutti i cicli disponibili.

</dd> <dt>

256 (0x100)
</dt> <dd>

Indica un processo con la massima priorità possibile. I thread di un processo della classe di priorità in tempo reale hanno la precedenza sui thread di tutti gli altri processi, inclusi i processi del sistema operativo che eseguono attività importanti. Ad esempio, un processo in tempo reale eseguito per più di un breve intervallo può causare la mancata scaricamento delle cache del disco o la mancata risposta del mouse.

</dd> </dl>

</dd> <dt>

**RunInteractively**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **true**, il processo viene avviato nella winstation interattiva. Se **false**, il processo viene avviato nel servizio predefinito WinStation. Questa proprietà esegue l'override della proprietà **desktopname** . Questa proprietà viene utilizzata solo localmente e solo se l'utente interattivo è lo stesso utente che ha configurato il consumer.

A partire da Windows Vista, il processo che esegue l'istanza di **CommandLineEventConsumer** viene avviato con l'account **LocalSystem** e si trova nella sessione 0. I servizi eseguiti nella sessione 0 non possono interagire con le sessioni utente.

</dd> <dt>

**ShowWindowCommand**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Mostra stato finestra. Può essere uno qualsiasi dei valori che possono essere specificati nel parametro *nCmdShow* per la funzione [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) .

</dd> <dt>

**UseDefaultErrorMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **true**, viene usata la modalità di errore predefinita.

</dd> <dt>

**WindowTitle**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Titolo visualizzato sulla barra del titolo del processo. Questa proprietà viene ignorata per le applicazioni GUI.

</dd> <dt>

**WorkingDirectory**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Directory di lavoro per questo processo.

</dd> <dt>

**XCoordinate**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Offset X, in pixel, dal bordo sinistro dello schermo al bordo sinistro della finestra, se viene creata una nuova finestra.

</dd> <dt>

**XNumCharacters**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Larghezza del buffer dello schermo, in colonne di tipo carattere, se viene creata una nuova finestra della console. Questa proprietà viene ignorata in un processo GUI.

</dd> <dt>

**XSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Larghezza, in pixel, di una nuova finestra, se viene creata una nuova finestra.

</dd> <dt>

**YCoordinate**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Offset Y, in pixel, dal bordo superiore dello schermo al bordo superiore della finestra, se viene creata una nuova finestra.

</dd> <dt>

**YNumCharacters**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Altezza del buffer dello schermo, in righe di caratteri, se viene creata una nuova finestra della console. Questa proprietà viene ignorata in un processo GUI.

</dd> <dt>

**YSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Altezza, in pixel, della nuova finestra, se viene creata una nuova finestra.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **CommandLineEventConsumer** è derivata dalla classe astratta [**\_ \_ EventConsumer**](--eventconsumer.md) .

La proprietà **CreateSeparateWowVdm** indica se il nuovo processo viene eseguito in una macchina virtuale DOS privata (VDM). Il vantaggio di eseguire separatamente è il fatto che un arresto anomalo termina solo il singolo VDM. I programmi in esecuzione in VDMs distinti continuano a funzionare normalmente e le applicazioni basate su Windows a 16 bit eseguite in VDMs separate hanno code di input separate. Ciò significa che se un'applicazione smette di rispondere momentaneamente, le applicazioni in VDMs separate continuano a ricevere input. Lo svantaggio dell'esecuzione separata è il fatto che richiede una quantità di memoria significativamente maggiore. È necessario impostare questa proprietà su **true** solo se l'utente richiede che le applicazioni basate su Windows a 16 bit vengano eseguite nel proprio VDM.

> [!Note]  
> **CommandLineEventConsumer** utilizza internamente il metodo [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) e passa le proprietà **ExecutablePath** e **CommandLineTemplate** come parametri *lpApplicationName* e *lpCommandLine* . Nell'esempio di codice seguente Managed Object Format (MOF) non viene utilizzato correttamente **CommandLineEventConsumer** .

 


```mof
instance of CommandLineEventConsumer
{
  ExecutablePath = "C:\\windows\\system32\\cscript.exe";
  CommandLineTemplate = "C:\\scripts\\MyScript.js param1 param2";
};
```



Il metodo [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) passa *lpCommandLine* come `argv[0]` , `argv[1]` e così via. Poiché `argv[0]` per le applicazioni a 16 bit utilizzate per essere riservate al nome del file eseguibile, il codice MOF precedente comporta la creazione del processo come se il comando seguente venisse immesso al prompt dei comandi: **c: \\ Windows \\ system32 \\cscript.exe param1 param2**.

Il comando precedente non ha esito positivo perché Cscript.exe non è in grado di osservare `argv[0]` , quindi non riconosce che non contiene il proprio nome, ma un altro ("c: \\ \\ Scripts \\ \\MyScript.js"). Nell'esempio seguente viene identificato l'utilizzo consigliato di **CommandLineEventConsumer**.


```mof
instance of CommandLineEventConsumer
{
  ExecutablePath = "C:\\windows\\system32\\cscript.exe";
  CommandLineTemplate = "C:\\windows\\system32\\cscript.exe"
    "C:\\scripts\\MyScript.js param1 param2";
};
```



L'uso precedente di **CommandLineEventConsumer** genera il processo creato come se il comando seguente venisse immesso al prompt dei comandi: **c: \\ Windows \\ system32 \\cscript.exe c: \\ Scripts \\MyScript.js param1 param2**

Poiché "c: \\ \\ scripts \\ \\MyScript.js" è ora `argv[1]` visibile da Cscript.exe e il comando ha esito positivo.

Per ulteriori informazioni, vedere la funzione [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .

## <a name="examples"></a>Esempio

Per un esempio dell'uso di **CommandLineEventConsumer** per creare un consumer, vedere [esecuzione di un programma dalla riga di comando in base a un evento](running-a-program-from-the-command-line-based-on-an-event.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\Sottoscrizione radice<br/>                                                           |
| MOF<br/>                      | <dl> <dt>Wbemcons. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemcons.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi consumer standard](standard-consumer-classes.md)
</dt> <dt>

[Monitoraggio e risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[Creazione di un consumer logico](creating-a-logical-consumer.md)
</dt> <dt>

[Ricezione di eventi in qualsiasi momento](receiving-events-at-all-times.md)
</dt> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> </dl>

 


---
description: La classe CommandLineEventConsumer avvia un processo arbitrario nel sistema locale quando vi viene recapitato un evento.
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
ms.openlocfilehash: dce5100ba83a04ef2f6252421ec49068e84730141830e7b01f177c81bbac21b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319590"
---
# <a name="commandlineeventconsumer-class"></a>Classe CommandLineEventConsumer

La **classe CommandLineEventConsumer** avvia un processo arbitrario nel sistema locale quando vi viene recapitato un evento. Questa classe è uno dei consumer di eventi standard forniti da WMI. Per altre informazioni, vedere [Monitoraggio e risposta agli eventi con consumer standard.](monitoring-and-responding-to-events-with-standard-consumers.md)

> [!Note]  
> Quando si usa **la classe CommandLineEventConsumer,** proteggere l'eseguibile da avviare. Se il file eseguibile non si trova in una posizione sicura o è protetto con un elenco di controllo di accesso (ACL) sicuro, un utente non autorizzato può sostituire l'eseguibile con un eseguibile dannoso. Per altre informazioni sugli ACL, visitare la sezione Sicurezza di Microsoft Windows Software Development Kit (SDK) e vedere Creazione di un descrittore di sicurezza per [un nuovo oggetto](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).

 

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

La **classe CommandLineEventConsumer** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CommandLineEventConsumer** ha queste proprietà.

<dl> <dt>

**CommandLineTemplate**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Modello di stringa standard che specifica il processo da iniziare. Questa proprietà può essere **NULL** e la **proprietà ExecutablePath** viene usata come riga di comando.

</dd> <dt>

**CreateNewConsole**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Non usato. Se a questa proprietà viene assegnato un valore, viene generato un messaggio di traccia. Per altre informazioni, vedere [Traccia dell'attività WMI.](tracing-wmi-activity.md)

</dd> <dt>

**CreateNewProcessGroup**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **True**, il nuovo processo è il processo radice di un nuovo gruppo di processi. Il gruppo di processi include tutti i processi discendenti di questo processo radice. L'identificatore di processo del nuovo gruppo di processi è lo stesso di questo identificatore di processo. I gruppi di processi vengono usati dal [**metodo GenerateConsoleCtrlEvent**](/windows/console/generateconsolectrlevent) per consentire l'invio di un segnale CTRL+C o CTRL+INTERR a un gruppo di processi della console.

</dd> <dt>

**CreateSeparateWowVdm**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **True,** il nuovo processo viene eseguito in una macchina DOS virtuale privata (VDM). Questo è valido solo quando si avvia un'applicazione in esecuzione in un sistema operativo Windows a 16 bit. Se impostato su **False**, tutte le applicazioni in esecuzione in un sistema operativo Windows a 16 bit vengono eseguite come thread in un singolo VDM condiviso. Per altre informazioni, vedere la sezione Osservazioni di questo argomento.

</dd> <dt>

**CreateSharedWowVdm**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **True,** il [**metodo CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) esegue il nuovo processo nella macchina DOS virtuale (VDM) condivisa. Questa proprietà può eseguire l'override dell'opzione DefaultSeparateVDM nella sezione Windows di Win.ini se impostata su **True.** Per altre informazioni, vedere la sezione Osservazioni di questo argomento.

</dd> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

ID di sicurezza (SID) che identifica in modo univoco l'utente che crea un filtro. WMI archivia il SID dell'utente che crea un'istanza di [**\_ \_ EventConsumer**](--eventconsumer.md) o il SID amministratore, a seconda del sistema operativo. Per altre informazioni, vedere [Associazione di un filtro eventi con](binding-an-event-filter-with-a-logical-consumer.md) un consumer logico e Monitoraggio e Risposta agli eventi con consumer [standard.](monitoring-and-responding-to-events-with-standard-consumers.md)

Questa proprietà viene ereditata da [**\_ \_ EventConsumer.**](--eventconsumer.md)

</dd> <dt>

**DesktopName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Non usato. Se a questa proprietà viene assegnato un valore, viene generato un messaggio di traccia. Per altre informazioni, vedere [Traccia dell'attività WMI.](tracing-wmi-activity.md)

</dd> <dt>

**ExecutablePath**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Modulo da eseguire. La stringa può specificare il percorso completo e il nome file del modulo da eseguire oppure può specificare un nome parziale. Se viene specificato un nome parziale, vengono considerate l'unità corrente e la directory corrente.

La **proprietà ExecutablePath** può essere **NULL.** In tal caso, il nome del modulo deve essere il primo token delimitato da spazi vuoti nel valore **della proprietà CommandLineTemplate.** Se si usa un nome di file lungo che contiene uno spazio, usare stringhe tra virgolette per indicare dove termina il nome del file e gli argomenti iniziano a chiarire il nome del file.

> [!Note]  
> Poiché la proprietà **CommandLineTemplate** può essere un modello in cui il modulo da eseguire viene fornito da una variabile, una proprietà **ExecutablePath** **NULL** consente l'esecuzione del modulo specificato nel parametro e quindi è fuori controllo. Impostare sempre la **proprietà ExecutablePath** nella registrazione **di CommandLineEventConsumer** per includere l'eseguibile richiesto, evitando la sovrascrittura dei parametri degli eventi. Se è necessario usare un modello e una variabile per specificare il modulo da eseguire, prestare attenzione a chi viene concesso il privilegio di scrittura completo nello spazio dei nomi .

 

</dd> <dt>

**FillAttribute**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica il testo iniziale e i colori di sfondo se viene creata una nuova finestra della console in un'applicazione console

</dd> <dt>

**Attributi FillAttributes**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Colori iniziali del testo e dello sfondo, se viene creata una nuova finestra della console in un'applicazione console. Questa proprietà viene ignorata in un'applicazione GUI. Il valore può essere qualsiasi combinazione dei valori seguenti.

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

intensità di primo piano

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

intensità dello sfondo

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

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **True,** il cursore di feedback viene disattivato durante l'avvio del processo. Viene visualizzato il cursore normale.

</dd> <dt>

**ForceOnFeedback**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **True,** il cursore è in modalità feedback per due secondi dopo [**la chiamata a CreateProcess.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) Durante questi due secondi, se il processo effettua la prima chiamata gui, il sistema concede altri cinque secondi al processo. Durante questi cinque secondi, se il processo mostra una finestra, il sistema concede altri cinque secondi al processo per completare il disegno della finestra.

</dd> <dt>

**KillTimeout**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero, in secondi, che il servizio WMI attende prima di elaborare 0 (zero) indica che un processo non deve essere atteso. L'esecuzione di un processo impedisce l'esecuzione illimitata di un processo.

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del computer a cui Windows Management Instrumentation (WMI).

Questa proprietà viene ereditata da [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**MaximumQueueSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Coda massima per un consumer specifico, in byte.

Questa proprietà viene ereditata da [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
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

Livello di priorità di pianificazione dei thread di processo. Nell'elenco seguente sono elencati i livelli di priorità disponibili.

<dt>

32 (0x20)
</dt> <dd>

Indica un processo normale senza necessità di pianificazione.

</dd> <dt>

64 (0x40)
</dt> <dd>

Indica un processo i cui thread vengono eseguiti solo quando il sistema è inattivo e sono preempted dai thread di qualsiasi processo in esecuzione in una classe con priorità più alta. Un esempio è un screen saver. La classe di priorità inattiva viene ereditata dai processi figlio.

</dd> <dt>

128 (0x80)
</dt> <dd>

Indica un processo che esegue attività ad alta priorità e time critical. I thread di un processo di classe ad alta priorità pre-elaborano i thread dei processi di classe con priorità normale o inattiva. Un esempio è il Elenco attività, che deve rispondere rapidamente quando viene chiamato dall'utente indipendentemente dal carico sul sistema. Usare estrema attenzione quando si usa la classe con priorità alta, perché un'applicazione associata alla CPU con una classe con priorità alta può usare quasi tutti i cicli disponibili.

</dd> <dt>

256 (0x100)
</dt> <dd>

Indica un processo con la priorità più alta possibile. I thread di un processo della classe di priorità in tempo reale hanno la precedenza rispetto ai thread di tutti gli altri processi, inclusi i processi del sistema operativo che eseguono attività importanti. Ad esempio, un processo in tempo reale che viene eseguito per più di un breve intervallo può causare la non scaricamento delle cache del disco o la non risposta del mouse.

</dd> </dl>

</dd> <dt>

**RunInteractively**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **True,** il processo viene avviato in WinStation interattivo. Se **False,** il processo viene avviato nel servizio predefinito WinStation. Questa proprietà esegue l'override **della proprietà DesktopName.** Questa proprietà viene usata solo in locale e solo se l'utente interattivo è lo stesso utente che ha configurato il consumer.

A partire Windows Vista, il processo che esegue l'istanza **CommandLineEventConsumer** viene avviato con l'account **LocalSystem** e si trova nella sessione 0. I servizi eseguiti nella sessione 0 non possono interagire con le sessioni utente.

</dd> <dt>

**ShowWindowCommand**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato di visualizzazione della finestra. Può essere uno dei valori che possono essere specificati nel *parametro nCmdShow* per la [funzione ShowWindow.](/windows/desktop/api/winuser/nf-winuser-showwindow)

</dd> <dt>

**UseDefaultErrorMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **True,** viene usata la modalità di errore predefinita.

</dd> <dt>

**Windowtitle**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Titolo visualizzato sulla barra del titolo del processo. Questa proprietà viene ignorata per le applicazioni GUI.

</dd> <dt>

**WorkingDirectory**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Directory di lavoro per questo processo.

</dd> <dt>

**XCoordinate**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Offset X, in pixel, dal bordo sinistro dello schermo al bordo sinistro della finestra, se viene creata una nuova finestra.

</dd> <dt>

**XNumCharacters**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Larghezza del buffer dello schermo, in colonne di tipo carattere, se viene creata una nuova finestra della console. Questa proprietà viene ignorata in un processo GUI.

</dd> <dt>

**XSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Larghezza, in pixel, di una nuova finestra, se viene creata una nuova finestra.

</dd> <dt>

**YCoordinate**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Offset Y, in pixel, dal bordo superiore dello schermo al bordo superiore della finestra, se viene creata una nuova finestra.

</dd> <dt>

**YNumCharacters**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Altezza del buffer dello schermo, in righe di caratteri, se viene creata una nuova finestra della console. Questa proprietà viene ignorata in un processo GUI.

</dd> <dt>

**YSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Altezza, in pixel, della nuova finestra, se viene creata una nuova finestra.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe CommandLineEventConsumer** è derivata dalla [**\_ \_ classe astratta EventConsumer.**](--eventconsumer.md)

La **proprietà CreateSeparateWowVdm** indica se il nuovo processo viene eseguito o meno in un computer DOS virtuale (VDM) privato. Il vantaggio dell'esecuzione separata è che un arresto anomalo termina solo il singolo VDM. I programmi in esecuzione in VM distinte continuano a funzionare normalmente e le applicazioni basate su Windows a 16 bit in esecuzione in VM separate hanno code di input separate. Ciò significa che se un'applicazione smette di rispondere momentaneamente, le applicazioni in VM separate continuano a ricevere input. Lo svantaggio dell'esecuzione separata è che questa operazione richiede una quantità di memoria significativamente maggiore. È consigliabile impostare questa proprietà su **True** solo se l'utente richiede l'esecuzione di applicazioni Windows a 16 bit nel proprio VDM.

> [!Note]  
> **CommandLineEventConsumer** usa internamente il metodo [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) e passa le proprietà **ExecutablePath** e **CommandLineTemplate** come parametri *lpApplicationName* e *lpCommandLine.* L'Managed Object Format di codice MOF **(CommandLineEventConsumer)** seguente non usa correttamente CommandLineEventConsumer.

 


```mof
instance of CommandLineEventConsumer
{
  ExecutablePath = "C:\\windows\\system32\\cscript.exe";
  CommandLineTemplate = "C:\\scripts\\MyScript.js param1 param2";
};
```



Il [**metodo CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) passa *lpCommandLine* come `argv[0]` , e così `argv[1]` via. Poiché per le applicazioni a 16 bit era riservato per il nome del file eseguibile, il codice MOF precedente comporta la creazione del processo come se al prompt dei comandi fosse immesso il comando `argv[0]` seguente: **c: \\ windows \\ system32 \\cscript.exe param1 param2**.

Il comando precedente non ha esito positivo perché Cscript.exe non osserva e quindi non riconosce che non contiene il proprio nome, ma un altro elemento `argv[0]` ("c: \\ \\ scripts \\ \\MyScript.js"). L'esempio seguente identifica l'uso consigliato **di CommandLineEventConsumer**.


```mof
instance of CommandLineEventConsumer
{
  ExecutablePath = "C:\\windows\\system32\\cscript.exe";
  CommandLineTemplate = "C:\\windows\\system32\\cscript.exe"
    "C:\\scripts\\MyScript.js param1 param2";
};
```



L'uso precedente di **CommandLineEventConsumer** comporta il processo creato come se al prompt dei comandi fosse stato immesso il comando seguente: **c: \\ windows \\ system32 \\cscript.exe c: scriptsMyScript.js \\ \\ param1 param2**

Poiché "c: scriptsMyScript.js" è ora , viene visualizzato da Cscript.exe \\ \\ e il comando ha \\ \\ `argv[1]` esito positivo.

Per altre informazioni, vedere la [**funzione CreateProcess.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)

## <a name="examples"></a>Esempio

Per un esempio dell'uso **di CommandLineEventConsumer** per creare un consumer, vedere Esecuzione di un programma dalla riga di comando [in base a un evento](running-a-program-from-the-command-line-based-on-an-event.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Sottoscrizione \\ radice<br/>                                                           |
| MOF<br/>                      | <dl> <dt>Wbemcons.mof</dt> </dl> |
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

 


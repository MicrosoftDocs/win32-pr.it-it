---
description: Questo argomento è un riferimento per le voci che possono essere usate in un file Autorun. inf. Una voce è costituita da una chiave e un valore.
ms.assetid: 5b8fd559-b1be-4552-a7be-19ad107855af
title: Voci Autorun. inf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56d93244f177d107bddc720fab1d0c774fd94735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225936"
---
# <a name="autoruninf-entries"></a>Voci Autorun. inf

Questo argomento è un riferimento per le voci che possono essere usate in un file Autorun. inf. Una voce è costituita da una chiave e un valore.

-   [\[\]Chiavi Autorun](#autorun-keys)
    -   [action](#parameters)
    -   [CustomEvent](#customevent)
    -   [icona](#parameters)
    -   [label](#parameters)
    -   [open](#parameters)
    -   [UseAutoPlay](#parameters)
    -   [ShellExecute](#shellexecute)
    -   [Shell](#autoruninf-entries)
    -   [Verbo della shell \\](#shellverb)
-   [\[\]Chiavi simmetriche](#content-keys)
-   [\[Chiavi di ExclusiveContentPaths \]](#exclusivecontentpaths-keys)
-   [\[Chiavi di IgnoreContentPaths \]](#ignorecontentpaths-keys)
-   [\[Chiavi di DeviceInstall \]](#deviceinstall-keys)
    -   [DriverPath](#driverpath)

## <a name="autorun-keys"></a>\[\]Chiavi Autorun

-   [action](#parameters)
-   [CustomEvent](#customevent)
-   [icona](#parameters)
-   [label](#parameters)
-   [open](#parameters)
-   [UseAutoPlay](#parameters)
-   [ShellExecute](#shellexecute)
-   [Shell](#autoruninf-entries)
-   [Verbo della shell \\](#shellverb)

### <a name="action"></a>azione

La voce **Action** specifica il testo usato nella finestra di dialogo AutoPlay per il gestore che rappresenta il programma specificato nella voce [Open](#parameters) o [ShellExecute](#shellexecute) nel file Autorun. inf del supporto. Il valore può essere espresso come testo o come risorsa archiviata in un file binario.


```
action=ActionText
```




```
action=@[filepath\]filename,-resourceID
```



### <a name="parameters"></a>Parametri

-   *ActionText*

    Testo utilizzato nella finestra di dialogo AutoPlay per il gestore che rappresenta il programma specificato nella voce [Open](#parameters) o [ShellExecute](#shellexecute) nel file Autorun. inf del supporto.

-   *FilePath*

    Stringa che contiene il percorso completo della directory che contiene il file binario contenente la stringa. Se non viene specificato alcun percorso, il file deve trovarsi nella directory radice dell'unità.

-   *filename*

    Stringa che contiene il nome del file binario.

-   *resourceID*

    ID della stringa nel file binario.

### <a name="remarks"></a>Commenti

La chiave **Action** viene utilizzata solo in Windows XP Service Pack 2 (SP2) o versioni successive. È supportato solo per le unità di tipo unità \_ rimovibili e unità \_ fisse. Nel caso di un'unità \_ rimovibile, la chiave dell' **azione** è obbligatoria. Un comando di **azione** nel file Autorun. inf di un CD audio o di un DVD di film viene ignorato e questi supporti continuano a funzionare come in Windows XP Service Pack 1 (SP1) e versioni precedenti.

La stringa visualizzata nella finestra di dialogo AutoPlay viene costruita combinando il testo specificato nella voce di **azione** con un testo hardcoded che denomina il provider, fornito dalla Shell. L' [icona](#parameters) viene visualizzata accanto a essa. Questa voce viene sempre visualizzata come prima opzione nella finestra di dialogo AutoPlay ed è selezionata per impostazione predefinita. Se l'utente accetta l'opzione, viene avviata l'applicazione specificata dalla voce [Open](#parameters) o [ShellExecute](#shellexecute) nel file Autorun. inf del supporto. L'opzione **Esegui sempre l'azione selezionata** non è disponibile in questa situazione.

I tasti [Action](#parameters) e [Icon](#parameters) definiscono insieme la rappresentazione dell'applicazione visualizzata dall'utente finale nella finestra di dialogo AutoPlay. Devono essere composte in modo che gli utenti possano identificarle facilmente. Devono indicare che l'applicazione deve essere eseguita, la società che la ha creata ed eventuali personalizzazioni associate.

Per compatibilità con le versioni precedenti, la voce **azione** è facoltativa per i dispositivi di tipo unità \_ fisse. Per questo tipo, nella finestra di dialogo AutoPlay viene utilizzata una voce predefinita se nel file Autorun. inf non è presente alcuna voce di **azione** .

La voce di **azione** è obbligatoria per i dispositivi di tipo unità \_ rimovibile, che fino a questo momento non dispone del supporto Autorun. inf. Se non è presente alcuna voce di **azione** , viene visualizzata la finestra di dialogo AutoPlay, ma senza l'opzione per avviare il contenuto aggiuntivo.

### <a name="customevent"></a>CustomEvent

La voce **CustomEvent** specifica un evento di contenuto AutoPlay personalizzato.


```
CustomEvent=CustomEventName
```



### <a name="parameters"></a>Parametri

-   *CustomEventName*

    Stringa di testo contenente il nome dell'evento di contenuto AutoPlay. Il nome non deve contenere più di 100 caratteri alfanumerici.

### <a name="remarks"></a>Commenti

È possibile includere un nome di evento personalizzato nel file Autorun. inf di un volume. Quando AutoPlay chiede all'utente l'uso di un'applicazione con il volume, Visualizza solo le applicazioni che hanno effettuato la registrazione per il nome dell'evento personalizzato specificato. Per informazioni su come registrare un'applicazione come gestore per l'evento di contenuto AutoPlay personalizzato, vedere [avvio automatico con AutoPlay](/previous-versions/windows/apps/hh452731(v=win.10)) o [come registrare un gestore eventi](how-to-register-an-event-handler.md).

Nell'esempio seguente viene specificato il valore "MyContentOnArrival" come nuovo evento di contenuto AutoPlay.


```
CustomEvent=MyContentOnArrival
```



### <a name="icon"></a>icon

La voce **icona** specifica un'icona che rappresenta l'unità abilitata per l'esecuzione automatica nell'interfaccia utente di Windows.


```
icon=iconfilename[,index]
```



### <a name="parameters"></a>Parametri

-   *IconFileName*

    Nome di un file con estensione ICO, BMP, exe o dll contenente le informazioni sull'icona. Se un file contiene più di un'icona, è necessario specificare anche un indice in base zero dell'icona.

### <a name="remarks"></a>Commenti

L'icona, insieme all'etichetta, rappresenta l'unità abilitata per l'esecuzione automatica nell'interfaccia utente di Windows. Ad esempio, in Esplora risorse l'unità viene rappresentata da questa icona anziché dall'icona dell'unità standard. Il file dell'icona deve trovarsi nella stessa directory del file specificato dal comando [Apri](#parameters) .

Nell'esempio seguente viene specificata la seconda icona nel file di MyProg.exe.


```
icon=MyProg.exe,1
```



### <a name="label"></a>label

La voce **etichetta** specifica un'etichetta di testo che rappresenta l'unità abilitata per l'esecuzione automatica nell'interfaccia utente di Windows.


```
label=LabelText
```



### <a name="parameters"></a>Parametri

-   *LabelText*

    Stringa di testo contenente l'etichetta. Può contenere spazi e non deve contenere più di 32 caratteri.

> [!Note]  
> È possibile inserire un valore nel parametro **LabelText** che supera i 32 caratteri e non viene visualizzato alcun messaggio di errore. Tuttavia, nel sistema vengono visualizzati solo i primi 32 caratteri. Qualsiasi carattere dopo la 32a viene troncato e non viene visualizzato. Ad esempio, se **LabelText** è il seguente: label = "questo CD è progettato per essere il CD musicale finale". verrà visualizzato quanto segue: "questo CD è progettato per essere UL".

 

### <a name="remarks"></a>Commenti

L'etichetta, insieme a un'icona, rappresenta l'unità abilitata per l'esecuzione automatica nell'interfaccia utente di Windows.

Nell'esempio seguente viene specificato il valore "My Drive label" come etichetta dell'unità.


```
label=My Drive Label
```



### <a name="open"></a>apre

La voce di **apertura** specifica il percorso e il nome file dell'applicazione avviata dall'avvio automatico quando un utente inserisce un disco nell'unità.


```
open=[exepath\]exefile [param1 [param2] ...] 
```



### <a name="parameters"></a>Parametri

-   *exefile*

    Percorso completo di un file eseguibile che viene eseguito al momento dell'inserimento del CD. Se viene specificato solo un nome file, deve trovarsi nella directory radice dell'unità. Per individuare il file in una sottodirectory, è necessario specificare un percorso. È inoltre possibile includere uno o più parametri della riga di comando da passare all'applicazione di avvio.

### <a name="useautoplay"></a>UseAutoPlay

In Windows XP, la voce **UseAutoPlay** specifica che è necessario usare AutoPlay anziché Autorun.

In Windows Vista e versioni successive, questa voce provoca l'eliminazione di tutte le azioni specificate per l'esecuzione automatica (usando le voci **Open** o **ShellExecute** ) dalla finestra di dialogo AutoPlay. Questa voce non ha alcun effetto sulle versioni di Windows precedenti a Windows XP.

In Windows 8 e versioni successive, se si specifica il valore 0 verrà disabilitato AutoPlay per questo dispositivo.

### <a name="parameters"></a>Parametri

Per usare questa opzione, aggiungere una voce per **UseAutoPlay** al file Autorun. inf e impostare la voce uguale a 1. Nessun altro valore è supportato nelle versioni di Windows precedenti a Windows 8.

In Windows 8 e versioni successive, specificare il valore 0 per disabilitare AutoPlay per questo dispositivo.


```
UseAutoPlay=1
```



### <a name="remarks"></a>Commenti

Attualmente, **UseAutoPlay** è applicabile solo in Windows XP o versioni successive e solo in un'unità che [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea) determina di essere di tipo **unità \_ CDROM**.

Quando si utilizza **UseAutoPlay** , qualsiasi azione specificata dalle voci **aperte** o **ShellExecute** in autorun. inf viene ignorata in Windows XP e omessa dalla finestra di dialogo AutoPlay in Windows Vista.

AutoRun viene in genere usato per eseguire automaticamente o caricare elementi contenuti nel supporto inserito, mentre AutoPlay visualizza una finestra di dialogo che include un elenco di azioni rilevanti che possono essere eseguite e consente all'utente di scegliere l'azione da eseguire. Per ulteriori informazioni sulla differenza tra AutoRun e AutoPlay, vedere [creazione di un'applicazione CD-ROM abilitata per l'autorun](autoplay.md) e [utilizzo e configurazione di AutoPlay](autoplay2k-using.md), rispettivamente.

### <a name="usage-example"></a>Esempio di utilizzo

Un CD contiene tre file: Autorun. inf, Readme.txt e Music. WMA. A seconda della versione di Windows in uso e delle opzioni specificate in autorun. inf, il CD può essere gestito da AutoRun o AutoPlay quando viene inserito (presupponendo che AutoRun/AutoPlay sia abilitato per l'unità in cui viene inserito il CD).

In primo luogo, si consideri un file Autorun. inf con il contenuto seguente, notando che **UseAutoPlay = 1** non è specificato:


```
[AutoRun]
shellexecute="Readme.txt"
```



L'azione eseguita dalla shell quando questo CD viene inserito dipende dalla versione di Windows in uso:

-   In Windows XP o versioni precedenti, questo CD viene gestito da AutoRun quando viene inserito. In questo caso, viene letta la voce **ShellExecute** e la shell richiama il gestore di file associato ai file con estensione txt; in genere, questo si apre Readme.txt nel blocco note.
-   In Windows Vista, la presenza di un file Autorun. inf con una voce **ShellExecute** fa sì che il supporto venga identificato come AutoPlay di tipo "software e giochi". In questo caso l'utente viene visualizzato con una finestra di dialogo AutoPlay che include l'azione specificata dalla voce **ShellExecute** (visualizzata come "Load Readme.txt" nella finestra di dialogo), insieme a azioni predefinite associate a supporti di tipo "software e giochi".

Per indicare che è necessario utilizzare AutoPlay anziché l'esecuzione automatica in Windows XP e che l'azione specificata dalla voce ShellExecute di AutoRun debba essere eliminata dalla finestra di dialogo AutoPlay in Windows Vista, inserire **UseAutoPlay** nel file Autorun. inf come indicato di seguito:


```
[AutoRun]
shellexecute="Readme.txt"
UseAutoPlay=1
```



Ancora una volta, l'azione eseguita dalla shell quando questo CD viene inserito dipende dalla versione di Windows in uso.

-   Nelle versioni di Windows precedenti a Windows XP, viene ancora utilizzato l'esecuzione automatica e viene eseguita l'azione specificata da **ShellExecute** , come descritto in precedenza. Si noti che solo l'esecuzione automatica è disponibile nelle versioni di Windows precedenti a Windows XP.
-   In Windows XP, la voce **UseAutoPlay** fa sì che AutoPlay venga usato al posto dell'autorun. In questo caso, AutoPlay determina che il supporto contiene un file di Windows Media Audio (WMA) e categorizza il contenuto come "file musicali". L'utente viene visualizzato con una finestra di dialogo AutoPlay contenente i gestori registrati per il tipo di supporto AutoPlay "Music Files"; la voce ShellExecute AutoRun viene ignorata.

### <a name="shellexecute"></a>ShellExecute

[Versione 5,0.](versions.md) La voce **ShellExecute** specifica un'applicazione o un file di dati che l'esecuzione automatica userà per chiamare [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).


```
shellexecute=[filepath\]filename[param1, [param2]...] 
```



### <a name="parameters"></a>Parametri

-   *FilePath*

    Stringa che contiene il percorso completo della directory che contiene i dati o il file eseguibile. Se non viene specificato alcun percorso, il file deve trovarsi nella directory radice dell'unità.

-   *filename*

    Stringa che contiene il nome del file. Se è un file eseguibile, viene avviato. Se è un file di dati, deve essere un membro di un [tipo di file](fa-file-types.md). [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) avvia il comando predefinito associato al tipo di file.

-   *paramx*

    Contiene eventuali parametri aggiuntivi che devono essere passati a [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).

### <a name="remarks"></a>Commenti

Questa voce è simile a [Apri](#parameters), ma consente di usare le informazioni di [associazione file](fa-intro.md) per eseguire l'applicazione.

### <a name="shell"></a>shell

La voce della **Shell** specifica un comando predefinito per il menu di scelta rapida dell'unità.


```
shell=verb
```



### <a name="parameters"></a>Parametri

-   *verb*

    Verbo che corrisponde al comando di menu. Il verbo e il relativo comando di menu associato devono essere definiti nel file Autorun. inf con una voce del [ \\ verbo della shell](#shellverb) .

### <a name="remarks"></a>Commenti

Quando si fa clic con il pulsante destro del mouse sull'icona dell'unità, viene visualizzato un menu di scelta rapida. Se è presente un file Autorun. inf, viene sottratto il comando di menu di scelta rapida predefinito. Questo comando viene eseguito anche quando l'utente fa doppio clic sull'icona dell'unità.

Per specificare il comando di menu di scelta rapida predefinito, definirne innanzitutto il verbo, la stringa di comando e il testo del menu con il [ \\ verbo della shell](#shellverb). Usare quindi Shell per impostarlo come comando di menu di scelta rapida predefinito. In caso contrario, il testo predefinito della voce di menu sarà "AutoPlay", che avvia l'applicazione specificata dalla voce di [apertura](#parameters) .

### <a name="shellverb"></a>Verbo della shell \\

La voce del **\\ verbo della shell** aggiunge un comando personalizzato al menu di scelta rapida dell'unità.


```
shell\verb\command=Filename.exe 
shell\verb=MenuText
```



### <a name="parameters"></a>Parametri

-   *verb*

    Verbo del comando di menu. La voce di *_\\ comando_* del _verbo_ della **Shell \\** associa il verbo a un file eseguibile. I verbi non devono contenere spazi incorporati. Per impostazione predefinita, *Verb* è il testo visualizzato nel menu di scelta rapida.

-   *Filename.exe*

    Il percorso e il nome file dell'applicazione che esegue l'azione.

-   *MenuText*

    Questo parametro specifica il testo visualizzato nel menu di scelta rapida. Se viene omesso, viene visualizzato il *verbo* . *MenuText* può essere costituito da maiuscole e minuscole e può contenere spazi. È possibile impostare un tasto di scelta rapida per la voce di menu inserendo una e commerciale (&) davanti alla lettera.

### <a name="remarks"></a>Commenti

Quando si fa clic con il pulsante destro del mouse sull'icona dell'unità, viene visualizzato un menu di scelta rapida. L'aggiunta di voci di **\\ verbi Shell** al file Autorun. inf dell'unità consente di aggiungere comandi a questo menu di scelta rapida.

Questa voce è costituita da due parti, che devono essere su righe separate. La prima parte è il *_\\ comando_* del _verbo_ della **Shell \\**. Questo argomento è obbligatorio. Associa una stringa, denominata *verbo*, con l'applicazione da avviare quando viene eseguito il comando. La seconda parte è la voce del _verbo_ della **Shell \\**. Questo passaggio è facoltativo. È possibile includerlo per specificare il testo visualizzato nel menu di scelta rapida.

Per specificare un comando di menu di scelta rapida predefinito, definire il verbo con il **\\ verbo della shell** e impostarlo come comando predefinito con la voce della [Shell](#autoruninf-entries) .

Il frammento di autorun. inf di esempio seguente associa il verbo *pronto* con la stringa di comando "Notepad ABC \\readme.txt". Il testo del menu è "Read me" è m'è definito come il tasto di scelta rapida dell'elemento. Quando l'utente seleziona questo comando, \\ viene aperto il file abcreadme.txt dell'unità con il blocco note di Microsoft.


```
shell\readit\command=notepad abc\readme.txt 
shell\readit=Read &Me
```



## <a name="content-keys"></a>\[\]Chiavi simmetriche

Sono disponibili tre chiavi di tipo file: **MusicFiles**, **PictureFiles** e **VideoFiles**.

Se uno di questi contenuti viene impostato su true tramite uno dei valori 1, y, Yes, t o true senza distinzione tra maiuscole e minuscole, l'interfaccia utente di AutoPlay Visualizza i gestori associati a tale tipo di contenuto, indipendentemente dal fatto che il contenuto del tipo esista sul supporto.

Se uno di questi contenuti viene impostato su false tramite uno dei valori 0, n, no, f o false senza distinzione tra maiuscole e minuscole, l'interfaccia utente di AutoPlay non Visualizza i gestori associati a tale tipo di contenuto anche se il contenuto del tipo viene rilevato sul supporto.

L'uso di questa sezione consente agli autori di contenuti di comunicare lo scopo del contenuto a AutoPlay. Ad esempio, un CD può essere categorizzato in modo da contenere solo contenuto musicale anche se contiene anche immagini e video e altrimenti verrebbe visualizzato come contenuto misto.

La sezione **\[ Content \]** è supportata solo in Windows Vista e versioni successive.


```
[Content]
MusicFiles=Y
PictureFiles=0
VideoFiles=false
```



## <a name="exclusivecontentpaths-keys"></a>\[Chiavi di ExclusiveContentPaths \]

Le cartelle elencate in questa sezione limitano AutoPlay alla ricerca di contenuto solo nelle cartelle e nelle relative sottocartelle. Possono essere specificati con o senza una barra rovesciata principale ( \\ ). In entrambi i casi vengono considerati percorsi assoluti dalla directory radice del supporto. Nel caso di cartelle con spazi nei nomi, non racchiuderle tra virgolette poiché le virgolette vengono eseguite letteralmente come parte del percorso.

L'uso di questa sezione ha lo scopo di consentire agli autori di contenuti di comunicare lo scopo del contenuto a AutoPlay e di abbreviare il tempo di analisi limitando l'analisi a determinate aree significative del supporto.

Di seguito sono riportati tutti i percorsi validi


```
[ExclusiveContentPaths]
\music
\music\more music
music2
```



La sezione **\[ ExclusiveContentPaths \]** è supportata solo in Windows Vista e versioni successive.

## <a name="ignorecontentpaths-keys"></a>\[Chiavi di IgnoreContentPaths \]

Le cartelle elencate in questa sezione e le relative sottocartelle vengono ignorate da AutoPlay durante la ricerca di contenuto in un supporto. Possono essere specificati con o senza una barra rovesciata principale ( \\ ). In entrambi i casi vengono considerati percorsi assoluti dalla directory radice del supporto. Nel caso di cartelle con spazi nei nomi, non racchiuderle tra virgolette poiché le virgolette vengono eseguite letteralmente come parte del percorso.

I percorsi in questa sezione hanno la precedenza sui percorsi nella sezione **\[ ExclusiveContentPaths \]** . Se un percorso specificato in **\[ IgnoreContentPaths \]** è una sottocartella di un percorso specificato in **\[ ExclusiveContentPaths \]**, viene comunque ignorato.

L'uso di questa sezione ha lo scopo di consentire agli autori di contenuti di comunicare lo scopo del contenuto a AutoPlay e di abbreviare il tempo di analisi limitando l'analisi a determinate aree significative del supporto.

Di seguito sono riportati tutti i percorsi validi


```
[IgnoreContentPaths]
\music
\music\more music
music2
```



La sezione **\[ IgnoreContentPaths \]** è supportata solo in Windows Vista e versioni successive.

## <a name="deviceinstall-keys"></a>\[Chiavi di DeviceInstall \]

### <a name="driverpath"></a>DriverPath

La voce **DriverPath** specifica una directory in cui eseguire la ricerca in modo ricorsivo per i file del driver. Questo comando viene usato durante l'installazione di un driver e non fa parte di un'operazione di esecuzione automatica. La sezione **\[ DeviceInstall \]** è supportata solo in Windows XP.


```
[DeviceInstall]
DriverPath=directorypath
```



### <a name="parameters"></a>Parametri

-   *DirectoryPath*

    Percorso di una directory in cui Windows cerca i file del driver, insieme a tutte le relative sottodirectory.

### <a name="remarks"></a>Commenti

Non usare lettere di unità in *DirectoryPath* quando cambiano da un computer a quello successivo.

Per eseguire la ricerca in più directory, aggiungere una voce **DriverPath** per ogni directory come in questo esempio.


```
[DeviceInstall]
DriverPath=drivers\video 
DriverPath=drivers\audio
```



Se nella sezione **\[ DeviceInstall \]** non è specificata alcuna voce **DriverPath** o la voce **DriverPath** non ha alcun valore, l'unità viene ignorata durante la ricerca dei file del driver.

 

 

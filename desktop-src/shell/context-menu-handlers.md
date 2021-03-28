---
description: I gestori dei menu di scelta rapida, noti anche come gestori di menu di scelta rapida o gestori di verbi, sono un tipo di gestore di tipi di file. Analogamente a tutti questi gestori, si tratta di oggetti COM (Component Object Model in-process) implementati come dll.
ms.assetid: cff79cdc-8a01-4575-9af7-2a485c6a8e46
title: Creazione di gestori di menu di scelta rapida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e8b7091483726c322a8ae18bace883af126d404
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "103885882"
---
# <a name="creating-shortcut-menu-handlers"></a>Creazione di gestori di menu di scelta rapida

I gestori dei menu di scelta rapida, noti anche come gestori di menu di scelta rapida o gestori di verbi, sono un tipo di gestore di tipi di file. Analogamente a tutti questi gestori, si tratta di oggetti COM (Component Object Model in-process) implementati come dll.

> [!Note]  
> Quando si registrano i gestori che operano nel contesto di applicazioni a 32 bit, è necessario tenere presenti alcune considerazioni speciali per Windows a 64 bit: quando i verbi della shell vengono richiamati nel contesto di un'applicazione a 32 bit, il sottosistema WOW64 reindirizza file system accesso ad alcuni percorsi. Se il gestore. exe viene archiviato in uno di questi percorsi, non è accessibile in questo contesto. Pertanto, come soluzione alternativa, archiviare il file con estensione exe in un percorso che non viene reindirizzato oppure archiviare una versione stub del file exe che avvia la versione reale.

 

Questo argomento è organizzato nel modo seguente:

-   [Verbi canonici](#canonical-verbs)
-   [Verbi estesi](#extended-verbs)
-   [Personalizzazione di un menu di scelta rapida con verbi statici](#customizing-a-shortcut-menu-using-static-verbs)
    -   [Attivazione del gestore mediante l'interfaccia IDropTarget](#activating-your-handler-using-the-idroptarget-interface)
    -   [Specifica della posizione e dell'ordine dei verbi statici](#specifying-the-position-and-order-of-static-verbs)
    -   [Posizionamento dei verbi nella parte superiore o inferiore del menu](#positioning-verbs-at-the-top-or-bottom-of-the-menu)
    -   [Creazione di menu a cascata statici](#creating-static-cascading-menus)
    -   [Ottenere il comportamento dinamico per i verbi statici usando la sintassi di query avanzata](#getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax)
    -   [Deprecato: associazione di verbi a Dynamic Data Exchange comandi](#deprecated-associating-verbs-with-dynamic-data-exchange-commands)
-   [Completamento delle attività di implementazione del verbo](#completing-verb-implementation-tasks)
    -   [Personalizzazione del menu di scelta rapida per oggetti shell predefiniti](#customizing-the-shortcut-menu-for-predefined-shell-objects)
    -   [Estensione di un nuovo sottomenu](#extending-a-new-submenu)
    -   [Eliminazione di verbi e controllo della visibilità](#suppressing-verbs-and-controlling-visibility)
    -   [Uso del modello di selezione dei verbi](#employing-the-verb-selection-model)
    -   [Uso degli attributi degli elementi](#using-item-attributes)
    -   [Implementazione di verbi personalizzati per le cartelle tramite Desktop.ini](#implementing-custom-verbs-for-folders-through-desktopini)
-   [Argomenti correlati](#related-topics)

## <a name="canonical-verbs"></a>Verbi canonici

Le applicazioni sono in genere responsabili di fornire stringhe di visualizzazione localizzate per i verbi definiti. Tuttavia, per fornire un livello di indipendenza dal linguaggio, il sistema definisce un set standard di verbi comunemente usati, detti verbi canonici. Un verbo canonico non viene mai visualizzato all'utente e può essere usato con qualsiasi lingua dell'interfaccia utente. Il sistema usa il nome canonico per generare automaticamente una stringa di visualizzazione localizzata correttamente. Ad esempio, la stringa di visualizzazione del verbo aperto è impostata per essere **aperta** in un sistema in lingua inglese e per l'equivalente tedesco in un sistema tedesco.



| Verbo canonico | Descrizione                                                          |
|----------------|----------------------------------------------------------------------|
| Apri           | Apre il file o la cartella.                                            |
| OpenNew        | Apre il file o la cartella in una nuova finestra.                            |
| Stampa          | Stampa il file.                                                     |
| Printto        | Consente all'utente di stampare un file trascinandolo in un oggetto Printer. |
| Esplora        | Apre Esplora risorse con la cartella selezionata.                     |
| Proprietà     | Apre la finestra delle proprietà dell'oggetto.                                   |



 

> [!Note]  
> Anche il verbo **printto** è canonico, ma non viene mai visualizzato. La relativa inclusione consente all'utente di stampare un file trascinandolo in un oggetto Printer.

 

I gestori dei menu di scelta rapida possono fornire i propri verbi canonici tramite [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) con **GC \_ VERBW** o **GC \_ Verba**. Il sistema utilizzerà i verbi canonici come secondo parametro (*lpOperation*) passato a [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)e sarà [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo). membro **lpVerb** passato al metodo [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) .

## <a name="extended-verbs"></a>Verbi estesi

Quando l'utente fa clic con il pulsante destro del mouse su un oggetto, nel menu di scelta rapida vengono visualizzati i verbi predefiniti. Potrebbe essere necessario aggiungere e supportare i comandi in alcuni menu di scelta rapida che non vengono visualizzati in ogni menu di scelta rapida. Ad esempio, è possibile avere comandi che non sono comunemente usati o destinati a utenti esperti. Per questo motivo, è anche possibile definire uno o più verbi estesi. Questi verbi sono simili ai verbi normali, ma si distinguono dai verbi normali in base alla modalità di registrazione. Per avere accesso ai verbi estesi, è necessario fare clic con il pulsante destro del mouse su un oggetto mentre si preme il tasto MAIUSC. Quando l'utente esegue questa operazione, vengono visualizzati i verbi estesi oltre ai verbi predefiniti.

È possibile utilizzare il registro di sistema per definire uno o più verbi estesi. I comandi associati verranno visualizzati solo quando l'utente fa clic con il pulsante destro del mouse su un oggetto e preme anche il tasto MAIUSC. Per definire un verbo come esteso, aggiungere un valore "Extended" **reg \_ SZ** alla sottochiave del verbo. Al valore non devono essere associati dati.

## <a name="customizing-a-shortcut-menu-using-static-verbs"></a>Personalizzazione di un menu di scelta rapida con verbi statici

Dopo aver [scelto un verbo statico o dinamico per il menu di scelta rapida](shortcut-choose-method.md) , è possibile estendere il menu di scelta rapida per un tipo di file registrando un verbo statico per il tipo di file. A tale scopo, aggiungere una sottochiave della **Shell** sotto la sottochiave per il ProgID dell'applicazione associata al tipo di file. Facoltativamente, è possibile definire un verbo predefinito per il tipo di file rendendolo il valore predefinito della sottochiave della **Shell** .

Il verbo predefinito viene visualizzato per primo nel menu di scelta rapida. Il suo scopo è fornire alla shell un verbo che può usare quando viene chiamata la funzione [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) , ma non viene specificato alcun verbo. La shell non seleziona necessariamente il verbo predefinito quando **ShellExecuteEx** viene usato in questo modo.

La shell usa il primo verbo disponibile nell'ordine seguente:

1.  Verbo predefinito
2.  Primo verbo nel registro di sistema, se è specificato l'ordine dei verbi
3.  Verbo di **apertura**
4.  Il verbo **Apri con**

Se nessuno dei verbi elencati è disponibile, l'operazione ha esito negativo.

Creare una sottochiave per ogni verbo che si vuole aggiungere nella sottochiave della shell. Ognuna di queste sottochiavi deve avere un valore **reg \_ SZ** impostato sulla stringa di visualizzazione del verbo (stringa localizzata). Per ogni sottochiave verbo, creare una sottochiave del comando con il valore predefinito impostato sulla riga di comando per attivare gli elementi. Per i verbi canonici, ad esempio **Open** e **Print**, è possibile omettere la stringa di visualizzazione perché il sistema visualizza automaticamente una stringa localizzata correttamente. Per i verbi non canonici, se si omette la stringa di visualizzazione, viene visualizzata la stringa del verbo.

Nell'esempio di registro di sistema seguente si noti che:

-   Poiché **doit** non è un verbo canonico, viene assegnato un nome visualizzato, che può essere selezionato premendo il tasto D.
-   Il verbo **printto** non viene visualizzato nel menu di scelta rapida. Tuttavia, l'inclusione nel registro di sistema consente all'utente di stampare i file trascinandoli su un'icona della stampante.
-   Viene visualizzata una sottochiave per ogni verbo. **%1** rappresenta il nome del file e **%2** il nome della stampante.

```
HKEY_CLASSES_ROOT
   .myp-ms
      (Default) = MyProgram.1
      MyProgram.1
         (Default) = My Program Application
         Shell
            (Default) = doit
            doit
               (Default) = &Do It
               command
                  (Default) = c:\MyDir\MyProgram.exe /d "%1"
            open
               command
                  (Default) = c:\MyDir\MyProgram.exe /d "%1"
            print
               command
                  (Default) = c:\MyDir\MyProgram.exe /p "%1"
            printto
               command
                  (Default) = c:\MyDir\MyProgram.exe /p "%1" "%2"
```

Nel diagramma seguente viene illustrata l'estensione del menu di scelta rapida in base alle voci del registro di sistema riportate sopra. Questo menu di scelta rapida presenta i verbi **Apri**, **Esegui** e **stampa** nel menu, con **Esegui** come verbo predefinito.

![screenshot del menu di scelta rapida per i verbi predefiniti](images/context-menu/context-doitdefaultverb.png)

### <a name="activating-your-handler-using-the-idroptarget-interface"></a>Attivazione del gestore mediante l'interfaccia IDropTarget

Dynamic Data Exchange (DDE) è deprecato. in alternativa, usare [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) . **IDropTarget** è più affidabile e offre un supporto migliore per l'attivazione perché usa l'attivazione com del gestore. Nel caso di selezione di più elementi, **IDropTarget** non è soggetto alle limitazioni delle dimensioni del buffer presenti sia in DDE che in [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa). Inoltre, gli elementi vengono passati all'applicazione come oggetto dati che può essere convertito in una matrice di elementi tramite la funzione [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) . Questa operazione è più semplice e non perde le informazioni sullo spazio dei nomi come si verifica quando l'elemento viene convertito in un percorso per i protocolli della riga di comando o DDE.

Per ulteriori informazioni sulle query [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) e Shell per gli attributi di associazione file, vedere [tipi percepiti e registrazione di applicazioni](fa-perceivedtypes.md).

### <a name="specifying-the-position-and-order-of-static-verbs"></a>Specifica della posizione e dell'ordine dei verbi statici

In genere i verbi vengono ordinati in un menu di scelta rapida in base alla modalità di enumerazione. l'enumerazione è basata innanzitutto sull'ordine della matrice di associazioni, quindi sull'ordine degli elementi nella matrice di associazioni, come definito dall'ordinamento del registro di sistema.

È possibile ordinare i verbi specificando il valore predefinito della sottochiave della Shell per la voce di associazione. Questo valore predefinito può includere un singolo elemento, che verrà visualizzato nella posizione superiore del menu di scelta rapida o un elenco di elementi separati da spazi o virgole. Nel secondo caso, il primo elemento dell'elenco è l'elemento predefinito e gli altri verbi vengono visualizzati immediatamente sotto nell'ordine specificato.

Ad esempio, la voce del registro di sistema seguente produce i verbi del menu di scelta rapida nell'ordine seguente:

1.  Visualizza
2.  Gadget
3.  Personalization

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell
         Display
         Gadgets
         Personalization
```

Analogamente, la voce del registro di sistema seguente produce i verbi del menu di scelta rapida nell'ordine seguente:

1.  Personalization
2.  Gadget
3.  Visualizza

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell = "Personalization,Gadgets"
      Display
```

### <a name="positioning-verbs-at-the-top-or-bottom-of-the-menu"></a>Posizionamento dei verbi nella parte superiore o inferiore del menu

L'attributo del registro di sistema seguente può essere usato per inserire un verbo nella parte superiore o inferiore del menu. Se sono presenti più verbi che specificano questo attributo, l'ultimo a tale scopo ottiene la priorità:

``` syntax
Position=Top | Bottom 
```

### <a name="creating-static-cascading-menus"></a>Creazione di menu a cascata statici

In Windows 7 e versioni successive, l'implementazione del menu a cascata è supportata tramite le impostazioni del registro di sistema. Prima di Windows 7, la creazione dei menu a cascata era possibile solo tramite l'implementazione dell'interfaccia [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) . In Windows 7 e versioni successive, è consigliabile ricorrere alle soluzioni COM basate su codice solo quando i metodi statici sono insufficienti.

Lo screenshot seguente fornisce un esempio di menu a cascata.

![screenshot che mostra un esempio di menu a cascata](images/file-assoc/filecascademenu2ndex.png)

In Windows 7 e versioni successive sono disponibili tre modi per creare i menu a cascata:

-   [Creazione di menu a cascata con la voce del registro di sistema subcommands](#creating-cascading-menus-with-the-subcommands-registry-entry)
-   [Creazione di menu a cascata con la voce del registro di sistema ExtendedSubCommandsKey](#creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry)
-   [Creazione di menu a cascata con l'interfaccia IExplorerCommand](#creating-cascading-menus-with-the-iexplorercommand-interface)

### <a name="creating-cascading-menus-with-the-subcommands-registry-entry"></a>Creazione di menu a cascata con la voce del registro di sistema subcommands

In Windows 7 e versioni successive, è possibile usare la voce sottocomandi per creare menu a cascata usando la procedura seguente.

**Per creare un menu a cascata utilizzando la voce sottocomandi**

1.  Creare una sottochiave in **HKEY \_ classi \_ radice** \\ *ProgID* \\ **Shell** per rappresentare il menu a cascata. In questo esempio viene assegnata questa sottochiave al nome *CascadeTest*. Verificare che il valore predefinito della sottochiave *CascadeTest* sia vuoto e visualizzato come **(valore non impostato)**.

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
    ```

2.  Nella sottochiave *CascadeTest* aggiungere una voce MUIVerb di tipo **reg \_ SZ** e assegnarle il testo che verrà visualizzato come nome nel menu di scelta rapida. In questo esempio viene assegnato il "menu test Cascade".

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu
    ```

3.  Nella sottochiave *CascadeTest* aggiungere una voce di sottocomandi di tipo **reg \_ SZ** a cui viene assegnato un elenco, demlimited da punti e virgola, dei verbi che devono essere visualizzati nel menu in ordine di aspetto. Ad esempio, di seguito viene assegnato un numero di verbi forniti dal sistema:

    ```
    HKEY_CLASSES_ROOT
       *
          Shell
             CascadeTest
                SubCommands
                Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
    ```

4.  Nel caso di verbi personalizzati, implementarli usando uno dei metodi di implementazione del verbo statico ed elencarli sotto la sottochiave **CommandStore** , come illustrato in questo esempio per un verbo fittizio *verbname*:

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      CommandStore
                         Shell
                            VerbName
                            command
                               (Default) = notepad.exe %1
    ```

> [!Note]  
> Questo metodo ha il vantaggio di poter registrare i verbi personalizzati una volta e riutilizzarli elencando il nome del verbo nella voce dei sottocomandi. Tuttavia, richiede che l'applicazione disponga delle autorizzazioni necessarie per modificare il registro di sistema nel **\_ \_ computer locale HKEY**.

 

### <a name="creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry"></a>Creazione di menu a cascata con la voce del registro di sistema ExtendedSubCommandsKey

In Windows 7 e versioni successive, è possibile usare la voce ExtendedSubCommandKey per creare menu a cascata estesi: menu a cascata nei menu a cascata.

Lo screenshot seguente è un esempio di menu a cascata esteso.

![screenshot che mostra il menu a cascata esteso per i dispositivi](images/file-assoc/extendedsubcommandskey.png)

Poiché **la \_ \_ radice delle classi HKEY** è una combinazione di **HKEY \_ Current \_ User** e **HKEY \_ Local \_ computer**, è possibile registrare i verbi personalizzati nella sottochiave classi software **\_ \_ utente corrente HKEY** \\  \\  . Il vantaggio principale di questa operazione è che non è necessaria l'autorizzazione con privilegi elevati. Inoltre, altre associazioni di file possono riutilizzare l'intero set di verbi specificando la stessa sottochiave ExtendedSubCommandsKey. Se non è necessario riutilizzare questo set di verbi, è possibile elencare i verbi sotto l'elemento padre, ma assicurarsi che il valore predefinito dell'elemento padre sia vuoto.

**Per creare un menu a cascata utilizzando una voce ExtendedSubCommandsKey**

1.  Creare una sottochiave in **HKEY \_ classi \_ radice** \\ *ProgID* \\ **Shell** per rappresentare il menu a cascata. In questo esempio viene assegnata questa sottochiave al nome *CascadeTest2*. Verificare che il valore predefinito della sottochiave *CascadeTest* sia vuoto e visualizzato come **(valore non impostato)**.

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest2
                (Default)
    ```

2.  Nella sottochiave *CascadeTest* aggiungere una voce MUIVerb di tipo **reg \_ SZ** e assegnarle il testo che verrà visualizzato come nome nel menu di scelta rapida. In questo esempio viene assegnato il "menu test Cascade".

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu 2
    ```

3.  Nella sottochiave *CascadeTest* creata aggiungere una sottochiave **ExtendedSubCommandsKey** e quindi aggiungere il documento sottocomandi (di tipo **reg \_ SZ** ), ad esempio:

    ```
    HKEY_CLASSES_ROOT
       txtfile
          Shell
             Test Cascade Menu 2
                (Default)
                ExtendedSubCommandsKey
                   Layout
                   Properties
                   Select all
    ```

    Verificare che il valore predefinito della sottochiave del *menu 2 di test Cascade* sia vuoto e visualizzato come **(valore non impostato)**.

4.  Popolare i sottoverbi utilizzando una delle seguenti implementazioni di verbi statici. Si noti che la sottochiave CommandFlags rappresenta i valori EXPCMDFLAGS. Se si desidera aggiungere un separatore prima o dopo la voce di menu a cascata, utilizzare ECF \_ SEPARATORBEFORE (0x20) o ECF \_ SEPARATORAFTER (0x40). Per una descrizione di questi flag di Windows 7 e versioni successive, vedere [**IExplorerCommand:: GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags). ECF \_ SEPARATORBEFORE funziona solo per le voci di menu di primo livello. MUIVerb è di tipo **reg \_ SZ** e CommandFlags è di tipo **reg \_ DWORD**.

    ```
    HKEY_CLASSES_ROOT
       txtile
          Shell
             Test Cascade Menu 2
                (Default)
                ExtendedSubCommandsKey
                   Shell
                      cmd1
                         MUIVerb = Notepad
                         command
                            (Default) = %SystemRoot%\system32\notepad.exe %1
                      cmd2
                         MUIVerb = Wordpad
                         CommandFlags = 0x20
                         command
                            (Default) = "C:\Program Files\Windows NT\Accessories\wordpad.exe" %1
    ```

Lo screenshot seguente illustra i precedenti esempi di voci della chiave del registro di sistema.

![screenshot che mostra un esempio di menu a cascata che mostra le scelte del blocco note e di WordPad](images/file-assoc/testcascademenu2.png)

### <a name="creating-cascading-menus-with-the-iexplorercommand-interface"></a>Creazione di menu a cascata con l'interfaccia IExplorerCommand

Un'altra opzione per l'aggiunta di verbi a un menu a cascata consiste nell'usare [**IExplorerCommand:: EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands). Questo metodo consente alle origini dati che forniscono i comandi del modulo di comando tramite [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) di utilizzare tali comandi come verbi in un menu di scelta rapida. In Windows 7 e versioni successive, è possibile fornire la stessa implementazione del verbo usando [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) , come è possibile con [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).

Le due schermate seguenti illustrano l'uso dei menu a cascata nella cartella **Devices** .

![Screenshot che mostra un esempio di menu a cascata nella cartella Devices (dispositivi).](images/file-assoc/filecascademenu.png)

Lo screenshot seguente illustra un'altra implementazione di un menu a cascata nella cartella **Devices** .

![screenshot che mostra un esempio di menu a cascata nella cartella Devices](images/file-assoc/cascadedevices2.png)

> [!Note]  
> Poiché [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) supporta solo l'attivazione in-process, è consigliabile usare le origini dati della shell che devono condividere l'implementazione tra i comandi e i menu di scelta rapida.

 

### <a name="getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax"></a>Ottenere il comportamento dinamico per i verbi statici usando la sintassi di query avanzata

La sintassi di query avanzata (AQS) può esprimere una condizione che verrà valutata utilizzando le proprietà dell'elemento per cui viene creata un'istanza del verbo. Questo sistema funziona solo con proprietà veloci. Si tratta di proprietà che l'origine dati della shell segnala come Fast senza restituire [* * * * SHCOLSTATE \_ Slow * *](/windows/win32/api/shtypes/ne-shtypes-shcolstate) * * da [**IShellFolder2:: GetDefaultColumnState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultcolumnstate).

Windows 7 e versioni successive supportano valori canonici che evitano problemi nelle compilazioni localizzate. La sintassi canonica seguente è obbligatoria per le compilazioni localizzate per sfruttare i vantaggi di questa funzionalità avanzata di Windows 7.

``` syntax
System.StructuredQueryType.Boolean#True
```

Nell'esempio seguente voce del registro di sistema:

-   Il valore **appliesTo** controlla se il verbo è visualizzato o nascosto.
-   Il valore DefaultAppliesTo controlla il verbo predefinito.
-   Il valore HasLUAShield controlla se viene visualizzato uno scudo controllo dell'account utente (UAC).

In questo esempio il valore **DefaultAppliesTo** rende questo verbo l'impostazione predefinita per qualsiasi file con la parola "exampleText1" nel nome file. Il valore **appliesTo** Abilita il verbo per tutti i file con "exampleText1" nel nome. Il valore **HasLUAShield** Visualizza lo scudo per i file con "exampleText2" nel nome.

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            DefaultAppliesTo = System.ItemName:"exampleText1"
            HasLUAShield = System.ItemName:"exampleText2"
            AppliesTo = System.ItemName:"exampleText1"
```

Aggiungere la sottochiave del **comando** e un valore:

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            Command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

Nel registro di sistema di Windows 7, vedere **HKEY \_ classi \_ radice** \\ **unità** come esempio di verbi BitLocker che usano l'approccio seguente:

-   AppliesTo = System. volume. BitlockerProtection: = 2
-   System. volume. BitlockerRequiresAdmin: = System. StructuredQueryType. Boolean \# true

Per ulteriori informazioni su AQS, vedere [sintassi di query avanzata](../search/-search-3x-advancedquerysyntax.md).

### <a name="deprecated-associating-verbs-with-dynamic-data-exchange-commands"></a>Deprecato: associazione di verbi a Dynamic Data Exchange comandi

Il DDE è deprecato; in alternativa, usare [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) . Il DDE è deprecato perché si basa su un messaggio della finestra di trasmissione per individuare il server DDE. Un blocco del server DDE blocca il messaggio della finestra di trasmissione e quindi blocca le conversazioni DDE per le altre applicazioni. Una singola applicazione bloccata può causare blocchi successivi nell'esperienza dell'utente.

Il metodo [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) è più affidabile e offre un supporto migliore per l'attivazione perché utilizza l'attivazione com del gestore. Nel caso di selezione di più elementi, **IDropTarget** non è soggetto alle limitazioni delle dimensioni del buffer presenti sia in DDE che in [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa). Inoltre, gli elementi vengono passati all'applicazione come oggetto dati che può essere convertito in una matrice di elementi tramite la funzione [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) . Questa operazione è più semplice e non perde le informazioni sullo spazio dei nomi come si verifica quando l'elemento viene convertito in un percorso per i protocolli della riga di comando o DDE.

Per ulteriori informazioni sulle query [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) e Shell per gli attributi di associazione file, vedere [tipi percepiti e registrazione di applicazioni](fa-perceivedtypes.md).

## <a name="completing-verb-implementation-tasks"></a>Completamento delle attività di implementazione del verbo

Le attività seguenti per l'implementazione dei verbi sono rilevanti per le implementazioni di verbi statici e dinamici. Per altre informazioni sui verbi dinamici, vedere [personalizzazione di un menu di scelta rapida con verbi dinamici](shortcut-menu-using-dynamic-verbs.md).

### <a name="customizing-the-shortcut-menu-for-predefined-shell-objects"></a>Personalizzazione del menu di scelta rapida per oggetti shell predefiniti

Molti oggetti shell predefiniti dispongono di menu di scelta rapida che possono essere personalizzati. Registrare il comando nello stesso modo in cui si registrano i tipi di file tipici, ma usare il nome dell'oggetto predefinito come nome del tipo di file.

Un elenco di oggetti predefiniti si trova nella sezione *oggetti shell predefiniti* della creazione di [gestori di estensioni della shell](handlers.md). Gli oggetti shell predefiniti i cui menu di scelta rapida possono essere personalizzati aggiungendo verbi nel registro di sistema vengono contrassegnati nella tabella con il verbo di parola.

### <a name="extending-a-new-submenu"></a>Estensione di un nuovo sottomenu

Quando un utente apre il menu **file** in Esplora risorse, uno dei comandi visualizzati è **nuovo**. Se si seleziona questo comando, verrà visualizzato un sottomenu. Per impostazione predefinita, il sottomenu contiene due comandi, **cartella** e **collegamento**, che consentono agli utenti di creare sottocartelle e collegamenti. Questo sottomenu può essere esteso in modo da includere i comandi per la creazione di file per qualsiasi tipo di file.

Per aggiungere un comando per la creazione di file al **nuovo** sottomenu, i file dell'applicazione devono avere un tipo di file associato. Includere una sottochiave **ShellNew** sotto il nome del file. Quando si seleziona il comando **nuovo** del menu **file** , la shell aggiunge il tipo di file al **nuovo** sottomenu. La stringa di visualizzazione del comando è la stringa descrittiva assegnata al ProgID del programma.

Per specificare il metodo di creazione del file, assegnare uno o più valori di dati alla sottochiave **ShellNew** . I valori disponibili sono elencati nella tabella seguente.



| Valore sottochiave ShellNew | Descrizione                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Comando               | Esegue un'applicazione. Questo valore **reg \_ SZ** specifica il percorso dell'applicazione da eseguire. Ad esempio, è possibile impostarlo per avviare una procedura guidata.                  |
| Dati                  | Crea un file contenente i dati specificati. Questo **valore \_ binario REG** specifica i dati del file. Se è specificato **NullFile** o **filename** , **i dati** vengono ignorati. |
| FileName              | Crea un file che è una copia di un file specificato. Questo valore **reg \_ SZ** specifica il percorso completo del file da copiare.                                   |
| NullFile              | Crea un file vuoto. A **NullFile** non è stato assegnato alcun valore. Se viene specificato **NullFile** , i valori del registro di sistema **Data** e **filename** verranno ignorati.                    |



 

Il seguente esempio di chiave del registro di sistema e screenshot illustrano il **nuovo** sottomenu per il tipo di file. MYP-ms. Dispone di un comando, **applicazione programmi**.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      MyProgram.1
         ShellNew
         NullFile
```

Lo screenshot illustra il **nuovo** sottomenu. Quando un utente seleziona l' **applicazione di programma** dal **nuovo** sottomenu, la shell crea un file denominato **nuovo programma Application. MYP-ms** e lo passa a **MyProgram.exe**.

![Screenshot di Esplora risorse che mostra un nuovo comando "programma applicazione" nel sottomenu "nuovo"](images/context-menu/context-myprogramexe.png)

### <a name="creating-drag-and-drop-handlers"></a>Creazione di gestori di trascinamento della selezione

La procedura di base per l'implementazione di un gestore di trascinamento della selezione è identica a quella dei gestori di menu di scelta rapida convenzionali. Tuttavia, i gestori dei menu di scelta rapida usano in genere solo il puntatore [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) passato al metodo [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) del gestore per estrarre il nome dell'oggetto. Un gestore di trascinamento della selezione può implementare un gestore dati più sofisticato per modificare il comportamento dell'oggetto trascinato.

Quando un utente fa clic con il pulsante destro del mouse su un oggetto Shell per trascinare un oggetto, viene visualizzato un menu di scelta rapida quando l'utente tenta di eliminare l'oggetto. Lo screenshot seguente illustra un tipico menu di scelta rapida con trascinamento della selezione.

![screenshot del menu di scelta rapida del trascinamento della selezione](images/context-menu/context-dragdrop.png)

Un gestore di trascinamento della selezione è un gestore di menu di scelta rapida che consente di aggiungere elementi a questo menu di scelta rapida. I gestori di trascinamento della selezione vengono in genere registrati nella sottochiave seguente.

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
```

Aggiungere una sottochiave nella sottochiave **DragDropHandlers** denominata per il gestore di trascinamento della selezione e impostare il valore predefinito della sottochiave sul formato stringa del GUID dell'identificatore di classe del gestore (CLSID). Nell'esempio seguente viene abilitato il gestore di trascinamento della selezione **MyDD** .

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
            MyDD
               (Default) = {MyDD CLSID GUID}
```

### <a name="suppressing-verbs-and-controlling-visibility"></a>Eliminazione di verbi e controllo della visibilità

È possibile utilizzare le impostazioni dei criteri di Windows per controllare la visibilità dei verbi. I verbi possono essere eliminati tramite le impostazioni dei criteri aggiungendo un valore **SuppressionPolicy** o un valore GUID **SuppressionPolicyEx** alla sottochiave del registro di sistema del verbo. Impostare il valore della sottochiave **SuppressionPolicy** sull'ID criterio. Se il criterio è attivato, il verbo e la voce del menu di scelta rapida associato vengono eliminati. Per i possibili valori ID dei criteri, vedere l'enumerazione [**restrictions**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) .

### <a name="employing-the-verb-selection-model"></a>Uso del modello di selezione dei verbi

I valori del registro di sistema devono essere impostati per i verbi per gestire le situazioni in cui un utente può selezionare un singolo elemento, più elementi o una selezione da un elemento. Un verbo richiede valori di registro distinti per ognuna di queste tre situazioni supportate dal verbo. I valori possibili per il modello di selezione dei verbi sono i seguenti:

-   Specificare il valore MultiSelectModel per tutti i verbi. Se il valore MultiSelectModel non è specificato, viene dedotto dal tipo di implementazione del verbo scelto. Per i metodi basati su COM, ad esempio DropTarget e ExecuteCommand, viene utilizzato il **lettore** e per gli altri metodi viene utilizzato il **documento** .
-   Specificare **Single** per i verbi che supportano una sola selezione.
-   Specificare il **lettore** per i verbi che supportano un numero qualsiasi di elementi.
-   Specificare il **documento** per i verbi che creano una finestra di primo livello per ogni elemento. Questa operazione limita il numero di elementi attivati e consente di evitare l'esaurimento delle risorse di sistema se l'utente apre troppe finestre.

Quando il numero di elementi selezionati non corrisponde al modello di selezione dei verbi o è maggiore dei limiti predefiniti indicati nella tabella seguente, il verbo non viene visualizzato.



| Tipo di implementazione del verbo | Documento | Lettore    |
|-----------------------------|----------|-----------|
| Legacy                      | 15 elementi | 100 elementi |
| COM                         | 15 elementi | Nessun limite  |



 

Di seguito sono riportate alcune voci del registro di sistema che usano il valore MultiSelectModel.

```
HKEY_CLASSES_ROOT
   Folder
      shell
         open
             = MultiSelectModel = Document
```

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         verb
             = MultiSelectModel = Single | Document | Player
```

### <a name="using-item-attributes"></a>Uso degli attributi degli elementi

È possibile testare i valori del flag [**SFGAO**](sfgao.md) degli attributi della Shell per un elemento per determinare se il verbo deve essere abilitato o disabilitato.

Per usare questa funzionalità di attributo, aggiungere i seguenti valori **reg \_ DWORD** sotto il verbo:

-   Il valore AttributeMask specifica il valore [**SFGAO**](sfgao.md) dei valori di bit della maschera con cui eseguire il test.
-   Il valore AttributeValue specifica il valore [**SFGAO**](sfgao.md) dei bit sottoposti a test.
-   ImpliedSelectionModel specifica zero per i verbi di elemento o un valore diverso da zero per i verbi nel menu di scelta rapida in background.

Nell'esempio seguente di voce del registro di sistema, AttributeMask è impostato su [**SFGAO \_ ReadOnly**](sfgao.md) (0x40000).

```
HKEY_CLASSES_ROOT
   txtfile
      Shell
         test.verb2
            AttributeMask = 0x40000
            AttributeValue = 0x0
            ImpliedSelectionModel = 0x0
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

### <a name="implementing-custom-verbs-for-folders-through-desktopini"></a>Implementazione di verbi personalizzati per le cartelle tramite Desktop.ini

In Windows 7 e versioni successive, è possibile aggiungere verbi a una cartella tramite Desktop.ini. Per ulteriori informazioni sui file di Desktop.ini, vedere [How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md).

> [!Note]  
> I file di Desktop.ini devono essere sempre contrassegnati come nascosti dal **sistema**  +   , in modo che non vengano visualizzati dagli utenti.

 

**Per aggiungere verbi personalizzati per le cartelle tramite un file di Desktop.ini, seguire questa procedura:**

1.  Creare una cartella contrassegnata come di sola **lettura** o di **sistema**.
2.  Creare un file di Desktop.ini che includa un \[ . ShellClassInfo \] DirectoryClass = cartella ProgID.
3.  Nel registro di sistema creare **HKEY \_ classi \_ radice** \\ **ProgID** con un valore CanUseForDirectory. Il valore CanUseForDirectory evita l'utilizzo improprio dei ProgID impostati per non partecipare all'implementazione di verbi personalizzati per le cartelle tramite Desktop.ini.
4.  Aggiungere i verbi nella sottochiave ProgID della **cartella**, ad esempio:

    ```
    HKEY_CLASSES_ROOT
       CustomFolderType
          Shell
             MyVerb
                command
                   (Default) = %SystemRoot%\system32\notepad.exe %1\desktop.ini
    ```

> [!Note]  
> Questi verbi possono essere il verbo predefinito, nel qual caso fare doppio clic sulla cartella per attivare il verbo.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Procedure consigliate per i gestori di menu di scelta rapida e più verbi di selezione](verbs-best-practices.md)
</dt> <dt>

[Scelta di un verbo statico o dinamico per il menu di scelta rapida](shortcut-choose-method.md)
</dt> <dt>

[Personalizzazione di un menu di scelta rapida tramite verbi dinamici](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[Menu di scelta rapida (contesto) e gestori di menu di scelta rapida](context-menu.md)
</dt> <dt>

[Verbi e associazioni di file](fa-verbs.md)
</dt> <dt>

[Riferimento al menu di scelta rapida](context-menu-reference.md)
</dt> </dl>

 

 

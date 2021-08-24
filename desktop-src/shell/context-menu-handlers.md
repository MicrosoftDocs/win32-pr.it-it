---
description: I gestori dei menu di scelta rapida, noti anche come gestori di menu di scelta rapida o gestori di verbi, sono un tipo di gestore del tipo di file. Come tutti questi gestori, si tratta di oggetti COM (In-Process Component Object Model) implementati come DLL.
ms.assetid: cff79cdc-8a01-4575-9af7-2a485c6a8e46
title: Creazione di gestori del menu di scelta rapida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3a6b6f812772b884e12c45a48bae8075d90df28fb3b60f895cfd4c4263be74c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715767"
---
# <a name="creating-shortcut-menu-handlers"></a>Creazione di gestori del menu di scelta rapida

I gestori dei menu di scelta rapida, noti anche come gestori di menu di scelta rapida o gestori di verbi, sono un tipo di gestore del tipo di file. Questi gestori possono essere impelmentedati in modo che possano essere caricati nel proprio processo, nello explorer o in altri processi di terze parti. Quando si creano gestori in-process, è necessario fare attenzione perché possono causare danni al processo che li carica.

> [!Note]  
> Esistono considerazioni speciali per le versioni basate su 64 bit di Windows durante la registrazione di gestori che funzionano nel contesto delle applicazioni a 32 bit: quando viene richiamato nel contesto di un'applicazione con un numero di bit diverso, il sottosistema WOW64 reindirizza l'accesso file system alcuni percorsi. Se il .exe è archiviato in uno di questi percorsi, non è accessibile in questo contesto. Di conseguenza, per risolvere il problema, archiviare il .exe in un percorso che non viene reindirizzato o archiviare una versione stub del .exe che avvia la versione reale.

Questo argomento è organizzato come segue:

-   [Verbi canonici](#canonical-verbs)
-   [Verbi estesi](#extended-verbs)
-   [Verbi solo accesso a livello di codice](#programmaticaccessonly-verbs)
-   [Personalizzazione di un menu di scelta rapida tramite verbi statici](#customizing-a-shortcut-menu-using-static-verbs)
    -   [Attivazione del gestore tramite l'interfaccia IDropTarget](#activating-your-handler-using-the-idroptarget-interface)
    -   [Specifica della posizione e dell'ordine dei verbi statici](#specifying-the-position-and-order-of-static-verbs)
    -   [Posizionamento dei verbi nella parte superiore o inferiore del menu](#positioning-verbs-at-the-top-or-bottom-of-the-menu)
    -   [Creazione di menu a cascata statici](#creating-static-cascading-menus)
    -   [Recupero del comportamento dinamico per i verbi statici tramite la sintassi di query avanzata](#getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax)
    -   [Deprecato: Associazione di verbi a Dynamic Data Exchange comandi](#deprecated-associating-verbs-with-dynamic-data-exchange-commands)
-   [Completamento delle attività di implementazione dei verbi](#completing-verb-implementation-tasks)
    -   [Personalizzazione del menu di scelta rapida per gli oggetti predefiniti della shell](#customizing-the-shortcut-menu-for-predefined-shell-objects)
    -   [Estensione di un nuovo sottomenu](#extending-a-new-submenu)
    -   [Eliminazione di verbi e controllo della visibilità](#suppressing-verbs-and-controlling-visibility)
    -   [Utilizzo del modello di selezione dei verbi](#employing-the-verb-selection-model)
    -   [Uso degli attributi degli elementi](#using-item-attributes)
    -   [Implementazione di verbi personalizzati per le cartelle tramite Desktop.ini](#implementing-custom-verbs-for-folders-through-desktopini)
-   [Argomenti correlati](#related-topics)

## <a name="canonical-verbs"></a>Verbi canonici

Le applicazioni sono in genere responsabili di fornire stringhe di visualizzazione localizzate per i verbi definiti. Tuttavia, per fornire un grado di indipendenza del linguaggio, il sistema definisce un set standard di verbi di uso comune denominati verbi canonici. Un verbo canonico non viene mai visualizzato all'utente e può essere usato con qualsiasi lingua dell'interfaccia utente. Il sistema usa il nome canonico per generare automaticamente una stringa di visualizzazione localizzata correttamente. Ad esempio, la stringa di visualizzazione del verbo aperto è impostata su **Apri** in un sistema inglese e sull'equivalente tedesco in un sistema tedesco.


| Verbo canonico | Descrizione                                                          |
|----------------|----------------------------------------------------------------------|
| Apri           | Apre il file o la cartella.                                            |
| Opennew        | Apre il file o la cartella in una nuova finestra.                            |
| Stampa          | Stampa il file.                                                     |
| Printto        | Consente all'utente di stampare un file trascinandolo in un oggetto stampante. |
| Esplora        | Apre Windows Explorer con la cartella selezionata.                     |
| Proprietà     | Apre la finestra delle proprietà dell'oggetto.                                   |

> [!Note]  
> Anche **il verbo Printto** è canonico, ma non viene mai visualizzato. La sua inclusione consente all'utente di stampare un file trascinandolo in un oggetto stampante.

I gestori del menu di scelta rapida possono fornire i propri verbi canonici tramite [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) con **GCS \_ VERBW** o **GCS \_ VERBA.** Il sistema userà i verbi canonici come secondo parametro (*lpOperation*) passato a [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)e è [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo). **Membro lpVerb** passato al [**metodo IContextMenu::InvokeCommand.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)

## <a name="extended-verbs"></a>Verbi estesi

Quando l'utente fa clic con il pulsante destro del mouse su un oggetto, nel menu di scelta rapida vengono visualizzati i verbi predefiniti. Potrebbe essere necessario aggiungere e supportare comandi in alcuni menu di scelta rapida che non vengono visualizzati in ogni menu di scelta rapida. Ad esempio, è possibile avere comandi non comunemente usati o destinati a utenti esperti. Per questo motivo, è anche possibile definire uno o più verbi estesi. Questi verbi sono simili ai verbi normali, ma si distinguono dai verbi normali per il modo in cui vengono registrati. Per accedere ai verbi estesi, l'utente deve fare clic con il pulsante destro del mouse su un oggetto premendo MAIUSC. Quando l'utente esegue questa operazione, oltre ai verbi predefiniti vengono visualizzati anche i verbi estesi.

È possibile usare il Registro di sistema per definire uno o più verbi estesi. I comandi associati verranno visualizzati solo quando l'utente fa clic con il pulsante destro del mouse su un oggetto e preme anche MAIUSC. Per definire un verbo come esteso, aggiungere un valore **\_ REG SZ** "extended" alla sottochiave del verbo. Al valore non deve essere associato alcun dato.

## <a name="programmatic-access-only"></a>Solo accesso a livello di codice

Questi verbi non vengono mai visualizzati in un menu di scelta rapida. È possibile accedervi tramite [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) e specificando il campo **lpVerb** del *parametro pExecInfo* (un [oggetto SHELLEXECUTEINFO).](/windows/win32/api/shellapi/ns-shellapi-shellexecuteinfoa) Per definire un verbo solo come accesso a livello di codice, aggiungere un valore **\_ REG SZ** "ProgrammaticAccessOnly" alla sottochiave del verbo. Al valore non deve essere associato alcun dato.

È possibile usare il Registro di sistema per definire uno o più verbi estesi. I comandi associati verranno visualizzati solo quando l'utente fa clic con il pulsante destro del mouse su un oggetto e preme anche MAIUSC. Per definire un verbo come esteso, aggiungere un valore **\_ REG SZ** "extended" alla sottochiave del verbo. Al valore non deve essere associato alcun dato.

## <a name="customizing-a-shortcut-menu-using-static-verbs"></a>Personalizzazione di un menu di scelta rapida tramite verbi statici

Dopo [aver scelto un verbo](shortcut-choose-method.md) statico o dinamico per il menu di scelta rapida, è possibile estendere il menu di scelta rapida per un tipo di file registrando un verbo statico per il tipo di file. A tale scopo, aggiungere una **sottochiave Shell** sotto la sottochiave per il ProgID dell'applicazione associata al tipo di file. Facoltativamente, è possibile definire un verbo predefinito per il tipo di file impostandolo come valore predefinito della **sottochiave Shell.**

Il verbo predefinito viene visualizzato per primo nel menu di scelta rapida. Lo scopo è fornire alla shell un verbo che può usare quando viene chiamata la [**funzione ShellExecuteEx,**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) ma non viene specificato alcun verbo. Shell non seleziona necessariamente il verbo predefinito quando **shellExecuteEx** viene usato in questo modo.

La shell usa il primo verbo disponibile nell'ordine seguente:

1.  Verbo predefinito
2.  Primo verbo nel Registro di sistema, se viene specificato l'ordine dei verbi
3.  Verbo **Open**
4.  Verbo **Open With**

Se nessuno dei verbi elencati è disponibile, l'operazione non riesce.

Creare una sottochiave per ogni verbo che si vuole aggiungere sotto la sottochiave Shell. Ognuna di queste sottochiavi deve avere un **valore \_ REG SZ** impostato sulla stringa di visualizzazione del verbo (stringa localizzata). Per ogni sottochiave verbo, creare una sottochiave del comando con il valore predefinito impostato sulla riga di comando per l'attivazione degli elementi. Per i verbi canonici, ad esempio **Open** e **Print,** è possibile omettere la stringa di visualizzazione perché il sistema visualizza automaticamente una stringa localizzata correttamente. Per i verbi non canonici, se si omette la stringa di visualizzazione, viene visualizzata la stringa del verbo.

Nell'esempio del Registro di sistema seguente si noti che:

-   Poiché **Doit** non è un verbo canonico, gli viene assegnato un nome visualizzato, che può essere selezionato premendo il tasto D.
-   Il **verbo Printto** non viene visualizzato nel menu di scelta rapida. Tuttavia, la sua inclusione nel Registro di sistema consente all'utente di stampare i file rilasciandoli su un'icona della stampante.
-   Viene visualizzata una sottochiave per ogni verbo. **%1 rappresenta** il nome del file e **%2 il** nome della stampante.

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

Il diagramma seguente illustra l'estensione del menu di scelta rapida in base alle voci del Registro di sistema precedenti. Questo menu di scelta **rapida** include i **verbi** Apri , Do **It** e Stampa , con **Do It** come verbo predefinito.

![Screenshot del menu di scelta rapida del verbo predefinito do it](images/context-menu/context-doitdefaultverb.png)

### <a name="activating-your-handler-using-the-idroptarget-interface"></a>Attivazione del gestore tramite l'interfaccia IDropTarget

Dynamic Data Exchange (DDE) è deprecato. usare [**invece IDropTarget.**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) **IDropTarget è** più affidabile e ha un supporto di attivazione migliore perché usa l'attivazione COM del gestore. Nel caso di selezione di più elementi, **IDropTarget** non è soggetto alle restrizioni relative alle dimensioni del buffer presenti sia in DDE che in [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa). Inoltre, gli elementi vengono passati all'applicazione come oggetto dati che può essere convertito in una matrice di elementi usando la [**funzione SHCreateShellItemArrayFromDataObject.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) Questa operazione è più semplice e non perde le informazioni sullo spazio dei nomi come si verifica quando l'elemento viene convertito in un percorso per i protocolli della riga di comando o DDE.

Per altre informazioni sulle [**query IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) e Shell per gli attributi di associazione file, vedere [Tipi percepiti e Registrazione dell'applicazione](fa-perceivedtypes.md).

### <a name="specifying-the-position-and-order-of-static-verbs"></a>Specifica della posizione e dell'ordine dei verbi statici

In genere i verbi vengono ordinati in un menu di scelta rapida in base alla modalità di enumerazione; l'enumerazione si basa prima sull'ordine della matrice di associazioni e quindi sull'ordine degli elementi nella matrice di associazione, come definito dall'ordinamento del Registro di sistema.

I verbi possono essere ordinati specificando il valore predefinito della sottochiave Shell per la voce di associazione. Questo valore predefinito può includere un singolo elemento, che verrà visualizzato nella posizione superiore del menu di scelta rapida, o un elenco di elementi separati da spazi o virgole. Nel secondo caso, il primo elemento dell'elenco è l'elemento predefinito e gli altri verbi vengono visualizzati immediatamente sotto di esso nell'ordine specificato.

Ad esempio, la voce del Registro di sistema seguente produce verbi di menu di scelta rapida nell'ordine seguente:

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

Analogamente, la voce del Registro di sistema seguente produce verbi di menu di scelta rapida nell'ordine seguente:

1.  Personalization
2.  Gadget
3.  Visualizza

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell = "Personalization,Gadgets"
      Display
```

### <a name="positioning-verbs-at-the-top-or-bottom-of-the-menu"></a>Verbi di posizionamento nella parte superiore o inferiore del menu

L'attributo del Registro di sistema seguente può essere usato per posizionare un verbo nella parte superiore o inferiore del menu. Se sono presenti più verbi che specificano questo attributo, l'ultimo a tale scopo ottiene la priorità:

``` syntax
Position=Top | Bottom 
```

### <a name="creating-static-cascading-menus"></a>Creazione di menu a cascata statici

In Windows 7 e versioni successive, l'implementazione del menu a catena è supportata tramite le impostazioni del Registro di sistema. Prima di Windows 7, la creazione di menu a catena era possibile solo tramite l'implementazione [**dell'interfaccia IContextMenu.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) In Windows 7 e versioni successive, è consigliabile ricorrere a soluzioni basate su codice COM solo quando i metodi statici non sono sufficienti.

La schermata seguente fornisce un esempio di menu a cascata.

![Screenshot che mostra un esempio di menu a cascata](images/file-assoc/filecascademenu2ndex.png)

In Windows 7 e versioni successive sono disponibili tre modi per creare menu a cascata:

-   [Creazione di menu a catena con la voce del Registro di sistema SubCommands](#creating-cascading-menus-with-the-subcommands-registry-entry)
-   [Creazione di menu a catena con la voce del Registro di sistema ExtendedSubCommandsKey](#creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry)
-   [Creazione di menu a cascata con l'interfaccia IExplorerCommand](#creating-cascading-menus-with-the-iexplorercommand-interface)

### <a name="creating-cascading-menus-with-the-subcommands-registry-entry"></a>Creazione di menu a catena con la voce del Registro di sistema SubCommands

In Windows 7 e versioni successive, è possibile usare la voce Sottocomandi per creare menu a catena usando la procedura seguente.

**Per creare un menu a cascata usando la voce SubCommands**

1.  Creare una sottochiave in **HKEY \_ CLASSES \_ ROOT** \\ *ProgID* \\ **shell** per rappresentare il menu a cascata. In questo esempio si assegna a questa sottochiave il nome *CascadeTest*. Assicurarsi che il valore predefinito della *sottochiave CascadeTest* sia vuoto e visualizzato come **(valore non impostato).**

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
    ```

2.  Alla *sottochiave CascadeTest* aggiungere una voce MUIVerb di tipo **REG \_ SZ** e assegnarle il testo che verrà visualizzato come nome nel menu di scelta rapida. In questo esempio viene assegnato "Test Cascade Menu".

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu
    ```

3.  Alla *sottochiave CascadeTest* aggiungere una voce SubCommands di tipo **REG \_ SZ** a cui è assegnato l'elenco, delimitato da punti e virgola, dei verbi che devono essere visualizzati nel menu nell'ordine di visualizzazione. Ad esempio, qui viene assegnato un numero di verbi forniti dal sistema:

    ```
    HKEY_CLASSES_ROOT
       *
          Shell
             CascadeTest
                SubCommands
                Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
    ```

4.  Nel caso di verbi personalizzati, implementarli usando uno dei metodi di implementazione dei verbi statici ed elencarli nella sottochiave **CommandStore,** come illustrato in questo esempio per un verbo *fittizio VerbName*:

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
> Questo metodo ha il vantaggio che i verbi personalizzati possono essere registrati una sola volta e riutilizzati elencando il nome del verbo nella voce SubCommands. Tuttavia, è necessario che l'applicazione abbia l'autorizzazione per modificare il Registro di sistema in **HKEY \_ LOCAL \_ MACHINE**.

 

### <a name="creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry"></a>Creazione di menu a catena con la voce del Registro di sistema ExtendedSubCommandsKey

In Windows 7 e versioni successive, è possibile usare la voce ExtendedSubCommandKey per creare menu a cascata estesi: menu a cascata all'interno dei menu a cascata.

Lo screenshot seguente è un esempio di menu a cascata esteso.

![Screenshot che mostra il menu a cascata esteso per i dispositivi](images/file-assoc/extendedsubcommandskey.png)

Poiché **HKEY \_ CLASSES \_ ROOT** è una combinazione di **HKEY CURRENT \_ \_ USER** e **HKEY LOCAL \_ \_ MACHINE,** è possibile registrare qualsiasi verbo personalizzato nella sottochiave **HKEY CURRENT \_ \_ USER** \\ **Software** \\ **Classes.** Il vantaggio principale di questa operazione è che non è necessaria l'autorizzazione con privilegi elevati. Inoltre, altre associazioni di file possono riutilizzare l'intero set di verbi specificando la stessa sottochiave ExtendedSubCommandsKey. Se non è necessario riutilizzare questo set di verbi, è possibile elencare i verbi nell'elemento padre, ma assicurarsi che il valore Predefinito dell'elemento padre sia vuoto.

**Per creare un menu a cascata usando una voce ExtendedSubCommandsKey**

1.  Creare una sottochiave in **HKEY \_ CLASSES \_ ROOT** \\ *ProgID* \\ **shell** per rappresentare il menu a cascata. In questo esempio si assegna a questa sottochiave il nome *CascadeTest2*. Assicurarsi che il valore predefinito della *sottochiave CascadeTest* sia vuoto e visualizzato come **(valore non impostato).**

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest2
                (Default)
    ```

2.  Alla *sottochiave CascadeTest* aggiungere una voce MUIVerb di tipo **REG \_ SZ** e assegnarle il testo che verrà visualizzato come nome nel menu di scelta rapida. In questo esempio viene assegnato "Test Cascade Menu".

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu 2
    ```

3.  Nella *sottochiave CascadeTest* creata aggiungere una sottochiave **ExtendedSubCommandsKey** e quindi aggiungere i sottocomandi del documento (di tipo **REG \_ SZ);** ad esempio:

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

    Assicurarsi che il valore predefinito della *sottochiave Test Cascade Menu 2* sia vuoto e visualizzato come **(valore non impostato).**

4.  Popolare i sottoverbi usando una delle implementazioni di verbi statici seguenti. Si noti che la sottochiave CommandFlags rappresenta i valori EXPCMDFLAGS. Se si vuole aggiungere un separatore prima o dopo la voce di menu a catena, usare ECF \_ SEPARATORBEFORE (0x20) o ECF \_ SEPARATORAFTER (0x40). Per una descrizione di questi flag Windows 7 e versioni successive, vedere [**IExplorerCommand::GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags). ECF \_ SEPARATORBEFORE funziona solo per le voci di menu di primo livello. MUIVerb è di tipo **REG \_ SZ** e CommandFlags è di tipo **REG \_ DWORD**.

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

Lo screenshot seguente è un'illustrazione degli esempi precedenti di voci del Registro di sistema.

![Screenshot che mostra un esempio di menu a cascata che mostra le opzioni del Blocco note e del wordpad](images/file-assoc/testcascademenu2.png)

### <a name="creating-cascading-menus-with-the-iexplorercommand-interface"></a>Creazione di menu a cascata con l'interfaccia IExplorerCommand

Un'altra opzione per l'aggiunta di verbi a un menu a cascata è [**tramite IExplorerCommand::EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands). Questo metodo consente alle origini dati che forniscono i comandi del modulo di comando [**tramite IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) di usare tali comandi come verbi in un menu di scelta rapida. In Windows 7 e versioni successive, è possibile fornire la stessa implementazione del verbo [**usando IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) come è possibile con [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).

Le due schermate seguenti illustrano l'uso dei menu a cascata nella **cartella** Dispositivi.

![Screenshot che mostra un esempio di menu a cascata nella cartella devices.](images/file-assoc/filecascademenu.png)

La schermata seguente illustra un'altra implementazione di un menu a cascata nella **cartella** Dispositivi.

![Screenshot che mostra un esempio di menu a cascata nella cartella devices](images/file-assoc/cascadedevices2.png)

> [!Note]  
> Poiché [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) supporta solo l'attivazione in-process, è consigliabile usarlo dalle origini dati shell che devono condividere l'implementazione tra comandi e menu di scelta rapida.

 

### <a name="getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax"></a>Recupero del comportamento dinamico per i verbi statici tramite la sintassi di query avanzata

Advanced Query Syntax (AQS) può esprimere una condizione che verrà valutata usando le proprietà dell'elemento per cui viene creata un'istanza del verbo. Questo sistema funziona solo con proprietà veloci. Si tratta di proprietà segnalate dall'origine dati Shell con la velocità più veloce, senza restituire [****SHCOLSTATE \_ SLOW***](/windows/win32/api/shtypes/ne-shtypes-shcolstate) da [**IShellFolder2::GetDefaultColumnState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultcolumnstate).

Windows 7 e versioni successive supportano valori canonici che evitano problemi nelle compilazioni localizzate. La sintassi canonica seguente è necessaria nelle compilazioni localizzate per sfruttare questo Windows 7.

``` syntax
System.StructuredQueryType.Boolean#True
```

Nella voce del Registro di sistema di esempio seguente:

-   Il **valore AppliesTo** controlla se il verbo è visualizzato o nascosto.
-   Il valore DefaultAppliesTo controlla quale verbo è il valore predefinito.
-   Il valore HasLUAShield controlla se viene visualizzata una schermatura del controllo dell'account utente.

In questo esempio il **valore DefaultAppliesTo** rende questo verbo l'impostazione predefinita per qualsiasi file con la parola "exampleText1" nel nome file. Il **valore AppliesTo** abilita il verbo per qualsiasi file con "exampleText1" nel nome. Il **valore HasLUAShield** visualizza lo schermo per i file con "exampleText2" nel nome.

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            DefaultAppliesTo = System.ItemName:"exampleText1"
            HasLUAShield = System.ItemName:"exampleText2"
            AppliesTo = System.ItemName:"exampleText1"
```

Aggiungere la **sottochiave Command** e un valore:

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            Command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

Nel Registro Windows 7 vedere HKEY CLASSES ROOT drive (Unità **HKEY \_ CLASSES \_ ROOT)** come esempio di \\  verbi bitlocker che adottano l'approccio seguente:

-   AppliesTo = System.Volume.BitlockerProtection:=2
-   System.Volume.BitlockerRequiresAdmin:=System.StructuredQueryType.Boolean \# True

Per altre informazioni su AQS, vedere [Sintassi di query avanzate](../search/-search-3x-advancedquerysyntax.md).

### <a name="deprecated-associating-verbs-with-dynamic-data-exchange-commands"></a>Deprecato: Associazione di verbi a Dynamic Data Exchange comandi

DDE è deprecato. usare [**invece IDropTarget.**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) DDE è deprecato perché si basa su un messaggio di finestra di trasmissione per individuare il server DDE. Un blocco del server DDE blocca il messaggio della finestra di trasmissione e pertanto blocca le conversazioni DDE per altre applicazioni. È comune che una singola applicazione bloccata causa blocchi successivi nell'esperienza dell'utente.

Il [**metodo IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) è più affidabile e ha un supporto di attivazione migliore perché usa l'attivazione COM del gestore. In caso di selezione di più elementi, **IDropTarget** non è soggetto alle restrizioni relative alle dimensioni del buffer presenti sia in DDE che in [**CreateProcess.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) Inoltre, gli elementi vengono passati all'applicazione come oggetto dati che può essere convertito in una matrice di elementi usando la [**funzione SHCreateShellItemArrayFromDataObject.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) Questa operazione è più semplice e non perde le informazioni sullo spazio dei nomi come si verifica quando l'elemento viene convertito in un percorso per i protocolli della riga di comando o DDE.

Per altre informazioni sulle query [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) e Shell per gli attributi di associazione di file, vedere [Tipi percepiti e Registrazione dell'applicazione.](fa-perceivedtypes.md)

## <a name="completing-verb-implementation-tasks"></a>Completamento delle attività di implementazione dei verbi

Le attività seguenti per l'implementazione dei verbi sono rilevanti per le implementazioni di verbi statici e dinamici. Per altre informazioni sui verbi dinamici, vedere [Personalizzazione di un menu di scelta rapida tramite verbi dinamici.](shortcut-menu-using-dynamic-verbs.md)

### <a name="customizing-the-shortcut-menu-for-predefined-shell-objects"></a>Personalizzazione del menu di scelta rapida per gli oggetti predefiniti della shell

Molti oggetti shell predefiniti hanno menu di scelta rapida che possono essere personalizzati. Registrare il comando nello stesso modo in cui si registrano i tipi di file tipici, ma usare il nome dell'oggetto predefinito come nome del tipo di file.

Un elenco di oggetti predefiniti è disponibile nella *sezione Oggetti shell predefiniti* di Creazione di gestori di estensioni della [shell.](handlers.md) Gli oggetti shell predefiniti i cui menu di scelta rapida possono essere personalizzati aggiungendo verbi nel Registro di sistema vengono contrassegnati nella tabella con la parola Verbo.

### <a name="extending-a-new-submenu"></a>Estensione di un nuovo sottomenu

Quando un utente apre il menu **File** in Windows Explorer, uno dei comandi visualizzati è **Nuovo**. Selezionando questo comando viene visualizzato un sottomenu. Per impostazione predefinita, il sottomenu contiene due comandi, **Cartella** e **Collegamento**, che consentono agli utenti di creare sottocartelle e collegamenti. Questo sottomenu può essere esteso per includere i comandi di creazione di file per qualsiasi tipo di file.

Per aggiungere un comando di creazione file al sottomenu **Nuovo,** i file dell'applicazione devono avere un tipo di file associato. Includere una **sottochiave ShellNew** sotto il nome del file. Quando il comando Nuovo **del** menu **File** è selezionato, la shell aggiunge il tipo di file al **sottomenu Nuovo.** La stringa di visualizzazione del comando è la stringa descrittiva assegnata al ProgID del programma.

Per specificare il metodo di creazione del file, assegnare uno o più valori di dati alla **sottochiave ShellNew.** I valori disponibili sono elencati nella tabella seguente.



| ShellNuovo valore della sottochiave | Descrizione                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Comando               | Esegue un'applicazione. Questo **valore \_ REG SZ** specifica il percorso dell'applicazione da eseguire. Ad esempio, è possibile impostarlo per avviare una procedura guidata.                  |
| Dati                  | Crea un file contenente i dati specificati. Questo **valore \_ REG BINARY** specifica i dati del file. **I** dati vengono ignorati **se viene specificato NullFile** o **FileName.** |
| FileName              | Crea un file che è una copia di un file specificato. Questo **valore \_ REG SZ** specifica il percorso completo del file da copiare.                                   |
| NullFile              | Crea un file vuoto. **A NullFile** non è assegnato alcun valore. Se **viene specificato NullFile,** i valori **del Registro di sistema Data** e **FileName** vengono ignorati.                    |



 

L'esempio di chiave del Registro di sistema e lo screenshot seguenti **illustrano il** sottomenu Nuovo per il tipo di file .myp-ms. Include un comando **MyProgram Application.**

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      MyProgram.1
         ShellNew
         NullFile
```

Lo screenshot illustra il **sottomenu** Nuovo. Quando un utente seleziona **MyProgram Application** dal sottomenu **Nuovo,** la shell crea un file denominato **New MyProgram Application.myp-ms** e lo **passa aMyProgram.exe**.

![Screenshot di Esplora risorse che mostra un nuovo comando "myprogram application" nel sottomenu "nuovo"](images/context-menu/context-myprogramexe.png)

### <a name="creating-drag-and-drop-handlers"></a>Creazione di gestori di trascinamento della selezione

La procedura di base per l'implementazione di un gestore di trascinamento della selezione è la stessa utilizzata per i gestori di menu di scelta rapida convenzionali. Tuttavia, i gestori del menu di scelta rapida in genere usano solo il puntatore [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) passato al metodo [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) del gestore per estrarre il nome dell'oggetto. Un gestore di trascinamento della selezione potrebbe implementare un gestore dati più sofisticato per modificare il comportamento dell'oggetto trascinato.

Quando un utente fa clic con il pulsante destro del mouse su un oggetto Shell per trascinare un oggetto, viene visualizzato un menu di scelta rapida quando l'utente tenta di rilasciare l'oggetto. Lo screenshot seguente illustra un tipico menu di scelta rapida con trascinamento della selezione.

![Screenshot del menu di scelta rapida con trascinamento della selezione](images/context-menu/context-dragdrop.png)

Un gestore di trascinamento della selezione è un gestore del menu di scelta rapida che può aggiungere voci a questo menu di scelta rapida. I gestori di trascinamento della selezione vengono in genere registrati nella sottochiave seguente.

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
```

Aggiungere una sottochiave nella sottochiave **DragDropHandlers** denominata per il gestore di trascinamento della selezione e impostare il valore predefinito della sottochiave sul formato stringa del GUID dell'identificatore di classe (CLSID) del gestore. L'esempio seguente abilita il gestore di trascinamento della selezione **myDD.**

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
            MyDD
               (Default) = {MyDD CLSID GUID}
```

### <a name="suppressing-verbs-and-controlling-visibility"></a>Eliminazione di verbi e controllo della visibilità

È possibile usare le Windows dei criteri per controllare la visibilità dei verbi. I verbi possono essere eliminati tramite le impostazioni dei criteri aggiungendo un valore **SuppressionPolicy** o un valore GUID **SuppressionPolicyEx** alla sottochiave del Registro di sistema del verbo. Impostare il valore della **sottochiave SuppressionPolicy** sull'ID criteri. Se il criterio è attivato, il verbo e la voce di menu di scelta rapida associata vengono eliminati. Per i possibili valori id dei criteri, vedere [**l'enumerazione RESTRICTIONS.**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions)

### <a name="employing-the-verb-selection-model"></a>Utilizzo del modello di selezione dei verbi

I valori del Registro di sistema devono essere impostati per i verbi per gestire situazioni in cui un utente può selezionare un singolo elemento, più elementi o una selezione da un elemento. Un verbo richiede valori del Registro di sistema separati per ognuna di queste tre situazioni supportate dal verbo. I valori possibili per il modello di selezione dei verbi sono i seguenti:

-   Specificare il valore MultiSelectModel per tutti i verbi. Se il valore MultiSelectModel non viene specificato, viene dedotto dal tipo di implementazione del verbo scelto. Per i metodi basati su COM (ad esempio DropTarget ed ExecuteCommand) si presuppone **Player** e per gli altri metodi si presuppone **Document.**
-   Specificare **Single** per i verbi che supportano solo una selezione singola.
-   Specificare **Player** per i verbi che supportano un numero qualsiasi di elementi.
-   Specificare **Documento** per i verbi che creano una finestra di primo livello per ogni elemento. In questo modo si limita il numero di elementi attivati ed è possibile evitare l'estrazione di risorse di sistema se l'utente apre troppe finestre.

Quando il numero di elementi selezionati non corrisponde al modello di selezione del verbo o è maggiore dei limiti predefiniti descritti nella tabella seguente, il verbo non viene visualizzato.



| Tipo di implementazione del verbo | Documento | Lettore    |
|-----------------------------|----------|-----------|
| Legacy                      | 15 elementi | 100 elementi |
| COM                         | 15 elementi | Nessun limite  |



 

Di seguito sono riportati esempi di voci del Registro di sistema che usano il valore MultiSelectModel.

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

I valori del flag [**SFGAO**](sfgao.md) degli attributi della shell per un elemento possono essere testati per determinare se il verbo deve essere abilitato o disabilitato.

Per usare questa funzionalità di attributo, aggiungere i valori **\_ DWORD REG** seguenti sotto il verbo:

-   Il valore AttributeMask specifica il [**valore SFGAO**](sfgao.md) dei valori di bit della maschera con cui eseguire il test.
-   Il valore AttributeValue specifica il [**valore SFGAO**](sfgao.md) dei bit che vengono testati.
-   ImpliedSelectionModel specifica zero per i verbi elemento o diverso da zero per i verbi nel menu di scelta rapida di sfondo.

Nella voce del Registro di sistema di esempio seguente AttributeMask è impostato su [**SFGAO \_ READONLY**](sfgao.md) (0x40000).

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

In Windows 7 e versioni successive è possibile aggiungere verbi a una cartella tramite Desktop.ini. Per altre informazioni sui Desktop.ini, vedere [How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md).

> [!Note]  
> Desktop.ini file devono essere sempre contrassegnati come **Nascosti dal** sistema in modo che non siano visualizzati  +   dagli utenti.

 

**Per aggiungere verbi personalizzati per le cartelle tramite un file Desktop.ini, seguire questa procedura:**

1.  Creare una cartella contrassegnata come Di sola **lettura** o **Sistema.**
2.  Creare un file Desktop.ini che include un oggetto \[ . ShellClassInfo \] DirectoryClass=Folder ProgID.
3.  Nel Registro di sistema creare **HKEY \_ CLASSES \_ ROOT** Folder \\ **ProgID** con il valore CanUseForDirectory. Il valore CanUseForDirectory evita l'uso improprio dei ProgID impostati per non partecipare all'implementazione di verbi personalizzati per le cartelle tramite Desktop.ini.
4.  Aggiungere verbi nella **sottochiave** ProgID della cartella, ad esempio:

    ```
    HKEY_CLASSES_ROOT
       CustomFolderType
          Shell
             MyVerb
                command
                   (Default) = %SystemRoot%\system32\notepad.exe %1\desktop.ini
    ```

> [!Note]  
> Questi verbi possono essere il verbo predefinito, nel qual caso facendo doppio clic sulla cartella viene attivato il verbo.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Procedure consigliate per i gestori del menu di scelta rapida e più verbi di selezione](verbs-best-practices.md)
</dt> <dt>

[Scelta di un verbo statico o dinamico per il menu di scelta rapida](shortcut-choose-method.md)
</dt> <dt>

[Personalizzazione di un menu di scelta rapida tramite verbi dinamici](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[Menu di scelta rapida e gestori del menu di scelta rapida](context-menu.md)
</dt> <dt>

[Verbi e associazioni di file](fa-verbs.md)
</dt> <dt>

[Informazioni di riferimento sul menu di scelta rapida](context-menu-reference.md)
</dt> </dl>

 

 

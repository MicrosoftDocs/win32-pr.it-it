---
description: Quando si fa clic con il pulsante destro del mouse su un oggetto, viene visualizzata una finestra di scelta rapida. Questo menu contiene un elenco di comandi che l'utente può selezionare per eseguire varie azioni sull'oggetto. Questa sezione è un'introduzione ai menu di scelta rapida per gli oggetti file system.
ms.assetid: d951d1e8-0f88-49c4-8373-e6db0e18cd72
title: Estensione di menu di scelta rapida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 895550ff050d559b3523676ddaa2a58099398a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104555386"
---
# <a name="extending-shortcut-menus"></a>Estensione di menu di scelta rapida

Quando si fa clic con il pulsante destro del mouse su un oggetto, viene visualizzata una finestra di *scelta rapida*. Questo menu contiene un elenco di comandi che l'utente può selezionare per eseguire varie azioni sull'oggetto. Questa sezione è un'introduzione ai menu di scelta rapida per gli oggetti file system.

-   [Menu di scelta rapida per gli oggetti del file System](#shortcut-menus-for-file-system-objects)
-   [Verbi del menu di scelta rapida](#shortcut-menu-verbs)
    -   [Verbi canonici](#canonical-verbs)
    -   [Verbi estesi](#extended-verbs)
-   [Estensione del menu di scelta rapida per un tipo di file](#extending-the-shortcut-menu-for-a-file-type)
-   [Estensione del menu di scelta rapida per oggetti shell predefiniti](#extending-the-shortcut-menu-for-predefined-shell-objects)
-   [Registrazione di un'applicazione per gestire i tipi di file arbitrari](#registering-an-application-to-handle-arbitrary-file-types)
-   [Estensione del nuovo sottomenu](#extending-the-new-submenu)

Ulteriori informazioni sono disponibili qui:

-   [Come definire i verbi estesi](how-to-define-extended-verbs.md)
-   [Come associare i verbi ai comandi DDE](how-to-associate-verbs-with-dde-commands.md)

## <a name="shortcut-menus-for-file-system-objects"></a>Menu di scelta rapida per gli oggetti del file System

Quando un utente fa clic con il pulsante destro del mouse su un oggetto, ad esempio un file, che viene visualizzato in Esplora risorse o sul desktop, viene visualizzato un menu di scelta rapida con un elenco di comandi. L'utente può quindi eseguire un'azione sul file, ad esempio per aprirla o eliminarla, selezionando il comando appropriato.

Poiché i menu di scelta rapida vengono spesso utilizzati per la gestione dei file, la shell fornisce un set di comandi predefiniti, ad esempio taglia e copia, che vengono visualizzati nel menu di scelta rapida per qualsiasi file. Si noti che sebbene Open con sia un comando predefinito, non viene visualizzato per alcuni tipi di file standard, ad esempio WAV. Nell'illustrazione seguente della directory documenti di esempio, usata anche come esempio di [personalizzazione delle icone](icon.md), viene visualizzato un menu di scelta rapida predefinito visualizzato facendo clic con il pulsante destro del mouse su MyDocs4.xyz.

![screenshot del menu di scelta rapida predefinito per gli oggetti file system](images/context1.jpg)

Il motivo per cui MyDocs4.xyz Visualizza un menu di scelta rapida predefinito è che non è un membro di un [tipo di file](fa-file-types.md)registrato. D'altra parte, txt è un tipo di file registrato. Se si fa clic con il pulsante destro del mouse su uno dei file con estensione txt, si vedrà invece un menu di scelta rapida con due comandi aggiuntivi nella sezione superiore: **Apri** e **stampa**.

![screenshot del menu di scelta rapida personalizzato per oggetti file system](images/context2.jpg)

Una volta registrato un tipo di file, è possibile estendere il relativo menu di scelta rapida con comandi aggiuntivi. Vengono visualizzati sopra i comandi predefiniti quando si fa clic con il pulsante destro del mouse su un file di quel tipo. Sebbene la maggior parte dei comandi aggiunti in questo modo siano comuni, ad esempio **Print** o **Open**, è possibile aggiungere qualsiasi comando che può risultare utile per un utente.

Per estendere il menu di scelta rapida per un tipo di file, è necessario creare una voce del registro di sistema per ogni comando. Un approccio più sofisticato consiste nell'implementare un *gestore di menu di scelta rapida*, che consente di estendere il menu di scelta rapida per un tipo di file in base al file. Per altre informazioni, vedere [creazione di gestori di menu di scelta rapida](context-menu-handlers.md).

## <a name="shortcut-menu-verbs"></a>Verbi del menu di scelta rapida

Ogni comando nel menu di scelta rapida viene identificato nel registro di sistema in base al relativo *verbo*. Questi verbi corrispondono a quelli usati da [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) quando si avviano le applicazioni a livello di codice. Per ulteriori informazioni sull'utilizzo di **ShellExecuteEx**, vedere la discussione relativa all' [avvio delle applicazioni](launch.md).

Un verbo è una stringa di testo semplice utilizzata dalla Shell per identificare il comando associato. Ogni verbo corrisponde alla *stringa di comando* usata per avviare il comando in una finestra della console o in un file batch (. bat). Il verbo **Open** , ad esempio, avvia normalmente un programma per aprire un file. La relativa stringa di comando è in genere simile alla seguente:

``` syntax
"My Program.exe" "%1"
```

"%1" è il segnaposto standard per un parametro della riga di comando fornito con il nome file. Ad esempio, è possibile specificare una pagina specifica da visualizzare in una visualizzazione a schede.

> [!Note]  
> Se un elemento della stringa di comando contiene o potrebbe contenere spazi, deve essere racchiuso tra virgolette. In caso contrario, se l'elemento contiene uno spazio, non verrà analizzato correttamente. Ad esempio, "My Program.exe" avvierà correttamente l'applicazione. Se si utilizza My Program.exe, il sistema tenterà di avviare "My" con "Program.exe" come primo argomento della riga di comando. È consigliabile utilizzare sempre le virgolette con argomenti, ad esempio "%1", che vengono espanse in stringhe dalla shell, perché non è possibile essere certi che la stringa non conterrà uno spazio.

 

Ai verbi può essere associata anche una *stringa di visualizzazione* , che viene visualizzata nel menu di scelta rapida invece della stringa del verbo. La stringa di visualizzazione per **opens** , ad esempio, è aperta con. Analogamente alle normali stringhe di menu, inclusa una e commerciale (&) nella stringa di visualizzazione consente la selezione del comando da tastiera.

### <a name="canonical-verbs"></a>Verbi canonici

In generale, le applicazioni sono responsabili di fornire stringhe di visualizzazione localizzate per i verbi definiti. Tuttavia, per fornire un livello di indipendenza dal linguaggio, il sistema definisce un set standard di verbi comunemente usati, detti *verbi canonici*. Un verbo canonico può essere usato con qualsiasi linguaggio e il sistema genera automaticamente una stringa di visualizzazione localizzata correttamente. Ad esempio, la stringa di visualizzazione del verbo **aperto** verrà impostata per essere aperta in un sistema in lingua inglese e per öffnen in un sistema tedesco.

I verbi canonici includono:



| Valore      | Descrizione                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| apre       | Apre il file o la cartella.                                                                   |
| OpenNew    | Apre il file o la cartella in una nuova finestra.                                                   |
| print      | Stampa il file.                                                                            |
| esplorare    | Apre Esplora risorse con la cartella selezionata.                                            |
| trovare       | Apre la finestra di dialogo **ricerca di Windows** con la cartella impostata come percorso di ricerca predefinito. |
| Apri     | Apre la finestra **di dialogo Apri con** .                                                         |
| properties | Apre la finestra delle proprietà dell'oggetto.                                                          |



 

Il verbo printto è anche canonico ma non viene mai visualizzato. Consente all'utente di stampare un file trascinandolo in un oggetto Printer.

### <a name="extended-verbs"></a>Verbi estesi

Quando l'utente fa clic con il pulsante destro del mouse su un oggetto, il menu di scelta rapida contiene tutti i verbi normali. Tuttavia, potrebbero essere presenti comandi che si desidera supportare ma che non sono stati visualizzati in ogni menu di scelta rapida. Ad esempio, è possibile avere comandi che non sono comunemente usati o destinati a utenti esperti. Per questo motivo, è anche possibile definire uno o più *verbi estesi*. Questi verbi sono anche stringhe di caratteri e sono simili ai verbi normali. Si distinguono dai verbi normali in base alla modalità di registrazione. Per accedere ai comandi associati ai verbi estesi, è necessario fare clic con il pulsante destro del mouse su un oggetto quando si preme il tasto MAIUSC. Verranno quindi visualizzati i verbi estesi insieme ai verbi normali.

## <a name="extending-the-shortcut-menu-for-a-file-type"></a>Estensione del menu di scelta rapida per un tipo di file

Il modo più semplice per estendere il menu di scelta rapida per un tipo di file è con il registro di sistema. A tale scopo, aggiungere una sottochiave della **Shell** sotto la chiave per il ProgID dell'applicazione associata al [tipo di file](fa-file-types.md). Facoltativamente, è possibile definire un *verbo predefinito* per il tipo di file rendendolo il valore predefinito della sottochiave della **Shell** .

Il verbo predefinito viene visualizzato per primo nel menu di scelta rapida. Il suo scopo è fornire alla shell un verbo che può usare quando viene chiamato [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) , ma non viene specificato alcun verbo. La shell non seleziona necessariamente il verbo predefinito quando **ShellExecuteEx** viene usato in questo modo. Per le [versioni](versions.md) della Shell 5,0 e successive, disponibile nei sistemi Windows 2000 e versioni successive, la shell usa il primo verbo disponibile nell'elenco seguente. Se non ne sono disponibili, l'operazione non riesce.

-   Verbo di apertura
-   Verbo predefinito
-   Primo verbo nel registro di sistema
-   Verbo openWith

Per le versioni della shell precedenti alla [versione 5,0](versions.md), omettere il terzo elemento.

Sotto la sottochiave della **Shell** creare una sottochiave per ogni verbo che si vuole aggiungere. Ognuna di queste sottochiavi avrà un valore **reg \_ SZ** impostato sulla stringa di visualizzazione del verbo. È possibile omettere la stringa di visualizzazione per i verbi canonici perché il sistema visualizzerà automaticamente una stringa localizzata correttamente. Se si omette la stringa di visualizzazione per i verbi non canonici, verrà visualizzata la stringa del verbo. Per ogni sottochiave verbo creare una sottochiave del **comando** con il valore predefinito impostato sulla stringa di comando.

Nella figura seguente viene illustrato un menu di scelta rapida per il tipo di file MYP utilizzato nei [tipi di file](fa-file-types.md) e nelle [Icone di personalizzazione](icon.md). Dispone ora di verbi Open, doit, Print e printto nel relativo menu di scelta rapida, con doit come verbo predefinito. Il menu di scelta rapida ha un aspetto simile al seguente.

![screenshot del menu di scelta rapida personalizzato](images/context3.jpg)

Le voci del registro di sistema usate per estendere il menu di scelta rapida illustrato nella figura precedente sono:

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      (Default) = MyProgram Application
      Shell
         (Default) = doit
         open
            command
               (Default) = C:\MyDir\MyProgram.exe "%1"
         doit
            (Default) = &Do It
            command
               (Default) = C:\MyDir\MyProgram.exe /d "%1"
         print
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1"
         printto
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1" "%2" %3 %4
```

Sebbene il comando **Apri con** si trovi al di sopra del primo separatore, viene creato automaticamente dal sistema e non richiede una voce del registro di sistema. Il sistema crea automaticamente i nomi visualizzati per i verbi canonici Apri e stampa. Poiché doit non è un verbo canonico, viene assegnato un nome visualizzato, "&eseguirlo", che può essere selezionato premendo il tasto D. Il verbo printto non viene visualizzato nel menu di scelta rapida, ma l'inclusione consente all'utente di stampare i file trascinandoli su un'icona della stampante. In questo esempio, %1 rappresenta il nome del file e %2 il nome della stampante.

I verbi possono essere eliminati tramite le impostazioni dei criteri aggiungendo un valore SuppressionPolicy alla chiave del verbo. Impostare il valore di SuppressionPolicy sull'ID criterio. Se il criterio è attivato, il verbo e la voce del menu di scelta rapida associato vengono eliminati. Per i possibili valori ID dei criteri, vedere l'enumerazione [**restrictions**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) .

## <a name="extending-the-shortcut-menu-for-predefined-shell-objects"></a>Estensione del menu di scelta rapida per oggetti shell predefiniti

Molti oggetti shell predefiniti dispongono di menu di scelta rapida che possono essere estesi. Registrare il comando nello stesso modo in cui si registrano i tipi di file tipici, ma usare il nome dell'oggetto predefinito come nome del tipo di file.

È possibile trovare un elenco di oggetti predefiniti nella sezione *oggetti shell predefiniti* della pagina relativa alla [creazione di gestori di estensioni della shell](handlers.md). Gli oggetti shell predefiniti i cui menu di scelta rapida possono essere estesi aggiungendo verbi nel registro di sistema sono contrassegnati nella tabella con la parola "verbo".

## <a name="registering-an-application-to-handle-arbitrary-file-types"></a>Registrazione di un'applicazione per gestire i tipi di file arbitrari

Nelle sezioni precedenti di questo documento è stato illustrato come definire voci di menu di scelta rapida per un determinato tipo di file. Tra le altre cose, la definizione del menu di scelta rapida consente di specificare il modo in cui l'applicazione associata apre un membro del tipo di file. Tuttavia, come illustrato in [tipi di file](fa-file-types.md), le applicazioni possono anche registrare una procedura predefinita separata da usare quando un utente tenta di usare l'applicazione per aprire un tipo di file che non è stato associato all'applicazione. Questo argomento è illustrato in questo articolo perché la procedura predefinita è registrata in modo analogo alla registrazione delle voci di menu di scelta rapida.

La procedura predefinita si serve di due scopi di base. Uno consiste nel specificare come richiamare l'applicazione per aprire un tipo di file arbitrario. È possibile, ad esempio, usare un flag della riga di comando per indicare che è in corso l'apertura di un tipo di file sconosciuto. L'altro scopo è quello di definire le varie caratteristiche di un tipo di file, ad esempio le voci del menu di scelta rapida e l'icona. Se un utente associa l'applicazione a un tipo di file aggiuntivo, tale tipo avrà queste caratteristiche. Se il tipo di file aggiuntivo è stato precedentemente associato a un'altra applicazione, tali caratteristiche sostituiranno quelle originali.

Per registrare la procedura predefinita, inserire le stesse chiavi del registro di sistema create per il ProgID dell'applicazione nella sottochiave dell'applicazione delle applicazioni **\_ \_ radice delle classi HKEY** \\ . È anche possibile includere un valore FriendlyAppName per fornire al sistema un nome descrittivo per l'applicazione. Il nome descrittivo dell'applicazione può essere estratto anche dal file eseguibile, ma solo se il valore FriendlyAppName è assente. Il frammento di registro seguente mostra una procedura predefinita di esempio per MyProgram.exe che definisce un nome descrittivo e varie voci di menu di scelta rapida. Le stringhe di comando includono il flag/a per notificare all'applicazione che sta aprendo un tipo di file arbitrario. Se si include una sottochiave **DefaultIcon** , è consigliabile usare un'icona generica.

```
HKEY_CLASSES_ROOT
   Applications
      MyProgram.exe
         FriendlyAppName = Friendly Name
         shell
            open
               command
                  (Default) = C:\MyDir\MyProgram.exe /a "%1"
            print
               command
                  (Default) = C:\MyDir\MyProgram.exe /a /p "%1"
            printto
               command
                  (Default) = C:\MyDir\MyProgram.exe /a /p "%1" "%2" %3 %4
```

## <a name="extending-the-new-submenu"></a>Estensione del nuovo sottomenu

Quando un utente apre il menu **file** in Esplora risorse, il primo comando è **nuovo**. Se si seleziona questo comando, verrà visualizzato un sottomenu. Per impostazione predefinita, contiene due comandi, **cartella** e **collegamento**, che consentono agli utenti di creare sottocartelle e collegamenti. Questo sottomenu può essere esteso in modo da includere i comandi per la creazione di file per qualsiasi tipo di file.

Per aggiungere un comando per la creazione di file al **nuovo** sottomenu, i file dell'applicazione devono avere un [tipo di file](fa-file-types.md) associato. Includere una sottochiave **ShellNew** sotto la chiave per l'estensione del nome file. Quando si seleziona il comando **nuovo** del menu **file** , la shell lo aggiungerà al **nuovo** sottomenu. La stringa di visualizzazione del comando sarà la stringa descrittiva assegnata al ProgID del programma.

Assegnare uno o più valori di dati alla sottochiave **ShellNew** per specificare il metodo di creazione del file. I valori disponibili sono i seguenti.



| Valore    | Descrizione                                                                                                                                                   |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Comando  | Esegue un'applicazione. Si tratta di un valore **reg \_ SZ** che specifica il percorso dell'applicazione da eseguire. Ad esempio, è possibile impostarlo per avviare una procedura guidata. |
| Dati     | Crea un file contenente i dati specificati. I dati sono un valore **\_ binario REG** con i dati del file. Se è specificato NullFile o FileName, i dati vengono ignorati.  |
| FileName | Crea un file che è una copia di un file specificato. FileName è un valore **reg \_ SZ** , impostato sul percorso completo del file da copiare.                 |
| NullFile | Crea un file vuoto. A NullFile non è assegnato alcun valore. Se viene specificato NullFile, i valori dei dati e del nome file vengono ignorati.                                  |



 

Nella figura seguente viene illustrato il **nuovo** sottomenu per il tipo di file. MYP utilizzato come esempio in [tipi di file](fa-file-types.md) e personalizzazione di [Icone](icon.md). Dispone ora di un comando, **applicazione programmi**. Quando un utente seleziona l' **applicazione di programma** dal **nuovo** sottomenu, la shell crea un file denominato "nuovo programma Application. MYP" e lo passa a MyProgram.exe.

![screenshot del menu nuovo personalizzato](images/context5.png)

La voce del registro di sistema è ora la seguente:

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      MyProgram.1
         ShellNew
            NullFile
   MyProgram.1
      (Default) = MyProgram Application
      DefaultIcon
         (Default) = C:\MyDir\MyProgram.exe,2
      Shell
         (Default) = doit
         open
            command
               (Default) = C:\MyDir\MyProgram.exe "%1"
         doit
            (Default) = &Do It
            command
               (Default) = C:\MyDir\MyProgram.exe /d "%1"
         print
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1"
         printto
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1" "%2" %3 %4
```

 

 




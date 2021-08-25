---
description: Facendo clic con il pulsante destro del mouse su un oggetto viene in genere visualizzato un menu di scelta rapida. Questo menu contiene un elenco di comandi che l'utente può selezionare per eseguire varie azioni sull'oggetto. Questa sezione è un'introduzione ai menu di scelta rapida per file system oggetti.
ms.assetid: d951d1e8-0f88-49c4-8373-e6db0e18cd72
title: Estensione dei menu di scelta rapida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d046805ebc787f5cad2bfaa40538c51b826c3f0541f3ec1afad508202a4a25fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118460648"
---
# <a name="extending-shortcut-menus"></a>Estensione dei menu di scelta rapida

Facendo clic con il pulsante destro del mouse su un oggetto in genere viene visualizzato un *menu di scelta rapida.* Questo menu contiene un elenco di comandi che l'utente può selezionare per eseguire varie azioni sull'oggetto. Questa sezione è un'introduzione ai menu di scelta rapida per file system oggetti.

-   [Menu di scelta rapida per oggetti del file system](#shortcut-menus-for-file-system-objects)
-   [Verbi del menu di scelta rapida](#shortcut-menu-verbs)
    -   [Verbi canonici](#canonical-verbs)
    -   [Verbi estesi](#extended-verbs)
-   [Estensione del menu di scelta rapida per un tipo di file](#extending-the-shortcut-menu-for-a-file-type)
-   [Estensione del menu di scelta rapida per gli oggetti shell predefiniti](#extending-the-shortcut-menu-for-predefined-shell-objects)
-   [Registrazione di un'applicazione per gestire tipi di file arbitrari](#registering-an-application-to-handle-arbitrary-file-types)
-   [Estensione del nuovo sottomenu](#extending-the-new-submenu)

Altre informazioni sono disponibili qui:

-   [Come definire verbi estesi](how-to-define-extended-verbs.md)
-   [Come associare verbi ai comandi DDE](how-to-associate-verbs-with-dde-commands.md)

## <a name="shortcut-menus-for-file-system-objects"></a>Menu di scelta rapida per oggetti del file system

Quando un utente fa clic con il pulsante destro del mouse su un oggetto, ad esempio un file, visualizzato in Windows Explorer o sul desktop, viene visualizzato un menu di scelta rapida con un elenco di comandi. L'utente può quindi eseguire un'azione sul file, ad esempio l'apertura o l'eliminazione, selezionando il comando appropriato.

Poiché i menu di scelta rapida vengono spesso usati per la gestione dei file, Shell fornisce un set di comandi predefiniti, ad esempio Taglia e Copia, che vengono visualizzati nel menu di scelta rapida per qualsiasi file. Si noti che, anche se Open With è un comando predefinito, non viene visualizzato per alcuni tipi di file standard, ad esempio wav. La figura seguente della directory Documenti di esempio, usata anche come esempio [in](icon.md)Personalizzazione delle icone, mostra un menu di scelta rapida predefinito visualizzato facendo clic con il pulsante destro del mouse MyDocs4.xyz.

![Screenshot del menu di scelta rapida predefinito per file system oggetti](images/context1.jpg)

Il motivo per cui MyDocs4.xyz un menu di scelta rapida predefinito è che non è membro di un tipo [di file registrato.](fa-file-types.md) D'altra parte, .txt è un tipo di file registrato. Se si fa clic con il pulsante destro del mouse su uno dei file .txt, nella sezione superiore verrà invece visualizzato un menu di scelta rapida con due comandi aggiuntivi: **Apri** e **Stampa**.

![Screenshot del menu di scelta rapida personalizzato per gli oggetti file system personalizzati](images/context2.jpg)

Dopo aver registrato un tipo di file, è possibile estenderne il menu di scelta rapida con comandi aggiuntivi. Vengono visualizzati sopra i comandi predefiniti quando si fa clic con il pulsante destro del mouse su un file di quel tipo. Anche se la maggior parte dei comandi aggiunti in questo modo sono comuni, ad esempio **Stampa** o **Apri,** è possibile aggiungere qualsiasi comando che un utente potrebbe trovare utile.

Per estendere il menu di scelta rapida per un tipo di file, è necessario creare una voce del Registro di sistema per ogni comando. Un approccio più sofisticato consiste nell'implementare un gestore *del menu* di scelta rapida, che consente di estendere il menu di scelta rapida per un tipo di file per ogni file. Per altre informazioni, vedere [Creazione di gestori del menu di scelta rapida.](context-menu-handlers.md)

## <a name="shortcut-menu-verbs"></a>Verbi del menu di scelta rapida

Ogni comando del menu di scelta rapida viene identificato nel Registro di sistema dal *verbo*. Questi verbi sono gli stessi usati da [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) quando si avviano applicazioni a livello di codice. Per altre informazioni sull'uso di **ShellExecuteEx,** vedere la discussione in [Avvio di applicazioni](launch.md).

Un verbo è una stringa di testo semplice usata da Shell per identificare il comando associato. Ogni verbo corrisponde alla stringa *di comando* usata per avviare il comando in una finestra della console o in un file batch (.bat). Ad esempio, il **verbo open** in genere avvia un programma per aprire un file. La stringa di comando è in genere simile alla seguente:

``` syntax
"My Program.exe" "%1"
```

"%1" è il segnaposto standard per un parametro della riga di comando fornito con il nome file. Ad esempio, può specificare una pagina specifica da visualizzare in una visualizzazione a schede.

> [!Note]  
> Se un elemento della stringa di comando contiene o può contenere spazi, deve essere racchiuso tra virgolette. In caso contrario, se l'elemento contiene uno spazio, non verrà analizzato correttamente. Ad esempio, "My Program.exe" avvierà correttamente l'applicazione. Se si usa My Program.exe, il sistema tenterà di avviare "My" con "Program.exe" come primo argomento della riga di comando. È consigliabile usare sempre le virgolette con argomenti come "%1" espansi in stringhe da Shell, perché non è possibile essere certi che la stringa non conterrà uno spazio.

 

Ai verbi può  essere associata anche una stringa di visualizzazione, che viene visualizzata nel menu di scelta rapida anziché nella stringa del verbo stesso. Ad esempio, la stringa di visualizzazione **per openas** è Open With. Come le normali stringhe di menu, inclusa una e commerciale (&) nella stringa di visualizzazione consente la selezione da tastiera del comando.

### <a name="canonical-verbs"></a>Verbi canonici

In generale, le applicazioni sono responsabili di fornire stringhe di visualizzazione localizzate per i verbi definiti. Tuttavia, per fornire un certo grado di indipendenza del linguaggio, il sistema definisce un set standard di verbi di uso comune denominati *verbi canonici.* Un verbo canonico può essere usato con qualsiasi lingua e il sistema genera automaticamente una stringa di visualizzazione localizzata correttamente. Ad esempio, la **stringa** di visualizzazione del verbo aperto verrà impostata su Open in un sistema inglese e su Öffnen in un sistema tedesco.

I verbi canonici includono:



| Valore      | Descrizione                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| apre       | Apre il file o la cartella.                                                                   |
| Opennew    | Apre il file o la cartella in una nuova finestra.                                                   |
| print      | Stampa il file.                                                                            |
| Esplorare    | Apre Windows Explorer con la cartella selezionata.                                            |
| trovare       | Apre la **Windows finestra di dialogo** Cerca con la cartella impostata come percorso di ricerca predefinito. |
| openas     | Apre la **finestra di dialogo** Apri con .                                                         |
| properties | Apre la finestra delle proprietà dell'oggetto.                                                          |



 

Anche il verbo printto è canonico, ma non viene mai visualizzato. Consente all'utente di stampare un file trascinandolo in un oggetto stampante.

### <a name="extended-verbs"></a>Verbi estesi

Quando l'utente fa clic con il pulsante destro del mouse su un oggetto, il menu di scelta rapida contiene tutti i verbi normali. Tuttavia, potrebbero essere presenti comandi che si vuole supportare, ma che non sono stati visualizzati in ogni menu di scelta rapida. Ad esempio, è possibile avere comandi che non vengono comunemente usati o destinati a utenti esperti. Per questo motivo, è anche possibile definire uno o più *verbi estesi.* Questi verbi sono anche stringhe di caratteri e sono simili ai verbi normali. Si distinguono dai verbi normali in base alla modalità di registrazione. Per accedere ai comandi associati ai verbi estesi, l'utente deve fare clic con il pulsante destro del mouse su un oggetto premendo MAIUSC. I verbi estesi verranno quindi visualizzati insieme ai verbi normali.

## <a name="extending-the-shortcut-menu-for-a-file-type"></a>Estensione del menu di scelta rapida per un tipo di file

Il modo più semplice per estendere il menu di scelta rapida per un tipo di file è con il Registro di sistema. A tale scopo, aggiungere una **sottochiave Shell** sotto la chiave per il ProgID dell'applicazione associata al [tipo di file](fa-file-types.md). Facoltativamente, è possibile definire un *verbo predefinito* per il tipo di file impostandolo come valore predefinito della **sottochiave Shell.**

Il verbo predefinito viene visualizzato per primo nel menu di scelta rapida. Il suo scopo è fornire alla shell un verbo che può usare quando [**shellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) viene chiamato ma non viene specificato alcun verbo. Shell non seleziona necessariamente il verbo predefinito quando **shellExecuteEx** viene usato in questo modo. Per shell [versioni 5.0](versions.md) e successive, disponibili Windows 2000 e versioni successive, shell usa il primo verbo disponibile nell'elenco seguente. Se non sono disponibili, l'operazione ha esito negativo.

-   Verbo aperto
-   Verbo predefinito
-   Primo verbo nel Registro di sistema
-   Verbo openwith

Per le versioni della shell [precedenti alla versione 5.0,](versions.md)omettere il terzo elemento.

Sotto la **sottochiave Shell** creare una sottochiave per ogni verbo che si vuole aggiungere. Ognuna di queste sottochiavi avrà un **valore \_ REG SZ** impostato sulla stringa di visualizzazione del verbo. È possibile omettere la stringa di visualizzazione per i verbi canonici perché il sistema visualizza automaticamente una stringa localizzata correttamente. Se si omette la stringa di visualizzazione per i verbi non canonici, verrà visualizzata la stringa del verbo. Per ogni sottochiave verbo, creare una **sottochiave del** comando con il valore predefinito impostato sulla stringa di comando.

La figura seguente mostra un menu di scelta rapida per il tipo di file myp usato in [Tipi di file](fa-file-types.md) e [Personalizzazione delle icone](icon.md). Il menu di scelta rapida include ora verbi open, doit, print e printto, con doit come verbo predefinito. Il menu di scelta rapida è simile al seguente.

![Screenshot del menu di scelta rapida personalizzato](images/context3.jpg)

Le voci del Registro di sistema usate per estendere il menu di scelta rapida illustrato nella figura precedente sono:

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

Anche se **il comando Apri** con è sopra il primo separatore, viene creato automaticamente dal sistema e non richiede una voce del Registro di sistema. Il sistema crea automaticamente nomi visualizzati per i verbi canonici aperti e stampati. Poiché doit non è un verbo canonico, gli viene assegnato un nome visualizzato, "&Do It", che può essere selezionato premendo il tasto D. Il verbo printto non viene visualizzato nel menu di scelta rapida, ma l'inclusione consente all'utente di stampare i file rilasciandoli su un'icona della stampante. In questo esempio% 1 rappresenta il nome del file e %2 il nome della stampante.

I verbi possono essere eliminati tramite le impostazioni dei criteri aggiungendo un valore SuppressionPolicy alla chiave del verbo. Impostare il valore di SuppressionPolicy sull'ID criteri. Se il criterio è attivato, il verbo e la voce di menu di scelta rapida associata vengono eliminati. Per i possibili valori id dei criteri, vedere [**l'enumerazione RESTRICTIONS.**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions)

## <a name="extending-the-shortcut-menu-for-predefined-shell-objects"></a>Estensione del menu di scelta rapida per gli oggetti shell predefiniti

Molti oggetti shell predefiniti hanno menu di scelta rapida che possono essere estesi. Registrare il comando nello stesso modo in cui si registrano i tipi di file tipici, ma usare il nome dell'oggetto predefinito come nome del tipo di file.

Un elenco di oggetti predefiniti è disponibile nella sezione Oggetti predefiniti *della shell* di Creazione di gestori di estensioni [della shell.](handlers.md) Gli oggetti shell predefiniti i cui menu di scelta rapida possono essere estesi aggiungendo verbi nel Registro di sistema vengono contrassegnati nella tabella con la parola "Verbo".

## <a name="registering-an-application-to-handle-arbitrary-file-types"></a>Registrazione di un'applicazione per gestire tipi di file arbitrari

Nelle sezioni precedenti di questo documento è stato illustrato come definire voci di menu di scelta rapida per un particolare tipo di file. Tra le altre cose, la definizione del menu di scelta rapida consente di specificare come l'applicazione associata apre un membro del tipo di file. Tuttavia, come illustrato in Tipi di [file](fa-file-types.md), le applicazioni possono anche registrare una procedura predefinita separata da usare quando un utente tenta di usare l'applicazione per aprire un tipo di file non associato all'applicazione. Questo argomento viene illustrato in questo argomento perché la procedura predefinita viene registrare in modo molto identico a come si registrano le voci del menu di scelta rapida.

La procedura predefinita ha due scopi di base. Uno è specificare come deve essere richiamata l'applicazione per aprire un tipo di file arbitrario. È possibile, ad esempio, usare un flag della riga di comando per indicare che è in corso l'apertura di un tipo di file sconosciuto. L'altro scopo è definire le varie caratteristiche di un tipo di file, ad esempio le voci del menu di scelta rapida e l'icona. Se un utente associa l'applicazione a un tipo di file aggiuntivo, tale tipo avrà queste caratteristiche. Se il tipo di file aggiuntivo è stato precedentemente associato a un'altra applicazione, queste caratteristiche sostituiranno gli originali.

Per registrare la procedura predefinita, inserire le stesse chiavi del Registro di sistema create per il ProgID dell'applicazione nella sottochiave dell'applicazione **HKEY \_ CLASSES \_ ROOT** \\ **Applications**. È anche possibile includere un valore FriendlyAppName per fornire al sistema un nome descrittivo per l'applicazione. Il nome descrittivo dell'applicazione può anche essere estratto dal relativo file eseguibile, ma solo se il valore FriendlyAppName è assente. Nel frammento del Registro di sistema seguente viene illustrata una procedura predefinita di esempio per MyProgram.exe che definisce un nome descrittivo e diverse voci del menu di scelta rapida. Le stringhe di comando includono il flag /a per notificare all'applicazione che sta aprendo un tipo di file arbitrario. Se si include una **sottochiave DefaultIcon,** è consigliabile usare un'icona generica.

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

Quando un utente apre il menu **File** in Windows Explorer, il primo comando è **Nuovo**. Selezionando questo comando viene visualizzato un sottomenu. Per impostazione predefinita, contiene due comandi, **Cartella** e **Collegamento**, che consentono agli utenti di creare sottocartelle e collegamenti. Questo sottomenu può essere esteso per includere i comandi di creazione di file per qualsiasi tipo di file.

Per aggiungere un comando di creazione file al sottomenu **Nuovo,** ai file dell'applicazione deve essere associato un tipo di [file.](fa-file-types.md) Includere una **sottochiave ShellNew** sotto la chiave per l'estensione di file. Quando il comando Nuovo **del** menu **File** è selezionato, shell lo aggiungerà al **sottomenu Nuovo.** La stringa di visualizzazione del comando sarà la stringa descrittiva assegnata al ProgID del programma.

Assegnare uno o più valori di dati alla **sottochiave ShellNew** per specificare il metodo di creazione del file. Seguono i valori disponibili.



| Valore    | Descrizione                                                                                                                                                   |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Comando  | Esegue un'applicazione. Si tratta di **un \_ valore REG SZ** che specifica il percorso dell'applicazione da eseguire. Ad esempio, è possibile impostarlo per avviare una procedura guidata. |
| Dati     | Crea un file contenente i dati specificati. I dati sono **\_ un valore REG BINARY** con i dati del file. I dati vengono ignorati se viene specificato NullFile o FileName.  |
| FileName | Crea un file che è una copia di un file specificato. FileName è un **valore \_ REG SZ,** impostato sul percorso completo del file da copiare.                 |
| NullFile | Crea un file vuoto. A NullFile non è assegnato un valore. Se viene specificato NullFile, i valori Data e FileName vengono ignorati.                                  |



 

La figura seguente mostra il **sottomenu Nuovo** per il tipo di file myp usato come esempio in Tipi di [file](fa-file-types.md) e [personalizzazione delle icone](icon.md). È ora disponibile un comando, **MyProgram Application.** Quando un utente seleziona MyProgram Application (Applicazione **MyProgram)** dal sottomenu **New** (Nuovo), shell crea un file denominato "New MyProgram Application.myp" e lo passa a MyProgram.exe.

![Screenshot del nuovo menu personalizzato](images/context5.png)

La voce del Registro di sistema è ora la seguente:

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

 

 




---
description: Un oggetto gestore dell'estensione della shell deve essere registrato prima che la shell possa usarlo. Questo argomento è una descrizione generale di come registrare un gestore dell'estensione della shell.
ms.assetid: e4b98c18-746b-4909-8821-f25de9d15373
title: Registrazione di gestori estensioni della shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca50bfaff984884b74ecc8572d4af9d96c55d0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980202"
---
# <a name="registering-shell-extension-handlers"></a>Registrazione di gestori estensioni della shell

Un oggetto gestore dell'estensione della shell deve essere registrato prima che la shell possa usarlo. Questo argomento è una descrizione generale di come registrare un gestore dell'estensione della shell.

Ogni volta che si crea o si modifica un gestore dell'estensione della shell, è importante notificare al sistema che è stata apportata una modifica. A tale scopo, chiamare [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), specificando l'evento **SHCNE \_ ASSOCCHANGED** . Se non si chiama **SHChangeNotify**, è possibile che la modifica non venga riconosciuta fino al riavvio del sistema.

Esistono alcuni fattori aggiuntivi che si applicano ai sistemi Windows 2000. Per informazioni dettagliate, vedere la sezione relativa alla [registrazione dei gestori estensioni della shell in sistemi Windows 2000](#registering-shell-extension-handlers) .

Come con tutti gli oggetti Component Object Model (COM), è necessario creare un GUID per il gestore usando uno strumento come Guidgen.exe, fornito con Windows Software Development Kit (SDK). Creare una sottochiave in **HKEY \_ classi \_ radice** \\ **CLSID** il cui nome è il formato stringa del GUID. Poiché i gestori di estensioni della shell sono server in-process, è necessario creare anche una sottochiave **InprocServer32** sotto tale sottochiave GUID con il valore (predefinito) impostato sul percorso della dll del gestore. Utilizzare il modello di threading dell'Apartment. Di seguito è riportato un esempio:

```
HKEY_CLASSES_ROOT
   CLSID
      {00021500-0000-0000-C000-000000000046}
         InprocServer32
            (Default) = %windir%\System32\Example.dll
            ThreadingModel = Apartment
```

Ogni volta che la shell esegue un'azione che può coinvolgere un gestore dell'estensione della shell, verifica la sottochiave del registro di sistema appropriata. La sottochiave nella quale viene registrato un gestore di estensione controlla quando verrà chiamato. Ad esempio, è pratica comune avere un gestore di menu di scelta rapida chiamato quando la shell Visualizza un menu di scelta rapida per un membro di un [tipo di file](fa-file-types.md). In questo caso, il gestore deve essere registrato nella sottochiave **ProgID** del tipo di file.

In questo argomento vengono illustrati gli argomenti seguenti:

-   [Nomi dei gestori](#handler-names)
-   [Oggetti shell predefiniti](#predefined-shell-objects)
-   [Esempio di registrazione di un gestore estensioni](#example-of-an-extension-handler-registration)
    -   [Registrazione di gestori estensioni della shell](#registering-shell-extension-handlers)
-   [Argomenti correlati](#related-topics)

## <a name="handler-names"></a>Nomi dei gestori

Per abilitare un gestore dell'estensione della shell, creare una sottochiave con il nome della sottochiave del gestore (vedere di seguito) nella sottochiave **ShellEx** del **ProgID** (per i tipi di file) o il nome del tipo di oggetto della shell (per [ \_ \_ gli oggetti shell predefiniti](handlers.md)).

Ad esempio, se si desidera registrare un gestore dell'estensione del menu di scelta rapida per il programma. 1, iniziare creando la sottochiave seguente:

```
HKEY_CLASSES_ROOT
   MyProgram.1
      ShellEx
         ContextMenuHandlers
```

Per i gestori seguenti, creare una sottochiave sotto la sottochiave "gestore della sottochiave" denominata come versione in formato stringa dell'identificatore di classe (CLSID) dell'estensione della shell. È possibile registrare più estensioni nel nome della sottochiave del gestore creando più sottochiavi.



| Gestore                 | Interfaccia          | Nome sottochiave gestore       |
|-------------------------|--------------------|---------------------------|
| Gestore del provider di colonne | IColumnProvider    | **ColumnHandlers**        |
| Gestore del menu di scelta rapida   | IContextMenu       | **ContextMenuHandlers**   |
| Gestore CopyHook        | ICopyHook          | **CopyHookHandlers**      |
| Gestore di trascinamento della selezione   | IContextMenu       | **DragDropHandlers**      |
| Gestore della finestra delle proprietà  | IShellPropSheetExt | **PropertySheetHandlers** |



 

Per i gestori seguenti, il valore predefinito della chiave del nome della sottochiave del gestore è la versione in formato stringa del CLSID dell'estensione della shell. Per questi gestori è possibile registrare solo un'estensione.



| Gestore                 | Interfaccia            | Nome sottochiave gestore                        |
|-------------------------|----------------------|--------------------------------------------|
| Gestore dati            | IDataObject          | **DataHandler**                            |
| Gestore di trascinamento            | IDropTarget          | **DropHandler**                            |
| Gestore icone            | IExtractIconA/W      | **IconHandler**                            |
| Gestore immagini di anteprima | IThumbnailProvider   | **{E357FCCD-A995-4576-B01F-234630154E96}** |
| Gestore della finestra popup         | IQueryInfo           | **{00021500-0000-0000-C000-000000000046}** |
| Collegamento della shell (ANSI)       | IShellLinkA          | **{000214EE-0000-0000-C000-000000000046}** |
| Collegamento Shell (UNICODE)    | IShellLinkW          | **{000214F9-0000-0000-C000-000000000046}** |
| Archiviazione strutturata      | IStorage             | **{0000000B-0000-0000-C000-000000000046}** |
| Metadati                | IPropertySetStorage  | **Gestoreproprietà**                        |
| Aggiungi a menu Start       | IStartMenuPinnedList | **{a2a9545d-a0c2-42b4-9708-a0b2badd77c8}** |
| Aggiungere alla barra delle applicazioni          |                      | **{90AA3A4E-1CBA-4233-B8BB-535773D48449}** |



 

Le sottochiavi specificate per aggiungere **pin al menu Start** e aggiungere **alla barra delle applicazioni** al menu di scelta rapida di un elemento sono necessarie solo per i tipi di file che includono la voce di [collegamento](./links.md) .

## <a name="predefined-shell-objects"></a>Oggetti shell predefiniti

La shell definisce oggetti aggiuntivi sotto **la \_ \_ radice delle classi HKEY** che possono essere estese in modo analogo ai tipi di file. Per aggiungere un gestore della finestra delle proprietà per tutti i file, ad esempio, è possibile eseguire la registrazione nella sottochiave **PropertySheetHandlers** .

```
HKEY_CLASSES_ROOT
   *
      shellex
         PropertySheetHandlers
```

La tabella seguente fornisce le varie sottochiavi della **\_ \_ radice delle classi HKEY** in cui è possibile registrare i gestori di estensione. Si noti che molti gestori di estensioni non possono essere registrati in tutte le sottochiavi elencate. Per ulteriori informazioni, vedere la documentazione del gestore specifico.



| Sottochiave                    | Descrizione                                                          | Possibili gestori                                |
|---------------------------|----------------------------------------------------------------------|--------------------------------------------------|
| **\** _                    | Tutti i file                                                            | Menu di scelta rapida, finestra delle proprietà, verbi (vedere di seguito) |
| _ *AllFileSystemObjects**  | Tutti i file e le cartelle di file                                           | Menu di scelta rapida, finestra delle proprietà, verbi             |
| **Cartella**                | Tutte le cartelle                                                          | Menu di scelta rapida, finestra delle proprietà, verbi             |
| **Directory**             | Cartelle di file                                                         | Menu di scelta rapida, finestra delle proprietà, verbi             |
| **\\Sfondo directory** | Sfondo cartella file                                               | Solo menu di scelta rapida                               |
| **DesktopBackground**     | Sfondo del desktop (Windows 7 e versioni successive)                            | Menu di scelta rapida, verbi                             |
| **Unità**                 | Tutte le unità in computer, ad esempio "C: \\ "                             | Menu di scelta rapida, finestra delle proprietà, verbi             |
| **Network**               | Intera rete (in risorse di rete)                             | Menu di scelta rapida, finestra delle proprietà, verbi             |
| **Tipo di rete \\\\\#**     | Tutti gli oggetti di tipo \# (vedere di seguito)                                   | Menu di scelta rapida, finestra delle proprietà, verbi             |
| **NetShare**              | Tutte le condivisioni di rete                                                   | Menu di scelta rapida, finestra delle proprietà, verbi             |
| **NetServer**             | Tutti i server di rete                                                  | Menu di scelta rapida, finestra delle proprietà, verbi             |
| *\_Nome provider di rete \_* | Tutti gli oggetti forniti dal provider di rete "*Network \_ provider \_ Name*" | Menu di scelta rapida, finestra delle proprietà, verbi             |
| **Stampanti**              | Tutte le stampanti                                                         | Menu di scelta rapida, finestra delle proprietà                    |
| **AudioCD**               | CD audio nell'unità CD                                                 | Solo verbi                                       |
| **DVD**                   | Unità DVD (Windows 2000)                                             | Menu di scelta rapida, finestra delle proprietà, verbi             |



 

### <a name="notes"></a>Note

-   Per accedere al menu di scelta rapida dello sfondo della cartella file, fare clic con il pulsante destro del mouse all'interno di una cartella di file, ma non su uno dei contenuti della cartella.
-   I "verbi" sono comandi speciali registrati nel verbo della shell della sottochiave **\_ \_ radice delle classi HKEY** \\  \\  \\ .
-   Per il tipo di **rete** \\  \\ **\#** , " \# " è un codice del tipo di provider di rete in decimale. Il codice del tipo di provider di rete è la parola più elevata di un tipo di rete. L'elenco dei tipi di rete viene specificato nel file di intestazione Winnetwk. h (WNNC \_ net \_ \* Values). Ad esempio, WNNC \_ net \_ Shiva è 0x00330000, quindi la sottochiave di tipo corrispondente sarà **HKEY \_ classi \_ radice** tipo di \\ **rete** \\  \\ **51**.
-   "*Network \_ provider \_ Name*" è un nome di provider di rete come specificato da [**WNetGetProviderName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea), con gli spazi convertiti in caratteri di sottolineatura. Ad esempio, se è installato il provider rete Microsoft Networking, il nome del provider è "rete Microsoft Windows" e il *nome del \_ provider \_ di rete* corrispondente è **\_ \_ rete Microsoft Windows**.

## <a name="example-of-an-extension-handler-registration"></a>Esempio di registrazione di un gestore estensioni

Per abilitare un particolare gestore, creare una sottochiave nella sottochiave del tipo di gestore dell'estensione con il nome del gestore. La shell non usa il nome del gestore, ma deve essere diverso da tutti gli altri nomi sotto tale sottochiave di tipo. Impostare il valore predefinito della sottochiave Name sul formato stringa del GUID del gestore.

Nell'esempio seguente vengono illustrate le voci del registro di sistema che consentono il menu di scelta rapida e i gestori dell'estensione della finestra delle proprietà, utilizzando un tipo di file MYP.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
      {11111111-2222-3333-4444-555555555555}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      Shellex
         ContextMenuHandler
            MyCommand
               (Default) = {00000000-1111-2222-3333-444444444444}
         PropertySheetHandlers
            MyPropSheet
               (Default) = {11111111-2222-3333-4444-555555555555}
```

### <a name="registering-shell-extension-handlers"></a>Registrazione di gestori estensioni della shell

La procedura di registrazione descritta in questa sezione deve essere seguita per tutti i sistemi Windows. Tuttavia, con i sistemi successivi, potrebbe essere necessario un passaggio aggiuntivo. Poiché queste versioni successive di Windows sono progettate per essere usate in un ambiente gestito, l'accesso al registro di sistema può essere limitato a livello amministrativo, richiedendo un approccio leggermente diverso rispetto a quello descritto nella sezione precedente.

> [!Note]  
> Generalmente, i programmi di installazione non devono scrivere direttamente nel registro di sistema. Al contrario, il programma di installazione deve essere eseguito con Windows Installer pacchetti. Questi strumenti garantiscono che il software venga eseguito correttamente e fornisca l'accesso a funzionalità come la registrazione di classi per utente.

 

I gestori di estensioni della shell vengono eseguiti nel processo della shell. Poiché si tratta di un processo di sistema, l'amministratore di un sistema può limitare i gestori di estensioni della shell a quelli in un elenco approvato impostando il valore EnforceShellExtensionSecurity della chiave **Explorer** su 1, come illustrato di seguito:

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
                     EnforceShellExtensionSecurity = 1
```

Per inserire un gestore dell'estensione della shell nell'elenco approvato, creare un valore **reg \_ SZ** il cui nome sia il formato stringa del GUID del gestore nella sottochiave **Approved** .

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Shell Extensions
                  Approved
```

Nell'esempio seguente, ad esempio, i gestori di *comando* e *MyPropSheet* vengono aggiunti all'elenco approvato.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Shell Extensions
                  Approved
                     {00000000-1111-2222-3333-444444444444} = MyCommand
                     {11111111-2222-3333-4444-555555555555} = MyPropSheet
```

La shell non utilizza il valore assegnato al GUID, ma deve essere impostato in modo da semplificare il controllo del registro di sistema.

L'applicazione di installazione può aggiungere valori alla sottochiave **approvata** solo se l'utente che installa l'applicazione dispone di privilegi sufficienti. Se il tentativo di aggiungere un gestore di estensione ha esito negativo, è necessario informare l'utente che sono necessari privilegi amministrativi per installare completamente l'applicazione. Se il gestore è essenziale per l'applicazione, è necessario interrompere l'installazione e inviare una notifica all'utente per contattare un amministratore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Inizializzazione di gestori estensioni della shell](int-shell-exts.md)
</dt> </dl>

 

 

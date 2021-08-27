---
description: Prima di poterlo usare, è necessario registrare un oggetto gestore dell'estensione shell. In questo argomento viene descritto in generale come registrare un gestore dell'estensione shell.
ms.assetid: e4b98c18-746b-4909-8821-f25de9d15373
title: Registrazione dei gestori delle estensioni della shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec883f6e843bdfbf663108c0acda123d786262916f4a347d9433e7fd5f77baca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111211"
---
# <a name="registering-shell-extension-handlers"></a>Registrazione dei gestori delle estensioni della shell

Prima di poterlo usare, è necessario registrare un oggetto gestore dell'estensione shell. In questo argomento viene descritto in generale come registrare un gestore dell'estensione shell.

Ogni volta che si crea o si modifica un gestore dell'estensione shell, è importante notificare al sistema che è stata apportata una modifica. A tale scopo, chiamare [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), specificando **l'evento SHCNE \_ ASSOCCHANGED.** Se non si chiama **SHChangeNotify**, la modifica potrebbe non essere riconosciuta fino al riavvio del sistema.

Esistono alcuni fattori aggiuntivi che si applicano ai Windows 2000. Per informazioni dettagliate, vedere [la sezione Registering Shell Extension Handlers on Windows 2000 Systems](#registering-shell-extension-handlers) (Registrazione dei gestori estensioni shell in Windows 2000 Systems).

Come per tutti gli oggetti Component Object Model (COM), è necessario creare un GUID per il gestore usando uno strumento come Guidgen.exe, fornito con Windows Software Development Kit (SDK). Creare una sottochiave in **HKEY \_ CLASSES \_ ROOT** \\ **CLSID** il cui nome è il formato stringa di tale GUID. Poiché i gestori delle estensioni shell sono server in-process, è necessario creare anche una sottochiave **InprocServer32** in tale sottochiave GUID con il valore (Predefinito) impostato sul percorso della DLL del gestore. Usare il modello di threading apartment. Di seguito è riportato un esempio:

```
HKEY_CLASSES_ROOT
   CLSID
      {00021500-0000-0000-C000-000000000046}
         InprocServer32
            (Default) = %windir%\System32\Example.dll
            ThreadingModel = Apartment
```

Ogni volta che Shell esegue un'azione che può coinvolgere un gestore dell'estensione Shell, controlla la sottochiave del Registro di sistema appropriata. La sottochiave in cui viene registrato un gestore di estensioni controlla quando verrà chiamato. Ad esempio, è pratica comune avere un gestore del menu di scelta rapida chiamato quando shell visualizza un menu di scelta rapida per un membro di un [tipo di file](fa-file-types.md). In questo caso, il gestore deve essere registrato nella sottochiave **ProgID** del tipo di file.

In questo argomento vengono illustrati gli argomenti seguenti:

-   [Nomi dei gestori](#handler-names)
-   [Oggetti shell predefiniti](#predefined-shell-objects)
-   [Esempio di registrazione di un gestore di estensioni](#example-of-an-extension-handler-registration)
    -   [Registrazione dei gestori delle estensioni della shell](#registering-shell-extension-handlers)
-   [Argomenti correlati](#related-topics)

## <a name="handler-names"></a>Nomi dei gestori

Per abilitare un gestore dell'estensione Shell, creare una sottochiave con il nome della sottochiave del gestore (vedere di seguito) nella sottochiave **ShellEx** del **ProgID** (per i tipi di file) o del nome del tipo di oggetto Shell (per gli oggetti [shell \_ predefiniti). \_](handlers.md)

Ad esempio, se si vuole registrare un gestore dell'estensione del menu di scelta rapida per MyProgram.1, creare la sottochiave seguente:

```
HKEY_CLASSES_ROOT
   MyProgram.1
      ShellEx
         ContextMenuHandlers
```

Per i gestori seguenti, creare una sottochiave sotto la sottochiave "Handler Subkey name" denominata come versione stringa dell'identificatore di classe (CLSID) dell'estensione Shell. È possibile registrare più estensioni nel nome della sottochiave del gestore creando più sottochiavi.



| Gestore                 | Interfaccia          | Nome della sottochiave del gestore       |
|-------------------------|--------------------|---------------------------|
| Gestore del provider di colonne | IColumnProvider    | **ColumnHandlers**        |
| Gestore del menu di scelta rapida   | IContextMenu       | **ContextMenuHandlers**   |
| Gestore copyhook        | ICopyHook          | **CopyHookHandlers**      |
| Gestore di trascinamento della selezione   | IContextMenu       | **DragDropHandlers**      |
| Gestore della finestra delle proprietà  | IShellPropSheetExt | **PropertySheetHandlers** |



 

Per i gestori seguenti, il valore predefinito della chiave "Handler Subkey Name" è la versione stringa del CLSID dell'estensione Shell. Per questi gestori è possibile registrare una sola estensione.



| Gestore                 | Interfaccia            | Nome della sottochiave del gestore                        |
|-------------------------|----------------------|--------------------------------------------|
| Gestore dati            | Idataobject          | **DataHandler**                            |
| Gestore di eliminazione            | Idroptarget          | **DropHandler**                            |
| Gestore dell'icona            | IExtractIconA/W      | **IconHandler**                            |
| Gestore dell'immagine di anteprima | IThumbnailProvider   | **{E357FCCD-A995-4576-B01F-234630154E96}** |
| Gestore della finestra popup         | IQueryInfo           | **{00021500-0000-0000-C000-0000000046}** |
| Collegamento alla shell (ANSI)       | IShellLinkA          | **{000214EE-0000-0000-C000-0000000046}** |
| Collegamento alla shell (UNICODE)    | IShellLinkW          | **{000214F9-0000-0000-C000-0000000046}** |
| Archiviazione strutturata      | Istorage             | **{0000000B-0000-0000-C000-0000000046}** |
| Metadati                | IPropertySetStorage  | **PropertyHandler**                        |
| Aggiungi al menu Start       | IStartMenuPinnedList | **{a2a9545d-a0c2-42b4-9708-a0b2badd77c8}** |
| Aggiungere alla barra delle applicazioni          |                      | **{90AA3A4E-1CBA-4233-B8BB-535773D48449}** |



 

Le sottochiavi specificate per aggiungere Aggiungi  al **menu Start** e Aggiungi alla barra delle applicazioni al menu di scelta rapida di un elemento sono necessarie solo per i tipi di file che includono la [voce IsShortCut.](./links.md)

## <a name="predefined-shell-objects"></a>Oggetti shell predefiniti

Shell definisce oggetti aggiuntivi in **HKEY \_ CLASSES \_ ROOT** che possono essere estesi allo stesso modo dei tipi di file. Ad esempio, per aggiungere un gestore della finestra delle proprietà per tutti i file, è possibile eseguire la registrazione nella **sottochiave PropertySheetHandlers.**

```
HKEY_CLASSES_ROOT
   *
      shellex
         PropertySheetHandlers
```

La tabella seguente fornisce le varie sottochiavi di **HKEY \_ CLASSES \_ ROOT** in cui è possibile registrare i gestori di estensioni. Si noti che molti gestori di estensioni non possono essere registrati in tutte le sottochiavi elencate. Per altri dettagli, vedere la documentazione del gestore specifico.



| Sottochiave                    | Descrizione                                                          | Gestori possibili                                |
|---------------------------|----------------------------------------------------------------------|--------------------------------------------------|
| **\***                    | Tutti i file                                                            | Menu di scelta rapida, finestra delle proprietà, verbi (vedere di seguito) |
| **AllFileSystemObjects**  | Tutti i file e le cartelle di file                                           | Menu di scelta rapida, finestra delle proprietà, verbi             |
| **Cartella**                | Tutte le cartelle                                                          | Menu di scelta rapida, finestra delle proprietà, verbi             |
| **Directory**             | Cartelle file                                                         | Menu di scelta rapida, finestra delle proprietà, verbi             |
| **Sfondo \\ della directory** | Sfondo della cartella file                                               | Solo menu di scelta rapida                               |
| **DesktopBackground**     | Sfondo del desktop (Windows 7 e versioni successive)                            | Menu di scelta rapida, Verbi                             |
| **Unità**                 | Tutte le unità in MyComputer, ad esempio "C: \\ "                             | Menu di scelta rapida, finestra delle proprietà, verbi             |
| **Network**               | Intera rete (in Risorse di rete)                             | Menu di scelta rapida, finestra delle proprietà, verbi             |
| **Tipo di \\ rete\\\#**     | Tutti gli oggetti di tipo \# (vedere di seguito)                                   | Menu di scelta rapida, finestra delle proprietà, verbi             |
| **Netshare**              | Tutte le condivisioni di rete                                                   | Menu di scelta rapida, finestra delle proprietà, verbi             |
| **Netserver**             | Tutti i server di rete                                                  | Menu di scelta rapida, finestra delle proprietà, verbi             |
| *nome \_ del provider di \_ rete* | Tutti gli oggetti forniti dal provider di rete "*nome \_ provider di \_ rete*" | Menu di scelta rapida, finestra delle proprietà, verbi             |
| **Stampanti**              | Tutte le stampanti                                                         | Menu di scelta rapida, finestra delle proprietà                    |
| **AudioCD**               | CD audio nell'unità CD                                                 | Solo verbi                                       |
| **Dvd**                   | Unità DVD (Windows 2000)                                             | Menu di scelta rapida, finestra delle proprietà, verbi             |



 

### <a name="notes"></a>Note

-   È possibile accedere al menu di scelta rapida in background della cartella file facendo clic con il pulsante destro del mouse all'interno di una cartella di file, ma non su alcun contenuto della cartella.
-   I "verbi" sono comandi speciali registrati in **HKEY \_ CLASSES ROOT \_ Subkey** \\  \\ **Shell** \\ **Verb**.
-   Per **tipo di** \\ **rete**, " " è un codice di tipo provider di rete in formato \\ **\#** \# decimale. Il codice del tipo di provider di rete è la parola più alta di un tipo di rete. L'elenco dei tipi di rete è specificato nel file di intestazione Winnetwk.h (valori WNNC \_ \_ \* NET). Ad esempio, WNNC NET SHIVA è 0x00330000, quindi la sottochiave del tipo corrispondente sarà \_ \_ **HKEY \_ CLASSES \_ ROOT** \\ **Network** \\ **Type** \\ **51**.
-   "*network \_ provider \_ name*" è un nome di provider di rete come specificato da [**WNetGetProviderName,**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea)con gli spazi convertiti in caratteri di sottolineatura. Ad esempio, se è installato il provider di rete Microsoft Networking, il nome del provider è "Microsoft Windows Network" e il nome del *\_ provider \_* di rete corrispondente è **Microsoft Windows \_ \_ Network**.

## <a name="example-of-an-extension-handler-registration"></a>Esempio di registrazione di un gestore di estensione

Per abilitare un gestore specifico, creare una sottochiave sotto la sottochiave del tipo di gestore di estensione con il nome del gestore. La shell non usa il nome del gestore, ma deve essere diversa da tutti gli altri nomi nella sottochiave del tipo. Impostare il valore predefinito della sottochiave name sul formato stringa del GUID del gestore.

Nell'esempio seguente vengono illustrate le voci del Registro di sistema che abilitano i gestori delle estensioni del menu di scelta rapida e della finestra delle proprietà, usando un tipo di file myp di esempio.

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

### <a name="registering-shell-extension-handlers"></a>Registrazione dei gestori di estensioni della shell

La procedura di registrazione descritta in questa sezione deve essere seguita per tutti Windows sistema operativo. Tuttavia, con i sistemi successivi, potrebbe essere necessario un passaggio aggiuntivo. Poiché queste versioni successive di Windows sono progettate per essere usate in un ambiente gestito, l'accesso al Registro di sistema potrebbe essere limitato a livello amministrativo, richiedendo un approccio all'installazione leggermente diverso da quello descritto nella sezione precedente.

> [!Note]  
> I programmi di installazione in genere non devono scrivere direttamente nel Registro di sistema. Al contrario, l'installazione deve essere eseguita con Windows del programma di installazione. Questi strumenti assicurano che il software funzioni bene e fornisce l'accesso a funzionalità come la registrazione delle classi per utente.

 

I gestori delle estensioni della shell vengono eseguiti nel processo shell. Poiché si tratta di un processo di sistema, l'amministratore di un sistema può limitare i gestori  delle estensioni shell a quelli di un elenco approvato impostando il valore EnforceShellExtensionSecurity della chiave explorer su 1, come illustrato di seguito:

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

Per inserire un gestore dell'estensione shell nell'elenco approvato, creare un valore **\_ REG SZ** il cui nome è il formato stringa del GUID del gestore nella **sottochiave Approved.**

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Shell Extensions
                  Approved
```

Ad esempio, l'esempio seguente aggiunge i gestori *MyCommand* e *MyPropSheet* all'elenco approvato.

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

La shell non usa il valore assegnato al GUID, ma deve essere impostata per semplificare il controllo del Registro di sistema.

L'applicazione di installazione può aggiungere valori alla **sottochiave Approved** solo se la persona che installa l'applicazione ha privilegi sufficienti. Se il tentativo di aggiungere un gestore estensioni ha esito negativo, è necessario informare l'utente che sono necessari privilegi amministrativi per installare completamente l'applicazione. Se il gestore è essenziale per l'applicazione, è necessario non eseguire l'installazione e informare l'utente di contattare un amministratore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Inizializzazione dei gestori di estensioni della shell](int-shell-exts.md)
</dt> </dl>

 

 

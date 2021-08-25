---
description: In questo argomento viene illustrato come le applicazioni possono esporre informazioni su se stesse necessarie per abilitare determinati scenari.
ms.assetid: F88AA3E6-6F7B-442d-935A-7D2CB4958E6B
title: Registrazione dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0b9647809f46c2147ab6ed464f0e8de1d7ef0df
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122464858"
---
# <a name="application-registration"></a>Registrazione dell'applicazione

In questo argomento viene illustrato come le applicazioni possono esporre informazioni su se stesse necessarie per abilitare determinati scenari. Sono incluse le informazioni necessarie per individuare l'applicazione, i verbi supportati dall'applicazione e i tipi di file che un'applicazione può gestire.

Questo argomento è organizzato come segue:

-   [Ricerca di un eseguibile dell'applicazione](#finding-an-application-executable)
-   [Registrazione di applicazioni](#registering-applications)
    -   [Uso della sottochiave App Paths](#using-the-app-paths-subkey)
    -   [Uso della sottochiave Applications](#using-the-applications-subkey)
-   [Registrazione di verbi e altre informazioni sull'associazione di file](#registering-verbs-and-other-file-association-information)
-   [Registrazione di un tipo percepito](#registering-a-perceived-type)
-   [Argomenti correlati](#related-topics)

> [!Note]  
> Le applicazioni possono anche essere registrate nelle applicazioni del pannello di controllo Imposta accesso ai programmi e Impostazioni predefinite del computer (SPAD) e Imposta programmi predefiniti (SYDP). Per informazioni sulla registrazione di applicazioni SPAD e SYDP, vedere Linee guida per associazioni di [file](appguide-fa-defpro.md)e programmi predefiniti e Impostare l'accesso ai programmi e le impostazioni predefinite del [computer (SPAD).](cpl-setprogramaccess.md)

 

## <a name="finding-an-application-executable"></a>Ricerca di un eseguibile dell'applicazione

Quando la [**funzione ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) viene chiamata con il nome di un file eseguibile nel parametro *lpFile,* la funzione cerca il file in diverse posizioni. È consigliabile registrare l'applicazione nella **sottochiave del Registro di** sistema Percorsi app. In questo modo si evita la necessità per le applicazioni di modificare la variabile di ambiente PATH di sistema.

Il file viene cercato nei percorsi seguenti:

-   Directory di lavoro corrente
-   Solo **Windows** directory (non viene cercata alcuna sottodirectory).
-   Directory **Windows \\ System32.**
-   Directory elencate nella variabile di ambiente PATH.
-   Consigliato: **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** percorsi \\ **dell'app** \\ **CurrentVersion**

## <a name="registering-applications"></a>Registrazione di applicazioni

Entrambe **le sottochiavi del** Registro di sistema App Paths e **Applications** vengono usate per registrare e controllare il comportamento del sistema per conto delle applicazioni. La **sottochiave Percorsi** app è la posizione preferita.

### <a name="using-the-app-paths-subkey"></a>Uso della sottochiave App Paths

In Windows 7 e versioni successive è consigliabile installare le applicazioni per utente anziché per computer. Un'applicazione installata per ogni utente può essere registrata in **HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** App \\ **Paths**. Un'applicazione installata per tutti gli utenti del computer può essere registrata in **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** App \\ **Paths**.

Le voci disponibili in **Percorsi app** vengono usate principalmente per gli scopi seguenti:

-   Per eseguire il mapping del nome file eseguibile di un'applicazione al percorso completo di tale file.
-   Per pre-aggiungere informazioni alla variabile di ambiente PATH per ogni applicazione, per processo.

Se il nome di una sottochiave di **Percorsi app** corrisponde al nome del file, la shell esegue due azioni:

-   La voce (predefinita) viene usata come percorso completo del file.
-   La voce Path per tale sottochiave è precondi nuovo alla variabile di ambiente PATH del processo. Se non è obbligatorio, il valore Path può essere omesso.

I potenziali problemi da tenere presenti includono:

-   La shell limita la lunghezza di una riga di comando a MAX \_ PATH \* 2 caratteri. Se sono presenti molti file elencati come voci del Registro di sistema o i relativi percorsi sono lunghi, i nomi di file successivi nell'elenco potrebbero andare persi quando la riga di comando viene troncata.
-   Alcune applicazioni non accettano più nomi di file in una riga di comando.
-   Alcune applicazioni che accettano più nomi di file non riconoscono il formato in cui vengono forniti dalla shell. La shell fornisce l'elenco di parametri come stringa tra virgolette, ma alcune applicazioni potrebbero richiedere stringhe senza virgolette.
-   Non tutti gli elementi che possono essere trascinati fanno parte del file system; ad esempio le stampanti. Questi elementi non hanno un percorso Win32 standard, quindi non è possibile fornire un valore *lpParameters* significativo a [**ShellExecuteEx.**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)

L'uso della voce DropTarget evita questi potenziali problemi fornendo l'accesso a tutti i formati degli Appunti, inclusi [CFSTR \_ SHELLIDLIST](clipboard.md) (per elenchi di file lunghi) e [CFSTR \_ FILECONTENTS](clipboard.md) (per gli oggetti non di file system).

**Per registrare e controllare il comportamento delle applicazioni con la sottochiave Percorsi app**:

1.  Aggiungere alla sottochiave Percorsi app una sottochiave con lo stesso nome del file eseguibile, come illustrato nella voce del Registro di sistema seguente. 

    ```
    HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   App Paths
                      file.exe
                         (Default)
                         DontUseDesktopChangeRouter
                         DropTarget
                         Path
                         UseUrl
    ```

2.  Per informazioni dettagliate sulle voci della sottochiave **Percorsi app,** vedere la tabella seguente. 

    
| Voce del Registro di sistema | Dettagli | 
|----------------|---------|
| Valore predefinito. | Percorso completo dell'applicazione. Il nome dell'applicazione specificato nella voce (predefinito) può essere indicato con o senza la relativa .exe predefinita. Se necessario, la <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>funzione ShellExecuteEx</strong></a> aggiunge l'estensione durante la ricerca nella <strong>sottochiave Percorsi</strong> app. La voce è del <strong>REG_SZ</strong> specificato. | 
| DontUseDesktopChangeRouter | È obbligatorio per le applicazioni debugger per evitare deadlock della finestra di dialogo file durante il debug del Windows Explorer. L'impostazione della voce DontUseDesktopChangeRouter produce tuttavia una gestione leggermente meno efficiente delle notifiche di modifica. La voce è del <strong>tipo REG_DWORD</strong> e il valore è 0x1. | 
| DropTarget | Identificatore di classe (CLSID). La voce DropTarget contiene il CLSID di un oggetto (in genere un server locale anziché un server in-process) che implementa <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget.</strong></a> Per impostazione predefinita, quando l'obiettivo di rilascio è un file eseguibile e non viene specificato alcun valore DropTarget, la shell converte l'elenco di file eliminati in un parametro della riga di comando e lo passa a <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> tramite <em>lpParameters.</em> | 
| Percorso | Fornisce una stringa (sotto forma di elenco di directory separate da punto e virgola) da aggiungere alla variabile di ambiente PATH quando un'applicazione viene avviata chiamando <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx.</strong></a> Si tratta del percorso completo del .exe. È di <strong>REG_SZ</strong>. In <strong>Windows 7 e versioni successive</strong>il tipo può essere <strong>REG_EXPAND_SZ</strong>e in genere REG_EXPAND_SZ %ProgramFiles%. <strong></strong>    <blockquote>    [!Note]<br />    Oltre alle voci (Default), Path e DropTarget riconosciute dalla shell, un'applicazione può anche aggiungere valori personalizzati alla sottochiave <strong>Percorsi</strong> app del file eseguibile. Si consiglia agli sviluppatori di applicazioni di usare la sottochiave <strong>Percorsi</strong> app per fornire un percorso specifico dell'applicazione anziché aggiungere il percorso di sistema globale.    </blockquote><br /> | 
| SupportedProtocols | Crea una stringa che contiene gli schemi di protocollo URL per una chiave specificata. Può contenere più valori del Registro di sistema per indicare gli schemi supportati. Questa stringa segue il formato <strong>di scheme1:scheme2</strong>. Se l'elenco non è <strong>vuoto, file:</strong> verrà aggiunto alla stringa. Questo protocollo è supportato in modo implicito quando è definito <em>SupportedProtocols.</em> <br /> | 
| UseUrl | Indica che l'applicazione può accettare un URL (anziché un nome file) nella riga di comando. Le applicazioni che possono aprire documenti direttamente da Internet, ad esempio Web browser e lettori multimediali, devono impostare questa voce. <br /> Quando la <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>funzione ShellExecuteEx</strong></a> avvia un'applicazione e il valore UseUrl=1 non è impostato, <strong>ShellExecuteEx</strong> scarica il documento in un file locale e richiama il gestore sulla copia locale.<br /> Ad esempio, se nell'applicazione è impostata questa voce e un utente fa clic con il pulsante destro del mouse su un file archiviato in un server Web, il verbo Apri sarà disponibile. In caso contrario, l'utente dovrà scaricare il file e aprire la copia locale. <br /> La voce UseUrl è <strong>di REG_DWORD</strong> e il valore è 0x1.<br /> In Windows Vista e versioni precedenti questa voce indica che l'URL deve essere passato all'applicazione insieme a un nome file locale, quando viene chiamato tramite ShellExecuteEx. In Windows 7, indica che l'applicazione è in grado di comprendere qualsiasi URL HTTP o HTTPS passato, senza dover specificare anche il nome del file di cache. Questa chiave del Registro di sistema è <em>associata alla chiave SupportedProtocols.</em><br /> | 


    

     

### <a name="using-the-applications-subkey"></a>Uso della sottochiave Applications

Tramite l'inclusione di voci del Registro di sistema nella sottochiave **HKEY \_ CLASSES \_ ROOT** \\ **Applications** \\ *ApplicationName.exe,* le applicazioni possono fornire le informazioni specifiche dell'applicazione illustrate nella tabella seguente.



| Voce del Registro di sistema                   | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| verbo \\ shell                      | Fornisce il metodo verbo per chiamare l'applicazione da OpenWith. Senza una definizione di verbo specificata qui, il sistema presuppone che l'applicazione supporti [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)e passi il nome del file nella riga di comando. Questa funzionalità si applica a tutti i metodi verbo, inclusi DropTarget, ExecuteCommand e Dynamic Data Exchange (DDE).                                                                                                                                                                                                                                                                                                                            |
| DefaultIcon                      | Consente a un'applicazione di fornire un'icona specifica per rappresentare l'applicazione anziché la prima icona archiviata nel file .exe.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| FriendlyAppName                  | Consente di ottenere un nome localizzabile da visualizzare per un'applicazione anziché solo le informazioni sulla versione visualizzate, che potrebbero non essere localizzabili. La query di associazione [**ASSOCSTR legge**](/windows/desktop/api/Shlwapi/ne-shlwapi-assocstr) questo valore della voce del Registro di sistema ed esegue il falls back per usare il nome FileDescription nelle informazioni sulla versione. Se tale nome non è presente, per impostazione predefinita la query di associazione viene impostata sul nome visualizzato del file. Le applicazioni devono **utilizzare ASSOCSTR \_ FRIENDLYAPPNAME** per recuperare queste informazioni per ottenere il comportamento corretto.                                                                                                                                                                        |
| Tipi supportati                   | Elenca i tipi di file supportati dall'applicazione. In questo modo l'applicazione viene elencata nel menu a cascata della **finestra Apri con** finestra di dialogo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| NoOpenWith                       | Indica che non è specificata alcuna applicazione per l'apertura di questo tipo di file. Tenere presente che se è stata impostata una sottochiave OpenWithProgIDs per un'applicazione in base al tipo di file e la sottochiave ProgID stessa non ha una voce NoOpenWith, tale applicazione verrà visualizzata nell'elenco delle applicazioni consigliate o disponibili anche se è stata specificata la voce NoOpenWith. Per altre informazioni, vedere [How to Include an Application in the Open With Dialog Box](how-to-include-an-application-on-the-open-with-dialog-box.md) e How to exclude an Application from the Apri con Dialog [Box](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md).<br/> |
| IsHostApp                        | Indica che il processo è un processo host, ad esempio Rundll32.exe o Dllhost.exe, e non deve essere considerato per l'aggiunta o l'inclusione nel menu **Start** nell'elenco Degli elementi usati più di frequente . Quando viene avviato con un collegamento che contiene un elenco di argomenti non Null o un ID modello utente applicazione [esplicito (AppUserModelIDs),](appids.md)il processo può essere aggiunto (come tale collegamento). Questi collegamenti sono candidati per l'inclusione nell'elenco MFU.                                                                                                                                                                                                                                                  |
| NoStartPage                      | Indica che l'eseguibile dell'applicazione e i collegamenti devono essere esclusi dal menu **Start** e dall'aggiunta o inclusione nell'elenco MFU. Questa voce viene in genere usata per escludere gli strumenti di sistema, i programmi di installazione e i programmi di disinstallazione e i file Leggimi.                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| UseExecutableForTaskbarGroupIcon | Fa in modo che la barra delle applicazioni usi l'icona predefinita di questo eseguibile se non esiste alcun collegamento bloccabile per questa applicazione e invece dell'icona della finestra rilevata per la prima volta.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| TaskbarGroupIcon                 | Specifica l'icona usata per eseguire l'override dell'icona della barra delle applicazioni. L'icona della finestra viene in genere usata per la barra delle applicazioni. L'impostazione della voce TaskbarGroupIcon fa sì che il sistema usi l'icona del .exe per l'applicazione.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

### <a name="examples"></a>Esempio

Di seguito sono riportati alcuni esempi di registrazioni di applicazioni tramite la sottochiave **HKEY \_ CLASSES \_ ROOT** \\ **Applications** \\ *ApplicationName.exe.* Tutti i valori delle voci del Registro di sistema sono di tipo **\_ REG SZ,** ad eccezione di **DefaultIcon,** che è di tipo **REG EXPAND \_ \_ SZ.**

```
HKEY_CLASSES_ROOT
   Applications
      wordpad.exe
         FriendlyAppName = @%SystemRoot%\System32\shell32.dll,-22069
```

```
HKEY_CLASSES_ROOT
   Applications
      wmplayer.exe
         SupportedTypes
            .3gp2
```

```
HKEY_CLASSES_ROOT
   Applications
      wmplayer.exe
         DefaultIcon
            (Default) = %SystemRoot%\system32\wmploc.dll,-730
```

```
HKEY_CLASSES_ROOT
   Applications
      WScript.exe
         NoOpenWith
```

```
HKEY_CLASSES_ROOT
   Applications
      photoviewer.dll
         shell
            open
               DropTarget
                  Clsid = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
```

```
HKEY_CLASSES_ROOT
   Applications
      mspaint.exe
         SupportedTypes
            .bmp
            .dib
            .rle
            .jpg
            .jpeg
            .jpe
            .jfif
            .gif
            .emf
            .wmf
            .tif
            .tiff
            .png
            .ico
```

## <a name="registering-verbs-and-other-file-association-information"></a>Registrazione di verbi e altre informazioni sull'associazione di file

Le sottochiavi registrate in **HKEY \_ CLASSES \_ ROOT** \\ **SystemFileAssociations** consentono alla shell di definire il comportamento predefinito degli attributi per i tipi di file e di abilitare le associazioni di file condivise. Quando gli utenti modificano l'applicazione predefinita per un tipo di file, il ProgID della nuova applicazione predefinita ha la priorità nel fornire verbi e altre informazioni di associazione. Questa priorità è dovuta al fatto che è la prima voce nella matrice di associazione. Se il programma predefinito viene modificato, le informazioni nel ProgID precedente non sono più disponibili.

Per gestire in modo proattivo le conseguenze di una modifica ai programmi predefiniti, è possibile usare **HKEY \_ CLASSES \_ ROOT** \\ **SystemFileAssociations** per registrare verbi e altre informazioni di associazione. A causa della loro posizione dopo il ProgID nella matrice di associazione, queste registrazioni hanno una priorità più bassa. Questeregistrazioni SystemFileAssociations sono stabili anche quando gli utenti modificano i programmi predefiniti e forniscono un percorso per registrare i verbi secondari che saranno sempre disponibili per un particolare tipo di file. Per un esempio del Registro di sistema, [vedere Registrazione di un tipo percepito](#registering-a-perceived-type) più avanti in questo argomento.

L'esempio del Registro di sistema  seguente mostra cosa accade quando l'utente esegue l'elemento Programmi predefiniti in Pannello di controllo per modificare l'impostazione predefinita per i file .mp3 in App2ProgID. Dopo aver modificato l'impostazione predefinita, Verb1 non è più disponibile e Verb2 diventa l'impostazione predefinita.

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = App1ProgID
```

```
HKEY_CLASSES_ROOT
   App1ProgID
      shell
         Verb1
```

```
HKEY_CLASSES_ROOT
   App2ProgID
      shell
         Verb2
```

## <a name="registering-a-perceived-type"></a>Registrazione di un tipo percepito

I valori del Registro di sistema per i tipi percepiti sono definiti come sottochiavi della sottochiave **HKEY \_ CLASSES \_ ROOT** \\ **SystemFileAssociations** del Registro di sistema. Ad esempio, il testo del tipo **percepito** viene registrato come segue:

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      text
         shell
            edit
               command
                  (Default) = "%SystemRoot%\system32\NOTEPAD.EXE" "%1"
            open
               command
                  (Default) = "%SystemRoot%\system32\NOTEPAD.EXE" "%1"
```

Il tipo percepito di un tipo di file è indicato dall'inclusione di un valore PerceivedType nella sottochiave del tipo di file. Il valore PerceivedType viene impostato sul nome del tipo percepito registrato nella sottochiave del Registro di sistema **HKEY \_ CLASSES \_ ROOT** \\ **SystemFileAssociations,** come illustrato nell'esempio precedente del Registro di sistema. Per dichiarare i file con estensione cpp come di tipo percepito "text", ad esempio, aggiungere la voce del Registro di sistema seguente:

```
HKEY_CLASSES_ROOT
   .cpp
      PerceivedType = text
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di file](fa-file-types.md)
</dt> <dt>

[Funzionamento delle associazioni di file](fa-how-work.md)
</dt> <dt>

[Visualizzazione contenuto per tipo o tipo di file](prophand-content-view.md)
</dt> <dt>

[Verifica del tipo di file](file-type-verifier.md)
</dt> <dt>

[Gestori di tipi di file](fa-file-extensions.md)
</dt> <dt>

[Identificatori a livello di codice](fa-progids.md)
</dt> <dt>

[Tipi percepiti](fa-perceivedtypes.md)
</dt> <dt>

[Matrici di associazioni](fa-associationarray.md)
</dt> </dl>


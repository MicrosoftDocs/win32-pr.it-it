---
description: In questo argomento viene illustrato il modo in cui le applicazioni possono esporre le informazioni necessarie per abilitare determinati scenari.
ms.assetid: F88AA3E6-6F7B-442d-935A-7D2CB4958E6B
title: Registrazione dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 857e96893d2fe717f1a4939d06c77af043ead318
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966529"
---
# <a name="application-registration"></a>Registrazione dell'applicazione

In questo argomento viene illustrato il modo in cui le applicazioni possono esporre le informazioni necessarie per abilitare determinati scenari. Sono incluse le informazioni necessarie per individuare l'applicazione, i verbi supportati dall'applicazione e i tipi di file che possono essere gestiti da un'applicazione.

Questo argomento è organizzato nel modo seguente:

-   [Ricerca di un eseguibile di un'applicazione](#finding-an-application-executable)
-   [Registrazione di applicazioni](#registering-applications)
    -   [Uso della sottochiave percorsi app](#using-the-app-paths-subkey)
    -   [Uso della sottochiave Applications](#using-the-applications-subkey)
-   [Registrazione di verbi e altre informazioni sull'associazione di file](#registering-verbs-and-other-file-association-information)
-   [Registrazione di un tipo percepito](#registering-a-perceived-type)
-   [Argomenti correlati](#related-topics)

> [!Note]  
> Le applicazioni possono anche essere registrate in Imposta accesso al programma e impostazioni predefinite computer (SPAD) e impostare le applicazioni del pannello di controllo programmi predefiniti (Imposta programmi predefiniti). Per informazioni sulla registrazione dell'applicazione SPAD e imposta programmi predefiniti, vedere [linee guida per le associazioni di file e programmi predefiniti](appguide-fa-defpro.md)e [impostare l'accesso ai programmi e le impostazioni predefinite del computer (SPAD)](cpl-setprogramaccess.md).

 

## <a name="finding-an-application-executable"></a>Ricerca di un eseguibile di un'applicazione

Quando viene chiamata la funzione [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) con il nome di un file eseguibile nel parametro *lpFile* , la funzione Cerca il file in diverse posizioni. Si consiglia di registrare l'applicazione nella sottochiave del registro di sistema **percorsi app** . In questo modo si evita la necessità di modificare la variabile di ambiente percorso di sistema per le applicazioni.

Il file viene cercato nei percorsi seguenti:

-   Directory di lavoro corrente
-   Solo la directory **Windows** (nessuna sottodirectory cercata).
-   Directory **\\ System32 di Windows** .
-   Directory elencate nella variabile di ambiente PATH.
-   Consigliato: **HKEY \_ Local \_ Machine** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **App Paths**

## <a name="registering-applications"></a>Registrazione di applicazioni

Le sottochiavi del registro di sistema per le **applicazioni** e i **percorsi delle app** vengono usate per registrare e controllare il comportamento del sistema per conto delle applicazioni. La sottochiave **percorsi dell'app** è la posizione preferita.

### <a name="using-the-app-paths-subkey"></a>Uso della sottochiave percorsi app

In Windows 7 e versioni successive, si consiglia vivamente di installare le applicazioni per utente anziché per computer. Un'applicazione installata per ogni utente può essere registrata in **HKEY \_ Current \_ User** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **App Paths**. Un'applicazione installata per tutti gli utenti del computer può essere registrata in **HKEY \_ Local \_ Machine** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **App Paths**.

Le voci trovate nei **percorsi delle app** vengono usate principalmente per gli scopi seguenti:

-   Per eseguire il mapping del nome del file eseguibile di un'applicazione al percorso completo di tale file.
-   Per pre-sospendere le informazioni sulla variabile di ambiente PATH per ogni singola applicazione, per processo.

Se il nome di una sottochiave dei **percorsi dell'app** corrisponde al nome del file, la shell esegue due azioni:

-   La voce (predefinita) viene utilizzata come percorso completo del file.
-   La voce di percorso per la sottochiave è preceduto dalla variabile di ambiente PATH di tale processo. Se questa operazione non è necessaria, il valore del percorso può essere omesso.

Di seguito sono riportati i potenziali problemi da tenere presente:

-   La shell limita la lunghezza di una riga di comando al numero massimo di \_ caratteri del percorso \* 2. Se sono presenti molti file elencati come voci del registro di sistema o i relativi percorsi sono lunghi, i nomi di file più avanti nell'elenco potrebbero andare perduti perché la riga di comando è troncata.
-   Alcune applicazioni non accettano più nomi di file in una riga di comando.
-   Alcune applicazioni che accettano più nomi di file non riconoscono il formato in cui sono fornite dalla Shell. La shell fornisce l'elenco di parametri come stringa tra virgolette, ma alcune applicazioni potrebbero richiedere stringhe senza virgolette.
-   Non tutti gli elementi che possono essere trascinati fanno parte del file system; ad esempio, stampanti. Questi elementi non hanno un percorso Win32 standard, quindi non esiste alcun modo per fornire un valore *lpParameters* significativo a [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).

L'utilizzo della voce DropTarget consente di evitare questi potenziali problemi fornendo l'accesso a tutti i formati degli Appunti, inclusi [CFSTR \_ SHELLIDLIST](clipboard.md) (per gli elenchi di file lunghi) e [CFSTR \_ fileContents](clipboard.md) (per gli oggetti non di file System).

**Per registrare e controllare il comportamento delle applicazioni con la sottochiave percorsi dell'app**:

1.  Aggiungere una sottochiave con lo stesso nome del file eseguibile alla sottochiave **percorsi dell'app** , come illustrato nella voce del registro di sistema seguente.

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

2.  Per informazioni dettagliate sulle voci delle sottochiavi dei **percorsi dell'app** , vedere la tabella seguente. 

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Voce del Registro di sistema</th>
    <th>Dettagli</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Valore predefinito.</td>
    <td>È il percorso completo dell'applicazione. Il nome dell'applicazione specificato nella voce (impostazione predefinita) può essere dichiarato con o senza la relativa estensione exe. Se necessario, la funzione <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> aggiunge l'estensione durante la ricerca della sottochiave dei <strong>percorsi dell'applicazione</strong> . La voce è del tipo di <strong>REG_SZ</strong> .</td>
    </tr>
    <tr class="even">
    <td>DontUseDesktopChangeRouter</td>
    <td>È obbligatorio per le applicazioni del debugger evitare deadlock di finestra di dialogo dei file durante il debug del processo di Esplora risorse. L'impostazione della voce DontUseDesktopChangeRouter produce tuttavia una gestione leggermente meno efficiente delle notifiche di modifica. La voce è del tipo di <strong>REG_DWORD</strong> e il valore è 0x1.</td>
    </tr>
    <tr class="odd">
    <td>DropTarget</td>
    <td>È un identificatore di classe (CLSID). La voce DropTarget contiene il CLSID di un oggetto (in genere un server locale anziché un server in-process) che implementa <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a>. Per impostazione predefinita, quando l'obiettivo di rilascio è un file eseguibile e non viene specificato alcun valore di DropTarget, la Shell converte l'elenco dei file eliminati in un parametro della riga di comando e lo passa a <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> tramite <em>lpParameters</em>.</td>
    </tr>
    <tr class="even">
    <td>Percorso</td>
    <td>Fornisce una stringa (sotto forma di elenco delimitato da punti e virgola di directory) da accodare alla variabile di ambiente PATH quando viene avviata un'applicazione chiamando <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a>. Si tratta del percorso completo del file con estensione exe. È <strong>REG_SZ</strong>. In <strong>Windows 7 e versioni successive</strong>, il tipo può essere <strong>REG_EXPAND_SZ</strong>ed è in genere <strong>REG_EXPAND_SZ</strong> % ProgramFiles%.
    <blockquote>
    [!Note]<br />
Oltre alle voci (impostazione predefinita), percorso e DropTarget riconosciute dalla shell, un'applicazione può anche aggiungere valori personalizzati alla sottochiave dei <strong>percorsi delle app</strong> del file eseguibile. Si consiglia agli sviluppatori di applicazioni di usare la sottochiave <strong>percorsi app</strong> per fornire un percorso specifico dell'applicazione anziché aggiungere al percorso di sistema globale.
    </blockquote>
    <br/></td>
    </tr>
    <tr class="odd">
    <td>SupportedProtocols</td>
    <td>Crea una stringa che contiene gli schemi di protocollo URL per una chiave specificata. Può contenere più valori del registro di sistema per indicare quali schemi sono supportati. Questa stringa segue il formato di <strong>scheme1: scheme2</strong>. Se l'elenco non è vuoto, <strong>file:</strong> verrà aggiunto alla stringa. Questo protocollo è supportato in modo implicito quando viene definito <em>SupportedProtocols: Recupera</em> . <br/></td>
    </tr>
    <tr class="even">
    <td>UseUrl</td>
    <td>Indica che l'applicazione può accettare un URL, anziché un nome di file, nella riga di comando. Le applicazioni che possono aprire documenti direttamente da Internet, come browser Web e lettori multimediali, devono impostare questa voce. <br/> Quando la funzione <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> avvia un'applicazione e il valore UseUrl = 1 non è impostato, <strong>ShellExecuteEx</strong> Scarica il documento in un file locale e richiama il gestore nella copia locale.<br/> Se ad esempio l'applicazione dispone di questo set di voci e un utente fa clic con il pulsante destro del mouse su un file archiviato in un server Web, il verbo aperto verrà reso disponibile. In caso contrario, l'utente dovrà scaricare il file e aprire la copia locale. <br/> La voce UseUrl è di tipo <strong>REG_DWORD</strong> e il valore è 0x1.<br/> In Windows Vista e versioni precedenti, questa voce indica che l'URL deve essere passato all'applicazione insieme a un nome di file locale, quando viene chiamato tramite ShellExecuteEx. In Windows 7 indica che l'applicazione può comprendere qualsiasi URL http o HTTPS passato, senza dover specificare anche il nome del file di cache. Questa chiave del registro di sistema è associata alla chiave <em>SupportedProtocols: Recupera</em> .<br/></td>
    </tr>
    </tbody>
    </table>

    

     

### <a name="using-the-applications-subkey"></a>Uso della sottochiave Applications

Tramite l'inclusione delle voci del registro di sistema nelle applicazioni **\_ \_ radice delle classi HKEY** \\  \\ *ApplicationName.exe* sottochiave, le applicazioni possono fornire le informazioni specifiche dell'applicazione mostrate nella tabella seguente.



| Voce del Registro di sistema                   | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Verbo della shell \\                      | Fornisce il metodo Verb per chiamare l'applicazione da OpenWith. Senza una definizione di verbo specificata in questo punto, il sistema presuppone che l'applicazione supporti [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)e passa il nome del file nella riga di comando. Questa funzionalità si applica a tutti i metodi verb, tra cui DropTarget, ExecuteCommand e Dynamic Data Exchange (DDE).                                                                                                                                                                                                                                                                                                                            |
| DefaultIcon                      | Consente a un'applicazione di fornire un'icona specifica per rappresentare l'applicazione anziché la prima icona archiviata nel file con estensione exe.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| FriendlyAppName                  | Fornisce un modo per ottenere un nome localizzabile da visualizzare per un'applicazione anziché solo le informazioni sulla versione visualizzate, che potrebbero non essere localizzabili. La query di associazione [**ASSOCSTR**](/windows/desktop/api/Shlwapi/ne-shlwapi-assocstr) legge questo valore di voce del registro di sistema e esegue il fallback per usare il nome FileDescription nelle informazioni sulla versione. Se tale nome non è presente, per impostazione predefinita la query di associazione corrisponde al nome visualizzato del file. Le applicazioni devono usare **ASSOCSTR \_ FRIENDLYAPPNAME** per recuperare queste informazioni per ottenere il comportamento appropriato.                                                                                                                                                                        |
| SupportedTypes                   | Elenca i tipi di file supportati dall'applicazione. Questa operazione consente di elencare l'applicazione nel menu a cascata della finestra di dialogo **Apri con** .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| NoOpenWith                       | Indica che per l'apertura di questo tipo di file non è specificata alcuna applicazione. Tenere presente che se è stata impostata una sottochiave OpenWithProgIDs per un'applicazione in base al tipo di file e la sottochiave ProgID stessa non ha anche una voce NoOpenWith, l'applicazione verrà visualizzata nell'elenco delle applicazioni consigliate o disponibili anche se ha specificato la voce NoOpenWith. Per ulteriori informazioni, vedere [come includere un'applicazione nella finestra di dialogo Apri con](how-to-include-an-application-on-the-open-with-dialog-box.md) e [come escludere un'applicazione dalla finestra di dialogo Apri con](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md).<br/> |
| IsHostApp                        | Indica che il processo è un processo host, ad esempio Rundll32.exe o Dllhost.exe, e non deve essere preso in considerazione per l'aggiunta o l'inclusione del menu **Start** nell'elenco usato più di frequente (MFU). Quando viene avviato con un collegamento che contiene un elenco di argomenti non null o un [ID del modello utente dell'applicazione esplicito (AppUserModelIDs)](appids.md), il processo può essere aggiunto (come tale collegamento). Questi tasti di scelta rapida sono candidati per l'inclusione nell'elenco MFU.                                                                                                                                                                                                                                                  |
| NoStartPage                      | Indica che l'eseguibile dell'applicazione e i collegamenti devono essere esclusi dal menu **Start** e dall'aggiunta o dall'inclusione nell'elenco MFU. Questa voce viene in genere usata per escludere gli strumenti di sistema, i programmi di installazione e i programmi di disinstallazione e i file Leggimi.                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| UseExecutableForTaskbarGroupIcon | Fa in modo che la barra delle applicazioni usi l'icona predefinita di questo eseguibile se non è presente alcun collegamento aggiungibili per questa applicazione e invece dell'icona della finestra che è stata rilevata per la prima volta.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| TaskbarGroupIcon                 | Specifica l'icona utilizzata per eseguire l'override dell'icona della barra delle applicazioni. L'icona della finestra viene in genere utilizzata per la barra delle applicazioni. Se si imposta la voce TaskbarGroupIcon, il sistema utilizzerà invece l'icona del file exe per l'applicazione.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

### <a name="examples"></a>Esempio

Di seguito sono riportati alcuni esempi di registrazioni di applicazioni tramite le applicazioni **\_ \_ radice delle classi HKEY** \\  \\ *ApplicationName.exe* sottochiave. Tutti i valori delle voci del registro di sistema sono di tipo **reg \_ SZ** , ad eccezione di **DefaultIcon** , che è di tipo **reg \_ expand \_ SZ** .

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

Le sottochiavi registrate **nelle \_ classi HKEY \_ radice** \\ **SystemFileAssociations** consentono alla shell di definire il comportamento predefinito degli attributi per i tipi di file e di abilitare le associazioni di file condivisi. Quando gli utenti modificano l'applicazione predefinita per un tipo di file, il ProgID della nuova applicazione predefinita ha la priorità per fornire verbi e altre informazioni di associazione. Questa priorità è dovuta al fatto che è la prima voce nella matrice di associazioni. Se il programma predefinito viene modificato, le informazioni contenute nel ProgID precedente non sono più disponibili.

Per gestire in modo proattivo le conseguenze di una modifica ai programmi predefiniti, è possibile usare **\_ le classi HKEY \_ radice** \\ **SystemFileAssociations** per registrare i verbi e altre informazioni di associazione. A causa della loro posizione dopo il ProgID nell'array di associazioni, queste registrazioni hanno una priorità inferiore. Questi SystemFileAssociationsregistrations sono stabili anche quando gli utenti modificano i programmi predefiniti e forniscono un percorso per registrare i verbi secondari che saranno sempre disponibili per un determinato tipo di file. Per un esempio di registro, vedere [registrazione di un tipo percepito](#registering-a-perceived-type) più avanti in questo argomento.

Nell'esempio di registro di sistema seguente viene illustrato cosa accade quando l'utente esegue l'elemento **programmi predefiniti** nel pannello di controllo per modificare il valore predefinito per i file con estensione MP3 in App2ProgID. Dopo aver modificato l'impostazione predefinita, Verb1 non è più disponibile e Verb2 diventa il valore predefinito.

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

I valori del registro di sistema per i tipi percepiti vengono definiti come sottochiavi della sottochiave del registro di sistema **HKEY delle \_ classi \_ radice** \\ **SystemFileAssociations** Il **testo** del tipo percepito, ad esempio, viene registrato come segue:

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

Il tipo percepito di un tipo di file è indicato includendo un valore PerceivedType nella sottochiave del tipo di file. Il valore PerceivedType è impostato sul nome del tipo percepito registrato nella sottochiave del registro di sistema **HKEY \_ classi \_ radice** \\ **SystemFileAssociations** , come illustrato nell'esempio di registro di sistema precedente. Per dichiarare i file con estensione cpp come di tipo "Text" percepito, ad esempio, aggiungere la seguente voce del registro di sistema:

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

[Visualizzazione contenuto per tipo di file o tipo](prophand-content-view.md)
</dt> <dt>

[Tipo di file Verifier](file-type-verifier.md)
</dt> <dt>

[Gestori di tipi di file](fa-file-extensions.md)
</dt> <dt>

[Identificatori a livello di codice](fa-progids.md)
</dt> <dt>

[Tipi percepiti](fa-perceivedtypes.md)
</dt> <dt>

[Matrici di associazione](fa-associationarray.md)
</dt> </dl>


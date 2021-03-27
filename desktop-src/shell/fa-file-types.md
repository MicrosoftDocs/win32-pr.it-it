---
description: Questo argomento illustra come creare nuovi tipi di file e come associare l'app al tipo di file e ad altri tipi di file ben definiti.
ms.assetid: 055648cd-46ce-4e61-80b2-bcf1d1823e20
title: Tipi di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d697c42626c6e1ab3e0b5cc0b88bd065523d53a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979743"
---
# <a name="file-types"></a>Tipi di file

Questo argomento illustra come creare nuovi tipi di file e come associare l'app al tipo di file e ad altri tipi di file ben definiti. I file con un'estensione del nome file comune condivisa (doc, HTML e così via) sono dello stesso *tipo*. Se ad esempio si crea un nuovo editor di testo, è possibile usare il tipo di file con estensione txt esistente. In altri casi, potrebbe essere necessario creare un nuovo tipo di file.

Questo argomento è organizzato nel modo seguente:

-   [Tipi di file pubblici e privati](#public-and-private-file-types)
-   [Registrazione di un tipo di file](#registering-a-file-type)
    -   [Impostazione degli attributi facoltativi delle sottochiavi e dell'estensione del tipo di file](#setting-optional-subkeys-and-file-type-extension-attributes)
    -   [Eliminazione delle informazioni del registro di sistema durante la disinstallazione](#deleting-registry-information-during-uninstallation)
-   [Tipi di file che supportano i metadati aperti](#file-types-that-support-open-metadata)
-   [Argomenti correlati](#related-topics)

Ulteriori informazioni sono disponibili negli argomenti seguenti:

-   [Come scegliere un'estensione del tipo di file](how-to-choose-a-file-type-extension.md)
-   [Come definire gli attributi del tipo di file](./how-to-define-file-type-attributes.md)
-   [Come includere un'applicazione nella finestra di dialogo Apri con](how-to-include-an-application-on-the-open-with-dialog-box.md)
-   [Come escludere un'applicazione dalla finestra di dialogo Apri con per i tipi di file non associati](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md)

## <a name="public-and-private-file-types"></a>Tipi di file pubblici e privati

I tipi di file pubblici sono noti anche come tipi più diffusi o controversi perché le applicazioni in competizione potrebbero voler essere associate a questi tipi di file. Le caratteristiche dei tipi di file pubblici includono:

-   Vengono in genere definiti da corpi di standard e/o vengono promossi dalle organizzazioni che lo definiscono come formati di interscambio.
-   Spesso vengono scambiati tra computer e utenti per diversi scopi.
-   Devono essere supportate su molte piattaforme diverse.
-   È probabile che le applicazioni di più fornitori li gestiscano.

Alcuni esempi di tipi di file che sono considerati pubblici sono i tipi di file immagine. png,. gif,. jpg e. bmp e i tipi audio. wav,. mp3 e. au.

A differenza dei tipi di file pubblici, i tipi di file privati o proprietari hanno in genere un formato implementato e compreso da una sola applicazione o fornitore. Di conseguenza, i tipi di file privati in genere non sono soggetti a conflitti tra le applicazioni. Alcuni tipi di file possono essere avviati come tipi di file privati, ma in seguito diventano tipi di file pubblici.

> [!Note]  
> Windows non distingue tra i tipi di file pubblici e privati. La distinzione è rilevante solo per prendere decisioni sulla scelta della registrazione del tipo di file.

 

## <a name="registering-a-file-type"></a>Registrazione di un tipo di file

Per associare il tipo di file a un'applicazione esistente, individuare il ProgID dell'applicazione nel registro di sistema. Per associare il tipo di file a una nuova applicazione, definire un ProgID per l'applicazione. Per informazioni sulla definizione di un nuovo ProgID, vedere [identificatori a livello di codice](fa-progids.md).

Le sottochiavi di estensione del nome file hanno il formato generale seguente: *estensione* = *ProgID*. Le sottochiavi dell'estensione del nome file sono archiviate nel sottoalbero **\_ \_ radice delle classi HKEY** .

Quando si creano sottochiavi di tipo file nel registro di sistema, è importante includere il punto principale (.). Ad esempio, se si desidera che un tipo di file con estensione. MYP e il file con estensione MYP lungo da aprire con un'applicazione denominata programma, utilizzare la sintassi seguente:

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = ApplicationVendor.MyProgram
   .myp-file
      (Default) = ApplicationVendor.MyProgram
   ApplicationVendor.MyProgram
      (Default) = MyProgram Application
```

Come illustrato nell'esempio precedente, se si registra anche un'estensione di file breve (MYP), è necessario creare una sottochiave per l'estensione lunga (file con estensione MYP). Per altre informazioni, vedere [gestori di tipi di file](fa-file-extensions.md).

### <a name="setting-optional-subkeys-and-file-type-extension-attributes"></a>Impostazione degli attributi facoltativi delle sottochiavi e dell'estensione del tipo di file

Le voci dell'estensione del tipo di file nel registro di sistema includono diverse sottochiavi e attributi facoltativi.

Nella tabella seguente vengono descritte le voci dell'estensione del tipo di file utilizzate dalle associazioni di file. Tutti i valori sono di tipo **reg \_ SZ** .



| Voce del Registro di sistema  | Azione                                                                                                                                                                                                                                                                                                                             |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Predefinito         | Impostare il valore predefinito della sottochiave Extension sul ProgID a cui è collegato.                                                                                                                                                                                                                                                 |
| Tipo di contenuto    | Impostare il valore del tipo di contenuto sul tipo di contenuto MIME del tipo di file.                                                                                                                                                                                                                                                                   |
| OpenWithList    | Non usare. Questa sottochiave contiene una o più sottochiavi dell'applicazione per le applicazioni visualizzate nella voce della finestra di dialogo **Apri con** per il tipo di file ed è destinata solo alle applicazioni exe nei sistemi operativi precedenti a Windows XP. In alternativa, usare OpenWithProgIds.                                                            |
| OpenWithProgIds | Questa sottochiave contiene un elenco di ProgID alternativi per questo tipo di file. I programmi per questi ProgID vengono visualizzati nel menu **Apri con** e sono disponibili come app di Windows Store predefinite per il tipo di file. Ogni volta che un'applicazione acquisisce questo tipo di file modificando il valore predefinito, deve aggiungere anche una voce a questo elenco. |
| PerceivedType   | Impostare il valore PerceivedType su PerceivedType a cui appartiene il file, se disponibile. Questa stringa non viene utilizzata dalle versioni di Windows precedenti a Windows Vista. Per ulteriori informazioni, vedere la pagina relativa alla [registrazione delle applicazioni e dei tipi percepiti](fa-perceivedtypes.md).                                                                           |



 

Il formato generale di una sottochiave di estensione del nome file è il seguente. Tutti i tipi di voce sono di tipo **reg \_ SZ** .

```
HKEY_CLASSES_ROOT
   .ext
      (Default) = ProgID.ext.1
      Content Type = MIME content type
      PerceivedType = PerceivedType
      OpenWithProgids
         ProgID2.ext.1
         ProgID3.ext.1
      ProgID.ext.1
         shellnew
```

Importanti considerazioni sui tipi di file includono:

-   Il sottoalbero **\_ \_ radice delle classi HKEY** è una visualizzazione formata unendo le classi software **\_ \_ dell'utente corrente di HKEY** \\  \\  e le classi software **\_ del \_ computer locale HKEY** \\  \\ 
-   In generale, **la \_ \_ radice delle classi HKEY** è destinata a essere letta da ma non scritta. Per altre informazioni, vedere l' [articolo \_ \_ radice delle classi HKEY](../sysinfo/hkey-classes-root-key.md) .
-   Per registrare un tipo di file a livello globale in un determinato computer, creare una voce per il tipo di file nella **\_ \_** \\  \\ sottochiave **classi** software del computer locale HKEY.
-   Per rendere visibile la registrazione di un tipo di file solo all'utente corrente, creare una voce per il tipo di file nella sottochiave classi software **\_ \_ dell'utente corrente di HKEY** \\  \\  .
-   Un'applicazione può fornire la propria implementazione di un verbo, ad esempio Open o Play, come illustrato nell'esempio di registro di sistema seguente.

    ```
    HKEY_CLASSES_ROOT
       Applications
          ApplicationName.exe
             shell
                verb
    ```

    Le sottochiavi della sottochiave del verbo includono la riga di comando e il metodo Drop target: **Command** e **DropTarget**.

-   Quando si crea o si modifica un'associazione di file, è importante notificare al sistema che è stata apportata una modifica. Eseguire questa operazione chiamando [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) e specificando l'evento **SHCNE \_ ASSOCCHANGED** . Se non si chiama **SHChangeNotify**, è possibile che la modifica non venga riconosciuta fino al riavvio del sistema.
-   Per recuperare le informazioni del registro di sistema relative a un'associazione di file, utilizzare l'interfaccia [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) . Per uno scenario che illustra questa procedura, vedere [scenario di esempio di associazione di file](fa-sample-scenarios.md).

> [!Note]  
> Le sottochiavi del registro di sistema per le **applicazioni** e i **percorsi delle app** vengono usate per registrare e controllare il comportamento del sistema per conto delle applicazioni. Per informazioni più dettagliate su questa funzionalità, vedere [registrazione dell'applicazione](app-registration.md).

 

### <a name="deleting-registry-information-during-uninstallation"></a>Eliminazione delle informazioni del registro di sistema durante la disinstallazione

Quando si disinstalla un'applicazione, i ProgID e la maggior parte delle altre informazioni di registro associate a tale applicazione devono essere eliminati come parte della disinstallazione. Tuttavia, le applicazioni che hanno assunto la proprietà di un tipo di file (impostando il valore predefinito della sottochiave **\_ \_ radice**. Extension del tipo di file Hkey \\  per il ProgID dell'applicazione) non devono tentare di rimuovere tale valore durante la disinstallazione. Se si lasciano i dati per il valore predefinito, si evita la difficoltà di determinare se un'altra applicazione ha assunto la proprietà del tipo di file e sovrascritto il valore predefinito dopo l'installazione dell'applicazione originale. Windows rispetta il valore predefinito solo se il ProgID individuato è un ProgID registrato. Se il ProgID viene annullata, viene ignorato.

Si noti che altre informazioni sulla proprietà dei tipi di file vengono archiviate nel sottoalbero dell' **\_ \_ utente corrente di HKEY** e vengono usate solo quando l'applicazione a cui fa riferimento è registrata. Pertanto, questi dati non devono essere rimossi durante la disinstallazione di un'applicazione.

Come esempio, di seguito viene illustrato lo stato del registro di sistema prima della disinstallazione di un'applicazione:

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = YourProgID
   YourProgID
      shell
         open
            command
               (Default) = yourapp.exe %1
```

Di seguito viene illustrato lo stato delle stesse voci del registro di sistema dopo la disinstallazione dell'applicazione.

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = YourProgID
   YourProgID subkey removed
```

## <a name="file-types-that-support-open-metadata"></a>Tipi di file che supportano i metadati aperti

In Windows 7 e versioni successive, i tipi di file seguenti supportano i metadati aperti.



| Tipo file                                                               | Estensioni di file                                          |
|-------------------------------------------------------------------------|---------------------------------------------------------------|
| Documenti di Office 2007                                                   | . docx,. xlsx,. pptx                                           |
| Documenti di Office 97-2003                                                | DOC, xls, PPT                                              |
| Ricerca salvata                                                            | . search-ms                                                    |
| Formati basati su Windows Media (contenitore ASF (Advanced Streaming Format) | . wmv,. WMA                                                    |
| MP4 (gestore proprietà)                                                  | . MP4,. m4a,. m4v,. mp4v,. M4P,. m4b,. 3GP,. 3GPP,. 3gp2,. MOV |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione dell'applicazione](app-registration.md)
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

 

 

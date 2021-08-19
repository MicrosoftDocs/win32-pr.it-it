---
description: Questo argomento illustra come creare nuovi tipi di file e come associare l'app al tipo di file e ad altri tipi di file ben definiti.
ms.assetid: 055648cd-46ce-4e61-80b2-bcf1d1823e20
title: Tipi di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 541e6068237b504ea8c9faf06e2083986ed5bb48a7c16dabb82e5096569d9f17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094206"
---
# <a name="file-types"></a>Tipi di file

Questo argomento illustra come creare nuovi tipi di file e come associare l'app al tipo di file e ad altri tipi di file ben definiti. I file con un'estensione di file comune condivisa (.doc, .html e così via) sono dello stesso *tipo.* Ad esempio, se si crea un nuovo editor di testo, è possibile usare il tipo di file .txt esistente. In altri casi, potrebbe essere necessario creare un nuovo tipo di file.

Questo argomento è organizzato come segue:

-   [Tipi di file pubblici e privati](#public-and-private-file-types)
-   [Registrazione di un tipo di file](#registering-a-file-type)
    -   [Impostazione di sottochiavi facoltative e attributi di estensione del tipo di file](#setting-optional-subkeys-and-file-type-extension-attributes)
    -   [Eliminazione delle informazioni del Registro di sistema durante la disinstallazione](#deleting-registry-information-during-uninstallation)
-   [Tipi di file che supportano metadati aperti](#file-types-that-support-open-metadata)
-   [Argomenti correlati](#related-topics)

Altre informazioni sono disponibili negli argomenti seguenti:

-   [Come scegliere un'estensione del tipo di file](how-to-choose-a-file-type-extension.md)
-   [Come definire gli attributi del tipo di file](./how-to-define-file-type-attributes.md)
-   [Come includere un'applicazione nella Apri con finestra di dialogo](how-to-include-an-application-on-the-open-with-dialog-box.md)
-   [Come escludere un'applicazione dalla finestra Apri con per i tipi di file nonssociati](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md)

## <a name="public-and-private-file-types"></a>Tipi di file pubblici e privati

I tipi di file pubblici sono noti anche come tipi comuni o conditi perché le applicazioni concorrenti potrebbero voler essere associate a questi tipi di file. Le caratteristiche dei tipi di file pubblici includono:

-   Sono in genere definiti dagli enti standard e/o vengono promossi dalle organizzazioni che definiscono come formati di interscambio.
-   Vengono spesso s scambiate tra computer e utenti per scopi diversi.
-   Devono essere supportati in molte piattaforme diverse.
-   È probabile che le applicazioni di più fornitori le gestiranno.

Alcuni esempi di tipi di file considerati pubblici sono i tipi di file immagine .png, .gif, .jpg e .bmp e i tipi audio wav, .mp3 e au.

A differenza dei tipi di file pubblici, i tipi di file privati o proprietari hanno in genere un formato implementato e compreso da una sola applicazione o fornitore. Di conseguenza, i tipi di file privati non sono in genere inclini a conflitti tra le applicazioni. Alcuni tipi di file possono iniziare come tipi di file privati, ma in un secondo momento diventano tipi di file pubblici.

> [!Note]  
> Windows non fa distinzione tra tipi di file pubblici e privati. La distinzione è rilevante solo per prendere decisioni sulla scelta della registrazione del tipo di file.

 

## <a name="registering-a-file-type"></a>Registrazione di un tipo di file

Per associare il tipo di file a un'applicazione esistente, individuare il ProgID dell'applicazione nel Registro di sistema. Per associare il tipo di file a una nuova applicazione, definire un ProgID per l'applicazione. Per informazioni sulla definizione di un nuovo ProgID, vedere [Identificatori a livello di codice.](fa-progids.md)

Le sottochiavi dell'estensione di file hanno il formato generale seguente: *estensione* = *ProgID*. Le sottochiavi dell'estensione di file vengono archiviate nel sottoalbero **HKEY \_ CLASSES \_ ROOT.**

È importante includere il punto iniziale (.) quando si creano sottochiavi del tipo di file nel Registro di sistema. Ad esempio, se si vuole aprire un tipo di file con estensione .myp breve e l'estensione lunga .myp-file con un'applicazione denominata MyProgram, usare la sintassi seguente:

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = ApplicationVendor.MyProgram
   .myp-file
      (Default) = ApplicationVendor.MyProgram
   ApplicationVendor.MyProgram
      (Default) = MyProgram Application
```

Come illustrato nell'esempio precedente, se si registra anche un'estensione di file breve (myp), è necessario creare anche una sottochiave per l'estensione lunga (file con estensione myp). Per altre informazioni, vedere [Gestori dei tipi di file](fa-file-extensions.md).

### <a name="setting-optional-subkeys-and-file-type-extension-attributes"></a>Impostazione di sottochiavi facoltative e attributi di estensione del tipo di file

Le voci di estensione del tipo di file nel Registro di sistema hanno diverse sottochiavi e attributi facoltativi.

Le voci di estensione del tipo di file usate dalle associazioni di file sono descritte nella tabella seguente. Tutti i valori sono di **tipo \_ REG SZ.**



| Voce del Registro di sistema  | Azione                                                                                                                                                                                                                                                                                                                             |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Predefinito         | Impostare il valore predefinito della sottochiave dell'estensione sul ProgID a cui è collegata.                                                                                                                                                                                                                                                 |
| Tipo di contenuto    | Impostare il valore Tipo di contenuto sul tipo di contenuto MIME del tipo di file.                                                                                                                                                                                                                                                                   |
| OpenWithList    | Non usare. Questa sottochiave contiene una o più sottochiavi dell'applicazione per le applicazioni visualizzate nella voce della finestra di dialogo Apri con per il tipo di file ed è destinata solo alle applicazioni .exe nei sistemi operativi precedenti a **Windows** XP. In alternativa, usare OpenWithProgIds.                                                            |
| OpenWithProgIds | Questa sottochiave contiene un elenco di ProgID alternativi per questo tipo di file. I programmi per questi ProgID vengono visualizzati nel menu **Apri con** e sono disponibili come app predefinite Windows Store per il tipo di file. Ogni volta che un'applicazione assume il controllo di questo tipo di file modificando il valore predefinito, deve anche aggiungere una voce a questo elenco. |
| PerceivedType   | Impostare il valore PerceivedType su PerceivedType a cui appartiene il file, se presente. Questa stringa non viene usata dalle Windows precedenti a Windows Vista. Per altre informazioni, vedere [Tipi percepiti e Registrazione dell'applicazione.](fa-perceivedtypes.md)                                                                           |



 

La forma generale di una sottochiave dell'estensione di file è la seguente. Tutti i tipi di voce sono di **tipo \_ REG SZ.**

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

Considerazioni importanti sui tipi di file includono:

-   Il sottoalbero **HKEY \_ CLASSES \_ ROOT** è una vista formata unendo le classi software **HKEY \_ CURRENT \_ USER** e \\  \\  **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Classes**
-   In generale, **HKEY \_ CLASSES \_ ROOT** deve essere letto ma non scritto in . Per altre informazioni, vedere [l'articolo HKEY \_ CLASSES \_ ROOT.](../sysinfo/hkey-classes-root-key.md)
-   Per registrare un tipo di file a livello globale in un computer specifico, creare una voce per il tipo di file nella **sottochiave \_ HKEY LOCAL \_ MACHINE** \\ **Software** \\ **Classes.**
-   Per rendere visibile la registrazione di un tipo di file solo per l'utente corrente, creare una voce per il tipo di file nella **sottochiave \_ HKEY CURRENT \_ USER** \\ **Software** \\ **Classes.**
-   Un'applicazione può fornire la propria implementazione di un verbo, ad esempio open o play, come illustrato nell'esempio del Registro di sistema seguente.

    ```
    HKEY_CLASSES_ROOT
       Applications
          ApplicationName.exe
             shell
                verb
    ```

    Le sottochiavi della sottochiave del verbo includono la riga di comando e il metodo drop target: **command** e **DropTarget**.

-   Quando si crea o si modifica un'associazione di file, è importante notificare al sistema che è stata apportata una modifica. A tale scopo, chiamare [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) e specificare **l'evento SHCNE \_ ASSOCCHANGED.** Se non si chiama **SHChangeNotify**, la modifica potrebbe non essere riconosciuta fino al riavvio del sistema.
-   Per recuperare le informazioni del Registro di sistema relative a un'associazione di file, usare [**l'interfaccia IQueryAssociations.**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) Per uno scenario che illustra questa procedura, vedere [Scenario di esempio di associazione file](fa-sample-scenarios.md).

> [!Note]  
> Le **sottochiavi del Registro di** sistema **Percorsi** app e Applicazioni vengono usate per registrare e controllare il comportamento del sistema per conto delle applicazioni. Per informazioni più dettagliate su questa funzionalità, vedere [Registrazione dell'applicazione](app-registration.md).

 

### <a name="deleting-registry-information-during-uninstallation"></a>Eliminazione delle informazioni del Registro di sistema durante la disinstallazione

Quando si disinstalla un'applicazione, i ProgID e la maggior parte delle altre informazioni del Registro di sistema associate a tale applicazione devono essere eliminati come parte della disinstallazione. Tuttavia, le applicazioni che hanno assunto la proprietà di un tipo di file (impostando il valore predefinito della sottochiave **HKEY \_ CLASSES \_ ROOT**.extension del tipo di file sul ProgID dell'applicazione) non devono tentare di rimuovere tale valore durante la \\  disinstallazione. Lasciare i dati sul posto per il valore Predefinito evita la difficoltà di determinare se un'altra applicazione ha assunto la proprietà del tipo di file e ha sovrascritto il valore Predefinito dopo l'installazione dell'applicazione originale. Windows rispetta il valore Predefinito solo se progID rilevato è un ProgID registrato. Se la registrazione di ProgID viene annullata, viene ignorata.

Si noti che altre informazioni sulla proprietà del tipo di file vengono archiviate nel sottoalbero **HKEY \_ CURRENT \_ USER** e vengono usate solo quando l'applicazione a cui fa riferimento è registrata. Pertanto, non è necessario rimuovere questi dati durante la disinstallazione di un'applicazione.

Ad esempio, di seguito viene illustrato lo stato del Registro di sistema prima della disinstallazione di un'applicazione:

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

Di seguito viene illustrato lo stato delle stesse voci del Registro di sistema dopo la disinstallazione dell'applicazione.

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = YourProgID
   YourProgID subkey removed
```

## <a name="file-types-that-support-open-metadata"></a>Tipi di file che supportano metadati aperti

In Windows 7 e versioni successive, i tipi di file seguenti supportano i metadati aperti.



| Tipo file                                                               | Estensioni dei nomi di file                                          |
|-------------------------------------------------------------------------|---------------------------------------------------------------|
| Office 2007 Documents                                                   | .docx, .xlsx, .pptx                                           |
| Office 97-2003 Documenti                                                | .doc, .xls, .ppt                                              |
| Ricerca salvata                                                            | .search-ms                                                    |
| Windows Formati basati su file multimediali (contenitore ASF (Advanced Streaming Format) | .wmv, .wma                                                    |
| MP4 (gestore delle proprietà)                                                  | .mp4, .m4a, .m4v, .mp4v, .m4p, .m4b, .3gp, .3gpp, .3gp2, .mov |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione dell'applicazione](app-registration.md)
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

 

 

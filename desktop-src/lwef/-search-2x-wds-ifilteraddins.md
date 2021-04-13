---
title: Sviluppo di componenti aggiuntivi IFilter
description: È possibile estendere Microsoft Windows Desktop Search (WDS) con i componenti aggiuntivi di filtro, i componenti che implementano IFilterinterface, per includere nuovi tipi di file.
ms.assetid: 71dd515d-a73e-4e0a-b0da-c8a6209d09fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79f846cf2101eefc17b1e92fbd7992529a06fb43
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104473027"
---
# <a name="developing-ifilter-add-ins"></a>Sviluppo di componenti aggiuntivi IFilter

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [Windows Search](../search/-search-3x-wds-overview.md) .

È possibile estendere Microsoft Windows Desktop Search (WDS) con i componenti aggiuntivi di filtro, i componenti che implementano l'interfaccia [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter), per includere nuovi tipi di file. I filtri sono responsabili dell'accesso e dell'analisi dei dati nei file e della restituzione di coppie di proprietà e valori, nonché di blocchi di testo per l'indicizzazione. Durante il processo di indicizzazione, WDS chiama il filtro appropriato con l'URL per ogni file o elemento. Il filtro estrae prima i metadati che corrispondono alle proprietà contrassegnate come recuperabili nello schema WDS, ad esempio titolo, dimensioni del file e data dell'Ultima modifica. Quindi suddivide il contenuto dell'elemento in blocchi di testo. WDS aggiunge le proprietà e il testo restituiti dal filtro al catalogo. WDS può indicizzare qualsiasi tipo di file per il quale è presente un filtro registrato.

In alcuni casi, non è necessario scrivere un nuovo filtro. WDS 2. x contiene filtri per più di 200 tipi di elementi (inclusi elementi di testo non crittografato, ad esempio HTML, XML e file di codice sorgente) e utilizza la stessa tecnologia [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)di SharePoint Services. Se i filtri sono già installati per i tipi di file, WDS può utilizzare i filtri esistenti per indicizzare i dati. WDS include inoltre un filtro generale per i tipi di file basati su testo normale. Se si dispone di un tipo di file che può essere elaborato da un filtro SharePoint Services esistente o dal filtro testo non crittografato, è possibile aggiungere l'estensione del nome file e il GUID filtro al registro di sistema in modo che WDS possa individuarlo e usarlo (vedere [per registrare un componente aggiuntivo di filtro](#to-register-a-filter-add-in) per ulteriori informazioni).

Se, tuttavia, si dispone di un formato di file o di dati non crittografato e proprietario, la scrittura di un'implementazione di filtro personalizzata è l'unico modo per garantire che WDS possa indicizzare il formato di file nel catalogo. È possibile disporre di un solo componente aggiuntivo di filtro per un tipo di file, pertanto è possibile eseguire l'override di un filtro esistente o di un altro filtro per un tipo di file specifico.

Questa sezione contiene i seguenti argomenti:

-   [Interfacce di filtro obbligatorie](#required-filter-interfaces)
    -   [Interfaccia IFilter](#ifilter-interface)
    -   [IPersistStream](#ipersiststream)
    -   [IPersistFile](#ipersistfile)
    -   [IPersistStorage](#ipersiststorage)
-   [Output delle proprietà con i filtri](#outputting-properties-with-filters)
    -   [Valori delle proprietà](#property-values)
-   [Filtra installazione del componente aggiuntivo](#filter-add-in-installation)
    -   [CLSID necessari per la registrazione](#clsids-required-for-registration)
    -   [Modello di registrazione](#registration-model)
    -   [Per registrare un componente aggiuntivo di filtro](#to-register-a-filter-add-in)
-   [Argomenti correlati](#related-topics)

## <a name="required-filter-interfaces"></a>Interfacce di filtro obbligatorie

Un componente aggiuntivo di filtro deve implementare l'interfaccia [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)e una delle interfacce seguenti:

-   [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) : per caricare i dati da un flusso. Questa operazione è più sicura dell'uso dei file perché non viene scritto alcun elemento sul disco. L'interfaccia IPersistStream è il metodo preferito per la compatibilità con le edizioni di Windows Vista.
-   [Interfaccia IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) : per caricare i dati da un file. Questa interfaccia non è supportata in Windows Vista.
-   [Interfaccia IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) : per caricare dati da un archivio strutturato OLE com.

Un componente aggiuntivo di filtro usa queste interfacce per ottenere il contenuto dell'elemento e restituirle in modo iterativo all'indice fino a quando non viene raggiunta la fine del file. Un componente aggiuntivo di filtro dovrebbe essere il più possibile affidabile per gestire i file danneggiati e quelli che non soddisfano i formati di input previsti.

### <a name="ifilter-interface"></a>Interfaccia IFilter

Si tratta di un'interfaccia necessaria per l'implementazione di un filtro. Per ulteriori informazioni, vedere la Guida di riferimento all'interfaccia [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter).



| Metodo       | Descrizione                                                                            |
|--------------|----------------------------------------------------------------------------------------|
| Init ()       | Inizializza una sessione di filtro.                                                       |
| GetChunk ()   | Posiziona il filtro all'inizio del blocco primo o successivo e restituisce un descrittore. |
| GetText ()    | Recupera il testo dal blocco corrente.                                                 |
| GetValue()   | Recupera i valori delle proprietà dal blocco corrente.                                      |
| BindRegion() | Attualmente riservata per uso interno; non implementare. Questo metodo restituisce E \_ NOTIMPL. |



 

### <a name="ipersiststream"></a>IPersistStream

Questa interfaccia carica un file da un flusso per un'elaborazione più sicura rispetto all' [interfaccia IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) perché il contesto in cui viene eseguito un filtro [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) non necessita dei diritti per aprire i file sul disco o sulla rete. Dei due metodi per l'accesso a un singolo file, si tratta del metodo preferito per la compatibilità con le edizioni di Windows.



| Metodo       | Descrizione                                                                                                                                        |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| IsDirty ()    | Verifica se è stata apportata una modifica. Questo metodo restituisce E \_ NOTIMPL nei filtri.                                                                      |
| InitNew ()    | Crea una nuova risorsa di archiviazione. Questo metodo restituisce E \_ NOTIMPL nei filtri.                                                                                  |
| Carica ()       | Inizializza un oggetto dal flusso in cui è stato salvato in precedenza.                                                                               |
| Salva ()       | Salva un oggetto nel flusso specificato e indica se l'oggetto deve reimpostare il relativo flag Dirty. Questo metodo restituisce E \_ NOTIMPL nei filtri. |
| GetSizeMax () | Restituisce la dimensione, in byte, del flusso necessario per salvare l'oggetto. Questo metodo restituisce E \_ NOTIMPL nei filtri.                                      |



 

### <a name="ipersistfile"></a>IPersistFile

Questa interfaccia carica un file in base al percorso assoluto e non è supportato in Windows Vista.



| Metodo          | Descrizione                                                                                                                  |
|-----------------|------------------------------------------------------------------------------------------------------------------------------|
| GetCurFile ()    | Ottiene il nome corrente del file associato all'oggetto. Restituisce il percorso specificato in Load ().                          |
| Carica ()          | Apre il file specificato e inizializza un oggetto dal contenuto del file. È possibile ritardare l'apertura del file fino a quando non è necessario. |
| GetClassID ()    | Restituisce l'identificatore di classe (CLSID) per il nuovo tipo di file. Per generare un CLSID univoco, è necessario utilizzare uuidgen.exe.           |
| IsDirty ()       | È necessario restituire solo E \_ NOTIMPL nei filtri                                                                                       |
| Salva ()          | È necessario restituire solo E \_ NOTIMPL nei filtri                                                                                       |
| SaveCompleted () | È necessario restituire solo E \_ NOTIMPL nei filtri                                                                                       |



 

### <a name="ipersiststorage"></a>IPersistStorage

Questa interfaccia supporta il modello di archiviazione strutturato, in cui ogni oggetto contenuto dispone di una propria archiviazione annidata all'interno dell'archiviazione del contenitore. Analogamente all' [interfaccia IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile), questa interfaccia viene caricata in base al percorso assoluto e non è supportata in Windows Vista.



| Metodo            | Descrizione                                                                                                   |
|-------------------|---------------------------------------------------------------------------------------------------------------|
| IsDirty ()         | Verifica se è stata apportata una modifica. Questo metodo restituisce E \_ NOTIMPL nei filtri.                                 |
| InitNew ()         | Crea una nuova risorsa di archiviazione. Questo metodo restituisce E \_ NOTIMPL nei filtri.                                             |
| Carica ()            | Salva l'archiviazione. Questo metodo restituisce E \_ NOTIMPL nei filtri.                                                 |
| Salva ()            | Restituisce la dimensione, in byte, del flusso necessario per salvare l'oggetto. Questo metodo restituisce E \_ NOTIMPL nei filtri. |
| SaveCompleted ()   | Riservato per utilizzo interno. Questo metodo restituisce E \_ NOTIMPL nei filtri.                                         |
| HandsOffStorage() | Riservato per utilizzo interno. Questo metodo restituisce E \_ NOTIMPL nei filtri.                                         |



 

## <a name="outputting-properties-with-filters"></a>Output delle proprietà con i filtri

Lo scopo di un filtro è quello di estrarre il contenuto e le proprietà dei file da includere nell'indice full-text. WDS chiama innanzitutto il metodo Load sulle implementazioni IPersistFile, IPersistStream o IPersistStorage e quindi richiama il metodo Init dell'implementazione di IFilter. **GetChunk** viene chiamato per recuperare i blocchi di dati del valore di testo o di proprietà, quindi **gettext** o **GetValue** viene chiamato il numero di volte necessario per recuperare tutti i valori di testo o di proprietà associati al blocco. Questo processo si **ripete fino a quando non viene** segnalato che il documento non contiene più blocchi.

Il metodo **GetChunk** recupera le informazioni sul primo o successivo blocco logico di informazioni dal file da filtrare e restituisce tali informazioni in una struttura di \_ blocco stat, inclusione di un ID blocco a incremento progressivo costante, informazioni sullo stato relative alla relazione tra il blocco corrente e il blocco precedente, un flag che indica se il blocco contiene testo o un valore, le impostazioni locali del blocco e la specifica della proprietà del blocco. La specifica della proprietà è un [**FULLPROPSPEC**](/windows/desktop/api/filter/ns-filter-fullpropspec) costituito da un CLSID e da un identificatore di proprietà Integer o stringa (ad esempio, D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedType). Identifica il tipo di proprietà anziché il valore della proprietà.

L'identificatore delle impostazioni locali del blocco viene usato per scegliere un Word breaker appropriato ed è molto importante identificarlo correttamente. Se il filtro non è in grado di determinare le impostazioni locali del testo, deve presupporre le impostazioni locali predefinite del sistema, disponibile tramite **GetSystemDefaultLCID**. Se si controlla il formato del file e attualmente non contiene informazioni sulle impostazioni locali, è necessario aggiungere una funzionalità utente per abilitare l'identificazione delle impostazioni locali corretta. L'utilizzo di un Word breaker non corrispondente può causare un'esperienza di query non valida per l'utente.

**GetChunk** gestisce solo l'accesso ai blocchi e non restituisce il testo o il valore della proprietà. Al contrario, le chiamate successive a **gettext** e **GetValue** recuperano il corpo del blocco. **Gettext** restituisce i blocchi di testo, che sono stringhe Unicode, dal blocco di testo del blocco corrente \_ . Se il blocco corrente è troppo grande, può essere necessaria più di una chiamata al metodo **gettext** . Ogni chiamata al metodo **gettext** Recupera il testo che segue immediatamente il testo dall'ultima chiamata al metodo **gettext** . Ad esempio, l'ultimo carattere di una chiamata può trovarsi al centro di una parola e il primo carattere nella chiamata successiva continuerà a essere la parola. I motori di ricerca devono gestire questa situazione.

**GetValue** restituisce i valori delle proprietà per il blocco del valore del blocco corrente \_ nelle strutture PROPVARIANT, che possono avere un'ampia gamma di tipi di dati. **GetValue** deve allocare la struttura PROPVARIANT usando CoTaskMemAlloc. Il chiamante di **GetValue** è responsabile della liberazione della memoria a cui punta PROPVARIANT usando PropVariantClear e della liberazione della struttura con CoTaskMemFree. Per ulteriori informazioni su PROPVARIANTs, vedere la Guida di riferimento a [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

### <a name="property-values"></a>Valori della proprietà

I filtri devono restituire almeno le proprietà seguenti, che sono le colonne predefinite nella visualizzazione dei risultati di WDS.



| GUID                                 | Campo PROPSPEC      | Nome descrittivo  | Descrizione                                                                                                                                     |
|--------------------------------------|---------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| F29F85E0-4FF9-1068-AB91-08002B27B3D9 | 2             | PrimaryTitle   | Titolo visualizzato per questo elemento.                                                                                                              |
| F29F85E0-4FF9-1068-AB91-08002B27B3D9 | 4             | PrimaryAuthors | Persona più associata a questo elemento.                                                                                                          |
| D5CDD505-2E9C-101B-9397-08002B2CF9AE | DataPrincipale   | DataPrincipale    | Data più importante per l'elemento, ad esempio la data di ricezione per la posta elettronica o la modifica dei file.                                                               |
| D5CDD505-2E9C-101B-9397-08002B2CF9AE | PerceivedType | PerceivedType  | Tipo di file da analizzare. Deve corrispondere a uno dei tipi di ricerca desktop di Windows elencati nel [tipo percepito](-search-2x-wds-perceivedtype.md)WDS. |



 

Per gli elementi di testo non crittografato, WDS estrae tutte le proprietà di testo e definite dal sistema, ad esempio le dimensioni del file o l'estensione, per includere nuovi tipi di file in testo normale nell'indice. Altri tipi di proprietà che possono essere restituiti all'indice includono:

-   Per i file: autore, titolo, stato, parole chiave
-   Per supporti: album, genere, fotocamera, data acquisita
-   Per le comunicazioni: da, a, CC, importanza
-   Per i contatti: titolo del processo, telefono aziendale, società

L'elenco sopra riportato raggruppa le proprietà comuni a un tipo percepito specificato. Tuttavia, qualsiasi proprietà può essere utilizzata indipendentemente dal tipo. Ad esempio, l'azienda può essere usata per il nome del datore di lavoro di un contatto e può anche essere usata per fare riferimento al nome di un client al quale è correlato il file. Molte di queste proprietà vengono usate per visualizzare i risultati della ricerca nella visualizzazione dei risultati di WDS. Ad esempio, la proprietà title di un file viene visualizzata come colonna principale nella visualizzazione dei risultati predefiniti. Gli oggetti IFilter devono restituire tutte le proprietà correlate al tipo di elemento analizzato. Non è possibile aggiungere proprietà personalizzate in WDS 2. x. Per un elenco completo delle proprietà disponibili, vedere lo [schema di WDS](-search-2x-wds-schematable.md).

## <a name="filter-add-in-installation"></a>Filtra installazione del componente aggiuntivo

L'installazione del filtro comporta la copia della DLL in una posizione appropriata nella directory Program Files e la relativa registrazione. I filtri devono implementare la registrazione automatica per l'installazione e attenersi alle linee guida seguenti:

-   Il programma di installazione deve usare il programma di installazione EXE o MSI.
-   È necessario fornire le note sulla versione.
-   È necessario creare una voce di installazione **applicazioni** per ogni componente aggiuntivo installato.
-   Il programma di installazione deve assumere tutte le impostazioni del registro di sistema per il tipo di file o l'archivio specifico che il componente aggiuntivo corrente riconosce.
-   Se un componente aggiuntivo precedente viene sovrascritto, il programma di installazione deve inviare una notifica all'utente.
-   Se un componente aggiuntivo più recente ha sovrascritto il componente aggiuntivo precedente, dovrebbe essere possibile ripristinare la funzionalità del componente aggiuntivo precedente e renderlo di nuovo il componente aggiuntivo predefinito per il tipo di file o l'archivio.

### <a name="clsids-required-for-registration"></a>CLSID necessari per la registrazione

Sono disponibili tre identificatori di classe, o CLSID, associati a ogni filtro. È necessario generare uno o più di questi (usare uuidgen.exe) per registrare il componente aggiuntivo di filtro.

-   Il primo oggetto identifica il gestore permanente di tutti i filtri, \_ ovvero IID IFilter, che è {89BCB740-6119-101A-BCB7-00DD010655AF}. Questo CLSID è costante per tutti i filtri che implementano IFilter.
-   Il secondo (il valore della \_ chiave IFILTER IID) identifica l'implementazione di IFilter per il tipo di file. Questa chiave contiene un valore InprocServer32 che specifica il nome della DLL in base al percorso e al modello di Threading. Se il filtro si trova nel percorso di sistema, ad esempio la directory system32, è sufficiente un nome file. In caso contrario, questo valore deve avere una specifica del percorso completo.
-   Il terzo identifica il tipo di file che il filtro elabora e viene restituito dal metodo GetClassID sull'interfaccia IPersist.

> [!Note]
>
> Nelle versioni future dei sistemi operativi Microsoft, l'installazione dei file nella directory system32 potrebbe risultare più complessa, pertanto è consigliabile installarli in programmi e includere un percorso completo del filtro nel registro di sistema. Per motivi di sicurezza, è inoltre consigliabile specificare un percorso completo della DLL nel registro di sistema. In caso contrario, è possibile caricare una versione "Trojan Horse" della DLL se si trova nel percorso del processo prima della versione.

 

### <a name="registration-model"></a>Modello di registrazione

Quando WDS è pronto per filtrare un file, Cerca nel registro di sistema sotto l'estensione del file per determinare quale filtro caricare. Segue quindi una serie di collegamenti al registro di sistema per trovare il nome della DLL di filtro, in questo ordine:

1.  Da CLSID disponibili in:

    **HKEY \_ \_ software utente \\ corrente \\ Microsoft \\ RSSearch \\ ContentIndexCommon \\ Filters \\ override \\ RSApp**

    **HKEY \_ \_ software utente \\ corrente \\ Microsoft \\ RSSearch \\ ContentIndexCommon \\ Filters**

2.  Dal tipo di contenuto del file:

    **\_Tipo di \_ \\ contenuto del \\ \\ database MIME per le classi software \\ del computer \\ locale HKEY**

3.  Dall'estensione del nome file (uguale all'API Win32 LoadIFilter) in:

    **HKEY \_ \_ software utente \\ corrente \\ Microsoft \\ RSSearch \\ ContentIndexCommon \\ Filters \\ override \\ RSApp**

    **HKEY \_ \_ software utente \\ corrente \\ Microsoft \\ RSSearch \\ ContentIndexCommon \\ Filters**

    **\_Classi HKEY \_ radice \\ EXTPERSISTENTHANDLER->CLSID->IID \_ IFilter->CLSID**

4.  Da impostazione predefinita:

    **HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ RSSearch \\ ContentIndexCommon \\ Filters**

### <a name="to-register-a-filter-add-in"></a>Per registrare un componente aggiuntivo di filtro

Per registrare il componente aggiuntivo del filtro, è necessario inserire un totale di otto voci nel registro di sistema:

-   **. ext** è la nuova estensione del nome di file
-   Il **GUID \_ 1** può essere qualsiasi nuovo GUID generato per questa estensione
-   **89BCB740-6119-101A-BCB7-00DD010655AF** è il GUID dell'interfaccia IFilter, che è una costante per tutte le implementazioni di IFilter.

1.  Registrare il gestore permanente per l'estensione del nome file con le chiavi e i valori seguenti:

    ```
    HKEY_CLASSES_ROOT\<.ext>\PersistentHandler
       (Default) = {GUID_1}
    ```

    ```
    HKEY_CLASSES_ROOT\CLSID\{GUID_1}
       (Default) = <Persistent Handler Description>
    ```

    ```
    HKEY_CLASSES_ROOT\CLSID\{GUID_1}\PersistentAddinsRegistered
       (Default) = (Value Not Set)
    ```

    ```
    HKEY_CLASSES_ROOT\CLSID\{GUID_1}\PersistentAddinsRegistered\{89BCB740-6119-101A-BCB7-00DD010655AF}
       (Default) = {CLSID of IFilter implementation}
    ```

    ```
    HKEY_CLASSES_ROOT\CLSID\{GUID_1}\PersistentHandler
       (Default) = {GUID_1}
    ```

2.  Registrare l'implementazione di IFilter con le chiavi e i valori seguenti:

    ```
    HKEY_CLASSES_ROOT\CLSID\{CLSID of IFilter implementation}
       (Default) = Extension IFilter Description">
    ```

    ```
    HKEY_CLASSES_ROOT\CLSID\{CLSID of IFilter implementation}\InprocServer32
       (Default) = <DLL Install Path>
       ThreadingModel = Both
    ```

3.  Registrare l'implementazione di IFilter con Windows Desktop Search con la chiave e il valore seguenti:

    ```
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\RSSearch\ContentIndexCommon\Filters\Extension\<.ext>
       (Default) = {CLSID of IFilter implementation}"
    ```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[SchemaTable](-search-2x-wds-schematable.md)
</dt> <dt>

[Tipi percepiti](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[Sviluppo di gestori di protocollo](-search-2x-wds-phaddins.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)
</dt> </dl>

 

 
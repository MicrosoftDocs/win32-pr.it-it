---
description: Microsoft Windows Search USA i gestori delle proprietà per estrarre i valori delle proprietà dagli elementi e usa lo schema del sistema di proprietà per determinare la modalità di indicizzazione di una proprietà specifica.
ms.assetid: b475329a-1ed7-43a4-8e11-3700889a4ce9
title: Sviluppo di gestori di proprietà per Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac96e47738040321025b7f600e2c91109b08d51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225959"
---
# <a name="developing-property-handlers-for-windows-search"></a>Sviluppo di gestori di proprietà per Windows Search

Microsoft Windows Search USA i gestori delle proprietà per estrarre i valori delle proprietà dagli elementi e usa lo schema del sistema di proprietà per determinare la modalità di indicizzazione di una proprietà specifica. Per leggere e indicizzare i valori delle proprietà, i gestori delle proprietà vengono richiamati out-of-process da Windows Search per migliorare la sicurezza e l'affidabilità. Al contrario, i gestori delle proprietà vengono richiamati in-process da Esplora risorse per leggere e scrivere i valori delle proprietà.

Questo argomento integra l'argomento del [sistema di proprietà](../properties/building-property-handlers.md) con informazioni specifiche di Windows Search e contiene le sezioni seguenti:

-   [Decisioni di progettazione per i gestori di proprietà](#design-decisions-for-property-handlers)
    -   [Decisioni sulle proprietà](#property-decisions)
    -   [Supporto full-text](#full-text-support)
    -   [Considerazioni sul Implementatation del sistema operativo](#operating-system-implementatation-considerations)
-   [Scrittura dei file di descrizione delle proprietà](#writing-property-description-files)
-   [Implementazione di gestori di proprietà](#implementing-property-handlers)
    -   [IInitializeWithStream](#iinitializewithstream)
    -   [IPropertyStore](#ipropertystore)
    -   [IPropertyStoreCapabilities](#ipropertystorecapabilities)
-   [Verifica dell'indicizzazione degli elementi](#ensuring-your-items-get-indexed)
-   [Installazione e registrazione di gestori di proprietà](#installing-and-registering-property-handlers)
-   [Test e risoluzione dei problemi relativi ai gestori di proprietà](#testing-and-troubleshooting-property-handlers)
    -   [Test di installazione e configurazione](#installation-and-setup-tests)
    -   [Risoluzione dei problemi relativi ai gestori di proprietà](#troubleshooting-property-handlers)
-   [Utilizzo di System-Supplied gestori di proprietà](#using-system-supplied-property-handlers)
-   [Argomenti correlati](#related-topics)

 

## <a name="design-decisions-for-property-handlers"></a>Decisioni di progettazione per i gestori di proprietà

L'implementazione dei gestori delle proprietà prevede i passaggi seguenti:

1.  Prendere decisioni di progettazione relative alle proprietà che si desidera supportare.
2.  Creazione di un file di descrizione della proprietà (. propdesc) per le proprietà non già presenti nel sistema di proprietà.
3.  Implementazione e test del gestore della proprietà.
4.  Installazione e registrazione dei file di descrizione della proprietà e del gestore della proprietà.
5.  Test dell'installazione e della registrazione del gestore proprietà.

Prima di iniziare, è necessario prendere in considerazione le seguenti domande di progettazione:

-   Quali proprietà sono supportate dal formato di file?
-   Queste proprietà sono già nello schema del sistema?
-   È possibile utilizzare un gestore di proprietà esistente fornito dal sistema?
-   Quali proprietà possono essere visualizzate agli utenti finali?
-   Quali proprietà possono essere modificate dagli utenti?
-   Il supporto per la ricerca full-text proviene da un gestore di proprietà o da un filtro?
-   È necessario supportare le applicazioni legacy? In tal caso, cosa si implementa?

> [!Note]  
> Prima di continuare, vedere [uso di System-Supplied gestori di proprietà](#using-system-supplied-property-handlers) per verificare se è possibile usare un gestore di proprietà fornito dal sistema, risparmiando tempo e risorse di sviluppo.

 

Dopo aver preso queste decisioni, è possibile scrivere descrizioni formali delle proprietà personalizzate in modo che il motore di ricerca di Windows possa iniziare a indicizzare i file e le proprietà. Queste descrizioni formali sono file XML, descritti nello [schema della descrizione della proprietà](/previous-versions//cc144127(v=vs.85)).

### <a name="property-decisions"></a>Decisioni sulle proprietà

Quando si considerano le proprietà da supportare, è necessario identificare le esigenze di indicizzazione e ricerca degli utenti. Ad esempio, si potrebbe essere in grado di identificare 100 proprietà potenzialmente utili per il tipo di file, ma gli utenti potrebbero essere interessati alla ricerca solo in pochi. Inoltre, è possibile che si desideri visualizzare un gruppo diverso, più grande o più piccolo, di tali proprietà per gli utenti in Esplora risorse e consentire agli utenti di modificare solo un subset di tali proprietà visualizzate.

Il tipo di file può supportare qualsiasi proprietà personalizzata definita dall'utente, oltre a un set di proprietà definite dal sistema. Prima di creare una proprietà personalizzata, verificare le [proprietà di sistema](https://msdn.microsoft.com/library/bb763010(VS.85).aspx) per verificare se la proprietà che si desidera supportare è già definita da una proprietà di sistema. Assicurarsi sempre di supportare le proprietà più importanti definite dal sistema.

Per progettare le proprietà è consigliabile usare una matrice:



| Nome proprietà | È indicizzabile? | È visualizzabile? | È modificabile? |
|---------------|---------------|-----------------|--------------|
| property1     | S             | S               | N            |
| Proprietà...   | S             | S               | N            |
| propertyN     | N             | N               | N            |



 

Per ognuna di queste proprietà, è necessario determinare gli attributi che devono avere e quindi descriverli formalmente in file XML di descrizione della proprietà (. propdesc). Gli attributi includono il tipo di dati della proprietà, l'etichetta, la stringa della guida e altro ancora. Per le proprietà indicizzabili, è necessario prestare particolare attenzione ai seguenti attributi di proprietà trovati nell'elemento XML [searchInfo](../properties/propdesc-schema-searchinfo.md)   del file di descrizione della proprietà.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attributo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>inInvertedIndex</td>
<td>facoltativo. Indica se il valore di una proprietà di stringa deve essere suddiviso in parole e ogni parola archiviata nell'indice invertito. L'indice invertito consente una ricerca efficiente di parole e frasi sul valore della proprietà usando CONTAINs o FREETEXT (ad esempio, SELECT... DOVE contiene &quot; someText &quot; ). Se è impostato su <strong>false</strong>, le ricerche vengono eseguite sull'intera stringa. La maggior parte delle proprietà di stringa deve avere questo valore impostato su <strong>true</strong>; per le proprietà non di stringa è necessario impostare questo valore su <strong>false</strong>. Il valore predefinito è <strong>false</strong>.</td>
</tr>
<tr class="even">
<td>isColumn</td>
<td>facoltativo. Indica se la proprietà deve essere archiviata nel database di ricerca di Windows come colonna. L'archiviazione della proprietà come colonna consente il recupero, l'ordinamento, il raggruppamento e il filtro, ovvero l'utilizzo di qualsiasi predicato eccetto CONTAINs o FREETEXT per l'intero valore della colonna. Le proprietà visualizzate per l'utente devono essere impostate su <strong>true</strong> , a meno che non si tratti di una proprietà testuale molto grande, ad esempio il corpo di un documento, in cui verrebbe eseguita la ricerca nell'indice invertito. Il valore predefinito è <strong>false</strong>.</td>
</tr>
<tr class="odd">
<td>isColumnSparse</td>
<td>facoltativo. Indica se una proprietà non occupa alcuno spazio se il valore è <strong>null</strong>. Una proprietà non di tipo sparse occupa spazio per ogni elemento, anche se il valore è <strong>null</strong>. Se la proprietà è multivalore, questo attributo è sempre <strong>true</strong>. Questo attributo deve essere <strong>false</strong> solo se è presente un valore per ogni elemento. Il valore predefinito è <strong>true</strong>.</td>
</tr>
<tr class="even">
<td>columnIndexType</td>
<td>facoltativo. Per ottimizzare l'esecuzione di query, il motore di ricerca di Windows può creare indici secondari per le proprietà con la colonna =<strong>true</strong>. Questa operazione richiede più spazio di elaborazione e spazio su disco durante l'indicizzazione, ma migliora le prestazioni durante l'esecuzione di query. Se la proprietà tende a essere ordinata, raggruppata o filtrata (ovvero usando =,! =, <, >, LIKE, corrisponde) spesso dagli utenti, questo attributo deve essere impostato su &quot; ondisk &quot; . Il valore predefinito è &quot; NotIndexed &quot; . I valori seguenti sono validi:
<ul>
<li>NotIndexed: non viene creato alcun indice secondario.</li>
<li>Ondisk: creare e archiviare un indice secondario sul disco.</li>
</ul></td>
</tr>
<tr class="odd">
<td>maxSize</td>
<td>facoltativo. Indica la dimensione massima consentita per il valore della proprietà archiviato nel database di ricerca di Windows. Questo limite si applica agli elementi ciascun indvidual di un vettore, non all'intero vettore. I valori che superano questa dimensione vengono troncati. Il valore predefinito è &quot; 128 &quot; (byte).<br/> Attualmente, Windows Search non usa maxSize durante il calcolo della quantità di dati accettati da un file. Al contrario, il limite usato da Windows Search è il prodotto delle dimensioni del file e il valore di MaxGrowFactor (file size N * MaxGrowFactor) letto dal registro di sistema in HKEY_LOCAL_MACHINE->software->Microsoft->Windows Search->Gathering Manager->MaxGrowFactor. Il valore predefinito di MaxGrowFactor è quattro (4). Di conseguenza, se il tipo di file tende a essere ridotto in dimensioni totali ma con proprietà più grandi, è possibile che Windows Search non accetti tutti i dati di proprietà che si desidera creare. Tuttavia, è possibile aumentare il MaxGrowFactor in base alle esigenze. <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Per l'attributo columnIndexType, il vantaggio di una query più veloce deve essere ponderato rispetto al tempo di indicizzazione e ai costi di spazio maggiori che gli indici secondari possono sostenere. Questo costo viene tuttavia pagato solo per gli elementi con un valore non **null** , quindi per la maggior parte delle proprietà questo attributo può essere impostato su "ondisk".

 

### <a name="full-text-support"></a>Supporto full-text

In generale, la ricerca full-text è supportata dai componenti chiamati [filtri](-search-3x-wds-extidx-filters.md); Tuttavia, per i tipi di file basati su testo con formati di file non complicati, i gestori di proprietà possono essere in grado di fornire questa funzionalità con un minor sforzo di sviluppo. È consigliabile esaminare la sezione del [contenuto full-text](../properties/building-property-handlers-property-handlers.md) per un confronto tra le funzionalità di filtro e di gestione delle proprietà che consentono di decidere quale sia la soluzione migliore per il tipo di file. Di particolare importanza è il fatto che i filtri possono gestire gli identificatori di codice in più lingue (LCID) per ogni file, mentre i gestori di proprietà non possono.

> [!Note]  
> Poiché i gestori di proprietà non possono suddividere il contenuto nel modo in cui i filtri possono, i file di grandi dimensioni (anche se sono formati di file non complicati) devono essere completamente caricati in memoria.

 

### <a name="operating-system-implementatation-considerations"></a>Considerazioni sul Implementatation del sistema operativo

### <a name="implementation-information-for-windows-7"></a>Informazioni di implementazione per Windows 7

In Windows 7 e versioni successive, si verifica un nuovo comportamento quando si registra un gestore di proprietà, un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)o una nuova estensione. Quando viene installato un nuovo gestore di proprietà e/o **IFilter** , i file con le estensioni corrispondenti vengono automaticamente reindicizzati.

In Windows 7 è consigliabile installare un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) insieme ai gestori di proprietà corrispondenti e che **IFilter** venga registrato prima del gestore della proprietà. La registrazione del gestore delle proprietà avvia la reindicizzazione immediata dei file indicizzati in precedenza senza dover prima riavviare il computer e sfrutta tutti gli IFilter registrati in precedenza ai fini dell'indicizzazione del contenuto.

Se è installato solo un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) , senza un gestore proprietà corrispondente, la reindicizzazione automatica viene eseguita dopo il riavvio del servizio di indicizzazione o il riavvio del sistema.

Per i flag di descrizione della proprietà specifici di Windows 7, vedere gli argomenti di riferimento seguenti:

-   [GETPROPERTYSTOREFLAGS](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags)
-   [tipo di PROPDESC \_ COLUMNINDEX \_](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type)
-   [\_flag SEARCHINFO \_ PROPDESC](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags)

### <a name="implementation-information-for-windows-vista-and-earlier"></a>Informazioni di implementazione per Windows Vista e versioni precedenti

Prima di Windows Vista, i filtri fornivano il supporto per l'analisi e l'enumerazione di contenuto e proprietà del file. Con l'introduzione del sistema di proprietà, i gestori delle proprietà gestiscono le proprietà dei file mentre i filtri gestiscono il contenuto del file. Per Windows Vista, è necessario sviluppare solo un'implementazione parziale dell'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)in coordinamento con un gestore di proprietà, come descritto in [procedure consigliate per la creazione di gestori di filtro in Windows Search](-search-3x-wds-extidx-filters.md).

Sebbene il sistema di proprietà sia incluso anche nell'installazione di Windows Search per Windows XP, le applicazioni di terze parti e legacy possono richiedere che i filtri gestiscano sia il contenuto che le proprietà. Pertanto, se si sta sviluppando sulla piattaforma Windows XP, è necessario fornire un'implementazione di filtro completo e un gestore di proprietà per il tipo di file o la proprietà personalizzata.

 

## <a name="writing-property-description-files"></a>Scrittura dei file di descrizione delle proprietà

La struttura dei file XML di descrizione della proprietà (con estensione propdesc) è descritta nell'argomento [PropertyDescription](../properties/propdesc-schema-propertydescription.md) . Di particolare interesse per la ricerca sono gli attributi dell'elemento [searchInfo](../properties/propdesc-schema-searchinfo.md) . Dopo aver deciso quali proprietà supportare, è necessario creare e registrare i file di descrizione delle proprietà per ogni proprietà. Quando si registrano i file con estensione propdesc, questi vengono inclusi nell'elenco di descrizioni delle proprietà dello schema e diventano nomi di colonna all'interno dell'archivio delle proprietà del motore di ricerca.

È possibile registrare le descrizioni delle proprietà personalizzate utilizzando la funzione [PSRegisterPropertySchema](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema) , un'API wrapper che chiama IPropertySystem:: RegisterPropertySchema del sottosistema dello schema. Questa funzione informa il sottosistema dello schema dell'aggiunta di file di schema di descrizione della proprietà (. propdesc), usando i percorsi di file nei file con estensione propdesc nel computer locale, in genere la directory di installazione dell'applicazione in "programmi". In genere, un'installazione o un'applicazione (ad esempio, il programma di installazione del gestore di proprietà) chiamerà questo metodo dopo l'installazione dei file con estensione propdesc.

 

## <a name="implementing-property-handlers"></a>Implementazione di gestori di proprietà

Lo sviluppo di un gestore di proprietà comporta l'implementazione delle interfacce seguenti:

-   IInitialzeWithStream: fornisce l'inizializzazione basata sul flusso del gestore della proprietà.
-   IPropertyStore: enumera, ottiene e imposta i valori delle proprietà.
-   IPropertyStoreCapabilities: facoltativo. Indica se gli utenti possono modificare una proprietà da un'interfaccia utente.

### <a name="iinitializewithstream"></a>IInitializeWithStream

Come descritto nell'argomento relativo al [sistema di proprietà](../properties/building-property-handlers.md) , è consigliabile implementare i gestori di proprietà con **IInitializeWithStream** per eseguire l'inizializzazione basata sul flusso. Se si sceglie di non implementare IInitializeWithStream, il gestore della proprietà deve rifiutare esplicitamente l'esecuzione nel processo di isolamento impostando il flag DisableProcessIsolation nella chiave del registro di sistema del gestore proprietà. La disabilitazione dell'isolamento dei processi è in genere destinata solo ai gestori di proprietà legacy e deve essere evitata con qualsiasi nuovo codice.

### <a name="ipropertystore"></a>IPropertyStore

Per creare un gestore di proprietà, è necessario implementare l'interfaccia [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) con i metodi seguenti.



| Metodo   | Descrizione                                                         |
|----------|---------------------------------------------------------------------|
| Commit   | Salva una modifica apportata a una proprietà nel file.                                |
| GetAt    | Recupera una chiave di proprietà dalla matrice di proprietà di un elemento.        |
| GetCount | Ottiene il numero di proprietà associate al file.                 |
| GetValue | Recupera i dati per una proprietà specifica.                             |
| SetValue | Imposta un nuovo valore della proprietà o sostituisce o rimuove un valore esistente. |



 

 

 

Importanti considerazioni per l'implementazione di questa interfaccia sono incluse nella documentazione di [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .

> [!Note]  
> Se il gestore delle proprietà emette più valori per la stessa proprietà per un determinato elemento, solo l'ultimo valore emesso viene archiviato nel catalogo.

 

 

### <a name="ipropertystorecapabilities"></a>IPropertyStoreCapabilities

I gestori di proprietà possono implementare facoltativamente questa interfaccia per disabilitare la capacità di un utente di modificare proprietà specifiche. Queste proprietà sono in genere modificabili nella pagina dei dettagli e nel riquadro, ma non sono consentite nel gestore delle proprietà di implementazione. Implementare correttamente questa interfaccia offre un'esperienza utente migliore rispetto all'alternativa, ovvero un semplice errore di run-time dalla Shell.

 

## <a name="ensuring-your-items-get-indexed"></a>Verifica dell'indicizzazione degli elementi

Ora che è stato implementato il gestore delle proprietà, è necessario assicurarsi che gli elementi per i quali viene registrato il gestore vengano indicizzati. È possibile utilizzare [gestione catalogo](-search-3x-wds-mngidx-catalog-manager.md) per avviare la reindicizzazione ed è inoltre possibile utilizzare il [gestore dell'ambito di ricerca per indicizzazione](-search-3x-wds-extidx-csm.md) per configurare le regole predefinite che indicano gli URL per cui l'indicizzatore deve eseguire la ricerca per indicizzazione. Un'altra opzione consiste nel seguire l'esempio di codice REINDEX negli [esempi di Windows Search SDK](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).

Per ulteriori informazioni, vedere [utilizzo di gestione catalogo](-search-3x-wds-mngidx-catalog-manager.md) e [utilizzo di gestione ambito ricerca per indicizzazione](-search-3x-wds-extidx-csm.md).

 

## <a name="installing-and-registering-property-handlers"></a>Installazione e registrazione di gestori di proprietà

Con il gestore di proprietà implementato, deve essere registrato e la relativa estensione del nome file associata al gestore. Nell'esempio seguente vengono illustrate le chiavi del registro di sistema e i valori necessari per eseguire questa operazione.

```
HKEY_CLASSES_ROOT
   CLSID
      {<CLSID for property handler>}
         (Default) = <Property Handler Name>
         InProcServer32
            (Default) = <full path to property handler dll>
            ThreadingModel = <your threading model>
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PropertySystem
                  PropertyHandlers
                     <.fileextention>
                        (Default) = {<CLSID for property handler>}
```

 

## <a name="testing-and-troubleshooting-property-handlers"></a>Test e risoluzione dei problemi relativi ai gestori di proprietà

Nell'elenco seguente vengono forniti consigli sui tipi di test da eseguire:

-   Testare il recupero dell'output da ogni singola proprietà supportata dal tipo di file.
-   Usare i valori di proprietà Big, ad esempio, usare un metatag di grandi dimensioni nei documenti HTML.
-   Verificare che il gestore delle proprietà non perda gli handle di file modificando l'output del gestore proprietà o utilizzando uno strumento come oh.exe prima e dopo l'enumerazione delle proprietà del file.
-   Testare tutti i tipi di file associati al gestore della proprietà. Verificare, ad esempio, che il filtro HTML funzioni con i tipi di file con estensione htm e HTML.
-   Eseguire test con file danneggiati. Il gestore delle proprietà dovrebbe avere esito negativo normalmente.
-   Se un'applicazione supporta la crittografia, verificare che il gestore della proprietà non restituisca il testo crittografato.
-   Se il gestore delle proprietà supporta la ricerca full-text:
    -   Usare più caratteri Unicode speciali nel contenuto del file e testarne l'output.
    -   Testare la gestione di documenti di dimensioni molto grandi per assicurarsi che il gestore di proprietà funzioni come previsto.

### <a name="installation-and-setup-tests"></a>Test di installazione e configurazione

Infine, è necessario testare le routine di installazione e disinstallazione.

-   L'installazione deve essere ripristinata da installazioni non riuscite, ad esempio dall'annullamento e dal riavvio del programma di installazione.
-   Uninstall deve eliminare tutti i file associati al gestore della proprietà.
-   La disinstallazione non deve eliminare file diversi da quelli associati all'installazione del gestore della proprietà.
-   Le chiavi del registro di sistema associate al gestore proprietà devono essere rimosse quando viene disinstallato.
-   La disinstallazione deve funzionare anche se i file vengono eliminati dalla directory di installazione.

### <a name="troubleshooting-property-handlers"></a>Risoluzione dei problemi relativi ai gestori di proprietà

Di seguito sono riportati alcuni errori comuni eseguiti durante lo sviluppo dei gestori delle proprietà:

-   Installazione di file con estensione propdesc o dll in una directory utente.
-   Registrazione dei componenti mediante percorsi relativi.
-   Registrazione dei componenti in HKEY \_ Current \_ User anziché HKEY \_ Local \_ computer.
-   Si dimentica di impostare DisableProcessIsolation per i gestori non di flusso.
-   Posizionamento del file di test in una posizione non indicizzata.

Se si verificano problemi durante l'utilizzo dell'indicizzatore da parte del gestore delle proprietà, di seguito sono riportati alcuni suggerimenti utili per risolvere i problemi:

-   Verificare che le descrizioni delle proprietà (file con estensione propdesc) siano contrassegnate come colonna = "**true**", visualizzabile = "**true**" e Queryable = "**true**" nel modo appropriato.
-   Verificare che i file con estensione propdesc si trovino in un percorso globale.
-   Verificare che i file con estensione propdesc siano stati registrati usando percorsi assoluti.
-   Verificare che nel registro eventi non siano stati registrati errori durante la registrazione del file con estensione propdesc.
-   Verificare che le dll si trovino in un percorso globale (e non nel profilo utente).
-   Verificare che le dll siano registrate in HKEY \_ Local \_ Machine \\ software \\ Classes.
-   Verificare che le dll siano registrate usando percorsi completi (o le \_ stringhe reg Expand \_ SZ che si espandono in percorsi assoluti usando le variabili di ambiente note dall'account di sistema).
-   Verificare che il gestore delle proprietà funzioni in Esplora risorse.
-   Sebbene sia consigliabile usare IInitializeWithStream, se è necessario usare IInitializeWithFile o IInitializeWithItem, verificare di specificare DisableProcessIsolation.
-   Verificare che il pannello di controllo opzioni di indicizzazione elenchi il tipo di file come tipo di file indicizzato.
-   Verificare che il file di test si trovi in una posizione indicizzata.
-   Verificare che il file di test sia stato modificato dopo l'installazione del gestore della proprietà.

Se il file di test si trova in una posizione indicizzata e l'indicizzatore ha già sottoposto a ricerca per indicizzazione, è necessario modificare il file in qualche modo per attivare una reindicizzazione del file.

 

## <a name="using-system-supplied-property-handlers"></a>Utilizzo di System-Supplied gestori di proprietà

Windows include diversi gestori di proprietà forniti dal sistema che è possibile usare se il formato del tipo di file è compatibile. Se si definisce una nuova estensione di file che usa uno di questi formati, è possibile usare i gestori forniti dal sistema registrando l'identificatore di classe del gestore (CLSID) per l'estensione di file.

È possibile utilizzare il CLSID elencato nella tabella seguente per registrare i gestori di proprietà forniti dal sistema per il tipo di formato di file.



| Formato          | CLSID                                  |
|-----------------|----------------------------------------|
| DocFile OLE     | {8d80504a-0826-40c5-97e1-ebc68f953792} |
| Salva XML del gioco   | {ECDD6472-2B9B-4b4b-AE36-F316DF3C8D60} |
| Gestore XPS/OPC | {45670FA8-ED97-4F44-BC93-305082590BFB} |
| XML             | {c73f6f30-97a0-4ad1-a08f-540d4e9bc7b9} |



 

Prima di creare una proprietà personalizzata, è necessario assicurarsi che non esista una proprietà definita dal sistema che è invece possibile usare. È possibile enumerare le proprietà definite dal sistema chiamando [**PSEnumeratePropertyDescriptions**](/windows/win32/api/propsys/nf-propsys-psenumeratepropertydescriptions) o utilizzando lo strumento da riga di comando prop.exe.

Lo schema del sistema definisce il modo in cui queste proprietà interagiscono con l'indicizzatore e non è possibile modificarlo. Inoltre, l'applicazione utilizzata per creare, modificare e salvare il tipo di file deve essere conforme anche a un determinato comportamento. Se, ad esempio, l'applicazione implementa il salvataggio sicuro (in base al quale viene creato un file temporaneo durante la modifica e quindi ReplaceFile () viene usato per scambiare la nuova versione per il vecchio), deve trasferire tutte le proprietà dal file originale al nuovo file. In caso contrario, il file perde le proprietà aggiunte dagli utenti o da altre applicazioni.

 

**Esempio**

Di seguito viene illustrata la registrazione del gestore DocFile OLE fornito dal sistema per un tipo di file con un oggetto. Estensione OLEDocFile.

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      .OLEDocFile
         shellex
            {BB2E617C-0920-11d1-9A0B-00C04FC2D6C1}
               (Default) = {9DBD2C50-62AD-11d0-B806-00C04FD706EC}
```

Di seguito viene illustrata la registrazione delle informazioni sull'elenco di proprietà in modo che le proprietà di. I file OLEDocFile vengono visualizzati nel riquadro e nella scheda Dettagli.

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      .OLEDocFile
         ExtendedTileInfo = prop:System.ItemType;System.Size;System.DateModified;System.Author;System.OfflineAvailability
         FullDetails = prop:System.PropGroup.Description;System.Title;System.Subject;
System.Keywords;System.Category;System.Comment;System.PropGroup.Origin;
System.Author;System.Document.LastAuthor;System.Document.RevisionNumber;
System.Document.Version;System.ApplicationName;System.Company;System.Document.Manager;
System.Document.DateCreated;System.Document.DateSaved;System.Document.DatePrinted;
System.Document.TotalEditingTime;System.PropGroup.Content;System.ContentStatus;
System.ContentType;System.Document.PageCount;System.Document.WordCount;
System.Document.CharacterCount;System.Document.LineCount;
System.Document.ParagraphCount;System.Document.Template;System.Document.Scale;
System.Document.LinksDirty;System.Language;System.PropGroup.FileSystem;
System.ItemNameDisplay;System.ItemType;System.ItemFolderPathDisplay;
System.DateCreated;System.DateModified;System.Size;System.FileAttributes;
System.OfflineAvailability;System.OfflineStatus;System.SharedWith;
System.FileOwner;System.ComputerName
         InfoTip = prop:System.ItemType;System.Size;System.DateModified;System.Document.PageCoun
         PerceivedType = document
         PreviewDetails = prop:*System.DateModified;System.Author;System.Keywords;
*System.Size;System.Title;System.Comment;System.Category;
*System.Document.PageCount;System.ContentStatus;System.ContentType;
*System.OfflineAvailability;*System.OfflineStatus;System.Subject;
*System.DateCreated;*System.SharedWith
```

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[Mapping delle proprietà](-search-3x-wds-propertymappings.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Procedure consigliate per la creazione di gestori di filtro in Windows Search](-search-3x-wds-extidx-filters.md)
</dt> <dt>

[Processo di indicizzazione](-search-indexing-process-overview.md)
</dt> <dt>

[Sviluppo di gestori di protocollo](-search-3x-wds-phaddins.md)
</dt> <dt>

[Proprietà definite dal sistema per formati di file personalizzati](-shell-systemdefinedpropertiesforfileformats.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[Sistema di proprietà](../properties/building-property-handlers.md)
</dt> <dt>

[Proprietà di sistema](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)
</dt> <dt>

[Esempi di Windows Search SDK](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)
</dt> </dl>

 

 

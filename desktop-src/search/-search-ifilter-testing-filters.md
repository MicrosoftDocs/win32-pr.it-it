---
description: Il gruppo di test IFilter convalida i gestori di filtri.
ms.assetid: 5ee02af1-1dc9-4d21-868f-4c439970b1ba
title: Test dei gestori di filtri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf58f14f0f8de4458dd887bf52b32fb68f869d64
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122621947"
---
# <a name="testing-filter-handlers"></a>Test dei gestori di filtri

Il gruppo di test [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) convalida i gestori di filtri. Il gruppo di test esegue questa operazione chiamando i [**metodi IFilter**](/windows/win32/api/filter/nn-filter-ifilter) e verificando la conformità dei valori restituiti con la **specifica dell'interfaccia IFilter.** e verificano che gli identificatori di blocco siano univoci e crescenti, che l'interfaccia **IFilter** si comporti in modo coerente dopo la nuova inizializzazione e che qualsiasi chiamata al metodo **IFilter** con parametri non validi restituirà i codici di errore previsti. I programmi del gruppo di test scaricano anche l'output di un file filtrato da un gestore di filtri e controllano le informazioni di registrazione **di IFilter** nel Registro di sistema.

Questo argomento è organizzato come segue:

- [Chiamata dalla riga di comando](#command-line-invocation)
  - [ifilttst.exe](#ifilttstexe)
  - [filtdump.exe](#filtdumpexe)
  - [filtreg.exe](#filtregexe)
  - [ifilttst.ini](#ifilttstini)
- [Procedura di test IFilter](#ifilter-test-procedure)
  - [Test di convalida](#validation-test)
  - [Test di coerenza](#consistency-test)
  - [Test di input non valido](#invalid-input-test)
  - [Test di configurazioni IFilter diverse](#testing-different-ifilter-configurations)
- [Verifica dell'indicizzazione degli elementi registrati](#ensuring-registered-items-get-indexed)
  - [File di log di esempio](#sample-log-file)
  - [File di dump di esempio](#sample-dump-file)
- [Risorse aggiuntive](#additional-resources)
- [Argomenti correlati](#related-topics)

> [!NOTE]  
> Se viene installato un nuovo gestore di filtri per un tipo di file in sostituzione di una registrazione di filtro esistente, il programma di installazione deve salvare la registrazione corrente e ripristinarla se il nuovo gestore di filtri viene disinstallato. Non esiste alcun meccanismo per concatenare i filtri. Di conseguenza, il nuovo gestore di filtri è responsabile della replica di tutte le funzionalità necessarie del filtro precedente.

## <a name="command-line-invocation"></a>Command-Line chiamata

Il gruppo di test [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) è costituito da tre applicazioni della riga di comando: [ifilttst.exe](#ifilttstexe), [filtdump.exe](#filtdumpexe)e [filtreg.exe](#filtregexe) e un file di inizializzazione, [ifilttst.ini](#ifilttstini).

> [!IMPORTANT]
> In Windows 7 e versioni successive, i filtri scritti in codice gestito vengono bloccati in modo esplicito. I filtri DEVONO essere scritti in codice nativo a causa di potenziali problemi di controllo delle versioni clr (Common Language Runtime) con il processo in cui vengono eseguiti più componenti aggiuntivi.

### <a name="ifilttstexe"></a>ifilttst.exe

Il ifilttst.exe esegue diversi test per convalidare un gestore di filtri. L'esempio seguente illustra come richiamare il ifilttst.exe dalla riga di comando:


```
ifilttst /i test.htm /l /d /v 1
```

Nell'esempio vengono eseguite le attività seguenti:

- Indica al programma di filtrare il file test.htm
- Reindirizza i messaggi di log test.htm.log
- Reindirizza i messaggi di dump test.htm.dmp
- Imposta il livello di dettaglio su 1

Per il funzionamento del comando precedente, è necessario che tre file si trovino nella directory di lavoro corrente: `test.htm` , [ifilttst.exe](#ifilttstexe)e [ifilttst.ini](#ifilttstini). Le opzioni della riga di comando sono elencate nella tabella seguente.

<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Switch e possibili variabili</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>/i nome file</strong></td>
<td>File o directory di input da filtrare. Il nome del file può contenere i caratteri jolly <code>*</code> e <code>?</code> .</td>
</tr>
<tr class="even">
<td><strong>/l</strong></td>
<td>I messaggi di log vengono indirizzati a un file anziché sullo schermo. I messaggi di log descrivono i singoli test eseguiti e i risultati superati/non superati dei test. Il nome del file di log corrisponde al nome del file di input, ma con estensione log.</td>
</tr>
<tr class="odd">
<td><strong>/d</strong></td>
<td>I messaggi dump vengono indirizzati a un file anziché sullo schermo. I messaggi di dump descrivono il contenuto dei blocchi. Viene dump della struttura del blocco quando il livello di dettaglio è 3. Il nome del file dump corrisponde al nome del file di input, ma con estensione dmp.</td>
</tr>
<tr class="even">
<td><strong>/-l</strong></td>
<td>Disabilitare la registrazione. Questo flag esegue l'override <code>/l</code> dell'opzione .</td>
</tr>
<tr class="odd">
<td><strong>/-d</strong></td>
<td>Disabilitare il dump. Questo flag esegue l'override <code>/d</code> dell'opzione .</td>
</tr>
<tr class="even">
<td><strong>/v integer</strong></td>
<td>Livello di dettaglio. Il valore predefinito è 3.
<ul>
<li>0 : il test registra solo i messaggi relativi a errori <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>specifici dell'interfaccia IFilter.</strong></a> Il test esegue il dump del contenuto del blocco.</li>
<li>1 : il test registra i messaggi di avviso e quelli per il livello 0.</li>
<li>2 - Il test registra i messaggi relativi ai test superati e quelli per il livello 1.</li>
<li>3 - Il test registra i messaggi informativi e quelli per il livello 2. Inoltre, il test esegue il dump della struttura del blocco.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>/t integer</strong></td>
<td>Numero di thread da avviare. Il valore predefinito è 1.</td>
</tr>
<tr class="even">
<td><strong>/r integer</strong>]</td>
<td>Filtra in modo ricorsivo le sottodirectory. Il parametro integer facoltativo specifica la profondità a cui eseguire la ricorsione. Se non viene specificato alcun numero intero o se il numero intero è 0, viene presupposta la ricorsione completa. Per impostazione predefinita, la profondità della ricorsione è 1.</td>
</tr>
<tr class="odd">
<td><strong>/c integer</strong></td>
<td>Numero di cicli. Se il numero intero è 0, il test viene cicliato all'infinito. Per impostazione predefinita, il test viene cicliato una sola volta.</td>
</tr>
</tbody>
</table>

> [!NOTE]  
> È necessario includere uno spazio tra l'opzione della riga di comando e il valore .

### <a name="filtdumpexe"></a>filtdump.exe

Il filtdump.exe carica un gestore di filtri per un documento specificato e stampa l'output prodotto dalla DLL [**IFilter.**](/windows/win32/api/filter/nn-filter-ifilter) Nell'esempio seguente viene illustrato come richiamare il filtdump.exe programma.

```
filtdump filename.ext
```
Filtdump.exe usa il [metodo ILoadFilter::LoadIFilter](/windows/desktop/api/filtereg/nf-filtereg-iloadfilter-loadifilter) per caricare la DLL [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) appropriata per l'estensione di file specificata e stampa i risultati. Ad esempio, il comando seguente indica filtdump.exe caricare il gestore di filtri smpfilt.dll per l'estensione smp, estrarre tutto il testo e le proprietà dal file myfile.smp e stampare i risultati.

```
filtdump myfile.smp
```

### <a name="filtregexe"></a>filtreg.exe

Il filtreg.exe controlla le informazioni [**di installazione di IFilter**](/windows/win32/api/filter/nn-filter-ifilter) nel Registro di sistema. È possibile richiamare il filtreg.exe dalla riga di comando digitandone il nome, come nell'esempio seguente.

```
filtreg
```

Filtreg.exe enumera tutte le estensioni di file a cui sono associati gestori di filtri stampando l'estensione del nome file e il nome della DLL [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) per l'estensione. Si tratta di un modo semplice per verificare la corretta installazione di **un filtro IFilter.**

### <a name="ifilttstini"></a>ifilttst.ini

[**Un'interfaccia IFilter**](/windows/win32/api/filter/nn-filter-ifilter) viene inizializzata chiamando il [**metodo IFilter::Init.**](/windows/win32/api/filter/nf-filter-ifilter-init) Il **metodo IFilter::Init** accetta i quattro parametri seguenti:

1. *grfFlags*
2. *Attributi cAttributes*
3. *aAttributes*
4. *pdwFlags*

L'utente del programma ifilttst.exe del gruppo di test [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) può specificare i valori per questi parametri in un file denominato ifilttst.ini. Nella tabella seguente vengono descritte le voci nel file ifilttst.ini che specificano i primi tre parametri (i parametri di input). Per un file di esempio, vedere [Esempio ifilttst.ini File](#sample-ifilttstini-file).

> [!NOTE]  
> Non è presente alcuna voce di tabella *per il parametro pdwFlags* perché è un parametro di output. non deve avere alcun valore speciale prima della chiamata al [**metodo IFilter::Init.**](/windows/win32/api/filter/nf-filter-ifilter-init)

 | Voce         | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Flags         | Nomi dei flag [**\_ IFILTER INIT**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) che devono essere uniti dall'operatore OR per formare il parametro *grfFlags* del [**metodo IFilter::Init.**](/windows/win32/api/filter/nf-filter-ifilter-init) I nomi dei flag devono essere tutti maiuscoli e sulla stessa riga.                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| *cAttributes* | Intero decimale che rappresenta il valore del *parametro cAttributes.*                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| *aAttributes* | Questa voce deve iniziare con *aAttributes* e deve essere diversa dalle altre *voci aAttributes* all'interno della sezione. I nomi validi per *la voce aAttributes* sono: *aAttributes*, *aAttributes1*, *aAttributes2* e così via. Il primo token deve essere un GUID. Il GUID deve essere formattato esattamente come illustrato nella `[Test3]` sezione Sample ifilttst.ini [File](#sample-ifilttstini-file). Il secondo token può essere un identificatore di proprietà (PID) costituito da un numero in notazione esadecimale o un puntatore a una stringa di caratteri wide (lpwstr). È possibile specificare un lpwstr racchiudendo la stringa tra virgolette doppie, come illustrato nella sezione `[Test6]` Sample ifilttst.ini File. |

Se le voci Flags *e cAttributes* non vengono specificate, il valore predefinito è 0. Se si imposta *cAttributes* su 2, è necessario specificare due *nomi aAttributes.* Nella sezione `[Test5]` dell'esempio *cAttributes* è 1, ma non è stato specificato *alcun oggetto aAttributes.* Il test chiama quindi il [**metodo IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) con *cAttributes* uguale a 1 e *aAttributes* uguale a **NULL.** Si tratta di un test case perché è probabile che si sia verificata una violazione di accesso nel **metodo IFilter::Init.**

Se ifilttst.exe trovare un file denominato ifilttst.ini nella directory di lavoro, viene usata una configurazione predefinita per inizializzare [**l'oggetto IFilter::Init.**](/windows/win32/api/filter/nf-filter-ifilter-init) Nell'esempio seguente viene illustrata la configurazione predefinita.

```
[default]
            grfFlags = IFILTER_INIT_APPLY_INDEX_ATTRIBUTES
            cAttributes = 0

```

### <a name="sample-ifilttstini-file"></a>File ifilttst.ini di esempio

Il ifilttst.ini file è organizzato in sezioni, con il nome della sezione racchiuso tra parentesi quadre. Nell'esempio le sezioni sono denominate `[Test1]` `[Test2]` , e così via. Tutti i nomi di sezione devono essere univoci. Il test legge i valori della prima sezione e inizializza [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) con tali valori. Quindi tutti i test vengono eseguiti usando questa **configurazione IFilter.** Il filtro **IFilter viene** quindi rilasciato e reinizializzato, usando i parametri elencati in precedenza. Il processo viene ripetuto fino a quando non vengono testate tutte le configurazioni.

```
; Only extract text from the object
            [Test1]
            Flags =
            cAttributes = 0

            // Get all attributes (text-type and internal value-type properties.
            [Test2]
            Flags = IFILTER_INIT_APPLY_INDEX_ATTRIBUTES
            cAttributes = 0

            // This also extracts just text from the object (the GUID is PSGUID_STORAGE, and the propid is
            // PID_STG_CONTENTS).
            [Test3]
            Flags = IFILTER_INIT_CANON_PARAGRAPHS IFILTER_INIT_HARD_LINE_BREAKS
            cAttributes = 1
            aAttributes1 = b725f130-47ef-101a-a5f1-02608c9eebac 13

            // Only extract requested attribute from the html object (the GUID corresponds to the HTML IFilter.
            [Test4]
            Flags = IFILTER_INIT_CANON_HYPHENS IFILTER_INIT_CANON_SPACES
            cAttributes = 1
            aAttributes1 = 70eb7a10-55d9-11cf-b75b-00aa0051fe20 2

            // Question: what happens if cAttributes is nonzero, but aAttributes is empty?
            [Test5]
            Flags = IFILTER_INIT_CANON_SPACES IFILTER_INIT_APPLY_INDEX_ATTRIBUTES IFILTER_INIT_APPLY_OTHER_ATTRIBUTES
            cAttributes = 1

            // Here is an attribute with a lpwstr instead of a propid (the lpwstr is enclosed in quotes).
            // The GUID corresponds to the meta tag clsid for the HTML IFilter.
            [Test6]
            Flags =
            cAttributes = 1
            aAttributes1 = D1B5D3F0-C0B3-11CF-9A92-00A0C908DBF1 "GENERATOR"
```

## <a name="ifilter-test-procedure"></a>Procedura di test IFilter

Dopo [**l'inizializzazione di IFilter,**](/windows/win32/api/filter/nn-filter-ifilter) il ifilttst.exe esegue una serie di test su **IFilter.** Oltre a seguire le procedure di test **IFilter,** assicurarsi che l'implementazione **di IFilter** si avvala di procedure di codice sicure. Vedere "Secure Code Practices for Windows Search" in [Implementing Filter Handlers in Windows Search](-search-ifilter-constructing-filters.md).

### <a name="validation-test"></a>Test di convalida

Il test di convalida passa attraverso l'oggetto un blocco alla volta, verificando ogni singolo blocco e tutti i codici restituiti. Il test di convalida salva tutte le [**strutture CHUNK STAT \_**](/windows/win32/api/filter/ns-filter-stat_chunk) restituite in un elenco.

Il test di convalida verifica le condizioni seguenti:

- [**STAT \_ CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk).*Gli ID blocco idChunk* devono essere univoci e in aumento.
- [**STAT \_ CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk).*il* parametro flags è uno stato di blocco riconosciuto, ad esempio le costanti [**CHUNKSTATE,**](/windows/win32/api/filter/ne-filter-chunkstate)CHUNK TEXT o \_ CenabledHUNK \_ VALUE.
- [**STAT \_ CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk).*il parametro breakType* è un tipo di interruzione riconosciuto (0, 1, 2, 3, 4).
- Se gli [**attributi di inizializzazione IFilter**](/windows/win32/api/filter/nn-filter-ifilter) specificano che **IFilter** deve restituire solo blocchi contenenti proprietà interne di tipo valore, *idChunkSource* deve essere uguale a 0.
- Se il blocco non è derivato, se non è una proprietà interna di tipo valore, [**STAT \_ CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk).*idChunkSource* deve essere uguale a **STAT \_ CHUNK.***idChunk*.
- [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) restituisce S OK o un altro valore restituito accettabile, ad esempio \_ FILTER E END OF \_ \_ \_ \_ CHUNKS, FILTER \_ E LINK UNAVAILABLE e così \_ \_ via.
- Se il blocco contiene testo, [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) restituisce S OK, FILTER S LAST TEXT o \_ FILTER E NO MORE \_ \_ \_ \_ \_ \_ \_ TEXT.
- Se [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) restituisce FILTER S LAST TEXT, la chiamata successiva \_ a \_ \_ **IFilter::GetText** restituisce FILTER \_ E NO MORE \_ \_ \_ TEXT.
- Se il blocco contiene un valore, [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) restituisce S \_ OK o FILTER E NO MORE \_ \_ \_ \_ VALUES.

### <a name="consistency-test"></a>Test di coerenza

Il ifilttxt.exe inizializza nuovamente [**l'interfaccia IFilter**](/windows/win32/api/filter/nn-filter-ifilter) con gli stessi parametri del test di convalida ed esegue un test di coerenza. Se l'implementazione **di IFilter** è stata inizializzata con il flag [**IFILTER \_ INIT INIT**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) INDEXING ONLY, il test rilascia l'interfaccia IFilter e la associa nuovamente prima di effettuare un'altra chiamata al metodo \_ \_ \_ [**IFilter::Init.**](/windows/win32/api/filter/nf-filter-ifilter-init) 

Il test di coerenza verifica le condizioni seguenti:

- Ogni [**struttura STAT \_ CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk) restituita dal [**metodo IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) è identica alla corrispondente **struttura STAT \_ CHUNK** restituita nel test di convalida.
- [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) restituisce S OK o un altro valore restituito accettabile, ad esempio \_ FILTER E END OF \_ \_ \_ \_ CHUNKS, FILTER \_ E LINK UNAVAILABLE e così \_ \_ via.

### <a name="invalid-input-test"></a>Test di input non valido

Il ifilttst.exe inizializza nuovamente [**l'interfaccia IFilter**](/windows/win32/api/filter/nn-filter-ifilter) con gli stessi parametri ed esegue un test di input non valido. Questo test passa attraverso il documento un blocco alla volta effettuando chiamate di funzione in modo non corretto, ad esempio chiamando il metodo [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) quando l'oggetto corrente contiene testo. Il test verifica la conformità di tutti i codici restituiti alla **specifica IFilter.**

Il test di input non valido verifica le condizioni seguenti:

- Se il blocco corrente contiene testo, [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) restituisce FILTER E NO VALUES e una chiamata \_ \_ a \_ [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) ha esito positivo.
- Se il blocco corrente contiene un valore, [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) restituisce FILTER E NO TEXT e una chiamata \_ \_ a \_ [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) ha esito positivo.
- Se la chiamata precedente a [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) ha restituito FILTER E NO MORE TEXT, le chiamate successive a \_ \_ \_ \_ **IFilter::GetText** restituiscono FILTER \_ E \_ NO MORE \_ \_ TEXT.
- Se la chiamata precedente a [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) ha restituito FILTER E NO MORE VALUES, le chiamate successive a \_ \_ \_ \_ **IFilter::GetValue** restituiscono FILTER \_ E \_ NO MORE \_ \_ VALUES.
- Se la chiamata precedente a [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) ha restituito FILTER E END OF CHUNKS, le chiamate successive a \_ \_ \_ \_ **IFilter::GetChunk** restituiscono FILTER \_ E END OF \_ \_ \_ CHUNKS.

> [!NOTE]  
> Il test di input non valido confronta le strutture di blocchi correnti con quelle restituite nel test di convalida per assicurarsi che siano identiche.

### <a name="testing-different-ifilter-configurations"></a>Test di configurazioni IFilter diverse

Il ifilttst.exe rilascia [**l'interfaccia IFilter**](/windows/win32/api/filter/nn-filter-ifilter) e riassocia, questa volta inizializzando l'interfaccia con il set di parametri successivo. Il test ripete il ciclo: test di convalida, test di coerenza e test di input non valido, fino [a](#ifilttstini) quando non vengono testate tutte le configurazioni **IFilter** desiderate specificateifilttst.inifile.

## <a name="ensuring-registered-items-get-indexed"></a>Verifica dell'indicizzazione degli elementi registrati

Il test finale [**dell'IFilter**](/windows/win32/api/filter/nn-filter-ifilter) garantisce che **l'IFilter** sia registrato correttamente e che venga richiamato per indicizzare gli elementi registrati per usarlo. È possibile usare Gestione cataloghi per avviare nuovamente l'indicizzazione o usare Gestione ambito ricerca per indicizzazione (CSM) per configurare regole predefinite che indicano gli URL per cui si vuole che l'indicizzatore eserciti la ricerca per indicizzazione. Al termine dell'indicizzazione, usare l'interfaccia Windows di ricerca per cercare una stringa nel contenuto o nelle proprietà degli elementi. Se gli elementi sono stati indicizzati, verranno visualizzati nei risultati della ricerca.

Per altre informazioni sulla re-indicizzazione, vedere [Using the Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) e Using the [Gestione ambito ricerca per indicizzazione](-search-3x-wds-extidx-csm.md). L'esempio di codice ReindexMatchingUrls illustra come specificare i file da reindicizzare e come. L'esempio di codice CrawlScopeCommandLine illustra come definire le opzioni della riga di comando per le operazioni di Gestione ambito ricerca per indicizzazione (CSM). Entrambi gli esempi di codice sono disponibili [in GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch).

### <a name="sample-log-file"></a>File di log di esempio

Su richiesta, il Ifilttst.exe può produrre un log contenente una descrizione dei passaggi da eseguire durante l'esecuzione. Gli esempi seguenti sono estratti da un file di log, con il livello di dettaglio impostato sul valore più alto possibile 3.

```
            1. INFO----**** New configuration ****
            2.
            3. Section name : Test2
            4. grfFlags     : 63
            5. cAttributes  : 0
            6. aAttributes  : NONE
            7. pdwFlags     : 0
            8.
            9. INFO----Successfully bound filter.
            10.
            11. PASS----Init() returned a valid value for pdwFlags.
            12.
            13. INFO----Successfully initialized filter.
            14.
            15. INFO----Performing validation test. In this part of the test, the chunks structures
            16.         returned by the IFilter are checked for correctness, and the return values
            17.         of the IFilter calls are checked.
            18.
            19. PASS----GetChunk() succeeded.
            20.
            21. PASS----The current chunk has a legal value for the flags field.

```

La prima riga è un messaggio informativo che indica che è stata caricata una nuova configurazione dal file ifilttst.ini file. La riga (3) indica il nome della sezione nel file ifilttst.ini da cui è stata letta la configurazione corrente. Le righe da 4 a (7) elencano i parametri per [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init). Le righe che `INFO` iniziano con sono messaggi informativi sull'associazione di [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) e sull'inizio del test di convalida. Le righe che `PASS` iniziano con sono messaggi relativi a test specifici superati.

La riga nell'esempio di log seguente è un avviso. Gli avvisi richiamano [**l'attenzione**](/windows/win32/api/filter/nn-filter-ifilter) sul comportamento di IFilter che è problematico, anche se legale. Questo avviso indica che il [**metodo IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) ha restituito un blocco di testo che non contiene testo.

```
WARNING-First call to GetText() returned FILTER_E_NO_MORE_TEXT.
```

Il messaggio di errore di esempio seguente indica che [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ha generato un blocco che non è stato richiesto.

```
            ERROR---The IFilter has emitted a chunk which it was not requested to emit.
            Check the initialization parameters in section Test1 of the initialization file.
            INFO----Current chunk propid : 0x5
```

Nel caso di questo messaggio di errore di esempio, [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ha generato un blocco con un PID di `0x5` . L'ispezione della sezione ifilttst.ini che IFilter è stato configurato per non `[Test1]` generare blocchi con questo PID.  Ad esempio, se né IFILTER INIT APPLY INDEX ATTRIBUTES né IFILTER INIT APPLY OTHER ATTRIBUTES sono stati specificati nella voce Flags e \_ \_ se \_ \_ \_ \_ \_ \_ *cAttributes* è 0, **IFilter** `0x13` \_ \_ genera solo blocchi con un PID di e corrispondente a PID STG CONTENTS.

### <a name="sample-dump-file"></a>File di dump di esempio

Su richiesta, il Ifilttst.exe può produrre un dump contenente i blocchi trovati e il relativo contenuto. L'esempio seguente è un estratto di un file dump di questo tipo.

```
                1. Chunk ID: ........... 2
                2. Chunk Break Type: ... END OF SENTENCE
                3. Chunk State: ........ TEXT
                4. Chunk Locale: ....... 0x411
                5. Chunk Source ID: .... 2
                6. Chunk Start Source .. 0x0
                7. Chunk Length Source . 0x0
                8. GUID ................ b725f130-47ef-101a-a5f1-02608c9eebac
                9. Property ID ......... 0x13

                10. This is a HTML IFilter test page

                11. Chunk ID: ........... 3
                12. Chunk Break Type: ... END OF SENTENCE
                13. Chunk State: ........ TEXT
                14. Chunk Locale: ....... 0x411
                15. Chunk Source ID: .... 2
                16. Chunk Start Source .. 0x0
                17. Chunk Length Source . 0x0
                18. GUID ................ f29f85e0-4ff9-1068-ab91-08002b27b3d9
                19. Property ID ......... 0x2

                20. This is a HTML IFilter test page

                21. Chunk ID: ........... 4
                22. Chunk Break Type: ... END OF SENTENCE
                23. Chunk State: ........ VALUE
                24. Chunk Locale: ....... 0x411
                25. Chunk Source ID: .... 2
                26. Chunk Start Source .. 0x0
                27. Chunk Length Source . 0x0
                28. GUID ................ f29f85e0-4ff9-1068-ab91-08002b27b3d9
                29. Property ID ......... 0x2

                30. This is an HTML IFilter test page
```

Le prime nove righe descrivono la struttura del blocco corrente. Il GUID e il PID corrispondono a PSGUID \_ STORAGE/PID \_ STG \_ CONTENTS. Si tratta di un blocco contenente testo normale. Il testo si trova nella struttura del blocco seguente:

```
10. This is an HTML IFilter test page
```

Il blocco successivo, a partire dalla riga 11, ha un GUID diverso, corrispondente a , e `HTML IFilter` un PID diverso, corrispondente a un HREF HTML. Si tratta di una proprietà interna di tipo valore, esportata da `HTML IFilter` .

Il blocco successivo, a partire dalla riga 21, ha lo stesso GUID e PID, ma lo stato del blocco `VALUE` è invece di `TEXT` . Si noti che il testo in questi ultimi due blocchi è uguale a quello del primo blocco. Tuttavia, poiché [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) è progettato per l'applicazione di tre attributi (testo normale, HREF HTML come testo e HREF HTML come valore) a questa frase, i risultati vengono generati in tre blocchi separati.

## <a name="additional-resources"></a>Risorse aggiuntive

- L'esempio di codice [IFilterSample,](-search-sample-ifiltersample.md) disponibile in [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), illustra come creare una classe di base IFilter per l'implementazione [**dell'interfaccia IFilter.**](/windows/win32/api/filter/nn-filter-ifilter)
- Per una panoramica del processo di indicizzazione, vedere [Processo di indicizzazione.](-search-indexing-process-overview.md)
- Per una panoramica dei tipi di file, vedere [Tipi di file.](../shell/fa-file-types.md)
- Per eseguire query su attributi di associazione di file per un tipo di file, vedere [PerceivedTypes, SystemFileAssociations e Registrazione dell'applicazione.](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))

## <a name="related-topics"></a>Argomenti correlati

[Sviluppo di gestori di filtri](-search-ifilter-conceptual.md)

[Informazioni sui gestori di filtri in Windows ricerca](-search-ifilter-about.md)

[Procedure consigliate per la creazione di gestori di filtri in Windows ricerca](-search-3x-wds-extidx-filters.md)

[Restituzione di proprietà da un gestore di filtri](-search-ifilter-property-filtering.md)

[Gestori di filtri forniti con Windows](-search-ifilter-implementations.md)

[Implementazione di gestori di filtri in Windows ricerca](-search-ifilter-constructing-filters.md)

[Registrazione di gestori di filtri](-search-ifilter-registering-filters.md)

---
description: Il gruppo di test IFilter convalida i gestori dei filtri.
ms.assetid: 5ee02af1-1dc9-4d21-868f-4c439970b1ba
title: Test di gestori filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d2a2b0b6a6728051ab22590a481ad23a7197692
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128563"
---
# <a name="testing-filter-handlers"></a>Test di gestori filtro

Il gruppo di test [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) convalida i gestori dei filtri. Il gruppo di test esegue questa operazione: chiamando i metodi [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) e controllando la conformità dei valori restituiti con la specifica dell'interfaccia **IFilter** ; e verificare che gli identificatori del blocco siano univoci e in aumento, che l'interfaccia **IFilter** si comportano in modo coerente dopo la reinizializzazione e che tutte le chiamate al metodo **IFilter** con parametri non validi restituiscono codici di errore previsti. I programmi del gruppo di test effettuano inoltre il dump dell'output di un file filtrato da un gestore di filtri e controllano le informazioni di registrazione **IFilter** nel registro di sistema.

Questo argomento è organizzato nel modo seguente:

- [Chiamata della riga di comando](#command-line-invocation)
  - [ifilttst.exe](#ifilttstexe)
  - [filtdump.exe](#filtdumpexe)
  - [filtreg.exe](#filtregexe)
  - [ifilttst.ini](#ifilttstini)
- [Procedura di test di IFilter](#ifilter-test-procedure)
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
> Se è in corso l'installazione di un nuovo gestore di filtro per un tipo di file in sostituzione di una registrazione filtro esistente, il programma di installazione deve salvare la registrazione corrente e ripristinarla se il nuovo gestore di filtro viene disinstallato. Non esiste alcun meccanismo per concatenare i filtri. Di conseguenza, il nuovo gestore di filtro è responsabile della replica di tutte le funzionalità necessarie del filtro precedente.

## <a name="command-line-invocation"></a>Chiamata di Command-Line

Il gruppo di test [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) è costituito da tre applicazioni da riga di comando: [ifilttst.exe](#ifilttstexe), [filtdump.exe](#filtdumpexe)e [filtreg.exe](#filtregexe) e da un file di inizializzazione, [ifilttst.ini](#ifilttstini).

> [!IMPORTANT]
> In Windows 7 e versioni successive, i filtri scritti nel codice gestito vengono bloccati in modo esplicito. I filtri devono essere scritti in codice nativo a causa di potenziali problemi di controllo delle versioni di Common Language Runtime (CLR) con il processo di esecuzione di più componenti aggiuntivi.

### <a name="ifilttstexe"></a>ifilttst.exe

Il programma ifilttst.exe esegue diversi test per convalidare un gestore di filtro. Nell'esempio seguente viene illustrato come richiamare il programma ifilttst.exe dalla riga di comando:


```
ifilttst /i test.htm /l /d /v 1
```

Nell'esempio vengono eseguite le attività seguenti:

- Indica al programma di filtrare il file test.htm
- Reindirizza i messaggi di log a test.htm. log
- Reindirizza i messaggi di dump a test.htm. dmp
- Imposta il livello di dettaglio su 1

Per il corretto funzionamento del comando precedente, è necessario che i tre file si trovino nella directory di lavoro corrente: `test.htm` , [ifilttst.exe](#ifilttstexe)e [ifilttst.ini](#ifilttstini). Nella tabella seguente sono elencate le opzioni della riga di comando.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Switch e possibili variabili</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>nome file/i</strong></td>
<td>File o directory di input da filtrare. Il nome del file può contenere i caratteri jolly <code>*</code> e <code>?</code> .</td>
</tr>
<tr class="even">
<td><strong>/l</strong></td>
<td>I messaggi di log vengono indirizzati a un file anziché allo schermo. I messaggi di log descrivono i singoli test eseguiti e i risultati superati o non superati dei test. Il nome del file di log corrisponde al nome del file di input ma con estensione. log.</td>
</tr>
<tr class="odd">
<td><strong>/d</strong></td>
<td>Il dump dei messaggi viene indirizzato a un file anziché allo schermo. I messaggi dump descrivono il contenuto dei blocchi. Il dump della struttura del blocco viene eseguito quando il livello di dettaglio è 3. Il nome del file di dump corrisponde al nome del file di input ma con estensione dmp.</td>
</tr>
<tr class="even">
<td><strong>/-l</strong></td>
<td>Disabilitare la registrazione. Questo flag sostituisce l' <code>/l</code> opzione.</td>
</tr>
<tr class="odd">
<td><strong>/-d</strong></td>
<td>Disabilitare il dump. Questo flag sostituisce l' <code>/d</code> opzione.</td>
</tr>
<tr class="even">
<td><strong>/v Integer</strong></td>
<td>Livello di dettaglio. Il valore predefinito è 3.
<ul>
<li>0: il test registra solo i messaggi relativi a errori di interfaccia <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> specifici. Il test eseguirà il dump del contenuto del blocco.</li>
<li>1-il test registra i messaggi di avviso e quelli per il livello 0.</li>
<li>2: il test registra i messaggi relativi ai test superati, oltre a quelli per il livello 1.</li>
<li>3: il test registra i messaggi informativi e quelli per il livello 2. Inoltre, il test eseguirà il dump della struttura del blocco.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>/t Integer</strong></td>
<td>Numero di thread da avviare. Il valore predefinito è 1.</td>
</tr>
<tr class="even">
<td><strong>/r Integer</strong>]</td>
<td>Filtra in modo ricorsivo le sottodirectory. Il parametro integer facoltativo specifica la profondità a cui esercitare la ricorsione. Se non viene specificato alcun Integer o se il valore integer è 0, viene utilizzata la ricorsione completa. Per impostazione predefinita, la profondità di ricorsione è 1.</td>
</tr>
<tr class="odd">
<td><strong>/c Integer</strong></td>
<td>Il numero di volte in cui eseguire il ciclo. Se il valore integer è 0, il test viene eseguito in un ciclo infinito. Per impostazione predefinita, i cicli di test sono una sola volta.</td>
</tr>
</tbody>
</table>

> [!NOTE]  
> È necessario includere uno spazio tra l'opzione della riga di comando e il valore.

### <a name="filtdumpexe"></a>filtdump.exe

Il programma filtdump.exe carica un gestore di filtro per un documento specificato e stampa l'output generato dalla dll [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) . Nell'esempio seguente viene illustrato come richiamare il programma filtdump.exe.

```
filtdump filename.ext
```
Filtdump.exe usa il metodo [ILoadFilter:: LoadIFilter](/windows/desktop/api/filtereg/nf-filtereg-iloadfilter-loadifilter) per caricare la dll [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) appropriata per l'estensione del nome file specificata e stampa i risultati. Il comando seguente, ad esempio, indica filtdump.exe di caricare il gestore di filtri smpfilt.dll per l'estensione SMP, estrarre tutto il testo e le proprietà dal file MyFile. SMP e stampare i risultati.

```
filtdump myfile.smp
```

### <a name="filtregexe"></a>filtreg.exe

Il programma filtreg.exe controlla le informazioni di installazione di [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) nel registro di sistema. Per richiamare il programma filtreg.exe dalla riga di comando, digitarne il nome, come nell'esempio seguente.

```
filtreg
```

Filtreg.exe enumera tutte le estensioni di file a cui sono associati gestori di filtro stampando l'estensione del nome file e il nome della dll [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) per l'estensione. Si tratta di un modo semplice per verificare l'installazione corretta di un **IFilter**.

### <a name="ifilttstini"></a>ifilttst.ini

Un'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) viene inizializzata chiamando il metodo [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) . Il metodo **IFilter:: init** accetta i quattro parametri seguenti:

1. *grfFlags*
2. *cAttributes*
3. *aAttributes*
4. *pdwFlags*

L'utente del programma ifilttst.exe del gruppo di test [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) può specificare i valori per questi parametri in un file denominato ifilttst.ini. Nella tabella seguente vengono descritte le voci del file ifilttst.ini che specificano i primi tre parametri, ovvero i parametri di input. Per un file di esempio, vedere [esempio di file di ifilttst.ini](#sample-ifilttstini-file).

> [!NOTE]  
> Non è presente alcuna voce di tabella per il parametro *pdwFlags* perché è un parametro di output. non deve avere alcun valore speciale prima della chiamata al metodo [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) .

 | Voce         | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Flags         | Nomi dei flag di [**\_ inizializzazione IFilter**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) che devono essere Uniti dall'operatore OR per formare il parametro *grfFlags* del metodo [**IFILTER:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) . I nomi dei flag devono essere tutti in maiuscolo e sulla stessa riga.                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| *cAttributes* | Intero decimale che rappresenta il valore del parametro *CAttributes* .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| *aAttributes* | Questa voce deve iniziare con *aAttributes* e deve essere diversa dalle altre voci *aAttributes* nella sezione. I nomi validi per la voce *aAttributes* sono: *aAttributes*, *aAttributes1*, *aAttributes2* e così via. Il primo token deve essere un GUID. Il GUID deve essere formattato esattamente come illustrato nella `[Test3]` sezione del [File di ifilttst.ini di esempio](#sample-ifilttstini-file). Il secondo token può essere un identificatore di proprietà (PID) costituito da un numero in notazione esadecimale o un puntatore a una stringa di caratteri wide (LPWSTR). È possibile specificare LPWSTR racchiudendo la stringa tra virgolette doppie, come illustrato nella `[Test6]` sezione del file di ifilttst.ini di esempio. |

Se non si specificano le voci Flags e *CAttributes* , il valore predefinito è 0. Se si imposta *CAttributes* uguale a 2, è necessario specificare due nomi *aAttributes* . Nella `[Test5]` sezione dell'esempio *CAttributes* è 1, ma non è stato specificato alcun *aAttributes* . Il test chiama quindi il metodo [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) con *CAttributes* uguale a 1 e *aAttributes* uguale a **null**. Si tratta di un test case utile perché è probabile che si verifichi una violazione di accesso nel metodo **IFilter:: init** .

Se ifilttst.exe non riesce a trovare un file denominato ifilttst.ini nella directory di lavoro, viene usata una configurazione predefinita per inizializzare l'oggetto [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) . Nell'esempio seguente viene illustrata la configurazione predefinita.

```
[default]
            grfFlags = IFILTER_INIT_APPLY_INDEX_ATTRIBUTES
            cAttributes = 0

```

### <a name="sample-ifilttstini-file"></a>File ifilttst.ini di esempio

Il file di ifilttst.ini è organizzato in sezioni, con il nome della sezione racchiuso tra parentesi quadre. Nell'esempio, le sezioni sono denominate `[Test1]` , `[Test2]` e così via. Tutti i nomi di sezione devono essere univoci. Il test legge i valori dalla prima sezione e Inizializza l' [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) con tali valori. Quindi, tutti i test vengono eseguiti utilizzando questa configurazione **IFilter** . Quindi, l' **IFilter** viene rilasciato e reinizializzato, usando i parametri elencati in precedenza. Il processo viene ripetuto fino a quando non vengono testate tutte le configurazioni.

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

## <a name="ifilter-test-procedure"></a>Procedura di test di IFilter

Dopo l'inizializzazione di [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) , il programma ifilttst.exe esegue una serie di test sull' **IFilter**. Oltre a seguire le procedure di test di **IFilter** , assicurarsi che l'implementazione di **IFilter** usi procedure di codice sicure. Vedere "procedure di sicurezza del codice per la ricerca di Windows" nell' [implementazione di gestori di filtri in Windows Search](-search-ifilter-constructing-filters.md).

### <a name="validation-test"></a>Test di convalida

Il test di convalida passa l'oggetto un blocco alla volta, verificando ogni singolo blocco e tutti i codici restituiti. Il test di convalida Salva tutte le strutture di [**\_ blocco stat**](/windows/win32/api/filter/ns-filter-stat_chunk) restituite in un elenco.

Il test di convalida verifica le condizioni seguenti:

- [**\_ Blocco stat**](/windows/win32/api/filter/ns-filter-stat_chunk).** gli ID blocco idChunk devono essere univoci e incrementali.
- [**\_ Blocco stat**](/windows/win32/api/filter/ns-filter-stat_chunk).*il parametro flags* è uno stato di blocco riconosciuto, ad esempio [**CHUNKSTATE**](/windows/win32/api/filter/ne-filter-chunkstate), chunk \_ text o CenabledHUNK \_ value costanti.
- [**\_ Blocco stat**](/windows/win32/api/filter/ns-filter-stat_chunk).** il parametro breakType è un tipo di break riconosciuto (0, 1, 2, 3, 4).
- Se gli attributi di inizializzazione [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) specificano che **IFilter** deve restituire solo blocchi contenenti proprietà del tipo di valore interno, *idChunkSource* deve essere uguale a 0.
- Se il blocco non è derivato, ovvero se non è una proprietà del tipo di valore interna, il blocco [**Stat \_**](/windows/win32/api/filter/ns-filter-stat_chunk).*idChunkSource* deve essere uguale a **\_ blocco stat**.*idChunk*.
- [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) restituisce \_ OK o un altro valore restituito accettabile, ad esempio il filtro \_ e la \_ fine \_ dei \_ blocchi, il \_ collegamento filtro e non \_ \_ disponibile e così via.
- Se il blocco contiene testo, [**IFilter:: GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) restituisce \_ OK, \_ Last Text del \_ filtro \_ o filtro \_ E non è \_ \_ più \_ testo.
- Se [**IFilter:: GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) restituisce \_ il filtro S \_ Last \_ text, la chiamata successiva a **IFILTER:: GetText** restituisce Filter \_ E \_ non \_ più \_ testo.
- Se il blocco contiene un valore, [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) restituisce S \_ OK o Filter \_ E \_ non \_ più \_ valori.

### <a name="consistency-test"></a>Test di coerenza

Il programma di ifilttxt.exe Reinizializza nuovamente l'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) con gli stessi parametri del test di convalida ed esegue un test di coerenza. Se l'implementazione di **IFilter** è stata inizializzata con il flag IFilter [**\_ init**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) IFilter \_ init \_ indicizzazione \_ solo, il test rilascia l'interfaccia **IFilter** e la associa nuovamente prima di effettuare un'altra chiamata al metodo [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) .

Il test di coerenza verifica le condizioni seguenti:

- Ogni struttura del [**\_ blocco stat**](/windows/win32/api/filter/ns-filter-stat_chunk) restituita dal metodo [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) è identica al **\_ blocco stat** corrispondente restituito nel test di convalida.
- [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) restituisce \_ OK o un altro valore restituito accettabile, ad esempio il filtro \_ e la \_ fine \_ dei \_ blocchi, il \_ collegamento filtro e non \_ \_ disponibile e così via.

### <a name="invalid-input-test"></a>Test di input non valido

Il programma di ifilttst.exe Reinizializza nuovamente l'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) con gli stessi parametri ed esegue un test di input non valido. Questo test esegue il documento un blocco alla volta, facendo in modo non corretto le chiamate di funzione, ad esempio chiamando il metodo [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) quando il mandrino corrente contiene testo. Il test controlla tutti i codici restituiti per la conformità con la specifica **IFilter** .

Il test di input non valido verifica le condizioni seguenti:

- Se il blocco corrente contiene testo, [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) restituisce il filtro \_ e \_ nessun \_ valore e una chiamata a [**IFilter:: GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) ha esito positivo.
- Se il blocco corrente contiene un valore, [**IFilter:: GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) restituisce Filter \_ e \_ nessun \_ testo e una chiamata a [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) ha esito positivo.
- Se la chiamata precedente a [**IFilter:: GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) ha restituito Filter \_ e \_ nessun \_ altro \_ testo, le chiamate successive a **IFILTER:: GetText** restituiscono Filter \_ e \_ non \_ più \_ testo.
- Se la chiamata precedente a [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) ha restituito \_ un filtro e \_ non \_ più \_ valori, le chiamate successive a **IFILTER:: GetValue** restituiscono il filtro \_ e \_ non \_ più \_ valori.
- Se la chiamata precedente a [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) ha restituito il filtro \_ e \_ \_ la fine dei \_ blocchi, le chiamate successive a **IFilter:: GetChunk** restituiscono il filtro \_ e \_ \_ la fine dei \_ blocchi.

> [!NOTE]  
> Il test di input non valido Confronta le strutture dei blocchi correnti con quelle restituite nel test di convalida per assicurarsi che siano identiche.

### <a name="testing-different-ifilter-configurations"></a>Test di configurazioni IFilter diverse

Il programma ifilttst.exe rilascia l'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) e la riassociazione, questa volta inizializzarla con il set di parametri successivo. Il test ripete il ciclo: test di convalida, test di coerenza e test di input non valido, fino a quando non sono state testate tutte le configurazioni **IFilter** desiderate specificate in [ifilttst.ini](#ifilttstini) file.

## <a name="ensuring-registered-items-get-indexed"></a>Verifica dell'indicizzazione degli elementi registrati

Il test finale dell' [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) garantisce che **IFilter** sia registrato correttamente e che venga richiamato per indicizzare gli elementi registrati per l'utilizzo. È possibile utilizzare Gestione catalogo per avviare la reindicizzazione o utilizzare il gestore dell'ambito di ricerca per indicizzazione (CSM) per configurare le regole predefinite che indicano gli URL di cui si desidera eseguire la ricerca nell'indicizzatore. Al termine dell'indicizzazione, utilizzare l'interfaccia utente di ricerca di Windows per cercare una stringa nel contenuto o nelle proprietà degli elementi. Se gli elementi sono stati indicizzati, verranno visualizzati nei risultati della ricerca.

Per ulteriori informazioni sulla reindicizzazione, vedere [utilizzo di gestione catalogo](-search-3x-wds-mngidx-catalog-manager.md) e [utilizzo di gestione ambito ricerca per indicizzazione](-search-3x-wds-extidx-csm.md). L'esempio di codice ReindexMatchingUrls illustra i modi per specificare i file da indicizzare e il modo in cui. Nell'esempio di codice CrawlScopeCommandLine viene illustrato come definire le opzioni della riga di comando per le operazioni di indicizzazione di gestione dell'ambito di ricerca (CSM). Entrambi gli esempi di codice sono disponibili in [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch).

### <a name="sample-log-file"></a>File di log di esempio

Al momento della richiesta, il programma Ifilttst.exe può produrre un log contenente una descrizione dei passaggi necessari durante l'esecuzione. Gli esempi seguenti sono estratti da un file di log, con il livello di dettaglio impostato sul valore massimo possibile 3.

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

La prima riga è un messaggio informativo, che indica che una nuova configurazione è stata caricata dal file di ifilttst.ini. Riga (3) indica il nome della sezione nel file di ifilttst.ini da cui è stata letta la configurazione corrente. Righe (4) fino a (7) elenca i parametri per [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init). Le righe che iniziano con `INFO` sono messaggi informativi sull'associazione dell' [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) e sull'inizio del test di convalida. Le righe che iniziano con `PASS` sono messaggi relativi a test specifici che sono stati superati.

La riga nell'esempio di log seguente è un avviso. Gli avvisi chiamano l'attenzione sul comportamento di [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) problematico, anche se valido. Questo avviso indica che il metodo [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) ha restituito un blocco di testo che non contiene testo.

```
WARNING-First call to GetText() returned FILTER_E_NO_MORE_TEXT.
```

Il messaggio di errore di esempio seguente indica che [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ha emesso un blocco non richiesto.

```
            ERROR---The IFilter has emitted a chunk which it was not requested to emit.
            Check the initialization parameters in section Test1 of the initialization file.
            INFO----Current chunk propid : 0x5
```

Nel caso di questo messaggio di errore di esempio, l' [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ha emesso un blocco con un PID di `0x5` . L'ispezione della sezione `[Test1]` in ifilttst.ini indicherà che **IFilter** è stato configurato in modo da non generare blocchi con questo PID. Se, ad esempio, non \_ si applicano gli attributi di indice di IFilter init \_ \_ \_ o IFilter \_ init, gli \_ \_ altri \_ attributi sono stati specificati nella voce dei flag e se *CAttributes* è 0, **IFilter** genera solo i blocchi con un PID di `0x13` e corrispondente al \_ \_ contenuto del valore del PID.

### <a name="sample-dump-file"></a>File di dump di esempio

Al momento della richiesta, il programma Ifilttst.exe può produrre un dump contenente i blocchi trovati e il relativo contenuto. L'esempio seguente è un Estratto di un file dump di questo tipo.

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

Le prime nove righe descrivono la struttura del blocco corrente. Il GUID e il PID corrispondono al contenuto dell'PSGUID di \_ archiviazione/PID \_ STG \_ . Si tratta di un blocco contenente testo normale. Il testo si trova nella struttura di blocco seguente:

```
10. This is an HTML IFilter test page
```

Il blocco successivo, a partire dalla riga 11, ha un GUID diverso, corrispondente a `HTML IFilter` e un PID diverso, corrispondente a un href HTML. Si tratta di una proprietà del tipo di valore interna, esportata da `HTML IFilter` .

Il blocco successivo, a partire dalla riga 21, ha lo stesso GUID e PID, ma lo stato del blocco è `VALUE` invece di `TEXT` . Si noti che il testo negli ultimi due blocchi è identico a quello del primo blocco. Tuttavia, poiché [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) è progettato per tre attributi (testo normale, html href come testo e html href come valore) da applicare a questa frase, i risultati vengono emessi in tre blocchi distinti.

## <a name="additional-resources"></a>Risorse aggiuntive

- Nell'esempio di codice [IFilterSample](-search-sample-ifiltersample.md) , disponibile in [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), viene illustrato come creare una classe di base IFilter per implementare l'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .
- Per una panoramica del processo di indicizzazione, vedere [il processo di indicizzazione](-search-indexing-process-overview.md).
- Per una panoramica dei tipi di file, vedere [tipi di file](../shell/fa-file-types.md).
- Per eseguire query sugli attributi di associazione file per un tipo di file, vedere [PerceivedTypes, SystemFileAssociations e registrazione dell'applicazione](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).

## <a name="related-topics"></a>Argomenti correlati

[Sviluppo di gestori di filtri](-search-ifilter-conceptual.md)

[Informazioni sui gestori di filtro in Windows Search](-search-ifilter-about.md)

[Procedure consigliate per la creazione di gestori di filtro in Windows Search](-search-3x-wds-extidx-filters.md)

[Restituzione di proprietà da un gestore di filtro](-search-ifilter-property-filtering.md)

[Gestori di filtri forniti con Windows](-search-ifilter-implementations.md)

[Implementazione di gestori di filtro in Windows Search](-search-ifilter-constructing-filters.md)

[Registrazione di gestori di filtro](-search-ifilter-registering-filters.md)

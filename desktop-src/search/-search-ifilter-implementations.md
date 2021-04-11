---
description: Microsoft fornisce diversi filtri standard con Windows Search. I client chiamano questi gestori di filtro (che sono implementazioni dell'interfaccia IFilter) per estrarre testo e proprietà da un documento.
ms.assetid: e19ae220-5c59-482e-8b02-00889600c4d6
title: Gestori di filtri forniti con Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dd5603ab913117e2c968a7508b2fa061dfb4034
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128567"
---
# <a name="filter-handlers-that-ship-with-windows"></a>Gestori di filtri forniti con Windows

Microsoft fornisce diversi filtri standard con Windows Search. I client chiamano questi gestori di filtro (che sono implementazioni dell'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ) per estrarre testo e proprietà da un documento.

Questo argomento è organizzato nel modo seguente:

- [Note sull'implementazione di Windows Search](#windows-search-implementation-notes)
  - [Implementazione di Windows 7 e 10](#windows-7-and-10-implementation)
  - [Implementazione di Windows Vista](#windows-vista-implementation)
  - [Implementazione legacy](#legacy-implementation)
- [Filtri di ricerca di Windows](#filter-handlers-that-ship-with-windows)
  - [Gestore filtro MIME](#mime-filter-handler)
  - [Gestore filtro HTML](#html-filter-handler)
  - [Gestore filtro documenti](#document-filter-handler)
  - [Gestore filtro testo normale](#plain-text-filter-handler)
  - [Gestore di filtro binario o null](#binary-or-null-filter-handler)
- [Risorse aggiuntive](#additional-resources)
- [Argomenti correlati](#related-topics)

## <a name="windows-search-implementation-notes"></a>Note sull'implementazione di Windows Search

In Windows 7 e versioni successive, i filtri scritti nel codice gestito vengono bloccati in modo esplicito. I filtri devono essere scritti in codice nativo a causa di potenziali problemi di controllo delle versioni di CLR con il processo di esecuzione di più componenti aggiuntivi.

### <a name="windows-7-and-10-implementation"></a>Implementazione di Windows 7 e 10

In Windows 7 e versioni successive è presente un nuovo comportamento che si verifica quando si registra un gestore di filtro, un gestore di proprietà o una nuova estensione. Quando viene installato un nuovo gestore di proprietà e/o un gestore di filtro, i file con le estensioni corrispondenti vengono reindicizzati automaticamente.

In Windows 7 e versioni successive, è consigliabile installare un gestore di filtri insieme ai gestori di proprietà corrispondenti e registrare il gestore di filtro prima del gestore della proprietà. La registrazione del gestore delle proprietà avvia la reindicizzazione immediata dei file indicizzati in precedenza senza prima richiedere un riavvio e sfrutta tutti i gestori di filtro precedentemente registrati ai fini dell'indicizzazione del contenuto.

Se solo un gestore di filtro viene installato senza un gestore di proprietà corrispondente, la reindicizzazione automatica viene eseguita dopo il riavvio del servizio di indicizzazione o il riavvio del sistema.

Per i flag di descrizione della proprietà specifici di Windows 7, vedere gli argomenti di riferimento seguenti: [GETPROPERTYSTOREFLAGS](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags), [tipo di PROPDESC \_ COLUMNINDEX \_ ](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type) e [ \_ \_ flag PROPDESC SEARCHINFO](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags).

### <a name="windows-vista-implementation"></a>Implementazione di Windows Vista

In Windows Vista e versioni precedenti, l'installazione di un gestore di proprietà o [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) non avvia una reindicizzazione degli elementi esistenti a meno che un fornitore di software indipendente (ISV) non chiami in modo esplicito una ricompilazione o una reindicizzazione degli URL corrispondenti.

Esistono due principali differenze tra le applicazioni legacy, ad esempio il servizio di indicizzazione e le applicazioni più recenti, come Windows Search, di cui è necessario tenere conto quando si implementano i filtri:

- Utilizzo dell'interfaccia [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) .
- Uso dei gestori di proprietà.

Per prima cosa, Windows Vista e Windows Search 3,0 e versioni successive richiedono l'uso di [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) per i motivi seguenti:

- Per garantire prestazioni e compatibilità futura.
- Per aumentare la sicurezza. I filtri implementati con [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) sono più sicuri perché il contesto in cui viene eseguito il filtro non necessita dei diritti per aprire i file sul disco o sulla rete.

Mentre Windows Search USA solo [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream), è anche possibile includere nell' [interfaccia IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) e/o nelle implementazioni dell' [interfaccia IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) nei filtri per la compatibilità con le versioni precedenti.

La seconda differenza principale è che Windows Vista e Windows Search 3,0 e versioni successive dispongono di un nuovo [sistema di proprietà](../properties/building-property-handlers.md) che utilizza i gestori di proprietà per enumerare le proprietà degli elementi.

Tuttavia, in alcuni casi è necessario implementare un filtro che gestisce il contenuto e le proprietà per:

- Supportano le implementazioni di MSSearch legacy.
- Attraversare i collegamenti.
- Mantieni le informazioni sulla lingua.
- Filtrare in modo ricorsivo gli elementi incorporati.

In questi casi, è necessaria un'implementazione del filtro completo, incluso il metodo [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) per accedere ai valori delle proprietà.

### <a name="legacy-implementation"></a>Implementazione legacy

Come accennato in precedenza, Windows Vista e Windows Search includono un nuovo sistema di proprietà che incapsula le proprietà di un elemento separate dal contenuto di un elemento. Questo sistema di proprietà non esiste nelle versioni precedenti di Microsoft Windows Desktop Search (WDS) 2. x. Se il filtro deve supportare altre applicazioni, come descritto in precedenza, potrebbe essere necessario gestire sia il contenuto che le proprietà.

Per ulteriori informazioni sullo sviluppo di un filtro compatibile, vedere gli argomenti seguenti, [IFilter (per le applicazioni legacy)](/windows/win32/api/filter/nn-filter-ifilter)e [sviluppo di componenti aggiuntivi di filtro (per le applicazioni legacy)](../lwef/-search-2x-wds-ifilteraddins.md).

## <a name="windows-search-filters"></a>Filtri di ricerca di Windows

Microsoft fornisce diversi filtri standard con Windows Search. Il contenuto della dll [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)  viene riepilogato nella tabella seguente. Facendo clic sul nome di un gestore di filtro si passa alla descrizione dell'implementazione di **IFilter** .

| Gestore filtro                                                  | File filtrati                              | DLL IFilter  |
|-----------------------------------------------------------------|---------------------------------------------|--------------|
| [Gestore filtro MIME](#mime-filter-handler)                     | Multipurpose Internet Mail Extension (MIME) | mimefilt.dll |
| [Gestore filtro HTML](#html-filter-handler)                     | HTML 3,0 o versioni precedenti                         | nlhtml.dll   |
| [Gestore filtro documenti](#document-filter-handler)             | Microsoft Word, Excel, PowerPoint           | offfilt.dll  |
| [Gestore filtro testo normale](#plain-text-filter-handler)         | File di testo normale-IFilter predefinito          | query.dll    |
| [Gestore di filtro binario o null](#binary-or-null-filter-handler) | File binari-IFilter null                 | query.dll    |

### <a name="mime-filter-handler"></a>Gestore filtro MIME

Il gestore del filtro MIME (in mimefilt.dll) estrae le informazioni di testo e proprietà da file con estensioni. eml,. mht e. MHTML.

### <a name="html-filter-handler"></a>Gestore filtro HTML

Il gestore del filtro HTML (in nlhtml.dll) estrae le informazioni di testo e proprietà dalla classe "HtmlFiles" in modo che possa essere indicizzata tramite la ricerca di Windows. Per una descrizione dell'associazione tra [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) e il tipo di file, vedere "ricerca della dll IFilter per un file" in [registrazione dei gestori di filtro](-search-ifilter-registering-filters.md).

È possibile usare la `META` funzionalità tag dei documenti HTML per inviare richieste di gestione speciali all' [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)HTML. `META` i tag si verificano in prossimità dell'inizio di un file HTML all'interno dei `HEAD ... /HEAD` tag, come illustrato nell'esempio seguente.

```XML
   <head>
     <META NAME="DESCRIPTION"
           CONTENT="This text appears on the results page as the document's summary.">
   </head>
```

Alcuni `META` tag HTML vengono automaticamente mappati a valori noti per set di proprietà e ID proprietà (PID), in modo che le query su queste proprietà effettuino ricerche nel contenuto mappato. Alcuni esempi sono elencati nella tabella seguente. Per un elenco delle proprietà di sistema che è possibile usare per i formati di file, vedere [proprietà definite dal sistema per formati di file personalizzati](-shell-systemdefinedpropertiesforfileformats.md).

| Esempio di proprietà                              | Mapping a                                                               |
|-----------------------------------------------|-------------------------------------------------------------------------|
| meta Name = "Author" Content = "Ruth"             | Proprietà Author nel set di proprietà delle informazioni di riepilogo.            |
| meta Name = "Subject" Content = "elaborazione di testi" | Proprietà Subject nel set di proprietà informazioni di riepilogo.           |
| meta Name = "keywords" Content = "Fonts, serif"   | Proprietà della parola chiave nel set di proprietà delle informazioni di riepilogo.           |
| meta Name = "ms. Category" Content = "fiction"     | Proprietà Category nel set di proprietà informazioni di riepilogo del documento. |

Alcune funzionalità del [**IFILTER**](/windows/win32/api/filter/nn-filter-ifilter) HTML sono elencate nella tabella seguente.

[comment]: # (Questa tabella deve essere HTML per fare in modo che gli esempi vengano formattati correttamente)

<!-- markdownlint-disable MD033 -->
<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Attività</th>
<th>Operazione</th>
<th>Esempio</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Creazione di abstract speciali da file</td>
<td>Usare il <code>META NAME=&quot;DESCRIPTION&quot;...</code> tag per indicare a <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> di usare la stringa che segue la <code>CONTENT</code> parola chiave come abstract del documento.
<blockquote>
[!Note]<br />
Il processo di filtro può generare abstract per ogni file filtrato, che per impostazione predefinita è un set di caratteri all'inizio del file.
</blockquote>
<br/></td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
&lt;head&gt;
  &lt;META NAME=&quot;DESCRIPTION&quot; CONTENT=&quot;This text will appear on the results page as the document&#39;s summary.&quot;&gt;
&lt;/head&gt;
 </pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>Prevenzione del filtraggio di singoli file</td>
<td>Aggiungere un <code>meta name</code> tag al file.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
  &lt;meta name=&quot;robots&quot; content=&quot;noindex&quot;&gt;
</pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>Impostazione del codice lingua per un file (per garantire che il sistema scelga i Word breaker e i file di parole non significative corretti)</td>
<td>Aggiungere il <code>meta name</code> tag seguente al file, in cui il campo contenuto specifica il codice lingua appropriato (in caratteri o usando il valore delle impostazioni locali).</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
&lt;meta name=&quot;ms.locale&quot; content=&quot;EN&quot;&gt;
&lt;meta name=&quot;ms.locale&quot; content=1033&gt;
</pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>
<!-- markdownlint-enable MD033 -->

### <a name="document-filter-handler"></a>Gestore filtro documenti

Il gestore del filtro del documento (in offilt.dll) filtra i file per alcune estensioni dei documenti Microsoft Office. Sono inclusi i file con estensione doc, mdb, PPT e XLT, ad esempio.

### <a name="plain-text-filter-handler"></a>Gestore filtro testo normale

Per i file di testo normale, in Windows Search viene utilizzato il gestore del filtro del testo, che consente di filtrare le proprietà di sistema, ad esempio i nomi dei file, e il contenuto di un file. Quando un tipo di file non dispone di un'associazione [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) nel registro di sistema, Windows Search indicizza solo le proprietà della Shell per il file. Tuttavia, l'utente può utilizzare le **Opzioni avanzate** nel pannello di controllo **Opzioni di indicizzazione** per **indicizzare proprietà** o **proprietà di indice e contenuto del file**.

![screenshot che mostra la finestra di dialogo Opzioni avanzate](images/ifilteradvancedoptions.png)

Se l'utente sceglie questa opzione per un tipo di file senza un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)associato, viene utilizzato il gestore del filtro del testo per estrarre il contenuto del file. Il gestore del filtro del testo non "comprende" qualsiasi formato di documento; Quando si filtra il contenuto di un file, il file viene considerato come una sequenza di caratteri. Verifica il contrassegno Unicode per l'ordine dei byte all'inizio del file.

### <a name="binary-or-null-filter-handler"></a>Gestore di filtro binario o null

Quando viene rilevato un file binario registrato, viene utilizzato il gestore di filtri null. Il gestore di filtro null recupera solo le proprietà di sistema. Il contenuto di un file binario non viene filtrato. Esempi di proprietà di sistema sono **filename**, **LastWriteTime**, **Filesize** e **Attributes**.

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

[Implementazione di gestori di filtro in Windows Search](-search-ifilter-constructing-filters.md)

[Registrazione di gestori di filtro](-search-ifilter-registering-filters.md)

[Test di gestori filtro](-search-ifilter-testing-filters.md)

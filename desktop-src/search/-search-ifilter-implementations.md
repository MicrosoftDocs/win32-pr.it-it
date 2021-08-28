---
description: Microsoft fornisce diversi filtri standard con Windows ricerca. I client chiamano questi gestori filtri (implementazioni dell'interfaccia IFilter) per estrarre testo e proprietà da un documento.
ms.assetid: e19ae220-5c59-482e-8b02-00889600c4d6
title: Gestori di filtri forniti con Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1a245978482e0334d91e35031aa80186fd2cb32
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624367"
---
# <a name="filter-handlers-that-ship-with-windows"></a>Gestori di filtri forniti con Windows

Microsoft fornisce diversi filtri standard con Windows ricerca. I client chiamano questi gestori filtri (implementazioni [**dell'interfaccia IFilter)**](/windows/win32/api/filter/nn-filter-ifilter) per estrarre testo e proprietà da un documento.

Questo argomento è organizzato come segue:

- [Windows Note sull'implementazione della ricerca](#windows-search-implementation-notes)
  - [Windows 7 e 10 Implementazione](#windows-7-and-10-implementation)
  - [Windows Implementazione di Vista](#windows-vista-implementation)
  - [Implementazione legacy](#legacy-implementation)
- [Windows Filtri di ricerca](#filter-handlers-that-ship-with-windows)
  - [Gestore filtri MIME](#mime-filter-handler)
  - [Gestore filtri HTML](#html-filter-handler)
  - [Gestore del filtro dei documenti](#document-filter-handler)
  - [Gestore filtro testo normale](#plain-text-filter-handler)
  - [Gestore di filtri binari o Null](#binary-or-null-filter-handler)
- [Risorse aggiuntive](#additional-resources)
- [Argomenti correlati](#related-topics)

## <a name="windows-search-implementation-notes"></a>Windows Note sull'implementazione della ricerca

In Windows 7 e versioni successive, i filtri scritti nel codice gestito vengono bloccati in modo esplicito. I filtri DEVONO essere scritti in codice nativo a causa di potenziali problemi di controllo delle versioni CLR con il processo in cui vengono eseguiti più componenti aggiuntivi.

### <a name="windows-7-and-10-implementation"></a>Windows 7 e 10 Implementazione

In Windows 7 e versioni successive, è presente un nuovo comportamento che si verifica quando si registra un gestore filtri, un gestore delle proprietà o una nuova estensione. Quando viene installato un nuovo gestore delle proprietà e/o un gestore filtri, i file con le estensioni corrispondenti vengono indicizzati automaticamente.

In Windows 7 e versioni successive, è consigliabile installare un gestore filtri in combinazione con i gestori delle proprietà corrispondenti e registrare il gestore del filtro prima del gestore della proprietà. La registrazione del gestore delle proprietà avvia la nuova indicizzazione immediata dei file indicizzati in precedenza senza prima richiedere un riavvio e sfrutta tutti i gestori di filtri registrati in precedenza ai fini dell'indicizzazione del contenuto.

Se viene installato solo un gestore filtri senza un gestore delle proprietà corrispondente, la nuova indicizzazione automatica viene eseguita dopo un riavvio del servizio di indicizzazione o un riavvio del sistema.

Per i flag di descrizione delle proprietà specifici di Windows 7, vedere gli argomenti di riferimento seguenti: [GETPROPERTYSTOREFLAGS,](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags) [PROPDESC \_ COLUMNINDEX \_ TYPE](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type) e [PROPDESC \_ SEARCHINFO \_ FLAGS](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags).

### <a name="windows-vista-implementation"></a>Windows Implementazione di Vista

In Windows Vista e versioni precedenti, l'installazione di [**un IFilter**](/windows/win32/api/filter/nn-filter-ifilter) o di un gestore di proprietà non avvia una nuova indicizzazione degli elementi esistenti a meno che un fornitore di software indipendente (ISV) non chiami in modo esplicito una ricompilazione o una nuova indicizzazione degli URL corrispondenti.

Esistono due differenze principali tra le applicazioni legacy, ad esempio il servizio di indicizzazione e le applicazioni più nuove, ad esempio Windows Search, di cui è necessario tenere conto durante l'implementazione dei filtri:

- Uso [dell'interfaccia IPersistStream.](/windows/win32/api/objidl/nn-objidl-ipersiststream)
- Uso di gestori di proprietà.

Prima di Windows Vista e Windows Search 3.0 e versioni successive è necessario [usare IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) per i motivi seguenti:

- Per garantire le prestazioni e la compatibilità futura.
- Per aumentare la sicurezza. I filtri [implementati con IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) sono più sicuri perché il contesto in cui viene eseguito il filtro non richiede i diritti per aprire file sul disco o in rete.

Anche Windows ricerca usa [solo IPersistStream,](/windows/win32/api/objidl/nn-objidl-ipersiststream)è anche possibile includere le implementazioni dell'interfaccia [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) e/o [dell'interfaccia IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) nei filtri per garantire la compatibilità con le versioni precedenti.

La seconda differenza principale è che Windows Vista e Windows Search 3.0 [](../properties/building-property-handlers.md) e versioni successive hanno un nuovo sistema di proprietà che usa i gestori delle proprietà per enumerare le proprietà degli elementi.

Tuttavia, in alcuni casi è necessario implementare un filtro che gestisce sia il contenuto che le proprietà per:

- Supportare le implementazioni di MSSearch legacy.
- Attraversare i collegamenti.
- Mantenere le informazioni sulla lingua.
- Filtrare in modo ricorsivo gli elementi incorporati.

In queste situazioni è necessaria un'implementazione completa del filtro, incluso il metodo [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) per accedere ai valori delle proprietà.

### <a name="legacy-implementation"></a>Implementazione legacy

Come illustrato in precedenza, Windows Vista e Windows Search includono un nuovo sistema di proprietà che incapsula le proprietà di un elemento separato dal contenuto di un elemento. Questo sistema di proprietà non esiste nelle versioni precedenti di Microsoft Windows Desktop Search (WDS) 2.x. Se il filtro deve supportare altre applicazioni come descritto in precedenza, potrebbe essere necessario gestire sia il contenuto che le proprietà.

Per altre informazioni sullo sviluppo di un filtro compatibile, vedere gli argomenti seguenti, [IFilter (per](/windows/win32/api/filter/nn-filter-ifilter)le applicazioni legacy) e Sviluppo di componenti aggiuntivi filtro [(per le applicazioni legacy).](../lwef/-search-2x-wds-ifilteraddins.md)

## <a name="windows-search-filters"></a>Windows Filtri di ricerca

Microsoft fornisce diversi filtri standard con Windows ricerca. Il contenuto della DLL [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)  è riepilogato nella tabella seguente. Facendo clic sul nome di un gestore filtri si visualizza la descrizione **dell'implementazione di IFilter.**

| Gestore filtri                                                  | File filtrati                              | IFilter DLL  |
|-----------------------------------------------------------------|---------------------------------------------|--------------|
| [Gestore filtri MIME](#mime-filter-handler)                     | Multipurpose Internet Mail Extension (MIME) | mimefilt.dll |
| [Gestore filtri HTML](#html-filter-handler)                     | HTML 3.0 o versioni precedenti                         | nlhtml.dll   |
| [Gestore del filtro dei documenti](#document-filter-handler)             | Microsoft Word, Excel, PowerPoint           | offfilt.dll  |
| [Gestore filtro testo normale](#plain-text-filter-handler)         | File di testo normale - Filtro IFilter predefinito          | query.dll    |
| [Gestore di filtri binari o Null](#binary-or-null-filter-handler) | File binari - IFilter Null                 | query.dll    |

### <a name="mime-filter-handler"></a>Gestore filtri MIME

Il gestore del filtro MIME (in mimefilt.dll) estrae testo e informazioni sulle proprietà dai file con le estensioni .eml, .mht e .mhtml.

### <a name="html-filter-handler"></a>Gestore filtri HTML

Il gestore del filtro HTML (in nlhtml.dll) estrae le informazioni di testo e proprietà dalla classe "htmlfiles" in modo che possa essere indicizzata Windows Ricerca. Per una descrizione dell'associazione [**tra IFilter**](/windows/win32/api/filter/nn-filter-ifilter) e il tipo di file, vedere "Ricerca della DLL IFilter per un file" in [Registrazione dei gestori filtri](-search-ifilter-registering-filters.md).

È possibile usare la `META` funzionalità tag dei documenti HTML per trasmettere richieste di gestione speciali all'IFilter HTML. [](/windows/win32/api/filter/nn-filter-ifilter) `META` I tag si verificano vicino all'inizio di un file HTML all'interno dei `HEAD ... /HEAD` tag, come illustrato nell'esempio seguente.

```XML
   <head>
     <META NAME="DESCRIPTION"
           CONTENT="This text appears on the results page as the document's summary.">
   </head>
```

Alcuni tag HTML vengono mappati automaticamente ai valori PID (Property Identifier) e set di proprietà noti, in modo che le query su queste proprietà esereranno la ricerca nel contenuto `META` mappato. Nella tabella seguente sono elencati alcuni esempi. Per un elenco delle proprietà di sistema che è possibile usare per i formati di file, vedere Proprietà definite dal sistema [per i formati di file personalizzati](-shell-systemdefinedpropertiesforfileformats.md).

| Esempio di proprietà                              | Mapping a                                                               |
|-----------------------------------------------|-------------------------------------------------------------------------|
| meta name="author" content="ruth"             | Proprietà author nel set di proprietà Summary Information.            |
| meta name="subject" content="word processing" | Proprietà subject nel set di proprietà Summary Information.           |
| meta name="keywords" content="fonts, serif"   | Proprietà della parola chiave nel set di proprietà Informazioni di riepilogo.           |
| meta name="ms.category" content="fiction"     | Proprietà category nel set di proprietà Summary Information del documento. |

Alcune funzionalità del [**filtro IFilter**](/windows/win32/api/filter/nn-filter-ifilter) HTML sono elencate nella tabella seguente.

[comment]: # (Per formattare correttamente gli esempi, questa tabella deve essere HTML)

<!-- markdownlint-disable MD033 -->
<table>
<colgroup>
<col  />
<col  />
<col  />
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
<td>Creazione di astrazioni speciali dai file</td>
<td>Usare il <code>META NAME=&quot;DESCRIPTION&quot;...</code> tag per indicare a <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> di usare la stringa che segue la <code>CONTENT</code> parola chiave come documento astratto.
<blockquote>
[!Note]<br />
Il processo di filtro può generare astrazioni per ogni file filtrato, che per impostazione predefinita è un set di caratteri all'inizio del file.
</blockquote>
<br/></td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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
<td>Impedire che singoli file vengano filtrati</td>
<td>Aggiungere un <code>meta name</code> tag al file.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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
<td>Impostazione del codice lingua per un file (per assicurarsi che il sistema scempi i word breaker e i file di parole non corrette)</td>
<td>Aggiungere il tag seguente al file , in cui il campo del contenuto specifica il codice lingua appropriato (in caratteri o usando <code>meta name</code> il valore delle impostazioni locali).</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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

### <a name="document-filter-handler"></a>Gestore del filtro dei documenti

Il gestore del filtro documento (in offilt.dll) filtra i file per alcune estensioni dei documenti in Microsoft Office. Ad esempio, i file con .doc, mdb, .ppt e xlt.

### <a name="plain-text-filter-handler"></a>Gestore del filtro di testo normale

Per i file di testo normale, Windows ricerca usa il gestore del filtro di testo, che filtra sia le proprietà di sistema (ad esempio i nomi di file) che il contenuto di un file. Quando un tipo di file non ha un'associazione [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) nel Registro di sistema, Windows ricerca indicizza solo le proprietà della shell per il file. Tuttavia, l'utente può usare **opzioni avanzate** nel pannello di controllo **Opzioni** di indicizzazione per **proprietà** indice o Proprietà indice e **Contenuto file**.

![Screenshot che mostra la finestra di dialogo Opzioni avanzate](images/ifilteradvancedoptions.png)

Se l'utente sceglie questa opzione per un tipo di file senza un [**filtro IFilter**](/windows/win32/api/filter/nn-filter-ifilter)associato, il gestore del filtro di testo viene usato per estrarre il contenuto del file. Il gestore del filtro di testo non "comprende" alcun formato di documento. Quando si filtra il contenuto di un file, il file viene trattato come una sequenza di caratteri. Verifica l'indicatore dell'ordine dei byte Unicode all'inizio del file.

### <a name="binary-or-null-filter-handler"></a>Gestore del filtro binario o Null

Quando viene rilevato un file binario registrato, viene usato il gestore di filtri Null. Il gestore del filtro Null recupera solo le proprietà di sistema. Il contenuto di un file binario non viene filtrato. Esempi di proprietà di sistema **sono FileName**, **LastWriteTime**, **FileSize** e **Attributes**.

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

[Implementazione di gestori di filtri in Windows ricerca](-search-ifilter-constructing-filters.md)

[Registrazione di gestori di filtri](-search-ifilter-registering-filters.md)

[Test dei gestori di filtri](-search-ifilter-testing-filters.md)

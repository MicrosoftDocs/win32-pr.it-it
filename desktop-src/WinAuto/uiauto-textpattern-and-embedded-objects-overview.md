---
title: Come automazione interfaccia utente espone oggetti incorporati
description: Questo argomento descrive il modo in cui automazione interfaccia utente Microsoft espone oggetti incorporati o elementi figlio in un documento o un contenitore di testo.
ms.assetid: 5ecf5e94-5329-4abb-aedb-4e303688e5f7
keywords:
- Automazione interfaccia utente, panoramica del modello di testo
- Automazione interfaccia utente, Cenni preliminari sui controlli testo
- Automazione interfaccia utente, pattern di controllo Text
- Automazione interfaccia utente, Cenni preliminari sugli oggetti incorporati
- Automazione interfaccia utente, esposizione di oggetti incorporati
- Automazione interfaccia utente, scenari per oggetti incorporati
- modelli di testo, informazioni
- controlli testo, informazioni
- Pattern di controllo Text
- pattern di controllo, testo
- oggetti incorporati
- esposizione di oggetti incorporati
ms.topic: article
ms.date: 08/31/2019
ms.openlocfilehash: b85d7fa9e068400e3a339625acad1036a4cdd111
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727511"
---
# <a name="how-ui-automation-exposes-embedded-objects"></a>Come automazione interfaccia utente espone oggetti incorporati

Questo argomento descrive il modo in cui automazione interfaccia utente Microsoft usa i pattern di controllo Text e TextRange per esporre oggetti incorporati (elementi figlio/discendenti) in un documento o un contenitore di testo.

Per l'automazione dell'interfaccia utente, un oggetto incorporato è qualsiasi elemento con limiti non testuali, ad esempio un'immagine, un collegamento ipertestuale, una tabella o un tipo di documento (foglio di calcolo di Microsoft Excel, file Microsoft Windows Media e così via).

> [!NOTE]
> Questo comportamento è diverso dalla definizione OLE (COM) Component Object Model (vedere [oggetti incorporati](../com/embedded-objects.md)), in cui viene creato un elemento in un'applicazione e incorporato o collegato in un'altra applicazione. Il fatto che l'oggetto possa essere modificato nell'applicazione originale sia irrilevante nel contesto dell'automazione dell'interfaccia utente.

## <a name="embedded-objects-and-the-ui-automation-tree"></a>Oggetti incorporati e albero di automazione interfaccia utente

Gli oggetti incorporati vengono considerati come singoli elementi nella visualizzazione controlli dell'albero di automazione interfaccia utente. Vengono esposti come elementi figlio del contenitore di testo, in modo che sia possibile accedervi tramite lo stesso modello a oggetti di altri controlli nell'automazione interfaccia utente.

Nella tabella seguente sono elencati esempi di elementi contenitore e non contenitore.

:::row:::
   :::column span="2":::

      **Elementi contenitore**

   :::column-end:::
   :::column span="":::

      **Elementi non contenitore**

   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::

- Calendario
- Combobox
- DataGrid
- Documento
- Modifica
- Group
- Intestazione
- HeaderItem
- Elenco
- Menu

   :::column-end:::
   :::column span="":::

- MenuBar
- Riquadro
- SplitButton
- Scheda
- Tabella
- Barra degli strumenti
- Albero
- TreeItem
- Finestra

   :::column-end:::
   :::column span="":::

- Collegamento
- Caselle
- Pulsante

  :::column-end:::
:::row-end:::

Nell'immagine seguente viene illustrato un contenitore di testo (documento) con una tabella e un'immagine incorporata.

![illustrazione che mostra un documento con una tabella e un'immagine incorporata](images/embeddedtable.jpg)

Il diagramma seguente illustra la visualizzazione del contenuto di automazione interfaccia utente del documento precedente.

![diagramma della visualizzazione del contenuto di automazione interfaccia utente di un documento con oggetti incorporati](images/contenttree.jpg)

### <a name="compatible-and-non-compatible-embedded-objects"></a>Oggetti incorporati "compatibili" e "non compatibili"

Alcuni provider di automazione interfaccia utente utilizzano lo stesso archivio di testo per ogni oggetto TextPattern in essi contenuti.  Gli oggetti supportati dallo stesso archivio di testo del contenitore sono detti oggetti incorporati "compatibili". Questi oggetti possono essere oggetti TextPattern stessi e, in questo caso, gli intervalli di testo sono confrontabili con gli intervalli di testo ottenuti dal relativo contenitore. In questo modo i provider possono esporre le informazioni client sui singoli oggetti TextPattern come se fossero un provider di testo di grandi dimensioni.

Tuttavia, i provider possono usare archivi di testo diversi per oggetti TextPattern diversi incorporati in un contenitore TextPattern. Gli oggetti non supportati dall'archivio di testo del contenitore sono detti oggetti incorporati "non compatibili". Questi tipi di oggetti incorporati possono essere o meno oggetti basati su TextPattern.  

Nella tabella seguente sono elencati alcuni esempi di oggetti incorporati compatibili e non compatibili.

|   | Oggetti incorporati compatibili | Oggetti incorporati non compatibili |
| --- | --- | --- |
| Oggetti incorporati non di TextPattern | Pulsante in Microsoft Edge<br>Tabella dati in Microsoft Edge | Pulsante in RichTextBlock nel framework XAML di Microsoft<br>Immagini con alt-text in Microsoft Edge<br>ListView con ListItem in RichTextBlock nel framework XAML di Microsoft |
| Oggetti incorporati TextPattern | Controllo di input di tipo "Text" in Microsoft Edge<br>Tabella in un documento di Word | Elemento TextBox in un documento di Microsoft Word |

## <a name="exposing-embedded-objects"></a>Esposizione di oggetti incorporati

I pattern di controllo [Text e TextRange](uiauto-implementingtextandtextrange.md) espongono proprietà e metodi che facilitano la navigazione e l'esecuzione di query di oggetti incorporati.

Il contenuto testuale (o testo interno) di un contenitore di testo e di un oggetto incorporato, ad esempio un collegamento ipertestuale o una cella della tabella, viene esposto come singolo flusso di testo continuo sia nella visualizzazione controlli che nella visualizzazione contenuto dell'albero di automazione interfaccia utente. i limiti dell'oggetto vengono ignorati. Se un client di automazione interfaccia utente sta recuperando il testo per recitare, interpretare o analizzare in qualche modo, è necessario controllare l'intervallo di testo per i casi speciali, ad esempio una tabella con contenuto testuale o altri oggetti incorporati. Chiamare [**IUIAutomationTextRange:: GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) per ottenere un'interfaccia [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) per ciascun oggetto incorporato, quindi chiamare [**IUIAutomationTextPattern:: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) per ottenere un intervallo di testo per ogni elemento. Questa operazione viene eseguita in modo ricorsivo fino a quando non è stato recuperato l'intero contenuto testuale.

> [!NOTE]
> Un intervallo degenere (o compresso) è il punto in cui l'endpoint iniziale e l'endpoint finale sono uguali. Gli intervalli degenerati vengono spesso utilizzati per indicare la posizione del cursore del testo tramite i metodi [GetSelection](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextprovider-getselection) e [GetCaretRange](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextprovider2-getcaretrange) di [ITextProvider](/windows/win32/api/uiautomationcore/nn-uiautomationcore-itextprovider) .

Il diagramma seguente illustra un flusso di testo con oggetti incorporati e i relativi intervalli di intervallo.

![diagramma che mostra un flusso di testo con oggetti incorporati e i relativi intervalli di intervallo](images/rangespans.jpg)

## <a name="embedded-objects-and-textunit"></a>Oggetti incorporati e TextUnit

Un oggetto [ITextProvider](/windows/win32/api/uiautomationcore/nn-uiautomationcore-itextprovider) può essere attraversato e da un [TextUnit](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textunit)specificato. I provider che contengono oggetti incorporati possono essere attraversati nello stesso modo, ma gli oggetti incorporati interessano l'attraversamento. Ecco alcuni aspetti da tenere presenti:

- Tutti gli oggetti incorporati non compatibili sono rappresentati dal carattere di sostituzione U + FFFC nell'archivio di testo del TextPattern dell'elemento contenitore. Viene anche considerata un'unità di caratteri e un'unità di Word.
- Gli oggetti incorporati compatibili possono essere costituiti da più caratteri e parole.
- L'elemento contenitore è l'elemento più in basso che si estende sull'intero intervallo di testo.
- Gli elementi figlio di un intervallo sono anche elementi figlio di un elemento contenitore che è parzialmente o completamente racchiuso nell'intervallo.
- Idealmente, soprattutto nel caso di elementi contenitore come Table, un confine di parola non va oltre il limite dell'oggetto. Nell'esempio seguente, l'unità di parola "barra" non contiene alcuna posizione di testo esterna al `</td>` tag ( `<br \>` non fa parte della parola "barra").

```Xaml
<table style="width:100%">
  <tr>
    <th>Name</th>
    <th>Notes</th>
  </tr>
  <tr>
    <td>Eve Jackson</td>
    <td>Foo Bar</td>
  </tr>
</table>
<br/>
```

- In generale, `<br \>` viene considerato come una singola parola, in modo che non superi un limite di riga.
- Un'eccezione alla regola precedente è la posizione in cui un'unità di testo di Word contiene oggetti completi. Ad esempio, `<p>Hello <a href="#">link</a> here.</p>` , che include i contenitori inline, contiene le parole "Hello", "link" e "Here". Dove "link" ha un oggetto TextPattern come elemento contenitore e un oggetto collegamento come figlio.
- Nel caso di unità di caratteri, l'oggetto è l'elemento contenitore (le unità di testo come questa non devono contenere elementi figlio).
- Gli oggetti Annotation non devono essere rappresentati come oggetti incorporati. Ad esempio, la presenza di altri identificatori di autore in un documento co-autore.
- Gli oggetti incorporati utilizzano almeno una posizione del cursore. l'annotazione è solo metadati.
- I limiti di ogni oggetto (inizio e fine) sono rappresentati da un'interruzioni di formato nell'intervallo del documento TextPattern.
- Per HTML, ogni tag HTML non comporta necessariamente un oggetto di automazione interfaccia utente. Il contenuto all'interno dei tag di enfasi, ad esempio, <em></em> non deve essere rappresentato come elemento, bensì un flusso di testo in cui UIA_IsItalicAttributeId restituisce true.
- L'endpoint iniziale è incluso ed è l'endpoint preferito mentre l'endpoint finale è esclusivo. Questa operazione è utile quando l'intervallo è degenerato e gli endpoint iniziale e finale appartengono alla stessa posizione per tale intervallo.

## <a name="comparing-embedded-objects"></a>Confronto tra oggetti incorporati

Gli oggetti TextPattern annidati che si trovano in una relazione figlio simile e condividono lo stesso archivio di testo di backup sono denominati confrontabili. In questo caso, gli intervalli da uno degli oggetti TextPattern possono essere confrontati usando [ITextRangeProvider:: compare](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-compare) e [ITextRangeProvider:: CompareEndpoints](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-compareendpoints). Entrambe generano un valore numerico valido che ne specifica la posizione relativa.

Un oggetto non TextPattern incorporato in un oggetto TextPattern è paragonabile a TextPattern se l'oggetto ha un intervallo valido in TextPattern ([ITextProvider:: RangeFromChild](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextprovider-rangefromchild)) e il contenuto sottostante l'intervallo di testo non è vuoto e non è un carattere di sostituzione.

## <a name="embedded-textpattern-objects-and-the-document-textunit"></a>Oggetti TextPattern incorporati e documento TextUnit

Per gli oggetti TextPattern incorporati, l'unità del [documento](/windows/win32/api/uiautomationcore/ne-uiautomationcore-textunit) riconosce solo il contenuto contenuto all'interno di tale elemento.

### <a name="word-textpattern-element-hierarchy"></a>Gerarchia dell'elemento TextPattern di Word

- L'elemento document implementa TextPattern e [Document](/windows/win32/api/uiautomationcore/ne-uiautomationcore-textunit) restituisce l'intero intervallo di documenti di Word.
- Le singole pagine del documento implementano TextPattern e [Document](/windows/win32/api/uiautomationcore/ne-uiautomationcore-textunit) restituiscono il contenuto delle singole pagine (anche se le pagine condividono lo stesso archivio di testo con l'intero oggetto TextPattern).

### <a name="webpage-and-text-input-controls-in-edge"></a>Controlli di pagine Web e input di testo in Edge

- L'elemento del riquadro principale della pagina Web implementa TextPattern ed espone l'intero contenuto della pagina Web.
- I singoli controlli input di testo supportano TextPattern in cui un intervallo di documenti rappresenta il testo contenuto in ogni campo di input (anche se condividono lo stesso archivio di testo con l'intera pagina Web).

## <a name="common-scenarios"></a>Scenari comuni

In questa sezione vengono presentati esempi di scenari comuni che coinvolgono oggetti incorporati: collegamenti ipertestuali, immagini e tabelle. Negli esempi seguenti la parentesi graffa sinistra ({) rappresenta l'endpoint iniziale dell'intervallo di testo e la parentesi graffa destra (}) rappresenta l'endpoint finale.

### <a name="hyperlink-example-1-a-text-range-that-contains-an-embedded-text-hyperlink"></a>Collegamento ipertestuale esempio 1: intervallo di testo che contiene un collegamento ipertestuale con testo incorporato

L'intervallo di testo seguente contiene un collegamento ipertestuale con testo incorporato.

  {L'URL https://www.microsoft.com è incorporato nel testo}.

La chiamata ai metodi [**IUIAutomationTextRange:: GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext), [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement), [**GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)e [**IUIAutomationTextPattern:: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) comporta i comportamenti descritti nella tabella seguente.

| Metodo chiamato                                                                                                                                                                                                                                                     | Risultato                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange:: GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                                                                                                                                                                                  | Restituisce la stringa "l'URL https://www.microsoft.com è incorporato nel testo".                                                                               |
| [**IUIAutomationTextRange:: GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)                                                                                                                                                          | Restituisce l'elemento di automazione interfaccia utente più interno che racchiude l'intervallo di testo, in questo caso l'elemento di automazione che rappresenta il provider di testo stesso. |
| [**IUIAutomationTextRange:: GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)                                                                                                                                                                          | Restituisce un elemento di automazione interfaccia utente che rappresenta il controllo collegamento ipertestuale.                                                                                      |
| [**IUIAutomationTextPattern:: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild), in cui l'elemento di automazione interfaccia utente è stato restituito dal metodo [**IUIAutomationTextRange:: GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) precedente. | Restituisce l'intervallo che rappresenta " https://www.microsoft.com ".                                                                                            |
### <a name="hyperlink-example-2-a-text-range-that-partially-spans-an-embedded-text-hyperlink"></a>Collegamento ipertestuale esempio 2: intervallo di testo che si estende parzialmente su un collegamento ipertestuale con testo incorporato

L'intervallo di testo seguente si estende parzialmente su un collegamento ipertestuale con testo incorporato.

  L'URL https://{www} è incorporato nel testo.

La chiamata ai metodi [**IUIAutomationTextRange:: GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext), [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)e [**GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) comporta i comportamenti descritti nella tabella seguente.

| Metodo chiamato                                                                                            | Risultato                                                                                                         |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange:: GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                         | Restituisce la stringa "www".                                                                                      |
| [**IUIAutomationTextRange:: GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) | Restituisce l'elemento di automazione interfaccia utente più interno che racchiude l'intervallo di testo; in questo caso, il controllo collegamento ipertestuale. |
| [**IUIAutomationTextRange:: GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)                 | Restituisce **null** perché l'intervallo di testo non si estende sull'intera stringa dell'URL.                                   |

### <a name="hyperlink-example-3-a-text-range-that-partially-spans-the-content-of-a-text-container"></a>Collegamento ipertestuale esempio 3: intervallo di testo che si estende parzialmente sul contenuto di un contenitore di testo

L'intervallo di testo seguente si estende parzialmente sul contenuto di un contenitore di testo. Il contenitore di testo contiene testo incorporato che non fa parte dell'intervallo di testo.

  {URL} https://www.microsoft.com è incorporato nel testo.

La chiamata ai metodi [**IUIAutomationTextRange:: GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext), [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)e [**Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) comporta i comportamenti descritti nella tabella seguente.

| Metodo chiamato                                                                                            | Risultato                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange:: GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                         | Restituisce la stringa "L'URL".                                                                                                                                                                                                     |
| [**IUIAutomationTextRange:: GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) | Restituisce l'elemento di automazione interfaccia utente più interno che racchiude l'intervallo di testo, in questo caso l'elemento che rappresenta il provider di testo stesso.                                                                                     |
| [**IUIAutomationTextRange:: Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move)                               | Sposta l'intervallo di testo in "https://" perché il testo del collegamento ipertestuale è costituito da singole parole. In questo caso, il collegamento ipertestuale non viene considerato come oggetto singolo.<br/> L'URL {http} è incorporato nel testo.<br/> |

### <a name="image-example-1-a-text-range-that-contains-an-embedded-image"></a>Esempio di immagine 1: intervallo di testo che contiene un'immagine incorporata

L'intervallo di testo seguente contiene un'immagine incorporata di una navetta.

 {Immagine ![illustrazione di una navetta](images/shuttle.jpg) è incorporato nel testo}.

La chiamata ai metodi [**IUIAutomationTextRange:: GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext), [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement), [**GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)e [**IUIAutomationTextPattern:: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) comporta i comportamenti descritti nella tabella seguente.

| Metodo chiamato                                                                                                                                                                                                                                                    | Risultato                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange:: GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                                                                                                                                                                                 | Restituisce la stringa "l'immagine è incorporata nel testo". Qualsiasi testo alternativo associato all'immagine non è incluso nel flusso di testo.                |
| [**IUIAutomationTextRange:: GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)                                                                                                                                                         | Restituisce l'elemento di automazione interfaccia utente più interno che racchiude l'intervallo di testo, in questo caso l'elemento che rappresenta il provider di testo stesso. |
| [**IUIAutomationTextRange:: GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)                                                                                                                                                                         | Restituisce un elemento di automazione interfaccia utente che rappresenta il controllo immagine.                                                                               |
| [**IUIAutomationTextPattern:: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) in cui l'elemento di automazione interfaccia utente è stato restituito dal metodo [**IUIAutomationTextRange:: GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) precedente. | Restituisce l'intervallo degenerate.                                                                                                                 |

### <a name="image-example-2-a-text-range-that-partially-spans-the-content-of-a-text-container"></a>Immagine di esempio 2: intervallo di testo che si estende parzialmente sul contenuto di un contenitore di testo

L'intervallo di testo seguente si estende parzialmente sul contenuto di un contenitore di testo. Il contenitore di testo contiene un'immagine incorporata che non fa parte dell'intervallo di testo.

 {Immagine} ![illustrazione di una navetta](images/shuttle.jpg) è incorporato nel testo.

La chiamata ai metodi [**IUIAutomationTextRange:: GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext), [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)e [**Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) comporta i comportamenti descritti nella tabella seguente.

| Metodo chiamato                                                                                                          | Risultato                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange:: GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                                       | Restituisce la stringa "L'immagine".                                                                                                                                                                                                                                                 |
| [**IUIAutomationTextRange:: GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)               | Restituisce l'elemento di automazione interfaccia utente più interno che racchiude l'intervallo di testo, in questo caso l'elemento che rappresenta il provider di testo stesso.                                                                                                                                   |
| [**IUIAutomationTextRange:: Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) con i parametri di (**TextUnit \_ Word**, 2). | Sposta l'estensione dell'intervallo di testo a "è". Poiché solo gli oggetti incorporati basati su testo sono considerati parte del flusso di testo, l'immagine in questo esempio non influisce su [**IUIAutomationTextRange:: Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) o sul valore restituito, in questo caso, 2. |

### <a name="table"></a>Tabella

### <a name="table-example-1-gets-the-text-container-from-the-content-of-a-cell"></a>Tabella esempio 1: Ottiene il contenitore di testo dal contenuto di una cella

La tabella seguente consente di ottenere il contenitore di testo dal contenuto di una cella.

| Cella con immagine                                            | Cella con testo |
|------------------------------------------------------------|----------------|
| ![illustrazione di una navetta](images/shuttle.jpg)           | X              |
| ![illustrazione dello spazio e di un Telescope](images/space.jpg) | S              |
| ![illustrazione di un Microscope](images/microscope.jpg)     | Z              |

La chiamata ai metodi [**IUIAutomationGridPattern:: GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem), [**IUIAutomationTextPattern:: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild)e [**IUIAutomationTextRange:: GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) determina i comportamenti descritti nella tabella seguente.

| Metodo chiamato                                                                                                                                                                                                                       | Risultato                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationGridPattern:: GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem) con Parameters (0, 0).                                                                                                                        | Restituisce l'elemento di automazione interfaccia utente che rappresenta il contenuto della cella della tabella, in questo caso l'elemento è un controllo di testo.                                                               |
| [**iuiautomationtextpattern:: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild)                                                                                                                                  | Restituisce l'intervallo dell'immagine ![illustrazione di una navetta](images/shuttle.jpg).                                                                                                            |
| [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) per l'oggetto restituito dal metodo [**IUIAutomationTextPattern:: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) precedente. | Restituisce l'elemento di automazione interfaccia utente che rappresenta la cella della tabella. In questo caso, l'elemento è un controllo di testo che supporta il pattern di controllo [TableItem](uiauto-implementingtableitem.md) . |
| [**IUIAutomationTextRange:: GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) per l'oggetto restituito dal metodo **GetEnclosingElement** precedente.                                                    | Restituisce l'elemento di automazione interfaccia utente che rappresenta la tabella.                                                                                                                                   |
| [**IUIAutomationTextRange:: GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) per l'oggetto restituito dal metodo **GetEnclosingElement** precedente.                                                    | Restituisce l'elemento di automazione interfaccia utente che rappresenta il provider di testo stesso.                                                                                                                 |

### <a name="table-example-2-gets-the-text-content-of-a-cell"></a>Tabella esempio 2: Ottiene il contenuto di testo di una cella

La tabella nell'esempio precedente ottiene il contenuto di testo di una cella.

La chiamata ai metodi [**IUIAutomationGridPattern:: GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem) e [**IUIAutomationTextPattern:: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) comporta i comportamenti descritti nella tabella seguente.

| Metodo chiamato                                                                                                                                                                                                                                                          | Risultato                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationGridPattern:: GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem) con parametri (1,1).                                                                                                                                                            | Restituisce l'elemento di automazione interfaccia utente che rappresenta il contenuto della cella della tabella. In questo caso, l'elemento è un controllo di testo. |
| [**IUIAutomationTextPattern:: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) in cui l'elemento di automazione interfaccia utente è l'oggetto restituito dal metodo [**IUIAutomationGridPattern:: GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem) precedente. | Restituisce "Y".                                                                                                               |

Quando si sposta un documento in base alla [**\_ riga TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit), se l'intervallo di testo entra in una tabella incorporata, ogni riga di testo in una cella deve essere considerata come una linea.

## <a name="related-topics"></a>Argomenti correlati

### <a name="conceptual"></a>Informazioni concettuali

- [Informazioni sui pattern di controllo Text e TextRange](uiauto-about-text-and-textrange-patterns.md)
- [Attributi di testo di automazione interfaccia utente](uiauto-textattributes.md)
- [Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
- [Supporto di automazione interfaccia utente per contenuto testuale](uiauto-ui-automation-textpattern-overview.md)
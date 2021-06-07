---
title: Come Automazione interfaccia utente espone oggetti incorporati
description: Questo argomento descrive come Microsoft Automazione interfaccia utente oggetti incorporati, o elementi figlio, in un documento di testo o in un contenitore.
ms.assetid: 5ecf5e94-5329-4abb-aedb-4e303688e5f7
keywords:
- Automazione interfaccia utente,panoramica del modello di testo
- Automazione interfaccia utente,panoramica dei controlli di testo
- Automazione interfaccia utente,Pattern di controllo testo
- Automazione interfaccia utente,panoramica degli oggetti incorporati
- Automazione interfaccia utente,esposizione di oggetti incorporati
- Automazione interfaccia utente,scenari per oggetti incorporati
- modelli di testo, informazioni
- controlli di testo, informazioni
- Pattern di controllo del testo
- pattern di controllo,testo
- oggetti incorporati
- esposizione di oggetti incorporati
ms.topic: article
ms.date: 08/31/2019
ms.openlocfilehash: 8e9e0a8b9f70677778238908f8faf04e21ed9619
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443322"
---
# <a name="how-ui-automation-exposes-embedded-objects"></a>Come Automazione interfaccia utente espone oggetti incorporati

Questo argomento descrive come Microsoft Automazione interfaccia utente i pattern di controllo Text e TextRange per esporre oggetti incorporati (elementi figlio/discendenti) in un documento di testo o in un contenitore.

Ad Automazione interfaccia utente, un oggetto incorporato è qualsiasi elemento con limiti non testuali, ad esempio un'immagine, un collegamento ipertestuale, una tabella o un tipo di documento (foglio di calcolo di Microsoft Excel, file di Microsoft Windows Media e così via).

> [!NOTE]
> Ciò differisce dalla definizione OLE Component Object Model (COM) (vedere [Oggetti](../com/embedded-objects.md)incorporati ), in cui un elemento viene creato in un'applicazione e incorporato o collegato in un'altra applicazione. La modifica dell'oggetto nell'applicazione originale non è rilevante nel contesto di Automazione interfaccia utente.

## <a name="embedded-objects-and-the-ui-automation-tree"></a>Oggetti incorporati e albero di automazione interfaccia utente

Gli oggetti incorporati vengono considerati come singoli elementi nella visualizzazione controlli dell'Automazione interfaccia utente albero. Vengono esposti come elementi figlio del contenitore di testo in modo che sia possibile accedervi tramite lo stesso modello a oggetti degli altri controlli in Automazione interfaccia utente.

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
- Gruppo
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

L'immagine seguente mostra un contenitore di testo (documento) con una tabella e un'immagine incorporate.

![Figura che mostra un documento con una tabella e un'immagine incorporate](images/embeddedtable.jpg)

La Automazione interfaccia utente contenuto del documento precedente è illustrata nel diagramma seguente.

![Diagramma della visualizzazione contenuto di automazione interfaccia utente di un documento con oggetti incorporati](images/contenttree.jpg)

### <a name="compatible-and-non-compatible-embedded-objects"></a>Oggetti incorporati "Compatibili" e "Non compatibili"

Alcuni Automazione interfaccia utente usano lo stesso archivio di testo per ogni oggetto TextPattern che contengono.  Gli oggetti supportati dallo stesso archivio di testo del contenitore vengono definiti oggetti incorporati "compatibili". Questi oggetti possono essere oggetti TextPattern stessi e, in questo caso, i relativi intervalli di testo sono confrontabili con gli intervalli di testo ottenuti dal contenitore. Ciò consente ai provider di esporre le informazioni client sui singoli oggetti TextPattern come se fossero un unico provider di testo di grandi dimensioni.

Tuttavia, i provider possono usare archivi di testo diversi per diversi oggetti TextPattern incorporati all'interno di un contenitore TextPattern. Gli oggetti non supportati dall'archivio di testo del contenitore vengono definiti oggetti incorporati "non compatibili". Questi tipi di oggetti incorporati possono essere o meno oggetti basati su TextPattern.  

Nella tabella seguente sono elencati alcuni esempi di oggetti incorporati compatibili e non compatibili.

| Oggetti  | Oggetti incorporati compatibili | Oggetti incorporati non compatibili |
| --- | --- | --- |
| Oggetti incorporati non TextPattern | Pulsante in Microsoft Edge<br>Tabella dati in Microsoft Edge | Pulsante in RichTextBlock nel framework XAML di Microsoft<br>Immagini con testo alternativo in Microsoft Edge<br>ListView con ListItems in RichTextBlock nel framework XAML di Microsoft |
| Oggetti incorporati TextPattern | Controllo di input di tipo "text" in Microsoft Edge<br>Tabella in un documento di Word | Elemento TextBox in un documento di Microsoft Word |

## <a name="exposing-embedded-objects"></a>Esposizione di oggetti incorporati

I [pattern di controllo Text e TextRange](uiauto-implementingtextandtextrange.md) espongono proprietà e metodi che facilitano la navigazione e l'esecuzione di query su oggetti incorporati.

Il contenuto testuale (o testo interno) di un contenitore di testo e di un oggetto incorporato, ad esempio un collegamento ipertestuale o una cella di tabella, viene esposto come singolo flusso di testo continuo sia nella visualizzazione controlli che nella visualizzazione contenuto dell'albero Automazione interfaccia utente; I limiti degli oggetti vengono ignorati. Se un client Automazione interfaccia utente recupera il testo per interpretare, interpretare o analizzare in qualche modo, l'intervallo di testo deve essere controllato per casi speciali, ad esempio una tabella con contenuto testuale o altri oggetti incorporati. Chiamare [**IUIAutomationTextRange::GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) per ottenere [**un'interfaccia IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) per ogni oggetto incorporato e quindi [**chiamare IUIAutomationTextPattern::RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) per ottenere un intervallo di testo per ogni elemento. Questa operazione viene eseguita in modo ricorsivo fino a quando non è stato recuperato l'intero contenuto testuale.

> [!NOTE]
> Un intervallo degenerato (o compresso) è il punto in cui l'endpoint iniziale e l'endpoint finale sono uguali. Gli intervalli degenerati vengono spesso usati per indicare la posizione del cursore di testo tramite i metodi [ITextProvider](/windows/win32/api/uiautomationcore/nn-uiautomationcore-itextprovider) [GetSelection](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextprovider-getselection) e [GetCaretRange.](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextprovider2-getcaretrange)

Il diagramma seguente illustra un flusso di testo con oggetti incorporati e i relativi intervalli di intervalli.

![Diagramma che mostra un flusso di testo con oggetti incorporati e i relativi intervalli di intervalli](images/rangespans.jpg)

## <a name="embedded-objects-and-textunit"></a>Oggetti incorporati e TextUnit

Un [oggetto ITextProvider](/windows/win32/api/uiautomationcore/nn-uiautomationcore-itextprovider) può essere attraversato da un oggetto [TextUnit specificato.](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textunit) I provider che contengono oggetti incorporati possono essere attraversati nello stesso modo, ma gli oggetti incorporati influiscono sull'attraversamento. Ecco alcuni aspetti da tenere presenti:

- Qualsiasi oggetto incorporato non compatibile è rappresentato dal carattere di sostituzione U+FFFC nell'archivio di testo di TextPattern dell'elemento contenitore. Viene anche considerata sia un'unità carattere che un'unità di parole.
- Gli oggetti incorporati compatibili possono essere costituiti da più caratteri e parole.
- L'elemento di inclusione è l'elemento più in basso che si estende sull'intero intervallo di testo.
- Gli elementi figlio di un intervallo sono anche elementi figlio di un elemento contenitore parzialmente o completamente racchiusi all'interno dell'intervallo.
- Idealmente (soprattutto nel caso di elementi contenitore come Table) un limite di parola non va oltre il limite dell'oggetto. Nell'esempio seguente la parola unità "Bar" non contiene alcuna posizione di testo all'esterno del tag ( non fa parte `</td>` `<br \>` della parola "Bar").

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

- In generale, viene considerato come una singola parola in modo che non vada `<br \>` oltre un limite di linea.
- Un'eccezione alla regola precedente è il caso in cui un'unità di testo di Word contiene oggetti completi all'interno di se stessa. Ad esempio, `<p>Hello <a href="#">link</a> here.</p>` , che include contenitori inline, ha le parole "Hello", "link" e "here". Dove "link" ha un oggetto TextPattern come elemento contenitore e un oggetto collegamento come figlio.
- Nel caso delle unità carattere, l'oggetto è l'elemento contenitore (le unità di testo come questa non devono avere elementi figlio).
- Gli oggetti annotazione non devono essere rappresentati come oggetti incorporati. Ad esempio, la presenza di altri identificatori Author in un documento co-creato.
- Gli oggetti incorporati accettano almeno una posizione del cursore, l'annotazione è solo metadati.
- Ogni limite di oggetto (inizio e fine) è rappresentato da un'interruzione di formato nell'intervallo di documenti TextPattern.
- Per HTML, ogni tag HTML non comporta necessariamente un oggetto Automazione interfaccia utente html. Ad esempio, il contenuto all'interno dei tag di enfasi non deve essere rappresentato come elemento, ma come flusso di testo in cui UIA_IsItalicAttributeId <em></em> restituisce TRUE.
- L'endpoint iniziale è inclusivo ed è l'endpoint preferito mentre l'endpoint finale è esclusivo. Ciò è utile quando l'intervallo è degenerato e gli endpoint start e end appartengono alla stessa posizione per tale intervallo.

## <a name="comparing-embedded-objects"></a>Confronto tra oggetti incorporati

Gli oggetti TextPattern annidati in una relazione figlio simile e che condividono lo stesso archivio di testo sottostante sono denominati confrontabili. In questo caso, gli intervalli di uno degli oggetti TextPattern possono essere confrontati usando [ITextRangeProvider::Compare](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-compare) e [ITextRangeProvider::CompareEndpoints](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-compareendpoints). Entrambi i risultati sono un valore numerico valido che specifica la relativa posizione.

Un oggetto non TextPattern incorporato in un oggetto TextPattern è paragonabile a TextPattern se l'oggetto ha un intervallo valido in TextPattern ([ITextProvider::RangeFromChild](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextprovider-rangefromchild)) e il contenuto dietro l'intervallo di testo non è vuoto e non è un carattere di sostituzione.

## <a name="embedded-textpattern-objects-and-the-document-textunit"></a>Oggetti TextPattern incorporati e Document TextUnit

Per gli oggetti TextPattern incorporati, [l'unità Document](/windows/win32/api/uiautomationcore/ne-uiautomationcore-textunit) riconosce solo il contenuto contenuto all'interno di tale elemento.

### <a name="word-textpattern-element-hierarchy"></a>Gerarchia degli elementi TextPattern di Word

- L'elemento document implementa TextPattern e [Document](/windows/win32/api/uiautomationcore/ne-uiautomationcore-textunit) restituisce l'intero intervallo di documenti di Word.
- Le singole pagine del documento implementano TextPattern e [Document](/windows/win32/api/uiautomationcore/ne-uiautomationcore-textunit) restituisce il contenuto di tali singole pagine (anche se le pagine condividono lo stesso archivio di testo con l'intero documento TextPattern).

### <a name="webpage-and-text-input-controls-in-edge"></a>Controlli di input di testo e pagina Web in Edge

- L'elemento Pane della pagina Web principale implementa TextPattern ed espone l'intero contenuto della pagina Web.
- I singoli controlli di input di testo supportano TextPattern in cui un intervallo di documenti rappresenta il testo contenuto in ogni campo di input ,anche se condividono lo stesso archivio di testo con l'intera pagina Web.

## <a name="common-scenarios"></a>Scenari comuni

Questa sezione presenta esempi di scenari comuni che coinvolgono oggetti incorporati: collegamenti ipertestuali, immagini e tabelle. Negli esempi seguenti la parentesi graffa sinistra ({) rappresenta l'endpoint Start dell'intervallo di testo e la parentesi graffa destra (}) rappresenta l'endpoint finale.

### <a name="hyperlink-example-1-a-text-range-that-contains-an-embedded-text-hyperlink"></a>Esempio 1 di HyperLink: intervallo di testo che contiene un collegamento ipertestuale di testo incorporato

L'intervallo di testo seguente contiene un collegamento ipertestuale di testo incorporato.

  {L'URL https://www.microsoft.com è incorporato nel testo}.

La chiamata dei metodi [**IUIAutomationTextRange::GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext), [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement), [**GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)e [**IUIAutomationTextPattern::RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) determina i comportamenti descritti nella tabella seguente.

| Metodo chiamato                                                                                                                                                                                                                                                     | Result                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange::GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                                                                                                                                                                                  | Restituisce la stringa "L'URL https://www.microsoft.com è incorporato nel testo".                                                                               |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)                                                                                                                                                          | Restituisce l'elemento Automazione interfaccia utente che racchiude l'intervallo di testo, in questo caso l'elemento di automazione che rappresenta il provider di testo stesso. |
| [**IUIAutomationTextRange::GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)                                                                                                                                                                          | Restituisce un Automazione interfaccia utente elemento che rappresenta il controllo collegamento ipertestuale.                                                                                      |
| [**IUIAutomationTextPattern::RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild), in cui l'elemento Automazione interfaccia utente è stato restituito dal metodo [**IUIAutomationTextRange::GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) precedente. | Restituisce l'intervallo che rappresenta " https://www.microsoft.com ".                                                                                            |
### <a name="hyperlink-example-2-a-text-range-that-partially-spans-an-embedded-text-hyperlink"></a>Esempio 2 di HyperLink: intervallo di testo che si estende parzialmente su un collegamento ipertestuale di testo incorporato

L'intervallo di testo seguente si estende parzialmente su un collegamento ipertestuale di testo incorporato.

  L'URL https://{www} è incorporato nel testo.

La chiamata dei metodi [**IUIAutomationTextRange::GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext), [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)e [**GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) determina i comportamenti descritti nella tabella seguente.

| Metodo chiamato                                                                                            | Result                                                                                                         |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange::GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                         | Restituisce la stringa "www".                                                                                      |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) | Restituisce l'elemento Automazione interfaccia utente più interno che racchiude l'intervallo di testo. in questo caso, il controllo collegamento ipertestuale. |
| [**IUIAutomationTextRange::GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)                 | Restituisce **NULL** perché l'intervallo di testo non si estende sull'intera stringa url.                                   |

### <a name="hyperlink-example-3-a-text-range-that-partially-spans-the-content-of-a-text-container"></a>Esempio di HyperLink 3: intervallo di testo che si estende parzialmente sul contenuto di un contenitore di testo

L'intervallo di testo seguente si estende parzialmente sul contenuto di un contenitore di testo. Il contenitore di testo contiene testo incorporato che non fa parte dell'intervallo di testo.

  {URL} https://www.microsoft.com è incorporato nel testo.

La chiamata [**ai metodi IUIAutomationTextRange::GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext), [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)e [**Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) determina i comportamenti descritti nella tabella seguente.

| Metodo chiamato                                                                                            | Result                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange::GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                         | Restituisce la stringa "L'URL".                                                                                                                                                                                                     |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) | Restituisce l'elemento Automazione interfaccia utente che racchiude l'intervallo di testo, in questo caso l'elemento che rappresenta il provider di testo stesso.                                                                                     |
| [**IUIAutomationTextRange::Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move)                               | Sposta l'intervallo di testo in "https://" perché il testo del collegamento ipertestuale è costituito da singole parole. In questo caso, il collegamento ipertestuale non viene considerato come oggetto singolo.<br/> L'URL {http} è incorporato nel testo.<br/> |

### <a name="image-example-1-a-text-range-that-contains-an-embedded-image"></a>Esempio di immagine 1: intervallo di testo che contiene un'immagine incorporata

L'intervallo di testo seguente contiene un'immagine incorporata di una navicella.

 {L'immagine ![illustrazione di una navetta](images/shuttle.jpg) è incorporato nel testo}.

La chiamata dei metodi [**IUIAutomationTextRange::GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext), [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement), [**GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)e [**IUIAutomationTextPattern::RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) determina i comportamenti descritti nella tabella seguente.

| Metodo chiamato                                                                                                                                                                                                                                                    | Result                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange::GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                                                                                                                                                                                 | Restituisce la stringa "L'immagine è incorporata nel testo". Qualsiasi testo ALT associato all'immagine non è incluso nel flusso di testo.                |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)                                                                                                                                                         | Restituisce l'elemento Automazione interfaccia utente che racchiude l'intervallo di testo, in questo caso l'elemento che rappresenta il provider di testo stesso. |
| [**IUIAutomationTextRange::GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)                                                                                                                                                                         | Restituisce un Automazione interfaccia utente elemento che rappresenta il controllo immagine.                                                                               |
| [**IUIAutomationTextPattern::RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) in cui l'elemento Automazione interfaccia utente è stato restituito dal metodo [**IUIAutomationTextRange::GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) precedente. | Restituisce l'intervallo degenerato.                                                                                                                 |

### <a name="image-example-2-a-text-range-that-partially-spans-the-content-of-a-text-container"></a>Esempio di immagine 2: intervallo di testo che si estende parzialmente sul contenuto di un contenitore di testo

L'intervallo di testo seguente si estende parzialmente sul contenuto di un contenitore di testo. Il contenitore di testo contiene un'immagine incorporata che non fa parte dell'intervallo di testo.

 {Immagine} ![illustrazione di una navetta](images/shuttle.jpg) è incorporato nel testo.

La chiamata [**ai metodi IUIAutomationTextRange::GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext), [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)e [**Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) determina i comportamenti descritti nella tabella seguente.

| Metodo chiamato                                                                                                          | Result                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange::GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                                       | Restituisce la stringa "L'immagine".                                                                                                                                                                                                                                                 |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)               | Restituisce l'elemento Automazione interfaccia utente che racchiude l'intervallo di testo, in questo caso l'elemento che rappresenta il provider di testo stesso.                                                                                                                                   |
| [**IUIAutomationTextRange::Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) con parametri di (**TextUnit \_ Word**, 2). | Sposta l'estensione dell'intervallo di testo a "è". Poiché solo gli oggetti incorporati basati su testo vengono considerati parte del flusso di testo, l'immagine in questo esempio non influisce su [**IUIAutomationTextRange::Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) o sul relativo valore restituito, in questo caso 2. |

### <a name="table"></a>Tabella

### <a name="table-example-1-gets-the-text-container-from-the-content-of-a-cell"></a>Esempio di tabella 1: ottiene il contenitore di testo dal contenuto di una cella

La tabella seguente ottiene il contenitore di testo dal contenuto di una cella.

| Cella con immagine                                            | Cella con testo |
|------------------------------------------------------------|----------------|
| ![illustrazione di una navicella](images/shuttle.jpg)           | X              |
| ![illustrazione dello spazio e di un cannocchiale](images/space.jpg) | S              |
| ![illustrazione di un microscopio](images/microscope.jpg)     | Z              |

La chiamata dei metodi [**IUIAutomationGridPattern::GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem), [**IUIAutomationTextPattern::RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild)e [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) determina i comportamenti descritti nella tabella seguente.

| Metodo chiamato                                                                                                                                                                                                                       | Result                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationGridPattern::GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem) con parametri (0, 0).                                                                                                                        | Restituisce l Automazione interfaccia utente elemento che rappresenta il contenuto della cella della tabella, in questo caso l'elemento è un controllo di testo.                                                               |
| [**iuiautomationtextpattern::rangefromchild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild)                                                                                                                                  | restituisce l'intervallo dell'immagine ![illustrazione di una navicella](images/shuttle.jpg).                                                                                                            |
| [**GetEnclosingElement per**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) l'oggetto restituito dal metodo [**IUIAutomationTextPattern::RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) precedente. | Restituisce l Automazione interfaccia utente elemento che rappresenta la cella della tabella. In questo caso, l'elemento è un controllo di testo che supporta il pattern [di controllo TableItem.](uiauto-implementingtableitem.md) |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) per l'oggetto restituito dal metodo **GetEnclosingElement** precedente.                                                    | Restituisce l Automazione interfaccia utente elemento che rappresenta la tabella.                                                                                                                                   |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) per l'oggetto restituito dal metodo **GetEnclosingElement** precedente.                                                    | Restituisce l Automazione interfaccia utente elemento che rappresenta il provider di testo stesso.                                                                                                                 |

### <a name="table-example-2-gets-the-text-content-of-a-cell"></a>Esempio di tabella 2: ottiene il contenuto di testo di una cella

La tabella nell'esempio precedente ottiene il contenuto di testo di una cella.

La chiamata dei metodi [**IUIAutomationGridPattern::GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem) e [**IUIAutomationTextPattern::RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) comporta i comportamenti descritti nella tabella seguente.

| Metodo chiamato                                                                                                                                                                                                                                                          | Result                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationGridPattern::GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem) con parametri (1,1).                                                                                                                                                            | Restituisce l Automazione interfaccia utente elemento che rappresenta il contenuto della cella della tabella. In questo caso, l'elemento è un controllo di testo. |
| [**IUIAutomationTextPattern::RangeFromChild,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) dove l'elemento Automazione interfaccia utente è l'oggetto restituito dal metodo [**IUIAutomationGridPattern::GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem) precedente. | Restituisce "Y".                                                                                                               |

Quando si sposta un documento in base a [**TextUnit \_ Line**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit), se l'intervallo di testo entra in una tabella incorporata, ogni riga di testo in una cella deve essere considerata come una riga.

## <a name="related-topics"></a>Argomenti correlati

### <a name="conceptual"></a>Informazioni concettuali

- [Informazioni sui pattern di controllo Text e TextRange](uiauto-about-text-and-textrange-patterns.md)
- [Automazione interfaccia utente di testo](uiauto-textattributes.md)
- [Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
- [Automazione interfaccia utente supporto per il contenuto testuale](uiauto-ui-automation-textpattern-overview.md)
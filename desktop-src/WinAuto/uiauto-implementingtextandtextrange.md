---
title: Pattern di controllo Text e TextRange
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di ITextProvider, ITextProvider2 e ITextRangeProvider, incluse informazioni su proprietà e metodi.
ms.assetid: 4d541c31-11f7-4d7e-a0e0-9ed1da873d07
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo Text
- Automazione interfaccia utente, implementazione del pattern di controllo TextRange
- Automazione interfaccia utente, pattern di controllo Text
- Automazione interfaccia utente, pattern di controllo TextRange
- Automazione interfaccia utente, ITextProvider
- Automazione interfaccia utente, ITextRangeProvider
- ITextProvider
- ITextRangeProvider
- implementazione del pattern di controllo Text di automazione interfaccia utente
- implementazione del pattern di controllo TextRange di automazione interfaccia utente
- Pattern di controllo Text
- Pattern di controllo TextRange
- pattern di controllo, ITextProvider
- pattern di controllo, ITextRangeProvider
- pattern di controllo, implementazione del testo di automazione interfaccia utente
- pattern di controllo, implementazione del TextRange di automazione interfaccia utente
- pattern di controllo, testo
- pattern di controllo, TextRange
- interfacce, ITextProvider
- interfacce, ITextRangeProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f53429dc8ec137a83b6a40db377b5c84aeb36120
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104559660"
---
# <a name="text-and-textrange-control-patterns"></a>Pattern di controllo Text e TextRange

Vengono descritte le linee guida e le convenzioni per l'implementazione di [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider), [**ITextProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2)e [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider), incluse informazioni su proprietà e metodi. Il pattern di controllo **Text** consente a applicazioni e controlli di esporre un modello a oggetti testo semplice, consentendo ai client di recuperare contenuto testuale, attributi di testo e oggetti incorporati da controlli basati su testo.

Per supportare il pattern di controllo **Text** , i controlli implementano le interfacce [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) e [**ITextProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2) . I tipi di controllo che devono supportare il pattern di controllo **Text** includono i tipi di controllo [Edit](uiauto-supporteditcontroltype.md) e [Document](uiauto-supportdocumentcontroltype.md) e qualsiasi altro tipo di controllo che consente all'utente di immettere testo o selezionare testo di sola lettura.

Il pattern di controllo **Text** può essere usato con altri pattern di controllo di automazione interfaccia utente Microsoft per supportare diversi tipi di oggetti incorporati nel testo, tra cui tabelle, collegamenti ipertestuali e pulsanti di comando.

Le interfacce [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) e [**ITextProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2) includono diversi metodi per l'acquisizione di intervalli di testo. Un *intervallo di testo* è un oggetto che rappresenta un intervallo di testo contiguo, o più intervalli di testo non contigui, in un contenitore di testo. Un metodo **ITextProvider** acquisisce un intervallo di testo che rappresenta l'intero documento, mentre altri acquisiscono intervalli di testo che rappresentano una parte del documento, ad esempio il testo selezionato, il testo visibile o un oggetto incorporato nel testo.

Un oggetto intervallo di testo è rappresentato dal pattern di controllo **TextRange** , che viene implementato tramite l'interfaccia [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) . Il pattern di controllo **TextRange** fornisce metodi e proprietà usati per esporre informazioni sul testo nell'intervallo, spostare gli endpoint dell'intervallo, selezionare o deselezionare il testo, scorrere l'intervallo in visualizzazione e così via.

Per altre informazioni sui pattern di controllo **Text** e **TextRange** , vedere [supporto di automazione interfaccia utente per contenuti testuali](uiauto-ui-automation-textpattern-overview.md).

A partire da Windows 8.1 i provider possono implementare l'interfaccia [**ITextRangeProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider2) . Ciò consente di richiamare i menu di scelta rapida associati a un intervallo di testo. Sono supportati scenari come la correzione automatica del testo o la selezione del candidato IME (Input Method Editor).

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **ITextProvider**](#required-members-for-itextprovider)
-   [Membri obbligatori per **ITextRangeProvider**](#required-members-for-itextrangeprovider)
-   [Supporto di intervalli di testo](#supporting-text-ranges)
    -   [Modifica di un intervallo di testo in base all'unità di testo](#manipulating-a-text-range-by-text-unit)
    -   [Selezione di testo in un intervallo di testo](#selecting-text-in-a-text-range)
    -   [Acquisizione di testo da un intervallo di testo](#acquiring-text-from-a-text-range)
    -   [Implementazione di ShowContextMenu](#implementing-showcontextmenu)
-   [Interoperabilità con il cursore di sistema](#interoperability-with-the-system-caret)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern di controllo **Text** , tenere presenti le linee guida e le convenzioni seguenti:

-   Qualsiasi controllo che consente l'accesso al testo (ad esempio, l'immissione di testo o la selezione di testo di sola lettura) deve supportare il pattern di controllo **Text** .
-   Il pattern di controllo **Text** può essere usato con qualsiasi elemento dell'interfaccia utente che presenta testo, persino un'etichetta statica in un controllo Button standard. Tuttavia, non è necessario per i controlli di testo statici che non possono essere selezionati o che non dispongono di un punto di inserimento.
-   Per garantire che il testo sia completamente accessibile, i controlli che implementano [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) devono supportare anche l'interfaccia [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) . **IValueProvider** integra **ITextProvider** fornendo un modo programmatico per modificare il testo. Offre inoltre una maggiore compatibilità con le applicazioni client di Assistive Technology, incluse quelle basate su tecnologie legacy come Microsoft Active Accessibility. Quando vengono implementati entrambi i pattern di controllo, l'evento **TextChanged** ([**\_ \_ TextChangedEventId Text di UIA**](uiauto-event-ids.md)) e l'evento **AutomationPropertyChanged** ([**UIA \_ AutomationPropertyChangedEventId**](uiauto-event-ids.md)) sono equivalenti per la proprietà **value** ([**UIA \_ ValueValuePropertyId**](uiauto-control-pattern-propids.md)). Entrambi gli eventi devono essere supportati.
-   Il pattern di controllo **Text** supporta solo un flusso di testo e un viewport per controllo. Se l'applicazione offre più viste del documento nei riquadri, ogni visualizzazione (controllo) deve supportare [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) in modo indipendente.
-   Il metodo [**ITextProvider:: Getselectation**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection) può restituire un singolo intervallo di testo che rappresenta il testo attualmente selezionato. Se un controllo supporta la selezione di più intervalli di testo non contigui, il metodo **getselect** deve restituire una matrice che contiene un'interfaccia [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) per ogni intervallo di testo selezionato.
-   Il pattern di controllo **Text** rappresenta il punto di inserimento come un intervallo di testo degenerato (vuoto). Il metodo [**ITextProvider:: Getselectation**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection) deve restituire un intervallo di testo degenerato quando esiste il punto di inserimento e non è selezionato alcun testo. Per ulteriori informazioni, vedere [interoperabilità con il cursore di sistema](#interoperability-with-the-system-caret).
-   Il metodo [**ITextProvider:: GetVisibleRanges**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getvisibleranges) può restituire un singolo intervallo di testo se un intervallo di testo contiguo è visibile nel viewport oppure può restituire una matrice di intervalli di testo non contigui che rappresentano più righe di testo non visibili.
-   Il metodo [**ITextProvider:: RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) deve restituire un intervallo degenerato se l'elemento figlio non contiene testo. Poiché un oggetto incorporato può includere testo, il metodo **RangeFromChild** potrebbe non restituire sempre un intervallo di testo degenerato. Per ulteriori informazioni, vedere [come automazione interfaccia utente espone oggetti incorporati](uiauto-textpattern-and-embedded-objects-overview.md).
-   Il metodo [**ITextProvider:: RangeFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefrompoint) esegue l'hit test nell'area del documento usando le coordinate dello schermo specificate. L'intervallo di testo risultante deve essere coerente con il punto di inserimento o la selezione risultante facendo clic sulla posizione in corrispondenza delle coordinate dello schermo specificate. Se, ad esempio, un'immagine si trova in corrispondenza delle coordinate dello schermo specificate, l'intervallo di testo risultante deve corrispondere all'intervallo di testo che il metodo [**ITextProvider:: RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) acquisisce per l'immagine. Analogamente, se un'applicazione client richiede un intervallo di testo per la posizione al centro del cursore di sistema (punto di inserimento), l'intervallo di testo risultante deve essere uguale al percorso del cursore di sistema.
-   La proprietà [**ITextProvider::D ocumentrange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_documentrange) deve sempre fornire un intervallo di testo che includa tutto il testo supportato dall'implementazione di [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) corrispondente.
-   È necessario generare l'evento [**\_ \_ TextChangedEventId di testo UIA**](uiauto-event-ids.md) dopo che è stata apportata una modifica al testo, anche se la modifica non è visibile nel viewport. Ad esempio, il provider deve generare l'evento anche se l'utente incolla esattamente lo stesso testo sul testo selezionato.
-   Il [**\_ \_ TextSelectionChangedEventId di testo UIA**](uiauto-event-ids.md) deve essere generato ogni volta che viene modificata la selezione del testo o ogni volta che il punto di inserimento (cursore) si sposta tra il testo.

Quando si implementa il pattern di controllo **TextRange** , tenere presenti le linee guida e le convenzioni seguenti:

-   Tutti i metodi del pattern di controllo **TextRange** devono eseguire operazioni di testo indipendentemente dallo stato di visibilità del testo. Per **determinare la visibilità** di un intervallo di testo, è sempre possibile eseguire una query sull'attributo di testo [**\_ IsHiddenAttributeId (UIA**](uiauto-textattribute-ids.md)).
-   Se possibile, un provider deve garantire che tutte le modifiche apportate al testo, ad esempio le eliminazioni, gli inserimenti e gli spostamenti, vengano riflesse negli oggetti dell'intervallo di testo (istanze dell'interfaccia [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) ) associate e generino un evento [**\_ \_ TextChangedEventId di testo UIA**](uiauto-event-ids.md) . I client possono usare l'evento come hint per confermare le modifiche redazionali apportate al testo di un controllo.
-   Tutti gli oggetti intervallo di testo utilizzati dai metodi [**ITextRangeProvider:: compare**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compare), [**compareEndPoints**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compareendpoints)e [**MoveEndpointByRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyrange) devono essere peer della stessa implementazione del pattern di controllo di **testo** .
-   Sebbene non sia obbligatorio, il valore *pRetVal* recuperato dal metodo [**ITextRangeProvider:: CompareEndpoints**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compareendpoints) può indicare la distanza, in caratteri ([**\_ carattere TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)), tra i due endpoint. Tuttavia, le applicazioni client non devono dipendere dall'accuratezza di *pRetVal* oltre il relativo valore positivo o negativo.
-   I metodi [**ITextRangeProvider:: ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit), [**Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move)e [**MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit) richiedono un'attenta considerazione dell'unità di testo specificata. Per ulteriori informazioni, vedere modifica di un TextRange per unità di testo.
-   Per i requisiti di implementazione correlati ai metodi [**ITextRangeProvider:: Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select), [**AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-addtoselection)e [**RemoveFromSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-removefromselection) , vedere Selezione di testo in un intervallo di testo.
-   I metodi [**ITextRangeProvider:: FindText**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findtext) e [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute) cercano avanti o indietro per una singola stringa di testo o attributo di testo corrispondente. Devono restituire **null** se non viene trovata alcuna corrispondenza.
-   Il metodo [**ITextRangeProvider:: GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) deve restituire l'indirizzo acquisito dalla funzione [**UiaGetReservedMixedAttributeValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservedmixedattributevalue) o [**UiaGetReservedNotSupportedValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservednotsupportedvalue) se l'attributo associato varia nell'intervallo o se l'attributo non è supportato dal controllo testo. La specifica del pattern di controllo **TextRange** non consente l'aggiunta di nuovi identificatori di attributo di testo o la modifica del modo in cui vengono definiti gli attributi esistenti.
-   Se possibile, il metodo [**ITextRangeProvider:: GetBoundingRectangles**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getboundingrectangles) deve restituire una matrice che contiene un rettangolo di delimitazione per ogni riga di testo completamente o parzialmente visibile in un intervallo di testo. Se ciò non è possibile, il provider può restituire una matrice che contiene i rettangoli di delimitazione solo di righe completamente visibili; Tuttavia, questo limita la capacità di un'applicazione client di descrivere in modo accurato il modo in cui il testo viene visualizzato sullo schermo.
-   Il metodo [**ITextRangeProvider:: GetChildren**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getchildren) deve restituire tutti gli elementi figlio incorporati in un intervallo di testo, ma non deve restituire alcun elemento figlio degli elementi figlio. Se, ad esempio, un intervallo di testo contiene una tabella con un numero di celle figlio, il metodo **GetChildren** può restituire solo l'elemento Table e non gli elementi Cell. Per motivi di prestazioni o architettura, un provider potrebbe non essere in grado di esporre tutti gli oggetti incorporati ospitati in un documento nell'albero di automazione. In questo caso, il provider deve supportare almeno l'enumerazione degli oggetti figlio tramite il metodo **GetChildren** e, in alternativa, supportare il pattern di controllo [VirtualizedItem](uiauto-implementingvirtualizeditem.md) per il supporto di devirtualizzazione.
-   Il metodo [**ITextRangeProvider:: GetEnclosingElement**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getenclosingelement) restituisce in genere il provider di testo che fornisce l'intervallo di testo. Tuttavia, se il provider di testo supporta oggetti figlio quali tabelle o collegamenti ipertestuali, l'elemento contenitore potrebbe essere un discendente del provider di testo. L'elemento restituito da **GetEnclosingElement** deve essere l'elemento più vicino all'intervallo di testo specificato. Se, ad esempio, l'intervallo di testo si trova in una cella di una tabella, **GetEnclosingElement** deve restituire la cella contenitore anziché l'elemento Table.
-   Il metodo [**ITextRangeProvider:: GetText**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-gettext) deve restituire il testo normale nell'intervallo. Per ulteriori informazioni, vedere acquisizione di testo da un intervallo di testo.
-   La chiamata di [**ITextRangeProvider:: ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-scrollintoview) deve allineare il testo nel viewport del controllo di testo come specificato dal parametro *alignToTop* . Sebbene non esistano requisiti in termini di allineamento orizzontale, l'intervallo di testo deve essere visibile sia orizzontalmente che verticalmente. Quando si valuta il parametro *alignToTop* , un provider deve tenere conto dell'orientamento del controllo di testo e della direzione del flusso del testo. Se, ad esempio, *alignToTop* è **true** per un controllo di testo orientato verticalmente contenente testo che scorre da destra a sinistra, il provider deve allineare l'intervallo di testo al lato destro del viewport.
-   Quando si sposta un documento in base alla [**\_ riga TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit), se l'intervallo di testo entra in una tabella incorporata, ogni riga di testo in una cella deve essere considerata come una linea.

## <a name="required-members-for-itextprovider"></a>Membri obbligatori per **ITextProvider**

Le proprietà e i metodi seguenti sono necessari per implementare l'interfaccia [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) .



| Membri obbligatori                                                                                        | Tipo di membro | Note |
|---------------------------------------------------------------------------------------------------------|-------------|-------|
| [**DocumentRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_documentrange)                                             | Proprietà    | nessuno  |
| [**SupportedTextSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_supportedtextselection)                           | Proprietà    | nessuno  |
| [**GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection)                                               | Metodo      | nessuno  |
| [**GetVisibleRanges**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getvisibleranges)                                       | Metodo      | nessuno  |
| [**RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild)                                           | Metodo      | nessuno  |
| [**RangeFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefrompoint)                                           | Metodo      | nessuno  |
| [**\_TextChangedEventId testo \_ UIA**](uiauto-event-ids.md)                   | Evento       | nessuno  |
| [**\_TextSelectionChangedEventId testo \_ UIA**](uiauto-event-ids.md) | Evento       | nessuno  |



 

Per l'implementazione dell'interfaccia [**ITextProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2) sono necessari i metodi e le proprietà aggiuntive seguenti.



| Membri obbligatori                                                         | Tipo di membro | Note |
|--------------------------------------------------------------------------|-------------|-------|
| [**GetCaretRange**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextprovider2-getcaretrange)         | Metodo      | nessuno  |
| [**RangeFromAnnotation**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider2-rangefromannotation) | Metodo      | nessuno  |



 

## <a name="required-members-for-itextrangeprovider"></a>Membri obbligatori per **ITextRangeProvider**

Le proprietà e i metodi seguenti sono necessari per implementare l'interfaccia [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) .



| Membri obbligatori                                                                 | Tipo di membro | Note |
|----------------------------------------------------------------------------------|-------------|-------|
| [**AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-addtoselection)               | Metodo      | nessuno  |
| [**Clone**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-clone)                                 | Metodo      | nessuno  |
| [**Confronto**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compare)                             | Metodo      | nessuno  |
| [**CompareEndpoints**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compareendpoints)           | Metodo      | nessuno  |
| [**ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) | Metodo      | nessuno  |
| [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute)                 | Metodo      | nessuno  |
| [**FindText**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findtext)                           | Metodo      | nessuno  |
| [**GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue)         | Metodo      | nessuno  |
| [**GetBoundingRectangles**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getboundingrectangles) | Metodo      | nessuno  |
| [**GetChildren**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getchildren)                     | Metodo      | nessuno  |
| [**GetEnclosingElement**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getenclosingelement)     | Metodo      | nessuno  |
| [**GetText**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-gettext)                             | Metodo      | nessuno  |
| [**Spostare**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move)                                   | Metodo      | nessuno  |
| [**MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit)       | Metodo      | nessuno  |
| [**MoveEndpointByRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyrange)     | Metodo      | nessuno  |
| [**Selezionare**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select)                               | Metodo      | nessuno  |
| [**ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-scrollintoview)               | Metodo      | nessuno  |



 

Per l'implementazione dell'interfaccia [**ITextRangeProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider2) sono necessari i metodi e le proprietà aggiuntive seguenti.



| Membri obbligatori                                                      | Tipo di membro | Note                                      |
|-----------------------------------------------------------------------|-------------|--------------------------------------------|
| [**ShowContextMenu**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider2-showcontextmenu) | Metodo      | Vedere la sezione "implementazione di ShowContextMenu" |



 

Al pattern di controllo **TextRange** non sono associati eventi.

## <a name="supporting-text-ranges"></a>Supporto di intervalli di testo

Questa sezione descrive in che modo un provider deve implementare diversi metodi delle interfacce [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) e [**ITextRangeProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider2) per supportare il pattern di controllo **TextRange** .

### <a name="manipulating-a-text-range-by-text-unit"></a>Modifica di un intervallo di testo in base all'unità di testo

L'interfaccia [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) fornisce diversi metodi per la manipolazione e l'esplorazione degli intervalli di testo in un controllo basato su testo. I metodi [**ITextRangeProvider:: Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move), [**MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit)e [**ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) spostano un intervallo di testo o uno dei relativi endpoint in base all'unità di testo specificata, ad esempio il carattere, la parola, il paragrafo e così via. Per altre informazioni, vedere [unità di testo di automazione interfaccia utente](/windows/desktop/WinAuto/uiauto-uiautomationtextunits).

Nonostante il nome, il metodo [**ITextRangeProvider:: ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) non espande necessariamente un intervallo di testo. Ma "Normalizza" un intervallo di testo spostando gli endpoint in modo che l'intervallo includa l'unità di testo specificata. L'intervallo viene espanso se è più piccolo dell'unità specificata o abbreviato se è più lungo dell'unità specificata. È fondamentale che il metodo **ExpandToEnclosingUnit** normalizza sempre gli intervalli di testo in modo coerente. in caso contrario, altri aspetti della manipolazione dell'intervallo di testo in base all'unità di testo sarebbero imprevedibili. Il diagramma seguente illustra il modo in cui **ExpandToEnclosingUnit** normalizza un intervallo di testo spostando gli endpoint dell'intervallo.

![diagramma che mostra le posizioni degli endpoint dell'intervallo di testo prima e dopo una chiamata a ExpandToEnclosingUnit](images/expandtoenclosingunit.jpg)

Se l'intervallo di testo inizia all'inizio di un'unità di testo e termina all'inizio di o prima del limite dell'unità di testo successiva, l'endpoint finale viene spostato al limite dell'unità di testo successiva (vedere 1 e 2 nel diagramma precedente).

Se l'intervallo di testo inizia all'inizio di un'unità di testo e termina in corrispondenza di, o dopo, il limite dell'unità successiva, l'endpoint finale rimane o viene spostato indietro al limite dell'unità successiva dopo l'endpoint iniziale (vedere 3 e 4 nell'illustrazione precedente). Se è presente più di un limite di unità di testo tra gli endpoint iniziale e finale, l'endpoint finale viene spostato indietro al limite dell'unità successiva dopo l'endpoint iniziale, ottenendo un intervallo di testo di lunghezza pari a una unità di testo.

Se l'intervallo di testo inizia a metà dell'unità di testo, l'endpoint iniziale viene spostato all'inizio dell'unità di testo e l'endpoint finale viene spostato avanti o indietro, in base alle esigenze, al limite dell'unità successiva dopo l'endpoint iniziale (vedere da 5 a 8 nel diagramma precedente).

Quando viene chiamato il metodo [**ITextRangeProvider:: Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move) , il provider normalizza l'intervallo di testo in base all'unità di testo specificata, usando la stessa logica di normalizzazione del metodo [**ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) . Il provider sposta quindi l'intervallo avanti o indietro in base al numero di unità di testo specificato. Quando si muove l'intervallo, il provider deve ignorare i limiti degli oggetti incorporati nel testo. (Tuttavia, il limite dell'unità può essere influenzato dall'esistenza di un oggetto incorporato). Il diagramma seguente illustra il modo in cui il metodo **Move** sposta un intervallo di testo, unità per unità, tra oggetti incorporati e limiti di unità di testo.

![diagramma che illustra come il metodo Move sposta gli endpoint di intervallo tra gli oggetti e i limiti di unità di testo](images/move.jpg)

Il metodo [**ITextRangeProvider:: MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit) sposta uno degli endpoint avanti o indietro in base all'unità di testo specificata, come illustrato nella figura seguente.

![diagramma che illustra il modo in cui MoveEndpointByUnit sposta l'endpoint di un intervallo](images/moveendpointbyunit.gif)

Il metodo [**ITextRangeProvider:: MoveEndpointByRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyrange) consente a un'applicazione client di impostare un endpoint di un intervallo di testo nella stessa posizione dell'endpoint specificato di un secondo intervallo di testo.

### <a name="selecting-text-in-a-text-range"></a>Selezione di testo in un intervallo di testo

L'interfaccia [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) include diversi metodi per controllare la selezione del testo in un controllo basato su testo.

Il metodo [**ITextRangeProvider:: Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select) deve selezionare il testo che corrisponde a un intervallo di testo e rimuovere la selezione precedente, se presente, dal controllo di testo. Se **Select** viene chiamato su un intervallo di testo degenerato, il provider deve spostare il punto di inserimento nella posizione dell'intervallo di testo senza selezionare alcun testo.

Se un controllo supporta la selezione di più intervalli di testo non contigui, i metodi [**ITextRangeProvider:: AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-addtoselection) e [**RemoveFromSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-removefromselection) aggiungono intervalli di testo a e li rimuovino dalla raccolta di intervalli di testo selezionati. Se il controllo supporta solo un intervallo di testo selezionato alla volta, ma l'operazione di selezione comporterebbe la selezione di più intervalli di testo non contigui, il provider deve restituire un errore **E \_ INVALIDOPERATION** oppure deve estendere o troncare la selezione corrente. La proprietà [**ITextProvider:: SupportedTextSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_supportedtextselection) deve indicare se un controllo supporta la selezione di uno o più intervalli di testo o nessuno.

Se un controllo basato su testo supporta gli inserimenti di testo, la chiamata di [**ITextRangeProvider:: AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-addtoselection) o [**RemoveFromSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-removefromselection) in un intervallo di testo degenerato nel controllo deve spostare il punto di inserimento, ma non deve selezionare alcun testo.

### <a name="acquiring-text-from-a-text-range"></a>Acquisizione di testo da un intervallo di testo

Il metodo [**ITextRangeProvider:: GetText**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-gettext) deve restituire il testo normale di un intervallo di testo. Il testo normale deve includere tutti i caratteri di controllo trovati nel testo di origine, ad esempio i ritorni a capo e il contrassegno Unicode da sinistra a destra (LRM). Il testo normale non deve includere tag di markup, ad esempio HTML, che potrebbero essere presenti nel testo di origine. Inoltre, tutti i codici di escape nel testo di origine devono essere convertiti negli equivalenti di testo normale. Ad esempio, " &nbsp; " deve essere convertito in un carattere di spazio semplice.

Se un oggetto incorporato si estende su un intervallo di testo, il testo normale deve includere il testo interno dell'oggetto, ma non il testo alternativo (la proprietà Name dell'oggetto incorporato) perché potrebbe non essere coerente con il testo interno descrittivo. Per ulteriori informazioni, vedere [come automazione interfaccia utente espone oggetti incorporati](uiauto-textpattern-and-embedded-objects-overview.md).

### <a name="implementing-showcontextmenu"></a>Implementazione di ShowContextMenu

[**ITextRangeProvider2:: ShowContextMenu**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider2-showcontextmenu) deve sempre visualizzare il menu di scelta rapida in corrispondenza del punto finale iniziale dell'intervallo. Questa operazione dovrebbe essere equivalente a quanto accade se l'utente ha premuto il tasto del menu di scelta rapida o MAIUSC + F10 con il punto di inserimento all'inizio dell'intervallo.

Se la visualizzazione del menu di scelta rapida determina il passaggio del punto di inserimento in una determinata posizione, è consigliabile eseguire questa operazione per richiamare [**ShowContextMenu**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider2-showcontextmenu) a livello di codice per il supporto di automazione interfaccia utente.

## <a name="interoperability-with-the-system-caret"></a>Interoperabilità con il cursore di sistema

Il corretto supporto del punto di inserimento è fondamentale per molte applicazioni client, incluse quelle non basate sull'automazione dell'interfaccia utente. Nel pattern di controllo **Text** il punto di inserimento è rappresentato da un intervallo di testo degenerato (vuoto) in corrispondenza della posizione del cursore di sistema. Quando il punto di inserimento viene spostato, un controllo deve generare l'evento **TextSelectionChanged** ([**\_ \_ TextSelectionChangedEventId di testo UIA**](uiauto-event-ids.md)). Alcune applicazioni client dipendono da questo evento per monitorare la posizione del punto di inserimento e per tenere traccia della selezione del testo.

Quando un controllo contiene il testo selezionato, la struttura corrente del pattern di controllo **Text** non fornisce un modo per associare direttamente la posizione del punto di inserimento a un intervallo di testo specifico. Il provider deve tenere traccia della selezione del testo e impostare il percorso del punto di inserimento in modo appropriato. Poiché la selezione del testo viene in genere eseguita spostando il punto di inserimento tenendo premuto il tasto MAIUSC o CTRL oppure entrambi, un provider può tenere traccia della selezione del testo controllando lo stato di queste chiavi ogni volta che la selezione viene modificata.

Poiché il Framework di accessibilità fornisce supporto incorporato per il punto di inserimento del sistema, ma non per un accento circonflesso personalizzato, i controlli basati su testo devono usare il punto di inserimento del sistema laddove possibile. I controlli che usano un cursore personalizzato possono garantire che il punto di inserimento sia accessibile creando un cursore di sistema con le stesse dimensioni del cursore personalizzato e posizionando il cursore del sistema nella stessa posizione dell'interfaccia utente del controllo come cursore personalizzato, ovvero nel punto di inserimento. In alternativa, un controllo che usa un punto di inserimento personalizzato può implementare un provider Microsoft Active Accessibility per il punto di inserimento [**objid \_**](object-identifiers.md) per fornire informazioni sull'accessibilità direttamente per il punto di inserimento personalizzato.

Per ulteriori informazioni sul punto di inserimento del sistema, vedere la pagina relativa al punto di [inserimento](/windows/desktop/menurc/carets).

Per verificare se il controllo espone correttamente la posizione del punto di inserimento del sistema, usare gli strumenti di controllo degli eventi [ispezionabili](inspect-objects.md) e [accessibili](accessible-event-watcher.md) .

Le coordinate dello schermo del centro della bitmap del cursore di sistema devono corrispondere sempre alla posizione del punto di inserimento. In questo modo, un client può usare le coordinate dello schermo del cursore in una chiamata a [**ITextProvider:: RangeFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefrompoint) per recuperare un intervallo di testo che rappresenta accuratamente la posizione del punto di inserimento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Tipo di controllo Text](uiauto-supporttextcontroltype.md)
</dt> <dt>

[Pattern di controllo TextEdit](textedit-control-pattern.md)
</dt> <dt>

[Pattern di controllo TextChild](textchild-control-pattern.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Supporto di automazione interfaccia utente per contenuto testuale](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> </dl>

 

 
---
title: Pattern di controllo Text e TextRange
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di ITextProvider, ITextProvider2 e ITextRangeProvider, incluse informazioni su proprietà e metodi.
ms.assetid: 4d541c31-11f7-4d7e-a0e0-9ed1da873d07
keywords:
- Automazione interfaccia utente,implementazione del pattern di controllo Text
- Automazione interfaccia utente,implementazione del pattern di controllo TextRange
- Automazione interfaccia utente,Pattern di controllo testo
- Automazione interfaccia utente,Pattern di controllo TextRange
- Automazione interfaccia utente,ITextProvider
- Automazione interfaccia utente,ITextRangeProvider
- ITextProvider
- ITextRangeProvider
- Implementazione di Automazione interfaccia utente di controllo text
- Implementazione Automazione interfaccia utente di controllo TextRange
- Pattern di controllo del testo
- Pattern di controllo TextRange
- pattern di controllo,ITextProvider
- pattern di controllo,ITextRangeProvider
- pattern di controllo, implementazione di Automazione interfaccia utente text
- pattern di controllo, implementazione Automazione interfaccia utente TextRange
- pattern di controllo,testo
- pattern di controllo,TextRange
- interfacce, ITextProvider
- interfacce,ITextRangeProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99baf1af267e67ffe3f75a83fb970c991e9ebe5674497db2a2edad8d9cc328b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118826982"
---
# <a name="text-and-textrange-control-patterns"></a>Pattern di controllo Text e TextRange

Vengono descritte le linee guida e le convenzioni per l'implementazione di [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider), [**ITextProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2)e [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider), incluse informazioni su proprietà e metodi. Il **pattern di** controllo Text consente ad applicazioni e controlli di esporre un semplice modello a oggetti di testo, consentendo ai client di recuperare contenuto testuale, attributi di testo e oggetti incorporati da controlli basati su testo.

Per supportare il pattern di controllo **Text,** i controlli implementano [**le interfacce ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) e [**ITextProvider2.**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2) I tipi di  controllo che devono supportare il pattern di controllo Text includono i tipi di controllo [Edit](uiauto-supporteditcontroltype.md) e [Document](uiauto-supportdocumentcontroltype.md) e qualsiasi altro tipo di controllo che consente all'utente di immettere testo o selezionare testo di sola lettura.

Il **pattern di** controllo Text può essere usato con altri pattern di controllo di Microsoft Automazione interfaccia utente per supportare diversi tipi di oggetti incorporati nel testo, tra cui tabelle, collegamenti ipertestuali e pulsanti di comando.

Le [**interfacce ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) [**e ITextProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2) includono diversi metodi per l'acquisizione di intervalli di testo. Un *intervallo di* testo è un oggetto che rappresenta un intervallo contiguo di testo, o più intervalli di testo non contigui, in un contenitore di testo. Un **metodo ITextProvider** acquisisce un intervallo di testo che rappresenta l'intero documento, mentre altri acquisiscono intervalli di testo che rappresentano una parte del documento, ad esempio il testo selezionato, il testo visibile o un oggetto incorporato nel testo.

Un oggetto intervallo di testo è rappresentato dal pattern **di controllo TextRange,** implementato tramite l'interfaccia [**ITextRangeProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) Il pattern di **controllo TextRange** fornisce metodi e proprietà usati per esporre informazioni sul testo nell'intervallo, spostare gli endpoint dell'intervallo, selezionare o deselezionare il testo, scorrere l'intervallo nella visualizzazione e così via.

Per altre informazioni sui pattern **di controllo Text** e **TextRange,** [Automazione interfaccia utente supporto per il contenuto testuale](uiauto-ui-automation-textpattern-overview.md).

A partire da Windows 8.1 provider possono implementare [**l'interfaccia ITextRangeProvider2.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider2) In questo modo è possibile richiamare i menu di scelta rapida associati a un intervallo di testo. Supporta scenari come la correzione automatica del testo o la selezione candidata IME (Input Method Editor).

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **ITextProvider**](#required-members-for-itextprovider)
-   [Membri obbligatori per **ITextRangeProvider**](#required-members-for-itextrangeprovider)
-   [Supporto di intervalli di testo](#supporting-text-ranges)
    -   [Modifica di un intervallo di testo in base all'unità di testo](#manipulating-a-text-range-by-text-unit)
    -   [Selezione del testo in un intervallo di testo](#selecting-text-in-a-text-range)
    -   [Acquisizione di testo da un intervallo di testo](#acquiring-text-from-a-text-range)
    -   [Implementazione di ShowContextMenu](#implementing-showcontextmenu)
-   [Interoperabilità con l'oggetto System Caret](#interoperability-with-the-system-caret)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il **pattern di controllo Text,** tenere presente le linee guida e le convenzioni seguenti:

-   Qualsiasi controllo che consente l'accesso al testo,ad esempio l'immissione di testo o la selezione di testo di sola lettura, deve supportare il **pattern di controllo** Text.
-   Il **pattern di** controllo Text può essere usato con qualsiasi elemento dell'interfaccia utente che presenta testo, anche un'etichetta statica in un controllo pulsante standard. Tuttavia, non è necessario nei controlli di testo statico che non possono essere selezionati o non hanno un punto di inserimento.
-   Per garantire che il testo sia completamente accessibile, i controlli che implementano [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) devono supportare anche [**l'interfaccia IValueProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) **IValueProvider** integra **ITextProvider** fornendo un modo a livello di codice per modificare il testo. Offre anche una maggiore compatibilità con assistive technology client, incluse quelle basate su tecnologie legacy come Microsoft Active Accessibility. Quando vengono implementati entrambi i pattern di controllo, l'evento **TextChanged** ([**UIA \_ \_ TextChangedEventId**](uiauto-event-ids.md)) e l'evento **AutomationPropertyChanged** ([**UIA \_ AutomationPropertyChangedEventId**](uiauto-event-ids.md)) sono equivalenti per la proprietà **Value** ([**UIA \_ ValueValuePropertyId**](uiauto-control-pattern-propids.md)). Entrambi gli eventi devono essere supportati.
-   Il **pattern di** controllo Text supporta un solo flusso di testo e un viewport per ogni controllo. Se l'applicazione offre più visualizzazioni del documento nei riquadri, ogni visualizzazione (controllo) deve supportare [**ITextProvider in modo**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) indipendente.
-   Il [**metodo ITextProvider::GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection) può restituire un singolo intervallo di testo che rappresenta il testo attualmente selezionato. Se un controllo supporta la selezione di più intervalli di testo non contigui, il **metodo GetSelection** deve restituire una matrice contenente un'interfaccia [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) per ogni intervallo di testo selezionato.
-   Il **pattern di** controllo Text rappresenta il punto di inserimento come intervallo di testo degenerato (vuoto). Il [**metodo ITextProvider::GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection) deve restituire un intervallo di testo degenerato quando il punto di inserimento esiste e non viene selezionato alcun testo. Per altre informazioni, vedere [Interoperabilità con l'oggetto System Caret](#interoperability-with-the-system-caret).
-   Il metodo [**ITextProvider::GetVisibleRanges**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getvisibleranges) può restituire un singolo intervallo di testo se un intervallo contiguo di testo è visibile nel viewport oppure può restituire una matrice di intervalli di testo non contigui che rappresentano più righe di testo parzialmente visibili.
-   Il [**metodo ITextProvider::RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) deve restituire un intervallo degenerato se l'elemento figlio non contiene testo. Poiché un oggetto incorporato può includere testo, il **metodo RangeFromChild** potrebbe non restituire sempre un intervallo di testo degenerato. Per altre informazioni, vedere [Come Automazione interfaccia utente espone oggetti incorporati](uiauto-textpattern-and-embedded-objects-overview.md).
-   Il [**metodo ITextProvider::RangeFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefrompoint) esegue l'hit testing nell'area del documento usando le coordinate dello schermo specificate. L'intervallo di testo risultante deve essere coerente con il punto di inserimento o la selezione risultante facendo clic sulla posizione in corrispondenza delle coordinate dello schermo specificate. Ad esempio, se un'immagine si trova in corrispondenza delle coordinate dello schermo specificate, l'intervallo di testo risultante deve essere uguale all'intervallo di testo acquisito dal metodo [**ITextProvider::RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) per l'immagine. Analogamente, se un'applicazione client richiede un intervallo di testo per la posizione al centro del cursore di sistema (punto di inserimento), l'intervallo di testo risultante deve essere lo stesso della posizione del cursore di sistema.
-   La [**proprietà ITextProvider::D ocumentRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_documentrange) deve sempre fornire un intervallo di testo che include tutto il testo supportato dall'implementazione [**di ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) corrispondente.
-   [**L'evento \_ \_ TextChangedEventId**](uiauto-event-ids.md) dell'interfaccia utenteA deve essere generato dopo qualsiasi modifica al testo, anche se la modifica non è visibile nel viewport. Ad esempio, il provider deve generare l'evento anche se l'utente incolla esattamente lo stesso testo sul testo selezionato.
-   [**L'uiA \_ \_ TextSelectionChangedEventId**](uiauto-event-ids.md) deve essere generato ogni volta che la selezione del testo cambia o ogni volta che il punto di inserimento (cursore) si sposta tra il testo.

Quando si implementa il pattern **di controllo TextRange,** tenere presente le linee guida e le convenzioni seguenti:

-   Tutti i metodi del pattern **di controllo TextRange** devono eseguire operazioni di testo indipendentemente dallo stato di visibilità del testo. La visibilità di un intervallo di testo può sempre essere determinata tramite query sull'attributo di testo **IsHidden** ([**UIA \_ IsHiddenAttributeId**](uiauto-textattribute-ids.md)).
-   Se possibile, un provider deve garantire che eventuali modifiche al testo, ad esempio eliminazioni, inserimenti e spostamenti, siano riflesse negli oggetti intervallo di testo associati (istanze [**dell'interfaccia ITextRangeProvider)**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) e generare un evento TextChangedEventId dell'interfaccia [**utenteA \_ \_ TextChangedEventId.**](uiauto-event-ids.md) I client possono usare l'evento come suggerimento per confermare le modifiche editoriali apportate al testo di un controllo .
-   Tutti gli oggetti intervallo di testo usati dai metodi [**ITextRangeProvider::Compare**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compare), [**CompareEndpoints**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compareendpoints)e [**MoveEndpointByRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyrange) devono essere peer della stessa implementazione del pattern di controllo **Text.**
-   Sebbene non sia obbligatorio, il valore *pRetVal* recuperato dal metodo [**ITextRangeProvider::CompareEndpoints**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compareendpoints) può indicare la distanza, in caratteri ([**Carattere TextUnit \_**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)), tra i due endpoint. Tuttavia, le applicazioni client non devono dipendere dall'accuratezza *di pRetVal* oltre il valore positivo o negativo.
-   I [**metodi ITextRangeProvider::ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit), [**Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move)e [**MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit) richiedono un'attenta considerazione dell'unità di testo specificata. Per altre informazioni, vedere Modifica di un controllo TextRange in base all'unità di testo.
-   Per i requisiti di implementazione correlati ai metodi [**ITextRangeProvider::Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select), [**AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-addtoselection)e [**RemoveFromSelection,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-removefromselection) vedere Selezione di testo in un intervallo di testo.
-   I [**metodi ITextRangeProvider::FindText**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findtext) e [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute) consentono di cercare in avanti o indietro una singola stringa di testo o attributo di testo corrispondente. Devono restituire **NULL se** non viene trovata alcuna corrispondenza.
-   Il metodo [**ITextRangeProvider::GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) deve restituire l'indirizzo acquisito dalla funzione [**UiaGetReservedMixedAttributeValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservedmixedattributevalue) o [**UiaGetReservedNotSupportedValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservednotsupportedvalue) se l'attributo associato varia nell'intervallo o se l'attributo non è supportato dal controllo di testo. La specifica del pattern di controllo **TextRange** non consente l'aggiunta di nuovi identificatori di attributi di testo o la modifica della modalità di definizione degli attributi esistenti.
-   Se possibile, il metodo [**ITextRangeProvider::GetBoundingRectangles**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getboundingrectangles) deve restituire una matrice contenente un rettangolo di delimitazione per ogni riga di testo completamente o parzialmente visibile in un intervallo di testo. Se ciò non è possibile, il provider può restituire una matrice che contiene i rettangoli di delimitazione solo di linee completamente visibili. Tuttavia, ciò limita la capacità di un'applicazione client di descrivere in modo accurato come viene presentato il testo sullo schermo.
-   Il [**metodo ITextRangeProvider::GetChildren**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getchildren) deve restituire tutti gli elementi figlio incorporati in un intervallo di testo, ma non deve restituire elementi figlio degli elementi figlio. Ad esempio, se un intervallo di testo contiene una tabella con un numero di celle figlio, il **metodo GetChildren** può restituire solo l'elemento table e non gli elementi della cella. Per motivi di prestazioni o architettura, un provider potrebbe non essere in grado di esporre tutti gli oggetti incorporati ospitati in un documento nell'albero di automazione. In questo caso, il provider deve almeno supportare l'enumerazione di oggetti figlio tramite il **metodo GetChildren** e, come opzione, supportare il pattern di controllo [VirtualizedItem](uiauto-implementingvirtualizeditem.md) per il supporto della devirtualizzazione.
-   Il [**metodo ITextRangeProvider::GetEnclosingElement**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getenclosingelement) restituisce in genere il provider di testo che fornisce l'intervallo di testo. Tuttavia, se il provider di testo supporta oggetti figlio, ad esempio tabelle o collegamenti ipertestuali, l'elemento contenitore potrebbe essere un discendente del provider di testo. L'elemento restituito **da GetEnclosingElement** deve essere l'elemento più vicino all'intervallo di testo specificato. Ad esempio, se l'intervallo di testo si trova in una cella di una tabella, **GetEnclosingElement** deve restituire la cella contenitore anziché l'elemento tabella.
-   Il [**metodo ITextRangeProvider::GetText**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-gettext) deve restituire il testo normale nell'intervallo. Per altre informazioni, vedere Acquisizione di testo da un intervallo di testo.
-   La [**chiamata a ITextRangeProvider::ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-scrollintoview) deve allineare il testo nel riquadro di visualizzazione del controllo di testo come specificato dal *parametro alignToTop.* Anche se non esiste alcun requisito in termini di allineamento orizzontale, l'intervallo di testo deve essere visibile sia orizzontalmente che verticalmente. Quando si valuta il *parametro alignToTop,* un provider deve prendere in considerazione l'orientamento del controllo di testo e la direzione di flusso del testo. Ad esempio, se *alignToTop* è **TRUE** per un controllo testo orientato verticalmente contenente testo che scorre da destra a sinistra, il provider deve allineare l'intervallo di testo al lato destro del riquadro di visualizzazione.
-   Quando si passa attraverso un documento in base a [**TextUnit \_ Line**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit), se l'intervallo di testo immette una tabella incorporata, ogni riga di testo in una cella deve essere considerata come una riga.

## <a name="required-members-for-itextprovider"></a>Membri obbligatori per **ITextProvider**

Per implementare l'interfaccia [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) sono necessari i metodi e le proprietà seguenti.



| Membri obbligatori                                                                                        | Tipo di membro | Note |
|---------------------------------------------------------------------------------------------------------|-------------|-------|
| [**Controllo DocumentRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_documentrange)                                             | Proprietà    | Nessuno  |
| [**SupportedTextSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_supportedtextselection)                           | Proprietà    | Nessuno  |
| [**GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection)                                               | Metodo      | Nessuno  |
| [**GetVisibleRanges**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getvisibleranges)                                       | Metodo      | Nessuno  |
| [**RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild)                                           | Metodo      | Nessuno  |
| [**RangeFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefrompoint)                                           | Metodo      | Nessuno  |
| [**\_ \_ TextChangedEventId dell'interfaccia utente**](uiauto-event-ids.md)                   | Evento       | Nessuno  |
| [**\_TextSelectionChangedEventId dell'interfaccia utente \_**](uiauto-event-ids.md) | Evento       | Nessuno  |



 

Per implementare l'interfaccia [**ITextProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2) sono necessari i metodi e le proprietà aggiuntivi seguenti.



| Membri obbligatori                                                         | Tipo di membro | Note |
|--------------------------------------------------------------------------|-------------|-------|
| [**GetCaretRange**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextprovider2-getcaretrange)         | Metodo      | Nessuno  |
| [**RangeFromAnnotation**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider2-rangefromannotation) | Metodo      | Nessuno  |



 

## <a name="required-members-for-itextrangeprovider"></a>Membri obbligatori per **ITextRangeProvider**

Per implementare l'interfaccia [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) sono necessari i metodi e le proprietà seguenti.



| Membri obbligatori                                                                 | Tipo di membro | Note |
|----------------------------------------------------------------------------------|-------------|-------|
| [**AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-addtoselection)               | Metodo      | Nessuno  |
| [**Clone**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-clone)                                 | Metodo      | Nessuno  |
| [**Confronto**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compare)                             | Metodo      | Nessuno  |
| [**CompareEndpoints**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compareendpoints)           | Metodo      | Nessuno  |
| [**ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) | Metodo      | Nessuno  |
| [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute)                 | Metodo      | Nessuno  |
| [**Findtext**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findtext)                           | Metodo      | Nessuno  |
| [**GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue)         | Metodo      | Nessuno  |
| [**GetBoundingRectangles**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getboundingrectangles) | Metodo      | Nessuno  |
| [**GetChildren**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getchildren)                     | Metodo      | Nessuno  |
| [**GetEnclosingElement**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getenclosingelement)     | Metodo      | Nessuno  |
| [**GetText**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-gettext)                             | Metodo      | Nessuno  |
| [**Sposta**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move)                                   | Metodo      | Nessuno  |
| [**MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit)       | Metodo      | Nessuno  |
| [**MoveEndpointByRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyrange)     | Metodo      | Nessuno  |
| [**Selezionare**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select)                               | Metodo      | Nessuno  |
| [**ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-scrollintoview)               | Metodo      | Nessuno  |



 

Per l'implementazione dell'interfaccia [**ITextRangeProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider2) sono necessari i metodi e le proprietà aggiuntive seguenti.



| Membri obbligatori                                                      | Tipo di membro | Note                                      |
|-----------------------------------------------------------------------|-------------|--------------------------------------------|
| [**ShowContextMenu**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider2-showcontextmenu) | Metodo      | Vedere la sezione "Implementazione di ShowContextMenu" |



 

Il **pattern di controllo TextRange** non ha eventi associati.

## <a name="supporting-text-ranges"></a>Supporto di intervalli di testo

Questa sezione descrive come un provider deve implementare vari metodi delle interfacce [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) e [**ITextRangeProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider2) per supportare il pattern **di controllo TextRange.**

### <a name="manipulating-a-text-range-by-text-unit"></a>Modifica di un intervallo di testo in base all'unità di testo

[**L'interfaccia ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) fornisce diversi metodi per modificare ed esplorare intervalli di testo in un controllo basato su testo. I metodi [**ITextRangeProvider::Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move), [**MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit)e [**ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) spostano un intervallo di testo o uno dei relativi endpoint in base all'unità di testo specificata, ad esempio carattere, parola, paragrafo e così via. Per altre informazioni, vedere Automazione interfaccia utente [text units](/windows/desktop/WinAuto/uiauto-uiautomationtextunits).

Nonostante il nome, il [**metodo ITextRangeProvider::ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) non espande necessariamente un intervallo di testo. Al contrario, "normalizza" un intervallo di testo spostando gli endpoint in modo che l'intervallo comprersi l'unità di testo specificata. L'intervallo viene espanso se è minore dell'unità specificata o abbreviato se è più lungo dell'unità specificata. È fondamentale che il **metodo ExpandToEnclosingUnit** normalizzi sempre gli intervalli di testo in modo coerente; in caso contrario, altri aspetti della manipolazione dell'intervallo di testo in base all'unità di testo sarebbero imprevedibili. Il diagramma seguente illustra come **ExpandToEnclosingUnit** normalizza un intervallo di testo spostando gli endpoint dell'intervallo.

![Diagramma che mostra le posizioni dell'endpoint dell'intervallo di testo prima e dopo una chiamata a expandtoenclosingunit](images/expandtoenclosingunit.jpg)

Se l'intervallo di testo inizia all'inizio di un'unità di testo e termina all'inizio o prima del limite successivo dell'unità di testo, l'endpoint finale viene spostato al limite successivo dell'unità di testo (vedere 1 e 2 nel diagramma precedente).

Se l'intervallo di testo inizia all'inizio di un'unità di testo e termina in corrispondenza o dopo il limite di unità successivo, l'endpoint finale rimane o viene spostato all'indietro al limite di unità successivo dopo l'endpoint iniziale (vedere 3 e 4 nell'illustrazione precedente). Se è presente più di un limite di unità di testo tra gli endpoint iniziale e finale, l'endpoint finale viene spostato all'indietro al limite di unità successivo dopo l'endpoint iniziale, determinando un intervallo di testo di lunghezza pari a un'unità di testo.

Se l'intervallo di testo inizia in un punto centrale dell'unità di testo, l'endpoint iniziale viene spostato all'inizio dell'unità di testo e l'endpoint finale viene spostato in avanti o all'indietro, se necessario, al limite dell'unità successiva dopo l'endpoint iniziale (vedere da 5 a 8 nel diagramma precedente).

Quando viene chiamato il metodo [**ITextRangeProvider::Move,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move) il provider normalizza l'intervallo di testo in base all'unità di testo specificata, usando la stessa logica di normalizzazione del [**metodo ExpandToEnclosingUnit.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) Il provider sposta quindi l'intervallo all'indietro o in avanti del numero specificato di unità di testo. Quando si sposta l'intervallo, il provider deve ignorare i limiti di qualsiasi oggetto incorporato nel testo. Tuttavia, il limite di unità stesso può essere influenzato dall'esistenza di un oggetto incorporato. Il diagramma seguente illustra come il **metodo Move** sposta un intervallo di testo, unità per unità, tra oggetti incorporati e limiti di unità di testo.

![Diagramma che mostra come il metodo move sposta gli endpoint di intervallo tra i limiti di oggetti e unità di testo](images/move.jpg)

Il [**metodo ITextRangeProvider::MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit) sposta uno degli endpoint in avanti o indietro in base all'unità di testo specificata, come illustrato nella figura seguente.

![Diagramma che mostra come moveendpointbyunit sposta l'endpoint di un intervallo](images/moveendpointbyunit.gif)

Il [**metodo ITextRangeProvider::MoveEndpointByRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyrange) consente a un'applicazione client di impostare un endpoint di un intervallo di testo sulla stessa posizione dell'endpoint specificato di un secondo intervallo di testo.

### <a name="selecting-text-in-a-text-range"></a>Selezione del testo in un intervallo di testo

[**L'interfaccia ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) include diversi metodi per controllare la selezione di testo in un controllo basato su testo.

Il [**metodo ITextRangeProvider::Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select) deve selezionare il testo corrispondente a un intervallo di testo e rimuovere la selezione precedente, se presente, dal controllo di testo. Se **select** viene chiamato su un intervallo di testo degenerato, il provider deve spostare il punto di inserimento nella posizione dell'intervallo di testo senza selezionare alcun testo.

Se un controllo supporta la selezione di più intervalli di testo non contigui, i metodi [**ITextRangeProvider::AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-addtoselection) e [**RemoveFromSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-removefromselection) aggiungono intervalli di testo e li rimuovono dalla raccolta di intervalli di testo selezionati. Se il controllo supporta un solo intervallo di testo selezionato alla volta, ma l'operazione di selezione comporterebbe la selezione di più intervalli di testo non contigui, il provider deve restituire un errore **E \_ INVALIDOPERATION** oppure deve estendere o troncare la selezione corrente. La [**proprietà ITextProvider::SupportedTextSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_supportedtextselection) deve indicare se un controllo supporta la selezione di singoli o più intervalli di testo o nessuno.

Se un controllo basato su testo supporta gli inserimenti di testo, la chiamata a [**ITextRangeProvider::AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-addtoselection) [**o RemoveFromSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-removefromselection) in un intervallo di testo degenerato nel controllo deve spostare il punto di inserimento, ma non deve selezionare alcun testo.

### <a name="acquiring-text-from-a-text-range"></a>Acquisizione di testo da un intervallo di testo

Il [**metodo ITextRangeProvider::GetText**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-gettext) deve restituire il testo normale di un intervallo di testo. Il testo normale deve includere tutti i caratteri di controllo trovati nel testo di origine, ad esempio i ritorni a capo e il segno unicode da sinistra a destra (LRM). Il testo normale non deve includere tag di markup, ad esempio HTML, che possono essere presenti nel testo di origine. Inoltre, tutti i codici di escape nel testo di origine devono essere convertiti negli equivalenti di testo normale. Ad esempio, " &nbsp; " deve essere convertito in uno spazio semplice.

Se un oggetto incorporato si estende su un intervallo di testo, il testo normale deve includere il testo interno dell'oggetto, ma non il testo alternativo (la proprietà name dell'oggetto incorporato), perché potrebbe non essere coerente con il testo interno descrittivo. Per altre informazioni, vedere [Come Automazione interfaccia utente espone oggetti incorporati](uiauto-textpattern-and-embedded-objects-overview.md).

### <a name="implementing-showcontextmenu"></a>Implementazione di ShowContextMenu

[**ITextRangeProvider2::ShowContextMenu**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider2-showcontextmenu) deve sempre visualizzare il menu di scelta rapida all'inizio dell'intervallo. Questo dovrebbe essere equivalente a ciò che accade se l'utente preme il tasto del menu di scelta rapida o MAIUSC + F10 con il punto di inserimento all'inizio dell'intervallo.

Se la visualizzazione del menu di scelta rapida comporta in genere lo spostamento del punto di inserimento in una determinata posizione, è necessario farlo anche per richiamare a livello di codice [**ShowContextMenu**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider2-showcontextmenu) per Automazione interfaccia utente supporto.

## <a name="interoperability-with-the-system-caret"></a>Interoperabilità con l'oggetto System Caret

Il corretto supporto del punto di inserimento è fondamentale per molte applicazioni client, incluse quelle non basate su Automazione interfaccia utente. Nel pattern **di** controllo Text il punto di inserimento è rappresentato da un intervallo di testo degenerato (vuoto) nella posizione del cursore di sistema. Quando il punto di inserimento viene spostato, un controllo deve generare l'evento **TextSelectionChanged** ([**UIA \_ \_ TextSelectionChangedEventId**](uiauto-event-ids.md)). Alcune applicazioni client dipendono da questo evento per monitorare la posizione del punto di inserimento e tenere traccia della selezione del testo.

Quando un controllo contiene testo selezionato,  la progettazione corrente del pattern di controllo Testo non consente di associare direttamente la posizione del punto di inserimento a un intervallo di testo specifico. Il provider deve tenere traccia della selezione del testo e impostare la posizione del punto di inserimento in modo appropriato. Poiché la selezione del testo viene in genere eseguita spostando il punto di inserimento tenendo premuto MAIUSC o CTRL o entrambi, un provider può tenere traccia della selezione del testo controllando lo stato di questi tasti ogni volta che la selezione cambia.

Poiché il framework di accessibilità fornisce il supporto incorporato per il punto di caret di sistema, ma non per un punto di accesso personalizzato, i controlli basati su testo devono usare il punto di accesso al sistema quando possibile. I controlli che usano un cursore personalizzato possono garantire che il cursore sia accessibile creando un cursore di sistema con le stesse dimensioni del cursore personalizzato e posizionando il cursore di sistema nella stessa posizione nell'interfaccia utente del controllo del cursore personalizzato, ovvero nel punto di inserimento. In alternativa, un controllo che usa un punto di accesso personalizzato può implementare un provider Microsoft Active Accessibility per [**OBJID \_ CARET**](object-identifiers.md) per fornire informazioni di accessibilità direttamente per il punto di accesso personalizzato.

Per altre informazioni sul caret di sistema, vedere [Carets](/windows/desktop/menurc/carets).

Per verificare se il controllo espone correttamente la posizione del punto di controllo di sistema, usare gli strumenti [Inspect](inspect-objects.md) e [Accessible Event Watcher.](accessible-event-watcher.md)

Le coordinate dello schermo del centro della bitmap del cursore di sistema devono sempre corrispondere alla posizione del punto di inserimento. In questo modo, un client può usare le coordinate dello schermo del cursore in una chiamata a [**ITextProvider::RangeFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefrompoint) per recuperare un intervallo di testo che rappresenta in modo accurato la posizione del punto di inserimento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di controllo e relativi pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Tipo di controllo text](uiauto-supporttextcontroltype.md)
</dt> <dt>

[Pattern di controllo TextEdit](textedit-control-pattern.md)
</dt> <dt>

[Pattern di controllo TextChild](textchild-control-pattern.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Automazione interfaccia utente supporto per il contenuto testuale](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> </dl>

 

 
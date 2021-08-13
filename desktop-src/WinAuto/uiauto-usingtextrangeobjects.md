---
title: Uso di intervalli di testo
description: Questo argomento descrive come usare le proprietà e i metodi dell'interfaccia IUIAutomationTextRange per accedere al contenuto testuale di un controllo basato su testo e modificarlo.
ms.assetid: 66BC7324-5322-4996-AF62-766936559F0E
keywords:
- client, uso di oggetti intervallo di testo
- controlli basati su testo
- client, intervalli di testo
- client, pattern di controllo TextRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2c409f39d437135854463e83c361a9afd22204758c360119bd0033e4fd11416
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118564008"
---
# <a name="using-text-ranges"></a>Uso di intervalli di testo

Questo argomento descrive come usare le proprietà e i metodi [**dell'interfaccia IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) per accedere al contenuto testuale di un controllo basato su testo e modificarlo. Contiene le sezioni seguenti:

-   [Che cos'è un intervallo di testo?](#using-text-ranges)
-   [Acquisizione di oggetti intervallo di testo](#acquiring-text-range-objects)
-   [Selezione di testo in un intervallo di testo](#selecting-text-in-a-text-range)
-   [Recupero di testo da un intervallo di testo](#retrieving-text-from-a-text-range)
-   [Recupero di attributi di testo da un intervallo di testo](#retrieving-text-attributes-from-a-text-range)
-   [Recupero di oggetti incorporati da un intervallo di testo](#retrieving-embedded-objects-from-a-text-range)
-   [Modifica di un intervallo di testo](#manipulating-a-text-range)
-   [Scorrimento di un intervallo di testo nella visualizzazione](#scrolling-a-text-range-into-view)
-   [Recupero dell'elemento contenitore di un intervallo di testo](#retrieving-the-enclosing-element-of-a-text-range)
-   [Confronto e clonazione di intervalli di testo](#comparing-and-cloning-text-ranges)
-   [Recupero di annotazioni](#retrieving-annotations)
    -   [Recupero di tipi di annotazioni da un intervallo di testo](#retrieving-annotations-types-from-a-text-range)
    -   [Recupero di tutte le annotazioni da un intervallo di testo](#retrieving-all-annotations-from-a-text-range)
    -   [Recupero di informazioni su un'annotazione specifica](#retrieving-information-about-a-particular-annotation)
    -   [Recupero del testo di destinazione dell'annotazione](#retrieving-the-annotation-target-text)
-   [Recupero di stili di visualizzazione](#retrieving-visual-styles)
-   [Richiamo di menu di scelta rapida da intervalli di testo](#invoking-context-menus-from-text-ranges)
-   [Argomenti correlati](#related-topics)

## <a name="what-is-a-text-range"></a>Che cos'è un intervallo di testo?

Il modello Automazione interfaccia utente testo di Microsoft si basa sul concetto di intervallo *di testo*. Un intervallo di testo è un oggetto che espone [**l'interfaccia IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) e rappresenta un intervallo contiguo di testo in un controllo basato su testo. Ogni intervallo di testo ha sia un endpoint iniziale che un endpoint finale e tutto il contenuto testuale tra i due endpoint viene considerato parte dell'intervallo. Un intervallo di testo il cui endpoint iniziale e l'endpoint finale si trova nella stessa posizione sono denominati intervalli di testo *degenere* (o vuoti). Un intervallo di testo degenere viene usato per contrassegnare una posizione specifica all'interno del testo di un controllo, ad esempio la posizione del punto di inserimento del testo.

## <a name="acquiring-text-range-objects"></a>Acquisizione di oggetti intervallo di testo

Le applicazioni client acquisiscono oggetti intervallo di testo usando le proprietà e i metodi [**dell'interfaccia IUIAutomationTextPattern.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) La proprietà [**IUIAutomationTextRangePattern::D ocumentRange**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-get_documentrange) recupera un intervallo di testo che rappresenta l'intero contenuto testuale di un controllo basato su testo, mentre altri metodi acquisiscono intervalli di testo che rappresentano una parte del contenuto, ad esempio il testo selezionato, il testo visibile o un oggetto incorporato nel testo.

I [**metodi IUIAutomationTextRangePattern::GetVisibleRanges**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-getvisibleranges) e [**GetSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-getselection) possono recuperare matrici di oggetti intervallo di testo. Se un controllo viene parzialmente nascosto da una finestra sovrapposta o da un altro oggetto, **GetVisibleRanges** restituisce una matrice contenente un oggetto intervallo di testo per ogni riga di testo parzialmente visibile. Analogamente, se un controllo basato su testo supporta la selezione di più intervalli di testo non contigui, **GetSelection** restituisce una matrice che contiene un oggetto intervallo di testo per ogni intervallo selezionato.

Il [**metodo IUIAutomationTextRangePattern::RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) consente a un'applicazione client di recuperare un intervallo di testo che racchiude un oggetto incorporato nel contenuto testuale. Il client specifica il puntatore a interfaccia [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) di un oggetto incorporato, ad esempio un'immagine, una tabella o un collegamento ipertestuale, e il metodo restituisce un intervallo di testo che racchiude l'oggetto. Tuttavia, se all'oggetto incorporato non è associato alcun testo, il metodo restituisce un intervallo di testo degenere.

Un'applicazione client può usare il metodo [**IUIAutomationTextRangePattern::RangeFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefrompoint) per recuperare un intervallo di testo per il testo visibile o l'oggetto incorporato più vicino alle coordinate dello schermo specificate.

## <a name="selecting-text-in-a-text-range"></a>Selezione di testo in un intervallo di testo

[**L'interfaccia IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) include diversi metodi che consentono a un'applicazione client di controllare la selezione di testo in un controllo basato su testo.

Le applicazioni client possono usare il metodo [**IUIAutomationTextRange::Select**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-select) per selezionare il testo corrispondente a un intervallo di testo e rimuovere la selezione precedente, se presente, dal controllo di testo. Chiamando **Select** con un intervallo di testo degenerato, il punto di inserimento viene spostato nella posizione dell'intervallo di testo senza selezionare alcun testo.

Se un controllo supporta la selezione di più intervalli di testo non contigui, un client può usare i metodi [**IUIAutomationTextRange::AddToSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-addtoselection) e [**RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-removefromselection) per aggiungere e rimuovere intervalli di testo nella raccolta di intervalli di testo selezionati. Se il controllo supporta un solo intervallo di testo selezionato alla volta, ma l'operazione di selezione comporterebbe la selezione di più intervalli di testo non contigui, il metodo restituisce un errore **E \_ INVALIDOPERATION** oppure estende o tronca la selezione corrente. Un'applicazione client può determinare se un controllo supporta la selezione di uno o più intervalli di testo o nessuno controllando la proprietà [**IUIAutomationTextPattern::SupportedTextSelection.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-get_supportedtextselection)

Se un controllo basato su testo supporta gli inserimenti di testo, la chiamata di [**IUIAutomationTextRange::AddToSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-addtoselection) o [**RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-removefromselection) su un intervallo di testo degenere nel controllo sposta il punto di inserimento ma non seleziona alcun testo.

## <a name="retrieving-text-from-a-text-range"></a>Recupero di testo da un intervallo di testo

Le applicazioni client possono usare [**il metodo IUIAutomationTextRange::GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) per recuperare il testo normale di un intervallo di testo. Il testo normale include tutti i caratteri di controllo trovati nel testo di origine, ad esempio i ritorni a capo e il contrassegno Unicode da sinistra a destra (LRM). Il testo normale non include tag di markup, ad esempio HTML, che possono essere presenti nel testo di origine. Inoltre, tutti i codici di escape nel testo di origine vengono convertiti negli equivalenti di testo normale. Ad esempio, " &nbsp; " viene convertito in uno spazio semplice.

Se un oggetto incorporato si estende su un intervallo di testo, il testo normale include il testo interno dell'oggetto, ma non il testo alternativo (la proprietà name dell'oggetto incorporato). Per altre informazioni, vedere [How Automazione interfaccia utente Exposes Embedded Objects](uiauto-textpattern-and-embedded-objects-overview.md).

Il [**metodo IUIAutomationTextRange::FindText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findtext) cerca una determinata stringa in un intervallo di testo e, se viene trovata, restituisce un nuovo intervallo di testo che include la stringa.

## <a name="retrieving-text-attributes-from-a-text-range"></a>Recupero di attributi di testo da un intervallo di testo

Gli attributi di testo determinano lo stile di formattazione del testo in un controllo basato su testo e includono elementi come il colore di primo piano, lo stile punto elenco, le dimensioni del carattere e così via. Automazione interfaccia utente supporta diversi attributi di testo e definisce un identificatore per ogni attributo supportato. Un'applicazione client può eseguire una query su un intervallo di testo per il valore di un particolare attributo di testo specificando un identificatore di attributo in una chiamata al metodo [**IUIAutomationTextRange::GetAttributeValue,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) insieme a un puntatore a una struttura [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) che riceve il valore dell'attributo. Per informazioni dettagliate su ogni attributo di testo Automazione interfaccia utente, vedere [Identificatori di attributi di testo.](uiauto-textattribute-ids.md)

Il valore recuperato da [**GetAttributeValue rappresenta**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) il valore dell'attributo nell'intero intervallo di testo. Se tutto il testo nell'intervallo condivide lo stesso valore per l'attributo specificato, tale valore viene restituito da **GetAttributeValue.** Tuttavia, se il valore dell'attributo varia nell'intervallo di testo, **GetAttributeValue** restituisce un puntatore [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) a un oggetto token statico denominato **oggetto ReservedMixedAttribute.** Per scoprire se il valore di un attributo varia in un intervallo di testo, un'applicazione client deve confrontare i risultati di **GetAttributeValue** con l'oggetto **ReservedMixedAttribute** recuperato dalla proprietà [**IUIAutomation::ReservedMixedAttributeValue.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_reservedmixedattributevalue)

Non è necessario un controllo basato su testo per supportare tutti gli Automazione interfaccia utente di testo. Se un client chiama il metodo [**IUIAutomationTextRange::GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) e passa l'identificatore di un attributo non supportato, il metodo restituisce un puntatore [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) a un oggetto token statico denominato **oggetto ReservedNotSupported.** Per determinare se un attributo specifico è supportato, un'applicazione client deve confrontare i risultati di **GetAttributeValue** con l'oggetto **ReservedNotSupported** recuperato dalla proprietà [**IUIAutomation::ReservedNotSupportedValue.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_reservednotsupportedvalue)

Le applicazioni client possono usare il [**metodo IUIAutomationTextRange::FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute) per cercare in un intervallo di testo testo con un attributo di testo specifico. Se viene trovato, il metodo restituisce un nuovo intervallo di testo che include il testo corrispondente. Si noti **che FindAttribute** restituisce un intervallo di testo per la corrispondenza del testo anche se il testo non è visibile.

## <a name="retrieving-embedded-objects-from-a-text-range"></a>Recupero di oggetti incorporati da un intervallo di testo

Un intervallo di testo può includere oggetti incorporati, ad esempio tabelle, immagini, collegamenti ipertestuali e così via. Un'applicazione client può recuperare una raccolta di tutti gli oggetti incorporati in un intervallo chiamando il [**metodo IUIAutomationTextRange::GetChildren.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) Nella raccolta sono inclusi anche gli oggetti incorporati che si sovrappongono all'intervallo ma non sono interamente racchiusi da esso. Se l'intervallo non contiene oggetti incorporati, **GetChildren** recupera una raccolta vuota.

Anche se dipende dal provider del controllo basato su testo, il [**metodo GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) in genere non restituisce alcun elemento figlio degli elementi incorporati. Ad esempio, se un intervallo di testo contiene una tabella con un numero di celle figlio, il metodo **GetChildren** restituisce in genere solo l'elemento tabella e non gli elementi della cella.

Per motivi di prestazioni o architettura, [**GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) potrebbe non essere in grado di recuperare oggetti [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) per tutti gli oggetti incorporati in un intervallo di testo. Al contrario, il provider potrebbe restituire una raccolta che include elementi virtualizzati. Per altre informazioni, vedere [Utilizzo di elementi virtualizzati.](uiauto-workingwithvirtualizeditems.md)

## <a name="manipulating-a-text-range"></a>Modifica di un intervallo di testo

[**L'interfaccia IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) fornisce diversi metodi per la modifica e l'esplorazione di intervalli di testo in un controllo basato su testo. I [**metodi IUIAutomationTextRange::Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move), [**MoveEndpointByUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-moveendpointbyunit)e [**ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit) spostano un intervallo di testo o uno dei relativi endpoint in base all'unità di testo specificata, ad esempio carattere, parola, paragrafo e così via. Per altre informazioni, vedere Automazione interfaccia utente [Text Units](/windows/desktop/WinAuto/uiauto-uiautomationtextunits).

Nonostante il nome, il [**metodo ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit) non espande necessariamente un intervallo di testo. Al contrario, "normalizza" un intervallo di testo spostando gli endpoint in modo che l'intervallo comprersi esattamente l'unità di testo specificata. L'intervallo viene espanso se è inferiore all'unità specificata o abbreviato se è più lungo dell'unità specificata. Il diagramma seguente illustra come **ExpandToEnclosingUnit** normalizza un intervallo di testo spostando gli endpoint dell'intervallo.

![Diagramma che illustra le posizioni degli endpoint prima e dopo una chiamata a expandtoenclosingunit](images/expandtoenclosingunit.jpg)

Se l'intervallo di testo inizia all'inizio di un'unità di testo e termina all'inizio o prima del limite di unità di testo successivo, l'endpoint finale viene spostato al limite di unità di testo successivo (vedere 1 e 2 nella figura precedente).

Se l'intervallo di testo inizia all'inizio di un'unità di testo e termina in corrispondenza o dopo il limite di unità successivo, l'endpoint finale rimane o viene spostato indietro al limite di unità successivo dopo l'endpoint iniziale (vedere 3 e 4 nella figura precedente). Se è presente più di un limite di unità di testo tra gli endpoint iniziale e finale, l'endpoint finale viene spostato indietro al limite di unità successivo dopo l'endpoint iniziale, determinando un intervallo di testo di lunghezza pari a un'unità di testo.

Se l'intervallo di testo inizia al centro di un'unità di testo, l'endpoint iniziale viene spostato indietro all'inizio dell'unità di testo e l'endpoint finale viene spostato in avanti o indietro, se necessario, al limite di unità successivo all'endpoint iniziale (vedere da 5 a 8 nella figura precedente).

Quando viene [**chiamato il metodo IUIAutomationTextRange::Move,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) il provider normalizza l'intervallo di testo in base all'unità di testo specificata. Il provider sposta quindi l'intervallo all'indietro o in avanti del numero specificato di unità di testo. Quando si sposta l'intervallo, il provider ignora i limiti di qualsiasi oggetto incorporato nel testo. Tuttavia, il limite di unità stesso può essere influenzato dall'esistenza di un oggetto incorporato. Il diagramma seguente illustra come il **metodo Move** sposta un intervallo di testo, unità per unità, tra oggetti incorporati e limiti di unità di testo.

![diagramma che mostra come il metodo move sposta gli endpoint di intervallo tra i limiti di oggetti e unità di testo](images/move.jpg)

Il [**metodo IUIAutomationTextRange::MoveEndpointByUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-moveendpointbyunit) sposta uno degli endpoint in avanti o indietro in base all'unità di testo specificata. La figura seguente mostra come un endpoint si sposta in avanti.

![Diagramma che mostra come moveendpointbyunit sposta l'endpoint di un intervallo](images/moveendpointbyunit.gif)

Il [**metodo IUIAutomationTextRange::MoveEndpointByRange**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-moveendpointbyrange) consente a un'applicazione client di impostare un endpoint di un intervallo di testo sulla stessa posizione dell'endpoint specificato di un secondo intervallo di testo.

## <a name="scrolling-a-text-range-into-view"></a>Scorrimento di un intervallo di testo nella visualizzazione

Il [**metodo IUIAutomationTextRange::ScrollIntoView**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-scrollintoview) scorre un intervallo di testo in modo che il testo sia visibile nel riquadro di visualizzazione del controllo basato su testo. Quando si **chiama ScrollIntoView,** un client può specificare se il testo deve essere allineato alla parte superiore o inferiore del viewport.

## <a name="retrieving-the-enclosing-element-of-a-text-range"></a>Recupero dell'elemento di inclusione di un intervallo di testo

Un'applicazione client può usare il metodo [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) per recuperare il puntatore a interfaccia [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) dell'elemento più interno che racchiude un intervallo di testo. L'elemento di inclusione è in genere il provider di testo che fornisce l'intervallo di testo. Tuttavia, se il provider di testo supporta elementi figlio, ad esempio tabelle o collegamenti ipertestuali, l'elemento contenitore potrebbe essere un discendente del provider di testo.

## <a name="comparing-and-cloning-text-ranges"></a>Confronto e clonazione di intervalli di testo

[**L'interfaccia IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) include due metodi per confrontare gli intervalli di testo. Il [**metodo IUIAutomationTextRange::Compare**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-compareendpoints) confronta gli endpoint iniziale e finale di due intervalli di testo e restituisce **TRUE** se entrambi gli endpoint sono uguali. Il **metodo IUIAutomationTextRange::CompareEndpoints** confronta l'endpoint iniziale o finale dei due intervalli. Il valore restituito è zero se gli endpoint sono uguali oppure un valore positivo o negativo che indica le posizioni relative dei due endpoint.

Le applicazioni client possono usare il [**metodo IUIAutomationTextRange::Clone**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-clone) per creare una copia esatta dell'intervallo di testo. Il nuovo intervallo di testo può essere modificato indipendentemente dall'intervallo di testo originale.

## <a name="retrieving-annotations"></a>Recupero di annotazioni

Un intervallo di testo può includere annotazioni se il controllo basato su testo le supporta. Esistono molti tipi diversi di annotazioni. Il file di intestazione UIAutomationClient.h definisce un set di valori costanti denominati che identificano i tipi di annotazioni Automazione interfaccia utente supporta. Per altre informazioni, vedere [**Identificatori del tipo di annotazione**](uiauto-annotation-type-identifiers.md).

Alcuni tipi di annotazioni sono rappresentati da un elemento di automazione che supporta il pattern di controllo [Annotation](uiauto-implementingannotation.md) [**(interfaccia IUIAutomationAnnotationPattern).**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationannotationpattern) Altri tipi di annotazioni vengono esposti tramite il pattern [di controllo TextRange.](uiauto-about-text-and-textrange-patterns.md) Ad esempio, un provider può esporre un semplice indicatore di errore ortografico facendo in modo che il metodo [**IUIAutomationTextRange::GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) restituirà un attributo di testo [**AnnotationTypes**](uiauto-textattribute-ids.md) [**di AnnotationType \_ SpellingError**](uiauto-annotation-type-identifiers.md)e un valore Null per l'attributo di testo [**AnnotationObjects.**](uiauto-textattribute-ids.md)

### <a name="retrieving-annotations-types-from-a-text-range"></a>Recupero di tipi di annotazioni da un intervallo di testo

È possibile recuperare un elenco dei tipi di annotazioni presenti in un intervallo di testo usando il metodo [**IUIAutomationTextRange::GetAttributeValue.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) Quando si chiama il metodo , specificare un ID attributo di testo [**di UIA \_ AnnotationTypesAttributeId**](uiauto-textattribute-ids.md) e un puntatore a un parametro di tipo [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant). Quando il metodo viene restituito, il **parametro VARIANT** contiene un elenco di identificatori di tipo di annotazione, uno per ogni tipo di annotazione nell'intervallo di testo. Per altre informazioni, vedere [**Identificatori del tipo di annotazione**](uiauto-annotation-type-identifiers.md).

### <a name="retrieving-all-annotations-from-a-text-range"></a>Recupero di tutte le annotazioni da un intervallo di testo

Per recuperare le annotazioni da un intervallo di testo, chiamare il metodo [**IUIAutomationTextRange::GetAttributeValue,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) specificando un ID attributo di testo [**di UIA \_ AnnotationObjectsAttributeId**](uiauto-textattribute-ids.md) e un puntatore a un parametro di tipo [**VARIANT.**](/windows/win32/api/oaidl/ns-oaidl-variant) Quando il metodo viene restituito, il parametro **VARIANT** contiene [**un'interfaccia IUIAutomationElementArray**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray) che rappresenta una matrice di elementi di automazione, uno per ogni annotazione nell'intervallo di testo. La proprietà [**IUIAutomationElementArray::Length**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelementarray-get_length) indica il numero di elementi nella matrice e il metodo [**IUIAutomationElementArray::GetElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelementarray-getelement) recupera l'interfaccia [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) per un determinato elemento.

### <a name="retrieving-information-about-a-particular-annotation"></a>Recupero di informazioni su un'annotazione specifica

Per recuperare informazioni su una particolare annotazione, recuperare prima di tutto [**l'interfaccia IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) per l'elemento di annotazione, come descritto nella sezione precedente. Recuperare quindi [**l'interfaccia IUIAutomationAnnotationPattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationannotationpattern) per l'annotazione chiamando il metodo [**IUIAutomationElement::GetCurrentPatternAs**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpatternas) con un ID pattern di controllo [**UIA \_ AnnotationPatternId,**](uiauto-controlpattern-ids.md)un identificatore di interfaccia IID IUIAutomationAnnotationPattern e l'indirizzo di una variabile che riceve il puntatore \_ **IUIAutomationAnnotation** per l'annotazione. Eseguire una query nelle proprietà dell'interfaccia **IUIAutomationAnnotation** per recuperare il nome del tipo di annotazione e l'ID del tipo, il nome dell'autore dell'annotazione, la data e l'ora dell'annotazione e l'interfaccia **IUIAutomationElement** per l'elemento annotato.

### <a name="retrieving-the-annotation-target-text"></a>Recupero del testo di destinazione dell'annotazione

In genere, un'annotazione si applica a un subset di testo in un intervallo di testo. Dopo aver recuperato [**l'interfaccia IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) per un'annotazione, è possibile passare l'interfaccia al metodo [**IUIAutomationTextRange2::RangeFromAnnotation**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider2-rangefromannotation) per recuperare un intervallo di testo contenente il testo che rappresenta la destinazione dell'annotazione.

## <a name="retrieving-visual-styles"></a>Recupero degli stili di visualizzazione

Un provider implementa il pattern [di controllo Styles](/windows/desktop/WinAuto/uiauto-implementingstyles) per descrivere un elemento dell'interfaccia utente con uno stile, un colore di riempimento, un motivo di riempimento o una forma specifici. Ciò è particolarmente utile quando si descrivono elementi in un documento, che hanno spesso tali stili. Stili come questo spesso trasportano informazioni utili per i clienti con disabilità; Ad esempio, gli stili possono descrivere una determinata stringa come titolo di un documento o un determinato oggetto diagramma di flusso come rombo o cerchio.

È possibile usare il [**metodo IUIAutomationTextRange::GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) per recuperare i nomi e gli identificatori degli stili di visualizzazione usati in un intervallo di testo. Usare [**l'attributo di testo UIA \_ StyleNameAttributeId**](uiauto-textattribute-ids.md) per recuperare i nomi di stile e [**UIA \_ StyleIdAttributeId**](uiauto-textattribute-ids.md) per recuperare gli identificatori di stile.

Un controllo basato su testo che supporta gli stili di visualizzazione può implementare il pattern di controllo [Styles](/windows/desktop/WinAuto/uiauto-implementingstyles) per consentire ai client di accedere alle informazioni su uno stile di visualizzazione usato dal controllo. I client accedono al pattern di controllo Styles tramite [**l'interfaccia IUIAutomationStylesPattern.**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationstylespattern) È possibile recuperare questa interfaccia chiamando il metodo [**IUIAutomationElement::GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) o [**GetCurrentPatternAs,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpatternas) specificando [**UIA \_ StylesPatternId**](uiauto-controlpattern-ids.md) come identificatore del pattern di controllo.

[**L'interfaccia IUIAutomationStylesPattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationstylespattern) include proprietà e metodi che forniscono le informazioni seguenti su uno stile di visualizzazione:

-   Nome dello stile di visualizzazione, ad esempio "Normal" o "Heading 1".
-   Identificatore dello stile di visualizzazione. Per altre informazioni, vedere [**Identificatori di stile**](uiauto-style-identifiers.md).
-   Colore utilizzato per riempire il controllo basato su testo.
-   Colore del modello utilizzato per riempire il controllo basato su testo.
-   Forma del controllo basato su testo.
-   Proprietà estese. cio, un elenco di nomi e valori di stile specifici del controllo.

## <a name="invoking-context-menus-from-text-ranges"></a>Chiamata di menu di scelta rapida da intervalli di testo

A partire da Windows 8.1, gli intervalli di testo possono supportare [**l'interfaccia IUIAutomationTextRange2.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange2) Questa interfaccia supporta il [**metodo ShowContextMenu.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange2-showcontextmenu) È possibile chiamare questo metodo per richiamare qualsiasi menu di scelta rapida associato a un intervallo di testo. Lo scenario per questa operazione è la correzione automatica degli intervalli di testo o della selezione di candidati IME. In questi casi viene visualizzato un menu di scelta rapida che supporta l'interazione dell'utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pattern di controllo Text e TextRange](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[Automazione interfaccia utente supporto per il contenuto testuale](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Uso di controlli basati su testo](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 
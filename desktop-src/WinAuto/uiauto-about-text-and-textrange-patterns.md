---
title: Informazioni sui pattern di controllo Text e TextRange
description: Il contenuto testuale di un controllo viene esposto usando il pattern di controllo Text, che rappresenta il contenuto di un contenitore di testo come flusso di testo.
ms.assetid: acc2b513-9367-416a-b0d9-3c2bcc14a8a7
keywords:
- Automazione interfaccia utente, supporto del contenuto testuale
- Automazione interfaccia utente,panoramica del modello di testo
- Automazione interfaccia utente,panoramica dei controlli di testo
- Automazione interfaccia utente,Pattern di controllo testo
- Automazione interfaccia utente,Framework servizi di testo (TSF)
- Automazione interfaccia utente,TSF
- Automazione interfaccia utente, prestazioni
- modelli di testo, informazioni
- modelli di testo,Framework servizi di testo (TSF)
- controlli di testo, informazioni
- contenuto testuale, supporto per
- controlli di testo, prestazioni
- Pattern di controllo del testo
- pattern di controllo,testo
- Framework servizi di testo
- TSF (Framework servizi di testo)
- prestazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04112e0233db056c5ff3e81b68256229aa45f60cfdb1258e565e10aea1cd43ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052359"
---
# <a name="about-the-text-and-textrange-control-patterns"></a>Informazioni sui pattern di controllo Text e TextRange

Il contenuto testuale di un controllo viene esposto usando il pattern di controllo [Text,](uiauto-implementingtextandtextrange.md) che rappresenta il contenuto di un contenitore di testo come flusso di testo. Il pattern di controllo Text richiede il supporto del pattern di controllo TextRange per esporre gli attributi di formato e stile. Il pattern di controllo TextRange supporta il pattern di controllo Text rappresentando intervalli di testo contigui o multipli e non contigui (o intervalli) in un contenitore di testo con una raccolta di endpoint di inizio e fine. Il pattern di controllo TextRange supporta funzionalità quali selezione, confronto, recupero e attraversamento.

> [!Note]  
> Il [pattern di](uiauto-implementingtextandtextrange.md) controllo Text non fornisce un mezzo per inserire o modificare il testo. Tuttavia, a seconda del controllo, questa operazione può essere eseguita usando il pattern di controllo Microsoft Automazione interfaccia utente [Value](uiauto-implementingvalue.md) o tramite input diretto da tastiera. È anche disponibile un modello [**TextEdit**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itexteditprovider) che supporta la modifica a livello di codice del testo.

 

La funzionalità descritta in questo argomento è essenziale per assistive technology fornitori e gli utenti finali. Le tecnologie di assistive possono usare Automazione interfaccia utente per raccogliere informazioni complete sulla formattazione del testo per l'utente e fornire la navigazione a livello di codice e la selezione del testo in base a [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) (carattere, parola, riga o paragrafo).

In questo argomento sono incluse le sezioni seguenti:

-   [Automazione interfaccia utente TextPattern e il Framework servizi di testo](#ui-automation-textpattern-and-the-text-services-framework)
-   [Tipi di controllo](#control-types)
-   [Interfacce del provider](#provider-interfaces)
-   [Interfacce client](#client-interfaces)
-   [Prestazioni](#performance)
-   [Modello di testo e oggetti incorporati virtualizzati](#text-pattern-and-virtualized-embedded-objects)
-   [Uso del tipo di controllo personalizzato con il pattern di controllo del testo](#using-the-custom-control-type-with-the-text-control-pattern)
-   [Durata di un intervallo di testo](#lifetime-of-a-text-range)
-   [Argomenti correlati](#related-topics)

## <a name="ui-automation-textpattern-and-the-text-services-framework"></a>Automazione interfaccia utente TextPattern e il Framework servizi di testo

Framework servizi di testo (TSF) è un framework di sistema semplice e scalabile che consente servizi di linguaggio naturale e input di testo avanzato sul desktop e nelle applicazioni. Oltre a fornire alle applicazioni interfacce per esporre l'archivio di testo, supporta anche i metadati per l'archivio di testo.

TSF è stato progettato per le applicazioni che devono inserire input in scenari in grado di riconoscere il contesto. Il [pattern di](uiauto-implementingtextandtextrange.md) controllo Text, tuttavia, è una soluzione di sola lettura destinata a fornire l'accesso ottimizzato a un archivio di testo per utilità per la lettura dello schermo e dispositivi Braille.

Le tecnologie accessibili che richiedono l'accesso in sola lettura a un archivio di testo possono usare il pattern di controllo Text, ma richiedono la funzionalità di TSF per l'input in grado di riconoscere il contesto.

Per altre informazioni, [vedere](/windows/desktop/TSF/text-services-framework)Framework servizi di testo .

## <a name="control-types"></a>Tipi di controllo

Il Automazione interfaccia utente [di controllo Edit](uiauto-supporteditcontroltype.md) e il tipo di controllo [Document](uiauto-supportdocumentcontroltype.md) devono supportare il pattern di [controllo Text.](uiauto-implementingtextandtextrange.md) Per migliorare l'accessibilità, Microsoft consiglia che anche i [tipi di controllo ToolTip](uiauto-supporttooltipcontroltype.md) e Text supportino il pattern di controllo Text, ma non è obbligatorio.

## <a name="provider-interfaces"></a>Interfacce del provider

Automazione interfaccia utente provider supportano il [pattern di](uiauto-implementingtextandtextrange.md) controllo Text per un controllo implementando le [**interfacce ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) e [**ITextRangeProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) Queste interfacce espongono informazioni dettagliate sugli attributi per il testo nel controllo e forniscono funzionalità di navigazione affidabili.

Un provider non deve supportare tutti gli attributi di testo se il controllo non supporta alcun attributo specifico.

Un provider deve supportare i metodi [**ITextProvider::GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection) e [**ITextRangeProvider::Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select) se il controllo supporta la selezione del testo o la posizione del cursore di testo (o cursore di sistema) all'interno dell'area di testo. Se il controllo non supporta questa funzionalità, non è necessario supportare uno di questi metodi. Tuttavia, il controllo deve esporre il tipo di selezione di testo supportato implementando la [**proprietà ITextProvider::SupportedTextSelection.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_supportedtextselection)

Un provider deve sempre supportare le costanti [**TextUnit,**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) **TextUnit \_ Character** e **TextUnit \_ Document,** nonché qualsiasi altro elemento che è in grado di supportare.

> [!Note]  
> Il provider può ignorare il supporto per [**un oggetto TextUnit specifico**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) rinviando all'unità più grande successiva supportata nell'ordine seguente: Carattere **TextUnit \_**, **Formato TextUnit \_**, **TextUnit \_ Word**, **Riga TextUnit \_**, **Paragrafo TextUnit \_**, **Pagina TextUnit \_** e **Documento TextUnit \_**.

 

## <a name="client-interfaces"></a>Interfacce client

Automazione interfaccia utente applicazioni client usano le interfacce [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) e [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) per accedere al contenuto testuale di un controllo di testo. I client **usano IUIAutomationTextPattern** per selezionare intervalli di testo denominati intervalli di testo e per recuperare puntatori alle **interfacce IUIAutomationTextRange** per gli intervalli. **L'interfaccia IUIAutomationTextRange** consente ai client di modificare l'intervallo di testo e di recuperare informazioni sul testo nell'intervallo, inclusi attributi quali il nome del carattere, il colore di primo piano, lo stile di sottolineatura e così via. Per altre informazioni, vedere [Identificatori di attributi di testo](uiauto-textattribute-ids.md).

## <a name="performance"></a>Prestazioni

Il **pattern di** controllo Text si basa su chiamate tra processi per la maggior parte delle funzionalità, quindi non fornisce un meccanismo di memorizzazione nella cache per migliorare le prestazioni durante l'elaborazione del contenuto. È possibile accedere ad altri pattern di controllo in Microsoft Automazione interfaccia utente usando il metodo [**IUIAutomationElement::GetCachedPattern.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpattern)

Una tecnica per migliorare le prestazioni consiste nel garantire che i client Automazione interfaccia utente tentino di recuperare blocchi di testo di dimensioni moderate usando il metodo [**IUIAutomationTextRange::GetText.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) Ad esempio, l'uso di **GetText** per recuperare singoli caratteri comporta riscontri tra processi per ogni carattere, mentre se non si specifica una lunghezza massima quando si chiama **GetText** si verifica un solo hit cross-process, ma può avere una latenza elevata a seconda delle dimensioni dell'intervallo di testo.

## <a name="text-pattern-and-virtualized-embedded-objects"></a>Modello di testo e oggetti incorporati virtualizzati

Quando possibile, un'implementazione del provider [**di ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) e [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) deve supportare l'intero testo di un documento, incluso il testo all'esterno del viewport. Per il testo fuori schermo o gli oggetti incorporati virtualizzati, i provider devono supportare il pattern di controllo [VirtualizedItem](uiauto-implementingvirtualizeditem.md) ([**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider)).

Se un documento è virtualizzato mentre l'intero flusso di testo è ancora disponibile, la proprietà [**ITextProvider::D ocumentRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_documentrange) recupererà un intervallo di testo che include l'intero documento. Tuttavia, la chiamata [**al metodo ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getchildren) recupererà una raccolta di oggetti virtualizzati che rappresentano tutti gli oggetti incorporati nel documento. Per interagire con un oggetto incorporato virtualizzato, i client devono chiamare il metodo [**IVirtualizedItemProvider::Realize,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) che rende gli elementi completamente accessibili come Automazione interfaccia utente elementi. I client devono seguire un processo simile per usare gli elementi della griglia in una tabella incorporata in cui una parte della tabella è fuori schermo e virtualizzata.

## <a name="using-the-custom-control-type-with-the-text-control-pattern"></a>Uso del tipo di controllo personalizzato con il pattern di controllo del testo

Sebbene il [pattern di](uiauto-implementingtextandtextrange.md) controllo Text supporti molti attributi di testo e oggetti incorporati, non è possibile definire in anticipo tutti gli elementi del documento e i tipi di presentazione possibili. Per gli elementi del documento non supportati dagli attributi esistenti o dai tipi di controllo standard, i provider possono usare le funzionalità di estendibilità fornite dal tipo di controllo Automazione interfaccia utente **personalizzato.**

Per le applicazioni e le interfacce utente basate su presentazioni di pagine, il limite e la presentazione del layout di "pagina" possono essere espressi anche come oggetto incorporato con un tipo di controllo personalizzato , ovvero `LocalizedControlType="page"` . In questo modo, l'oggetto incorporato può ospitare altri elementi di pagina che non possono facilmente far parte del flusso di testo del documento, ad esempio i campi intestazione e piè di pagina di ogni pagina, come elementi figlio dell'oggetto incorporato "page". In alternativa, ogni oggetto "page" può supportare il pattern di controllo [Text](uiauto-implementingtextandtextrange.md) in modo indipendente, che funziona bene per applicazioni come strumenti di creazione per presentazioni di presentazioni di presentazioni o ambienti di pubblicazione desktop basati su pagina.

## <a name="lifetime-of-a-text-range"></a>Durata di un intervallo di testo

Se possibile, un provider deve garantire che eventuali modifiche al testo, ad esempio eliminazioni, inserimenti e spostamenti, siano riflesse nell'intervallo di testo associato. Se l'aggiornamento dell'intervallo di testo non è possibile, il provider deve generare un evento [**\_ \_ TextChangedEventId**](uiauto-event-ids.md) dell'interfaccia utente per notificare ai client che l'intervallo di testo non è più valido e che è necessario recuperarne uno nuovo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Come Automazione interfaccia utente supporta gli oggetti incorporati](uiauto-textpattern-and-embedded-objects-overview.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Automazione interfaccia utente supporto per il contenuto testuale](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Uso di controlli basati su testo](uiauto-workingwithtextbasedcontrols.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[Text Services Framework](/windows/desktop/TSF/text-services-framework)
</dt> </dl>

 

 
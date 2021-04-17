---
title: Informazioni sui pattern di controllo Text e TextRange
description: Il contenuto testuale di un controllo viene esposto usando il pattern di controllo Text, che rappresenta il contenuto di un contenitore di testo come flusso di testo.
ms.assetid: acc2b513-9367-416a-b0d9-3c2bcc14a8a7
keywords:
- Automazione interfaccia utente, supporto contenuto testuale
- Automazione interfaccia utente, panoramica del modello di testo
- Automazione interfaccia utente, Cenni preliminari sui controlli testo
- Automazione interfaccia utente, pattern di controllo Text
- Automazione interfaccia utente, Framework dei servizi di testo (TSF)
- Automazione interfaccia utente, TSF
- Automazione interfaccia utente, prestazioni
- modelli di testo, informazioni
- modelli di testo, Framework dei servizi di testo (TSF)
- controlli testo, informazioni
- contenuto testuale, supporto per
- controlli testo, prestazioni
- Pattern di controllo Text
- pattern di controllo, testo
- Framework servizi di testo
- TSF (Framework dei servizi di testo)
- prestazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb9ff1eb75227454e3e9df6035798a304096a958
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300356"
---
# <a name="about-the-text-and-textrange-control-patterns"></a>Informazioni sui pattern di controllo Text e TextRange

Il contenuto testuale di un controllo viene esposto usando il pattern di controllo [Text](uiauto-implementingtextandtextrange.md) , che rappresenta il contenuto di un contenitore di testo come flusso di testo. Il pattern di controllo Text richiede il supporto del pattern di controllo TextRange per esporre gli attributi di formato e stile. Il pattern di controllo TextRange supporta il pattern di controllo Text mediante la rappresentazione di intervalli di testo contigui o multipli, non contigui (o intervalli) in un contenitore di testo con una raccolta di endpoint di inizio e di fine. Il pattern di controllo TextRange supporta funzionalità quali la selezione, il confronto, il recupero e l'attraversamento.

> [!Note]  
> Il pattern di controllo [Text](uiauto-implementingtextandtextrange.md) non fornisce un mezzo per inserire o modificare il testo. Tuttavia, a seconda del controllo, questa operazione può essere eseguita usando il pattern di controllo [value](uiauto-implementingvalue.md) di automazione interfaccia utente Microsoft o l'input diretto della tastiera. È disponibile anche un modello [**TextEdit**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itexteditprovider) che supporta la modifica a livello di codice del testo.

 

La funzionalità descritta in questo argomento è fondamentale per i fornitori di tecnologie per l'accesso facilitato e per gli utenti finali. Le tecnologie per l'accesso facilitato possono usare l'automazione dell'interfaccia utente per raccogliere informazioni complete sulla formattazione del testo per l'utente e fornire navigazione a livello di codice e selezione del testo in base a [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) (carattere, parola, riga o paragrafo).

In questo argomento sono incluse le sezioni seguenti:

-   [Textpattern di automazione interfaccia utente e il Framework dei servizi di testo](#ui-automation-textpattern-and-the-text-services-framework)
-   [Tipi di controllo](#control-types)
-   [Interfacce del provider](#provider-interfaces)
-   [Interfacce client](#client-interfaces)
-   [Prestazioni](#performance)
-   [Modello di testo e oggetti incorporati virtualizzati](#text-pattern-and-virtualized-embedded-objects)
-   [Uso del tipo di controllo personalizzato con il pattern di controllo Text](#using-the-custom-control-type-with-the-text-control-pattern)
-   [Durata di un intervallo di testo](#lifetime-of-a-text-range)
-   [Argomenti correlati](#related-topics)

## <a name="ui-automation-textpattern-and-the-text-services-framework"></a>Textpattern di automazione interfaccia utente e il Framework dei servizi di testo

Il Framework di servizi di testo (TSF) è un Framework di sistema semplice e scalabile che Abilita servizi di linguaggio naturale e input di testo avanzato sul desktop e nelle applicazioni. Oltre a fornire interfacce per le applicazioni che espongono l'archivio di testo, supporta anche i metadati per l'archivio di testo.

TSF è stato progettato per le applicazioni che devono inserire input in scenari compatibili con il contesto. Il pattern di controllo [Text](uiauto-implementingtextandtextrange.md) , tuttavia, è una soluzione di sola lettura progettata per fornire accesso ottimizzato a un archivio di testo per i lettori dello schermo e i dispositivi Braille.

Le tecnologie accessibili che richiedono l'accesso in sola lettura a un archivio di testo possono usare il pattern di controllo Text, ma richiedono la funzionalità di TSF per l'input compatibile con il contesto.

Per altre informazioni, vedere [Framework di servizi di testo](/windows/desktop/TSF/text-services-framework).

## <a name="control-types"></a>Tipi di controllo

Il tipo di controllo di [modifica](uiauto-supporteditcontroltype.md) e [il tipo di controllo di](uiauto-supportdocumentcontroltype.md) automazione interfaccia utente devono supportare il pattern di controllo [Text](uiauto-implementingtextandtextrange.md) . Per migliorare l'accessibilità, è consigliabile che i tipi di controllo [ToolTip](uiauto-supporttooltipcontroltype.md) e Text supportino anche il pattern di controllo Text, ma non è obbligatorio.

## <a name="provider-interfaces"></a>Interfacce del provider

I provider di automazione interfaccia utente supportano il pattern di controllo [Text](uiauto-implementingtextandtextrange.md) per un controllo mediante l'implementazione delle interfacce [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) e [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) . Queste interfacce espongono informazioni dettagliate sugli attributi per il testo nel controllo e forniscono funzionalità di spostamento affidabili.

Non è necessario che un provider supporti tutti gli attributi di testo se il controllo non dispone del supporto per un attributo specifico.

Un provider deve supportare i metodi [**ITextProvider:: GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection) e [**ITextRangeProvider:: SELECT**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select) se il controllo supporta la selezione di testo o il posizionamento del cursore di testo (o cursore di sistema) all'interno dell'area di testo. Se il controllo non supporta questa funzionalità, non è necessario che supporti uno di questi metodi. Il controllo deve tuttavia esporre il tipo di selezione di testo supportato implementando la proprietà [**ITextProvider:: SupportedTextSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_supportedtextselection) .

Un provider deve supportare sempre le costanti [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) , il **\_ carattere TextUnit** e **il \_ documento TextUnit**, nonché tutti gli altri che è in grado di supportare.

> [!Note]  
> Il provider può ignorare il supporto per un [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) specifico facendo riferimento alla successiva unità più grande supportata nell'ordine seguente: **TextUnit \_ character**, **TextUnit \_ Format**, **TextUnit \_ Word**, **TextUnit \_ line**, **TextUnit \_ Paragraph**, **TextUnit \_ Page** e **TextUnit \_ Document**.

 

## <a name="client-interfaces"></a>Interfacce client

Le applicazioni client di automazione interfaccia utente utilizzano le interfacce [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) e [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) per accedere al contenuto testuale di un controllo di testo. I client usano **IUIAutomationTextPattern** per selezionare intervalli di testo denominati *intervalli di testo* e per recuperare i puntatori alle interfacce **IUIAutomationTextRange** per gli intervalli. L'interfaccia **IUIAutomationTextRange** consente ai client di modificare l'intervallo di testo e di recuperare informazioni sul testo nell'intervallo, inclusi attributi come il nome del tipo di carattere, il colore di primo piano, lo stile di sottolineatura e così via. Per altre informazioni, vedere [identificatori di attributi di testo](uiauto-textattribute-ids.md).

## <a name="performance"></a>Prestazioni

Il pattern di controllo **Text** si basa sulle chiamate tra processi per la maggior parte delle funzionalità, pertanto non fornisce un meccanismo di memorizzazione nella cache per migliorare le prestazioni durante l'elaborazione del contenuto. Per accedere ad altri pattern di controllo nell'automazione interfaccia utente Microsoft, è possibile usare il metodo [**IUIAutomationElement:: GetCachedPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpattern) .

Una tecnica per migliorare le prestazioni consiste nel garantire che i client di automazione interfaccia utente tentino di recuperare blocchi di testo di dimensioni moderate tramite il metodo [**IUIAutomationTextRange:: GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) . Ad esempio, l'utilizzo di **gettext** per recuperare i singoli caratteri comporterà riscontri tra processi per ogni carattere, mentre se non si specifica una lunghezza massima durante la chiamata di **gettext** , viene raggiunto un hit tra processi, ma può avere una latenza elevata a seconda delle dimensioni dell'intervallo di testo.

## <a name="text-pattern-and-virtualized-embedded-objects"></a>Modello di testo e oggetti incorporati virtualizzati

Quando possibile, un'implementazione del provider di [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) e [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) deve supportare l'intero testo di un documento, incluso il testo all'esterno del viewport. Per il testo non visualizzato o gli oggetti incorporati virtualizzati, i provider devono supportare il [pattern di controllo VirtualizedItem](uiauto-implementingvirtualizeditem.md) ([**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider)).

Se un documento è virtualizzato mentre è ancora disponibile l'intero flusso di testo, la proprietà [**ITextProvider::D ocumentrange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_documentrange) recupererà un intervallo di testo che include l'intero documento. La chiamata al metodo [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getchildren) , tuttavia, consente di recuperare una raccolta di oggetti virtualizzati che rappresentano tutti gli oggetti incorporati nel documento. Per interagire con un oggetto incorporato virtualizzato, i client devono chiamare il metodo [**IVirtualizedItemProvider:: réalisateur**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) , che rende gli elementi completamente accessibili come elementi di automazione interfaccia utente. I client devono seguire un processo simile per lavorare con gli elementi della griglia in una tabella incorporata in cui una parte della tabella è fuori schermo e virtualizzata.

## <a name="using-the-custom-control-type-with-the-text-control-pattern"></a>Uso del tipo di controllo personalizzato con il pattern di controllo Text

Sebbene il pattern di controllo [Text](uiauto-implementingtextandtextrange.md) supporti molti attributi di testo e oggetti incorporati, non è possibile definire in anticipo tutti i possibili elementi del documento e i tipi di presentazione. Per gli elementi del documento non supportati dagli attributi esistenti o dai tipi di controllo standard, i provider possono utilizzare le funzionalità di estendibilità fornite dal tipo di controllo **personalizzato** di automazione interfaccia utente.

Per le applicazioni e le interfacce utente basate sulle presentazioni della pagina, la presentazione del limite e del layout di "Page" può essere espressa anche come oggetto incorporato che dispone di un tipo di controllo personalizzato (ovvero `LocalizedControlType="page"` ). In questo modo, l'oggetto incorporato può ospitare altri elementi della pagina che non possono facilmente far parte del flusso di testo del documento, ad esempio i campi di intestazione e piè di pagina di ogni pagina, come elementi figlio dell'oggetto incorporato "Page". In alternativa, ogni oggetto "Page" può supportare il pattern di controllo [Text](uiauto-implementingtextandtextrange.md) in modo indipendente, che funziona bene per le applicazioni, ad esempio gli strumenti di creazione di presentazioni o gli ambienti di pubblicazione desktop basati su pagine.

## <a name="lifetime-of-a-text-range"></a>Durata di un intervallo di testo

Se possibile, un provider deve garantire che tutte le modifiche apportate al testo, ad esempio eliminazioni, inserimenti e spostamenti, siano riflesse nell'intervallo di testo associato. Se non è possibile aggiornare l'intervallo di testo, il provider deve generare un evento [**\_ \_ TextChangedEventId di testo UIA**](uiauto-event-ids.md) per notificare ai client che l'intervallo di testo non è più valido ed è necessario recuperarne uno nuovo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Come automazione interfaccia utente supporta oggetti incorporati](uiauto-textpattern-and-embedded-objects-overview.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Supporto di automazione interfaccia utente per contenuto testuale](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Utilizzo di controlli basati su testo](uiauto-workingwithtextbasedcontrols.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[Text Services Framework](/windows/desktop/TSF/text-services-framework)
</dt> </dl>

 

 
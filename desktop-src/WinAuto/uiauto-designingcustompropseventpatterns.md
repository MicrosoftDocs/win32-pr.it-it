---
title: Progettare proprietà personalizzate, eventi e pattern di controllo
description: La progettazione di una proprietà personalizzata, di un evento o di un pattern di controllo deve essere utile in un'ampia gamma di implementazioni di controlli.
ms.assetid: e4b224a0-3958-4ae7-96cb-fe6dc16511a7
keywords:
- Automazione interfaccia utente, proprietà personalizzate
- Automazione interfaccia utente, panoramica degli eventi
- Automazione interfaccia utente, Cenni preliminari sui pattern di controllo
- Automazione interfaccia utente, progettazione di proprietà personalizzate
- Automazione interfaccia utente, progettazione di eventi
- Automazione interfaccia utente, progettazione di pattern di controllo
- Automazione interfaccia utente, WinEvents
- Proprietà personalizzate, progettazione
- eventi, progettazione
- eventi, WinEvents
- pattern di controllo, progettazione
- WinEvents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e6973356fe6be922e73eef70e5107b6dcabe0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399083"
---
# <a name="design-custom-properties-events-and-control-patterns"></a>Progettare proprietà personalizzate, eventi e pattern di controllo

La progettazione di una proprietà personalizzata, di un evento o di un pattern di controllo deve essere utile in un'ampia gamma di implementazioni di controlli. Le progettazioni specifiche del controllo o dell'applicazione che risultano utili solo negli scenari limitati devono essere evitate. Il progetto deve seguire l'esempio delle proprietà, degli eventi e dei pattern di controllo esistenti di automazione interfaccia utente Microsoft, che sono stati accuratamente specificati per soddisfare le esigenze di un'ampia gamma di applicazioni di test automatizzate e di accessibilità.

L'implementazione della specifica per una proprietà, un evento o un pattern di controllo personalizzati implica la collaborazione e il contratto delle parti sul lato client e provider e richiede che entrambe le parti implementino la specifica in modo coerente. Le aziende sono incoraggiate a collaborare con le organizzazioni del settore, ad esempio l' [alleanza di interoperabilità di accessibilità (Aia)](https://www.atia.org/) , per progettare e pubblicare le specifiche per la proprietà personalizzata, l'evento o il pattern di controllo. In questo modo, è possibile raggiungere il consenso e garantire l'interoperabilità con la più ampia gamma di applicazioni.

In questo argomento sono incluse le sezioni seguenti:

-   [Quando usare proprietà ed eventi personalizzati](#when-to-use-custom-properties-and-events)
-   [Progettazione di proprietà personalizzate](#designing-custom-properties)
-   [Progettazione di eventi personalizzati](#designing-custom-events)
    -   [Eventi di automazione interfaccia utente personalizzati e WinEvents](#custom-ui-automation-events-and-winevents)
-   [Progettazione di pattern di controllo personalizzati](#designing-custom-control-patterns)
-   [Tipi di controlli personalizzati](#custom-control-types)
-   [Argomenti correlati](#related-topics)

## <a name="when-to-use-custom-properties-and-events"></a>Quando usare proprietà ed eventi personalizzati

Prima di creare una proprietà personalizzata, un evento o un pattern di controllo, assicurarsi che automazione interfaccia utente non fornisca una soluzione esistente. Ad esempio, la creazione di un pattern di controllo "click" personalizzato non è necessaria perché il pattern di controllo [Invoke](uiauto-implementinginvoke.md) già descrive tale funzionalità.

Se si decide che è necessaria una proprietà, un evento o un pattern di controllo personalizzati, assicurarsi che non sia troppo vago o generico. Un pattern di controllo denominato "Show", ad esempio, non è utile perché la visibilità di un controllo può essere indicata da una proprietà di disponibilità nell'elemento, ad esempio [**\_ IsExpandCollapsePatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md) di gestione dei criteri di [**\_ IsScrollItemPatternAvailablePropertyId o UIA**](uiauto-control-pattern-availability-propids.md).

Prima di implementare una soluzione personalizzata, verificare con attenzione che sia necessario e quindi progettare completamente la funzionalità.

## <a name="designing-custom-properties"></a>Progettazione di proprietà personalizzate

Automazione interfaccia utente include due tipi di proprietà di base: proprietà degli elementi di automazione e proprietà del pattern di controllo. Le proprietà degli elementi di automazione sono costituite da un set comune di proprietà, ad esempio Name, AcceleratorKey e NomeClasse, che sono esposte da tutti gli elementi di automazione interfaccia utente, indipendentemente dal tipo di controllo. Le proprietà del pattern di controllo sono esposte da un controllo tramite un determinato pattern di controllo. Ogni pattern di controllo ha un set corrispondente di proprietà del pattern di controllo che il controllo deve esporre. Ad esempio, un controllo che supporta il pattern di controllo [Grid](uiauto-implementinggrid.md) espone le proprietà ColumnCount e RowCount.

Una proprietà dell'elemento di automazione personalizzato o una proprietà del pattern di controllo deve rispettare le linee guida di progettazione seguenti:

-   Una proprietà personalizzata deve avere uno dei seguenti tipi di dati specificati dall'enumerazione [**UIAutomationType**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype) . Non sono supportati altri tipi di dati per le proprietà personalizzate.
    -   **\_Bool UIAutomationType**
    -   **UIAutomationType \_ Double**
    -   **\_Elemento UIAutomationType**
    -   **\_Int UIAutomationType**
    -   **Punto di UIAutomationType \_**
    -   **\_Stringa UIAutomationType**
-   Se la proprietà personalizzata contiene dati di stringa ([**BSTR**](/previous-versions/windows/desktop/automat/bstr)), la specifica deve indicare se la proprietà è localizzabile, ovvero se la stringa può essere convertita in lingue dell'interfaccia utente diverse.
-   La proprietà personalizzata non deve sovrapporsi alle caratteristiche o funzionalità delle proprietà esistenti.

## <a name="designing-custom-events"></a>Progettazione di eventi personalizzati

Le applicazioni usano le notifiche degli eventi di automazione interfaccia utente per rispondere alle modifiche e alle azioni che coinvolgono gli elementi dell'interfaccia utente. Alla maggior parte delle proprietà sono associati eventi di modifica della proprietà che automazione interfaccia utente genera quando cambia il valore della proprietà. Se si introduce una proprietà personalizzata, è necessario prendere in considerazione l'introduzione di eventuali eventi personalizzati corrispondenti che potrebbero essere necessari.

Un evento personalizzato deve rispettare le seguenti linee guida di progettazione:

-   L'evento personalizzato deve essere "senza stato". Non può essere associato a una proprietà o a un valore specifico.
-   L'evento personalizzato non deve sovrapporsi alla definizione o al ruolo di un evento esistente.

### <a name="custom-ui-automation-events-and-winevents"></a>Eventi di automazione interfaccia utente personalizzati e WinEvents

[WinEvents](winevents-infrastructure.md) sono un meccanismo di comunicazione interprocesso e di gestione degli eventi utile nella piattaforma Microsoft Windows. Tuttavia, l'introduzione di un nuovo ID WinEvent è rischiosa perché può causare conflitti con altre applicazioni o il sistema operativo, con conseguente instabilità del sistema. Per evitare i conflitti, Microsoft ha definito diverse categorie di WinEvents e, per ogni categoria, ha definito uno o più intervalli di valori da usare come ID WinEvent. Per altre informazioni, vedere [allocazione di ID WinEvent](allocation-of-winevent-ids.md).

Gli eventi di automazione interfaccia utente personalizzati evitano conflitti allocando l'ID evento internamente nel Framework di automazione interfaccia utente.

## <a name="designing-custom-control-patterns"></a>Progettazione di pattern di controllo personalizzati

Un pattern di controllo è un'interfaccia con proprietà, metodi ed eventi che definiscono una parte di funzionalità distinta disponibile da un elemento di automazione. I metodi del pattern di controllo consentono ai client di automazione interfaccia utente di modificare un aspetto specifico del controllo. Le proprietà e gli eventi del pattern di controllo forniscono informazioni su alcuni aspetti del controllo e forniscono informazioni sullo stato dell'elemento di automazione che implementa il pattern di controllo.

Un pattern di controllo personalizzato deve rispettare le linee guida di progettazione seguenti:

-   Un pattern di controllo personalizzato deve coprire un determinato scenario. Il pattern di controllo [ItemContainer](uiauto-implementingitemcontainer.md) , ad esempio, è progettato per eseguire query su un oggetto contenuto indipendentemente dallo stato di virtualizzazione, ma non enumera né conta gli oggetti contenuti.
-   Un pattern di controllo personalizzato non deve sovrapporsi alle funzionalità dei pattern di controllo esistenti. Ad esempio, i pattern di controllo [Invoke](uiauto-implementinginvoke.md) e [ExpandCollapse](uiauto-implementingexpandcollapse.md) non devono essere combinati e presentati come un nuovo pattern di controllo. È possibile riutilizzare i pattern di controllo esistenti o definire scenari univoci con nuovi pattern di controllo.
-   Più pattern di controllo personalizzati possono essere progettati insieme per supportare scenari complessi. I pattern di controllo [Selection](uiauto-implementingselection.md) e [SelectionItem](uiauto-implementingselectionitem.md) , ad esempio, interagiscono per supportare scenari generali di selezione degli oggetti.

## <a name="custom-control-types"></a>Tipi di controlli personalizzati

Sebbene questo argomento sia incentrato su come registrare proprietà, eventi e pattern di controllo personalizzati di automazione interfaccia utente, è anche possibile introdurre nuovi tipi di controllo. A differenza di proprietà, eventi e pattern di controllo personalizzati, un tipo di controllo personalizzato non può essere registrato a livello di codice in fase di esecuzione perché in realtà è solo un valore potenziale della proprietà ControlType di automazione interfaccia utente. Tuttavia, è possibile definire, pubblicare e rendere disponibili gli ID di un tipo di controllo personalizzato per l'uso da parte di altri client e provider. Per altre informazioni sui tipi di controllo, vedere [UI Automation Control types Overview](uiauto-controltypesoverview.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Registrazione di proprietà, eventi e pattern di controllo personalizzati](uiauto-regcustompropseventpatterns.md)
</dt> <dt>

[Cenni preliminari sulle proprietà di automazione interfaccia utente](uiauto-propertiesoverview.md)
</dt> <dt>

[Cenni preliminari sugli eventi di automazione interfaccia utente](uiauto-eventsoverview.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 
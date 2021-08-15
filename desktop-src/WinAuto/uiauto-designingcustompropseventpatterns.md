---
title: Progettare proprietà, eventi e pattern di controllo personalizzati
description: La progettazione di una proprietà personalizzata, di un evento o di un pattern di controllo deve essere utile in un'ampia gamma di implementazioni di controlli.
ms.assetid: e4b224a0-3958-4ae7-96cb-fe6dc16511a7
keywords:
- Automazione interfaccia utente, proprietà personalizzate
- Automazione interfaccia utente,panoramica degli eventi
- Automazione interfaccia utente,cenni preliminari sui pattern di controllo
- Automazione interfaccia utente,progettazione di proprietà personalizzate
- Automazione interfaccia utente,progettazione di eventi
- Automazione interfaccia utente,progettazione di pattern di controllo
- Automazione interfaccia utente,WinEvents
- proprietà personalizzate, progettazione
- eventi, progettazione
- eventi, WinEvents
- pattern di controllo, progettazione
- WinEvents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de5b95d7daa3570e8b4b9b1d61c7c5f5590c6456d83190195e57af66811f1672
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118324802"
---
# <a name="design-custom-properties-events-and-control-patterns"></a>Progettare proprietà, eventi e pattern di controllo personalizzati

La progettazione di una proprietà personalizzata, di un evento o di un pattern di controllo deve essere utile in un'ampia gamma di implementazioni di controlli. È consigliabile evitare progettazioni specifiche di controlli o applicazioni utili solo in scenari limitati. La progettazione deve seguire l'esempio delle proprietà, degli eventi e dei pattern di controllo di Microsoft Automazione interfaccia utente esistenti, che sono stati specificati con attenzione per soddisfare le esigenze di un'ampia gamma di applicazioni di accessibilità e test automatizzati.

L'implementazione della specifica per una proprietà personalizzata, un evento o un pattern di controllo comporta la cooperazione e l'accordo delle parti sia sul lato client che sul lato provider e richiede a entrambe le parti di implementare la specifica in modo coerente. Le aziende sono invitate a collaborare con organizzazioni del settore come [Accessibility Interoperability Alliance (AIA)](https://www.atia.org/) per progettare e pubblicare la specifica per la proprietà personalizzata, l'evento o il pattern di controllo. In questo modo, è possibile raggiungere il consenso e garantire l'interoperabilità con la più ampia gamma di applicazioni.

In questo argomento sono incluse le sezioni seguenti:

-   [Quando usare proprietà ed eventi personalizzati](#when-to-use-custom-properties-and-events)
-   [Progettazione di proprietà personalizzate](#designing-custom-properties)
-   [Progettazione di eventi personalizzati](#designing-custom-events)
    -   [Eventi Automazione interfaccia utente e WinEvent personalizzati](#custom-ui-automation-events-and-winevents)
-   [Progettazione di pattern di controllo personalizzati](#designing-custom-control-patterns)
-   [Tipi di controllo personalizzati](#custom-control-types)
-   [Argomenti correlati](#related-topics)

## <a name="when-to-use-custom-properties-and-events"></a>Quando usare proprietà ed eventi personalizzati

Prima di creare una proprietà personalizzata, un evento o un pattern di controllo, assicurarsi che Automazione interfaccia utente non fornise una soluzione esistente. Ad esempio, la creazione di un pattern di controllo "Click" personalizzato non è necessaria perché il pattern di controllo [Invoke](uiauto-implementinginvoke.md) descrive già tale funzionalità.

Se si decide che è necessario un pattern di controllo, un evento o una proprietà personalizzata, assicurarsi che non sia troppo generico o troppo generico. Ad esempio, un pattern di controllo denominato "Show" non è utile perché la visibilità di un controllo può essere indicata da una proprietà di disponibilità nell'elemento, ad esempio [**\_ UIA IsExpandCollapsePatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md) o [**UIA \_ IsScrollItemPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md).

Prima di implementare una soluzione personalizzata, verificare attentamente che sia necessaria e quindi progettare completamente la funzionalità.

## <a name="designing-custom-properties"></a>Progettazione di proprietà personalizzate

Automazione interfaccia utente include due tipi di proprietà di base: proprietà degli elementi di automazione e proprietà del pattern di controllo. Le proprietà degli elementi di automazione sono costituite da un set comune di proprietà, ad esempio Name, AcceleratorKey e ClassName, esposte da tutti gli elementi Automazione interfaccia utente, indipendentemente dal tipo di controllo. Le proprietà del pattern di controllo vengono esposte da un controllo tramite un particolare pattern di controllo. Ogni pattern di controllo ha un set corrispondente di proprietà del pattern di controllo che il controllo deve esporre. Ad esempio, un controllo che supporta il pattern [di controllo Grid](uiauto-implementinggrid.md) espone le proprietà ColumnCount e RowCount.

Una proprietà personalizzata dell'elemento di automazione o una proprietà del pattern di controllo deve rispettare le linee guida di progettazione seguenti:

-   Una proprietà personalizzata deve avere uno dei tipi di dati seguenti specificati [**dall'enumerazione UIAutomationType.**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype) Non sono supportati altri tipi di dati per le proprietà personalizzate.
    -   **UIAutomationType \_ Bool**
    -   **UIAutomationType \_ Double**
    -   **Elemento UIAutomationType \_**
    -   **UIAutomationType \_ Int**
    -   **Punto UIAutomationType \_**
    -   **Stringa UIAutomationType \_**
-   Se la proprietà personalizzata contiene dati stringa [**(BSTR),**](/previous-versions/windows/desktop/automat/bstr)la specifica deve indicare se la proprietà è localizzabile, ovvero se la stringa può essere convertita in lingue diverse dell'interfaccia utente.
-   La proprietà personalizzata non deve sovrapporsi alle caratteristiche o alle funzionalità delle proprietà esistenti.

## <a name="designing-custom-events"></a>Progettazione di eventi personalizzati

Le applicazioni usano Automazione interfaccia utente notifiche degli eventi per rispondere alle modifiche e alle azioni che coinvolgono gli elementi dell'interfaccia utente. Alla maggior parte delle proprietà sono associati eventi di modifica Automazione interfaccia utente che vengono generati quando il valore della proprietà cambia. Se si introduce una proprietà personalizzata, è consigliabile introdurre eventuali eventi personalizzati corrispondenti che potrebbero essere necessari.

Un evento personalizzato deve rispettare le linee guida di progettazione seguenti:

-   L'evento personalizzato deve essere "senza stato". Non può essere associato a una proprietà o a un valore specifico.
-   L'evento personalizzato non deve sovrapporsi alla definizione o al ruolo di alcun evento esistente.

### <a name="custom-ui-automation-events-and-winevents"></a>Eventi Automazione interfaccia utente e WinEvent personalizzati

[Gli eventi WinEvent](winevents-infrastructure.md) sono un utile meccanismo di comunicazione e gestione degli eventi interprocesso nella piattaforma Windows Microsoft. Tuttavia, l'introduzione di un nuovo ID WinEvent è rischiosa perché può causare conflitti con altre applicazioni o con il sistema operativo, causando l'instabilità del sistema. Per evitare conflitti, Microsoft ha definito diverse categorie di WinEvent e, per ogni categoria, ha definito uno o più intervalli di valori da usare come ID WinEvent. Per altre informazioni, vedere [Allocation of WinEvent IDs ( Allocazione di ID WinEvent).](allocation-of-winevent-ids.md)

Gli Automazione interfaccia utente personalizzati evitano conflitti allocando l'ID evento internamente nel Framework di automazione interfaccia utente.

## <a name="designing-custom-control-patterns"></a>Progettazione di pattern di controllo personalizzati

Un pattern di controllo è un'interfaccia con proprietà, metodi ed eventi che definiscono una parte discreta delle funzionalità disponibili da un elemento di automazione. I metodi del pattern di Automazione interfaccia utente consentono ai client di modificare un particolare aspetto del controllo. Le proprietà e gli eventi del pattern di controllo forniscono informazioni su alcuni aspetti del controllo e sullo stato dell'elemento di automazione che implementa il pattern di controllo.

Un pattern di controllo personalizzato deve rispettare le linee guida di progettazione seguenti:

-   Un pattern di controllo personalizzato deve coprire uno scenario specifico. Ad esempio, il pattern di controllo [ItemContainer](uiauto-implementingitemcontainer.md) è destinato all'esecuzione di query su un oggetto contenuto indipendentemente dallo stato di virtualizzazione, ma non enumera né conta gli oggetti contenuti.
-   Un pattern di controllo personalizzato non deve sovrapporsi alle funzionalità dei pattern di controllo esistenti. Ad esempio, i [pattern di](uiauto-implementinginvoke.md) controllo Invoke ed [ExpandCollapse](uiauto-implementingexpandcollapse.md) non devono essere combinati e presentati come nuovo pattern di controllo. Riutilizzare i pattern di controllo esistenti o definire scenari univoci con nuovi pattern di controllo.
-   Più pattern di controllo personalizzati possono essere progettati insieme per supportare scenari complessi. Ad esempio, i pattern [di controllo Selection](uiauto-implementingselection.md) e [SelectionItem](uiauto-implementingselectionitem.md) funzionano insieme per supportare scenari generali di selezione di oggetti.

## <a name="custom-control-types"></a>Tipi di controllo personalizzati

Anche se in questo argomento viene illustrato come registrare Automazione interfaccia utente, eventi e pattern di controllo personalizzati, è anche possibile introdurre nuovi tipi di controllo. A differenza delle proprietà, degli eventi e dei pattern di controllo personalizzati, un tipo di controllo personalizzato non può essere registrato a livello di codice in fase di esecuzione perché è in realtà solo un valore potenziale della Automazione interfaccia utente ControlType. Tuttavia, un ID del tipo di controllo personalizzato può essere definito, pubblicato e reso disponibile per l'uso da parte di altri client e provider. Per altre informazioni sui tipi di controllo, vedere [Cenni Automazione interfaccia utente cenni preliminari sui tipi di controllo.](uiauto-controltypesoverview.md)

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

 

 
---
title: Specifica di automazione interfaccia utente
description: Questo argomento fornisce una panoramica della specifica di automazione interfaccia utente Microsoft, che costituisce la base dell'implementazione di Windows dell'automazione dell'interfaccia utente.
ms.assetid: 45160767-09b0-4fd1-bd73-bc5ac0e6f75e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d3cbb7ed2caa49e855b25f749820de8cf24f1e9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046987"
---
# <a name="ui-automation-specification"></a>Specifica di automazione interfaccia utente

Questo argomento fornisce una panoramica della specifica di automazione interfaccia utente Microsoft, che costituisce la base dell'implementazione di Windows dell'automazione dell'interfaccia utente. La specifica di automazione interfaccia utente può essere supportata tra piattaforme diverse da Microsoft Windows. Per altre informazioni, vedere [specifica di automazione interfaccia utente](./uiauto-specandcommunitypromise.md)

In questo argomento sono incluse le sezioni seguenti:

-   [Introduzione](#introducton)
-   [Elementi di automazione interfaccia utente](#ui-automation-elements)
-   [Albero di automazione interfaccia utente](#ui-automation-tree)
-   [Proprietà di automazione interfaccia utente](#ui-automation-properties)
-   [Pattern di controllo per Automazione interfaccia utente](#ui-automation-control-patterns)
-   [Tipi di controllo per Automazione interfaccia utente](#ui-automation-control-types)
-   [Eventi di automazione interfaccia utente](#ui-automation-events)
-   [Argomenti correlati](#related-topics)

## <a name="introducton"></a>Introduzione

La specifica di automazione interfaccia utente offre accesso a livello di codice flessibile agli elementi dell'interfaccia utente sul desktop di Windows, consentendo a prodotti di Assistive Technology come le utilità per la lettura dello schermo di fornire informazioni sull'interfaccia utente agli utenti finali e di modificare l'interfaccia utente per mezzo di input standard.

L'automazione dell'interfaccia utente è più ampia nell'ambito rispetto alla semplice definizione di un'interfaccia. Fornisce:

-   Un modello a oggetti e funzioni che semplificano la ricezione di eventi da applicazioni client, il recupero dei valori delle proprietà e la modifica degli elementi dell'interfaccia utente.
-   Infrastruttura di base per l'individuazione e il recupero tra i limiti dei processi.
-   Set di interfacce per i provider per esprimere la struttura ad albero, le proprietà generali e la funzionalità degli elementi dell'interfaccia utente.
-   Proprietà del tipo di controllo che consente a client e provider di indicare chiaramente le proprietà, la funzionalità e la struttura comuni di un oggetto dell'interfaccia utente.

Automazione interfaccia utente migliora Microsoft Active Accessibility da:

-   Abilitazione dei client out-of-process efficienti, pur continuando a consentire l'accesso in-process.
-   Esponendo più informazioni sull'interfaccia utente in modo da consentire ai client di essere out-of-process.
-   Coesistenza con e sfruttando Active Accessibility Microsoft senza ereditarne le limitazioni. Per altre informazioni, vedere [confronto tra Active Accessibility e automazione interfaccia utente Microsoft](microsoft-active-accessibility-and-ui-automation-compared.md).
-   Fornire un'alternativa a [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) semplice da implementare.

Implementazione della specifica di automazione interfaccia utente nelle interfacce basate su Windows features Component Object Model (COM) e le interfacce gestite.

## <a name="ui-automation-elements"></a>Elementi di automazione interfaccia utente

Automazione interfaccia utente espone ogni parte dell'interfaccia utente alle applicazioni client come un *elemento di automazione*. I provider forniscono i valori delle proprietà per ogni elemento. Gli elementi vengono esposti come struttura ad albero, con il desktop come elemento radice.

Gli elementi di automazione espongono proprietà comuni degli elementi dell'interfaccia utente che rappresentano. Una di queste proprietà è il tipo di controllo, che ne descrive l'aspetto e le funzionalità di base, ad esempio un pulsante o una casella di controllo.

## <a name="ui-automation-tree"></a>Albero di automazione interfaccia utente

L'albero di automazione interfaccia utente rappresenta l'intera interfaccia utente: l'elemento radice è il desktop corrente e gli elementi figlio sono finestre dell'applicazione. Ognuno di questi elementi figlio può contenere elementi che rappresentano menu, pulsanti, barre degli strumenti e così via. Questi elementi possono a sua volta contenere elementi come gli elementi elenco, come illustrato nella figura seguente.

![screenshot che mostra l'albero di automazione interfaccia utente](images/uiatree.gif)

Tenere presente che l'ordine degli elementi di pari livello nell'albero di automazione interfaccia utente è piuttosto importante. Gli oggetti che sono vicini tra loro visivamente devono essere anche vicini nell'albero di automazione interfaccia utente.

I provider di automazione interfaccia utente per un particolare controllo supportano la navigazione tra gli elementi figlio di tale controllo. Tuttavia, i provider non sono interessati alla navigazione tra questi sottoalberi del controllo. Questa operazione viene gestita dal core di automazione interfaccia utente, usando le informazioni dei provider di finestra predefiniti.

Per aiutare i client a elaborare le informazioni sull'interfaccia utente in modo più efficace, il Framework supporta visualizzazioni alternative della struttura ad albero di automazione: visualizzazione non elaborata, visualizzazione controlli e visualizzazione contenuto. Come illustrato nella tabella seguente, il tipo di filtro determina le visualizzazioni e il client definisce l'ambito di una vista.



| Albero di automazione | Descrizione                                                                                                             |
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| Visualizzazione non elaborata        | Albero completo di oggetti elemento di automazione per il quale il desktop è la radice.                                          |
| Visualizzazione controlli    | Sottoinsieme della visualizzazione non elaborata che esegue attentamente il mapping alla struttura dell'interfaccia utente come viene percepita dall'utente.                                |
| Visualizzazione contenuto    | Sottoinsieme della visualizzazione controlli che contiene il contenuto più rilevante per l'utente, ad esempio i valori in una casella combinata a discesa. |



 

Per altre informazioni, vedere [Panoramica dell'albero di automazione interfaccia utente](uiauto-treeoverview.md).

## <a name="ui-automation-properties"></a>Proprietà di automazione interfaccia utente

La specifica di automazione interfaccia utente definisce due tipi di proprietà: proprietà degli elementi di automazione e proprietà del pattern di controllo. Le proprietà degli elementi di automazione si applicano alla maggior parte dei controlli, fornendo informazioni fondamentali sull'elemento, ad esempio il nome. Le proprietà del pattern di controllo si applicano ai pattern di controllo, che vengono descritti di seguito.

Diversamente da Microsoft Active Accessibility, ogni proprietà di automazione interfaccia utente è identificata da un GUID e da un nome a livello di codice, che semplifica l'introduzione di nuove proprietà.

Per altre informazioni, vedere [UI Automation Properties Overview](uiauto-propertiesoverview.md).

## <a name="ui-automation-control-patterns"></a>Pattern di controllo per automazione interfaccia utente

Un pattern di controllo descrive un aspetto specifico della funzionalità di un elemento di automazione. Ad esempio, un semplice controllo "click-able", come un pulsante o un collegamento ipertestuale, deve supportare il pattern di controllo Invoke per rappresentare l'azione "click".

Ogni pattern di controllo è una rappresentazione canonica delle funzionalità e delle funzioni dell'interfaccia utente possibili. L'implementazione corrente di automazione interfaccia utente definisce 22 pattern di controllo. L'API di automazione di Windows può supportare anche pattern di controllo personalizzati. Diversamente dalle proprietà di ruolo o stato di Microsoft Active Accessibility, un elemento di automazione può supportare più pattern di controllo di automazione interfaccia utente.

Per altre informazioni, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).

## <a name="ui-automation-control-types"></a>Tipi di controllo per l'automazione dell'interfaccia utente

Un tipo di controllo è una proprietà dell'elemento di automazione che specifica un controllo noto che l'elemento rappresenta. Attualmente, automazione interfaccia utente definisce i tipi di controllo 38, inclusi Button, CheckBox, ComboBox, DataGrid, Document, Hyperlink, image, ToolTip, Tree e Window.

Prima di poter assegnare un tipo di controllo a un elemento, è necessario che l'elemento soddisfi determinate condizioni, tra cui una particolare struttura ad albero di automazione, i valori delle proprietà, i pattern di controllo e gli eventi. Tuttavia, non si è limitati a questi. È possibile estendere un controllo con le proprietà e i modelli personalizzati, oltre a quelli predefiniti.

Il numero totale di tipi di controllo predefiniti è significativamente inferiore rispetto ai ruoli di Microsoft Active Accessibility [oggetto](object-roles.md), perché i tipi di controllo di automazione interfaccia utente possono essere combinati per esprimere un set di funzionalità più ampio mentre i ruoli di Microsoft Active Accessibility non possono.

Per altre informazioni, vedere [UI Automation Control Types Overview](uiauto-controltypesoverview.md).

## <a name="ui-automation-events"></a>Eventi di automazione interfaccia utente

Gli eventi di automazione interfaccia utente inviano notifiche alle applicazioni delle modifiche a e alle azioni eseguite con gli elementi di automazione. Sono disponibili quattro tipi diversi di eventi di automazione interfaccia utente che non indicano necessariamente che lo stato di visualizzazione dell'interfaccia utente è cambiato. Il modello di eventi di automazione interfaccia utente è indipendente dal framework [WinEvent](winevents-infrastructure.md) in Windows, sebbene l'API di automazione di Windows renda gli eventi di automazione interfaccia utente interoperabili con Microsoft Active Accessibility Framework.

Per altre informazioni, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).

## <a name="related-topics"></a>Argomenti correlati

[Specifica di automazione interfaccia utente](./uiauto-specandcommunitypromise.md), [Panoramica dell'API di automazione di Windows](windows-automation-api-overview.md)
---
title: Automazione interfaccia utente specifica
description: Questo argomento offre una panoramica di Microsoft Automazione interfaccia utente Specification, che costituisce la base dell'implementazione Windows di Automazione interfaccia utente.
ms.assetid: 45160767-09b0-4fd1-bd73-bc5ac0e6f75e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fc07b70128a401d48813ded68c31dfcfca5bb5a49d2ca46683e9a902af003ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118325098"
---
# <a name="ui-automation-specification"></a>Automazione interfaccia utente specifica

Questo argomento offre una panoramica di Microsoft Automazione interfaccia utente Specification, che costituisce la base dell'implementazione Windows di Automazione interfaccia utente. La Automazione interfaccia utente specifica può essere supportata in piattaforme diverse da Microsoft Windows. Per altre informazioni, vedere Specifica [Automazione interfaccia utente](./uiauto-specandcommunitypromise.md)

In questo argomento sono incluse le sezioni seguenti:

-   [Introduzione](#introducton)
-   [Automazione interfaccia utente elementi](#ui-automation-elements)
-   [Automazione interfaccia utente albero](#ui-automation-tree)
-   [Automazione interfaccia utente proprietà](#ui-automation-properties)
-   [Pattern di controllo per Automazione interfaccia utente](#ui-automation-control-patterns)
-   [Tipi di controllo per Automazione interfaccia utente](#ui-automation-control-types)
-   [Automazione interfaccia utente eventi](#ui-automation-events)
-   [Argomenti correlati](#related-topics)

## <a name="introducton"></a>Introduzione

La specifica Automazione interfaccia utente fornisce un accesso flessibile a livello di codice agli elementi dell'interfaccia utente sul desktop di Windows, consentendo ai prodotti assistive technology, ad esempio le utilità per la lettura dello schermo, di fornire informazioni sull'interfaccia utente agli utenti finali e di modificare l'interfaccia utente con mezzi diversi dall'input standard.

Automazione interfaccia utente ambito è più ampio rispetto alla semplice definizione di un'interfaccia. Fornisce:

-   Un modello a oggetti e funzioni che semplificano la ricezione di eventi, il recupero dei valori delle proprietà e la modifica degli elementi dell'interfaccia utente da parte delle applicazioni client.
-   Un'infrastruttura di base per la ricerca e il recupero tra i limiti del processo.
-   Set di interfacce per i provider per esprimere la struttura ad albero, le proprietà generali e la funzionalità degli elementi dell'interfaccia utente.
-   Proprietà "tipo di controllo" che consente a client e provider di indicare chiaramente le proprietà, le funzionalità e la struttura comuni di un oggetto dell'interfaccia utente.

Automazione interfaccia utente migliora l'Microsoft Active Accessibility da:

-   Abilitazione di client out-of-process efficienti, pur continuando a consentire l'accesso in-process.
-   Esposizione di altre informazioni sull'interfaccia utente in modo da consentire ai client di essere out-of-process.
-   Coesistendo con e sfruttando Microsoft Active Accessibility senza ereditarne le limitazioni. Per altre informazioni, vedere confronto [tra Microsoft Active Accessibility e Automazione interfaccia utente .](microsoft-active-accessibility-and-ui-automation-compared.md)
-   Fornire un'alternativa [**a IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) semplice da implementare.

Implementazione della specifica Automazione interfaccia utente in Windows funzionalità Component Object Model (COM) e interfacce gestite.

## <a name="ui-automation-elements"></a>Automazione interfaccia utente elementi

Automazione interfaccia utente espone ogni parte dell'interfaccia utente alle applicazioni client come elemento *di automazione*. I provider forniscono i valori delle proprietà per ogni elemento. Gli elementi vengono esposti come struttura ad albero, con il desktop come elemento radice.

Gli elementi di automazione espongono proprietà comuni degli elementi dell'interfaccia utente che rappresentano. Una di queste proprietà è il tipo di controllo , che ne descrive l'aspetto e la funzionalità di base, ad esempio un pulsante o una casella di controllo.

## <a name="ui-automation-tree"></a>Automazione interfaccia utente albero

L Automazione interfaccia utente albero rappresenta l'intera interfaccia utente: l'elemento radice è il desktop corrente e gli elementi figlio sono finestre dell'applicazione. Ognuno di questi elementi figlio può contenere elementi che rappresentano menu, pulsanti, barre degli strumenti e così via. Questi elementi a loro volta possono contenere elementi come gli elementi dell'elenco, come illustrato nella figura seguente.

![Screenshot che mostra l'albero di automazione interfaccia utente](images/uiatree.gif)

Tenere presente che l'ordine degli elementi di pari livello nell'Automazione interfaccia utente albero è piuttosto importante. Anche gli oggetti che sono uno accanto all'altro visivamente devono essere uno accanto all'altro nell'Automazione interfaccia utente albero.

Automazione interfaccia utente provider per un determinato controllo supportano lo spostamento tra gli elementi figlio di tale controllo. Tuttavia, i provider non sono interessati alla navigazione tra questi sottoal alberi dei controlli. Questa operazione viene gestita dal Automazione interfaccia utente core, usando le informazioni dei provider di finestre predefiniti.

Per consentire ai client di elaborare le informazioni dell'interfaccia utente in modo più efficace, il framework supporta visualizzazioni alternative dell'albero di automazione: visualizzazione non elaborata, visualizzazione controllo e visualizzazione contenuto. Come illustrato nella tabella seguente, il tipo di filtro determina le visualizzazioni e il client definisce l'ambito di una vista.



| Albero di automazione | Descrizione                                                                                                             |
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| Visualizzazione non elaborata        | Albero completo degli oggetti elemento di automazione per cui il desktop è la radice.                                          |
| Visualizzazione controlli    | Subset della visualizzazione non elaborata che esegue il mapping strettamente alla struttura dell'interfaccia utente quando l'utente la percepe.                                |
| Visualizzazione contenuto    | Subset della visualizzazione controlli che contiene il contenuto più pertinente per l'utente, ad esempio i valori in una casella combinata a discesa. |



 

Per altre informazioni, vedere Panoramica Automazione interfaccia utente [albero](uiauto-treeoverview.md).

## <a name="ui-automation-properties"></a>Automazione interfaccia utente proprietà

La Automazione interfaccia utente specifica definisce due tipi di proprietà: proprietà degli elementi di automazione e proprietà del pattern di controllo. Le proprietà degli elementi di automazione si applicano alla maggior parte dei controlli, fornendo informazioni fondamentali sull'elemento, ad esempio il nome. Le proprietà dei pattern di controllo si applicano ai pattern di controllo, descritti di seguito.

A differenza di Microsoft Active Accessibility, ogni Automazione interfaccia utente è identificata da un GUID e da un nome a livello di codice, che semplifica l'introduzione di nuove proprietà.

Per altre informazioni, vedere [UI Automation Properties Overview](uiauto-propertiesoverview.md).

## <a name="ui-automation-control-patterns"></a>Pattern di controllo per automazione interfaccia utente

Un pattern di controllo descrive un particolare aspetto della funzionalità di un elemento di automazione. Ad esempio, un semplice controllo "in grado di fare clic", ad esempio un pulsante o un collegamento ipertestuale, deve supportare il pattern di controllo Invoke per rappresentare l'azione "clic".

Ogni pattern di controllo è una rappresentazione canonica delle funzionalità e delle funzioni dell'interfaccia utente possibili. L'implementazione corrente Automazione interfaccia utente definisce 22 pattern di controllo. L Windows API di Automazione può supportare anche pattern di controllo personalizzati. A differenza Microsoft Active Accessibility proprietà del ruolo o dello stato, un elemento di automazione può supportare Automazione interfaccia utente pattern di controllo.

Per altre informazioni, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).

## <a name="ui-automation-control-types"></a>Tipi di controllo per l'automazione dell'interfaccia utente

Un tipo di controllo è una proprietà dell'elemento di automazione che specifica un controllo noto rappresentato dall'elemento. Attualmente, Automazione interfaccia utente definisce 38 tipi di controllo, tra cui Button, CheckBox, ComboBox, DataGrid, Document, Hyperlink, Image, ToolTip, Tree e Window.

Prima di poter assegnare un tipo di controllo a un elemento, l'elemento deve soddisfare determinate condizioni, tra cui una particolare struttura ad albero di automazione, valori di proprietà, pattern di controllo ed eventi. Tuttavia, non si è limitati a questi. È possibile estendere un controllo con modelli e proprietà personalizzati, nonché con quelli predefiniti.

Il numero totale di tipi di controllo predefiniti è notevolmente inferiore [Microsoft Active Accessibility](object-roles.md)ruoli oggetto , perché i tipi di controllo Automazione interfaccia utente possono essere combinati per esprimere un set più ampio di funzionalità, mentre i ruoli Microsoft Active Accessibility non possono.

Per altre informazioni, vedere [UI Automation Control Types Overview](uiauto-controltypesoverview.md).

## <a name="ui-automation-events"></a>Automazione interfaccia utente eventi

Automazione interfaccia utente eventi notificano alle applicazioni le modifiche e le azioni eseguite con gli elementi di automazione. Esistono quattro diversi tipi di eventi Automazione interfaccia utente e non significano necessariamente che lo stato di visualizzazione dell'interfaccia utente sia stato modificato. Il modello Automazione interfaccia utente eventi è indipendente dal framework [WinEvent](winevents-infrastructure.md) in Windows, anche se l'API di automazione di Windows rende gli eventi Automazione interfaccia utente interoperabili con il framework Microsoft Active Accessibility.

Per altre informazioni, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).

## <a name="related-topics"></a>Argomenti correlati

[Automazione interfaccia utente specifica ,](./uiauto-specandcommunitypromise.md)panoramica [dell'API Windows Automation](windows-automation-api-overview.md)
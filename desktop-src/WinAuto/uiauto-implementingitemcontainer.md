---
title: Pattern di controllo ItemContainer
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di IItemContainerProvider, incluse informazioni sui metodi. Il pattern di controllo ItemContainer viene usato per supportare la virtualizzazione degli elementi.
ms.assetid: 6f3dd94e-3563-4a13-9db9-5928a02bab77
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo ItemContainer
- Automazione interfaccia utente, pattern di controllo ItemContainer
- Automazione interfaccia utente, IItemContainerProvider
- IItemContainerProvider
- implementazione di pattern di controllo ItemContainer di automazione interfaccia utente
- Pattern di controllo ItemContainer
- pattern di controllo, IItemContainerProvider
- pattern di controllo, implementazione dell'automazione interfaccia utente ItemContainer
- pattern di controllo, ItemContainer
- interfacce, IItemContainerProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55246abde51e7053bf0c3266ccbe9c2b080b2fe7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709688"
---
# <a name="itemcontainer-control-pattern"></a>Pattern di controllo ItemContainer

Vengono descritte le linee guida e le convenzioni per l'implementazione di [**IItemContainerProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider), incluse informazioni sui metodi. Il pattern di controllo **ItemContainer** viene usato per supportare la virtualizzazione degli elementi.

I controlli che contengono un numero elevato di elementi figlio possono utilizzare la virtualizzazione per gestire in modo efficiente gli elementi. Con la virtualizzazione, il controllo mantiene le informazioni complete in memoria solo per un subset di elementi in un determinato momento. In genere, il subset include solo gli elementi attualmente visibili all'utente. Le informazioni complete sugli elementi virtualizzati rimanenti vengono mantenute nello spazio di archiviazione e vengono caricate in memoria, o realizzate, perché il controllo lo richiede, ad esempio, perché i nuovi elementi diventano visibili all'utente.

Il diagramma seguente, ad esempio, Mostra una casella di riepilogo contenente migliaia di elementi virtualizzati. Poiché il controllo mantiene le informazioni complete solo per gli elementi figlio attualmente visibili, il provider può esporre gli elementi di automazione interfaccia utente Microsoft solo per gli elementi 100-127.

![diagramma che Mostra gli elementi in una casella di riepilogo virtualizzati e non virtualizzati](images/virtualizeditems.jpg)

I controlli che usano la virtualizzazione rappresentano una sfida perché solo gli elementi realizzati (devirtualizzati) sono completamente disponibili come elementi di automazione interfaccia utente nell'albero di automazione interfaccia utente. Gli elementi virtualizzati non esistono nell'albero, quindi le informazioni su di essi non sono disponibili.

Per fornire informazioni sugli elementi virtualizzati, i provider implementano il pattern di controllo **ItemContainer** , che espone l'interfaccia [**IItemContainerProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider) . Il metodo [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) trova gli elementi figlio in base al valore di una determinata proprietà, ad esempio **Name**, **AutomationId** o **IsSelected**. Se un elemento è virtualizzato, **FindItemByProperty** recupera un elemento segnaposto di automazione interfaccia utente per l'elemento. Un elemento segnaposto è un'implementazione dell'interfaccia [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) che supporta solo il pattern di controllo [VirtualizedItem](uiauto-implementingvirtualizeditem.md) .

Il metodo [**IVirtualizedItemProvider:: réalisateur**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) consente a un client di richiedere che venga realizzato un elemento virtualizzato, esponendo in tal modo un elemento di automazione interfaccia utente completo per l'elemento in modo che siano disponibili tutte le proprietà e i modelli necessari.

Sebbene lo scopo principale del pattern di controllo **ItemContainer** sia quello di supportare scenari di contenitori virtualizzati, può essere implementato da qualsiasi contenitore che recupera gli elementi figlio in base al nome, indipendentemente dal fatto che il contenitore usi la virtualizzazione.

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per IItemContainerProvider](#required-members-for-iitemcontainerprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern di controllo **ItemContainer** , tenere presenti le linee guida e le convenzioni seguenti:

-   Qualsiasi controllo che può contenere elementi virtualizzati deve supportare il pattern di controllo **ItemContainer** . Qualsiasi contenitore che supporta il recupero di elementi in base a un valore di proprietà può supportare questo modello, indipendentemente dal fatto che il contenitore usi la virtualizzazione.
-   Quando un contenitore è virtualizzato, possono essere interessati altri pattern di controllo quali la [selezione](uiauto-implementingselection.md), la [tabella](uiauto-implementingtable.md)e la [griglia](uiauto-implementinggrid.md) . Il metodo [**ISelectionProvider:: Getselectation**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection) , ad esempio, può supportare solo elementi presenti nel viewport oppure solo elementi selezionati attualmente non virtualizzati.
-   Il pattern di controllo [Scroll](uiauto-implementingscroll.md) non dovrebbe essere influenzato dalla virtualizzazione.
-   Non sono disponibili informazioni sul conteggio degli elementi o sugli indici per gli elementi virtualizzati. Un controllo virtualizzato può utilizzare la proprietà **DescribedBy** o **ItemStatus** per fornire queste informazioni, se necessario.
-   Gli sviluppatori di controlli devono documentare e pubblicare i dettagli di tutte le proprietà e i pattern di controllo di automazione interfaccia utente interessati dall'uso della virtualizzazione. Sebbene i pattern di controllo ItemContainer e [VirtualizedItem](uiauto-implementingvirtualizeditem.md) offrano supporto di base, potrebbero non supportare alcuni comportamenti di virtualizzazione.

Le linee guida e i requisiti seguenti si applicano al metodo [**IItemContainerProvider:: FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) .

-   Sebbene non sia obbligatorio, Microsoft consiglia vivamente che [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) supporti le proprietà **Name**, **AutomationId** e **IsSelected** .
-   [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) può essere lento se è necessario attraversare più oggetti per trovarne uno corrispondente.
-   [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) può essere chiamato ripetutamente per trovare gli elementi in sequenza. Gli elementi possono essere in qualsiasi ordine, purché ogni elemento venga restituito una sola volta.
-   [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) può essere implementato per trovare solo gli elementi visualizzati nel controllo o nella visualizzazione contenuto dell'albero di automazione interfaccia utente. Gli elementi visualizzati solo nella visualizzazione non elaborata possono essere ignorati per evitare il recupero di più elementi che rappresentano solo una parte di un "elemento" all'utente.
-   Quando i criteri di ricerca corrispondono a un elemento virtualizzato, il provider può restituire un elemento segnaposto che supporta il pattern di controllo [VirtualizedItem](uiauto-implementingvirtualizeditem.md) . Le linee guida seguenti si applicano agli elementi segnaposto:
    -   Il recupero di un elemento segnaposto per un elemento virtualizzato non può causare modifiche dell'interfaccia utente.
    -   L'elemento segnaposto deve essere un peer di altri elementi figlio. è necessario un evento di modifica della struttura.
    -   Quando possibile, il provider può creare un elemento di automazione completo anziché un segnaposto.
-   Quando i criteri di ricerca corrispondono a un elemento non virtualizzato, il provider deve restituire l'elemento effettivo, non un segnaposto.
-   Quando non viene trovato alcun elemento, [**IItemContainerProvider:: FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) deve impostare il parametro *pFound* su **null** e restituire **S \_ OK**.
-   Quando il parametro *PropertyId* è 0, il provider deve restituire l'elemento successivo dopo *pStartAfter*.
-   Se il parametro *pStartAfter* è **null** e *PropertyId* è 0, il provider deve restituire il primo elemento nel contenitore.
-   Quando il parametro *PropertyId* è 0, il parametro value viene ignorato.

Le linee guida e i requisiti seguenti si applicano agli elementi segnaposto per gli elementi virtualizzati nell'albero di automazione interfaccia utente.

-   Sebbene i provider siano invitati a supportare più proprietà e pattern di controllo per un elemento segnaposto, è necessario solo il pattern di controllo [VirtualizedItem](uiauto-implementingvirtualizeditem.md) .
-   Il provider può invalidare un elemento segnaposto precedente quando [**IItemContainerProvider:: FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) viene chiamato nuovamente. Se un client deve realizzare l'elemento segnaposto, deve eseguire questa operazione immediatamente; in caso contrario, l'elemento può essere invalidato se **FindItemByProperty** viene chiamato nuovamente o se il viewport cambia per qualsiasi motivo.
-   Le azioni dell'interfaccia utente, ad esempio lo scorrimento o il ridimensionamento, possono causare la modifica del viewport del contenitore e un nuovo set di elementi figlio diventeranno visibili. In questo caso, gli elementi segnaposto recuperati in precedenza potrebbero non essere disponibili nell'albero di automazione interfaccia utente.
-   Il provider non deve virtualizzare gli elementi dell'interfaccia utente disponibili sullo schermo nel viewport dell'oggetto contenitore.

## <a name="required-members-for-iitemcontainerprovider"></a>Membri obbligatori per IItemContainerProvider

Il metodo seguente è necessario per implementare l'interfaccia [**IItemContainerProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider) .



| Membri obbligatori                                                               | Tipo di membro | Note |
|--------------------------------------------------------------------------------|-------------|-------|
| [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) | Metodo      | nessuno  |



 

Il pattern di controllo **ItemContainer** non dispone di proprietà o eventi associati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> <dt>

[Pattern di controllo VirtualizedItem](uiauto-implementingvirtualizeditem.md)
</dt> </dl>

 

 





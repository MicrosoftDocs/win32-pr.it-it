---
title: Pattern di controllo ItemContainer
description: Descrive le linee guida e le convenzioni per l'implementazione di IItemContainerProvider, incluse le informazioni sui metodi. Il pattern di controllo ItemContainer viene usato per supportare la virtualizzazione degli elementi.
ms.assetid: 6f3dd94e-3563-4a13-9db9-5928a02bab77
keywords:
- Automazione interfaccia utente,implementazione del pattern di controllo ItemContainer
- Automazione interfaccia utente,Pattern di controllo ItemContainer
- Automazione interfaccia utente,IItemContainerProvider
- IItemContainerProvider
- implementazione di Automazione interfaccia utente pattern di controllo ItemContainer
- Pattern di controllo ItemContainer
- pattern di controllo, IItemContainerProvider
- pattern di controllo, implementazione Automazione interfaccia utente ItemContainer
- pattern di controllo, ItemContainer
- interfacce, IItemContainerProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69c0407a8f167a3a89b908c1b5555a9d32363b38b3ce5ab4d1794e726666a8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413456"
---
# <a name="itemcontainer-control-pattern"></a>Pattern di controllo ItemContainer

Descrive le linee guida e le convenzioni per l'implementazione [**di IItemContainerProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider)incluse le informazioni sui metodi. Il **pattern di controllo ItemContainer** viene usato per supportare la virtualizzazione degli elementi.

I controlli che contengono un numero elevato di elementi figlio possono usare la virtualizzazione per gestire in modo efficiente gli elementi. Con la virtualizzazione, il controllo mantiene le informazioni complete in memoria solo per un subset di elementi in un determinato momento. In genere, il subset include solo gli elementi attualmente visibili all'utente. Le informazioni complete sugli elementi virtualizzati rimanenti vengono mantenute nella memoria e caricate in memoria o realizzati, in base alle esigenze del controllo, ad esempio quando i nuovi elementi diventano visibili all'utente.

Ad esempio, il diagramma seguente mostra una casella di riepilogo che contiene migliaia di elementi virtualizzati. Poiché il controllo mantiene informazioni complete solo per gli elementi figlio attualmente visibili, il provider può esporre gli elementi di Microsoft Automazione interfaccia utente solo per gli elementi 100-127.

![Diagramma che mostra gli elementi in una casella di riepilogo virtualizzati e non virtualizzati](images/virtualizeditems.jpg)

I controlli che usano la virtualizzazione rappresentano una sfida perché solo gli elementi realizzati (devirtualizzazioneti) sono completamente disponibili come Automazione interfaccia utente elementi nell'Automazione interfaccia utente albero. Gli elementi virtualizzati non esistono nell'albero, quindi le relative informazioni non sono disponibili.

Per fornire informazioni sugli elementi virtualizzati, i provider implementano il pattern di controllo **ItemContainer,** che espone [**l'interfaccia IItemContainerProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider) Il [**metodo FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) trova gli elementi figlio in base al valore di una determinata proprietà, ad esempio **Name,** **AutomationId** o **IsSelected.** Se un elemento è virtualizzato, **FindItemByProperty** recupera un Automazione interfaccia utente segnaposto per l'elemento. Un elemento segnaposto è un'implementazione [**dell'interfaccia IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) che supporta solo il pattern [di controllo VirtualizedItem.](uiauto-implementingvirtualizeditem.md)

Il [**metodo IVirtualizedItemProvider::Realize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) consente a un client di richiedere che un elemento virtualizzato sia realizzato, esponendo così un elemento Automazione interfaccia utente completo per l'elemento in modo che siano disponibili tutte le proprietà e i modelli necessari.

Anche se lo scopo principale del pattern di controllo **ItemContainer** è supportare scenari di contenitori virtualizzati, può essere implementato da qualsiasi contenitore che recupera gli elementi figlio in base al nome, indipendentemente dal fatto che il contenitore usi la virtualizzazione.

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per IItemContainerProvider](#required-members-for-iitemcontainerprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern **di controllo ItemContainer,** tenere presente le linee guida e le convenzioni seguenti:

-   Qualsiasi controllo che può contenere elementi virtualizzati deve supportare il pattern **di controllo ItemContainer.** Qualsiasi contenitore che supporta il recupero di elementi in base al valore di una proprietà può supportare questo modello, indipendentemente dal fatto che il contenitore usi la virtualizzazione.
-   Quando un contenitore è virtualizzato, possono essere interessati altri pattern di controllo, ad esempio [Selection,](uiauto-implementingselection.md) [Table](uiauto-implementingtable.md)e [Grid.](uiauto-implementinggrid.md) Ad esempio, il [**metodo ISelectionProvider::GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection) può supportare solo gli elementi presenti nel viewport o solo gli elementi selezionati attualmente non virtualizzati.
-   Il [pattern di](uiauto-implementingscroll.md) controllo Scroll non deve essere interessato dalla virtualizzazione.
-   Per gli elementi virtualizzati non sono disponibili informazioni sul conteggio degli elementi o sull'indice. Un controllo virtualizzato può usare **la proprietà DescribedBy** o **ItemStatus** per fornire queste informazioni, se necessario.
-   Gli sviluppatori di controlli devono documentare e pubblicare i dettagli Automazione interfaccia utente proprietà e i pattern di controllo interessati dall'uso della virtualizzazione. Anche se i pattern di controllo ItemContainer e [VirtualizedItem](uiauto-implementingvirtualizeditem.md) offrono supporto di base, potrebbero non supportare alcuni comportamenti di virtualizzazione.

Le linee guida e i requisiti seguenti si applicano [**al metodo IItemContainerProvider::FindItemByProperty.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty)

-   Sebbene non sia obbligatorio, Microsoft consiglia vivamente che [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) supporti **le proprietà Name,** **AutomationId** e **IsSelected.**
-   [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) può essere lento se deve attraversare più oggetti per trovarne uno corrispondente.
-   [**FindItemByProperty può**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) essere chiamato ripetutamente per trovare gli elementi in sequenza. Gli elementi possono essere in qualsiasi ordine, purché ogni elemento sia restituito una sola volta.
-   [**FindItemByProperty può**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) essere implementato per trovare solo gli elementi visualizzati nel controllo o nella visualizzazione contenuto dell'Automazione interfaccia utente albero. Gli elementi visualizzati solo nella visualizzazione non elaborata possono essere ignorati per evitare di recuperare all'utente più elementi che rappresentano solo una parte di un "elemento".
-   Quando i criteri di ricerca corrispondono a un elemento virtualizzato, il provider può restituire un elemento segnaposto che supporta il pattern [di controllo VirtualizedItem.](uiauto-implementingvirtualizeditem.md) Le linee guida seguenti si applicano agli elementi segnaposto:
    -   Il recupero di un elemento segnaposto per un elemento virtualizzato non deve causare modifiche all'interfaccia utente.
    -   L'elemento segnaposto deve essere un peer di altri elementi figlio (è necessario un evento di modifica della struttura).
    -   Quando possibile, il provider può creare un elemento di automazione completo anziché un segnaposto.
-   Quando i criteri di ricerca corrispondono a un elemento non virtualizzato, il provider deve restituire l'elemento effettivo, non un segnaposto.
-   Quando non viene trovato alcun elemento, [**IItemContainerProvider::FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) deve impostare il *parametro pFound* su **NULL** e restituire **S \_ OK.**
-   Quando il *parametro propertyId* è 0, il provider deve restituire l'elemento successivo dopo *pStartAfter*.
-   Se il *parametro pStartAfter* è **NULL** e *propertyId* è 0, il provider deve restituire il primo elemento nel contenitore.
-   Quando il *parametro propertyId* è 0, il parametro value viene ignorato.

Le linee guida e i requisiti seguenti si applicano agli elementi segnaposto per gli elementi virtualizzati nell'Automazione interfaccia utente albero.

-   Sebbene i provider siano invitati a supportare più proprietà e pattern di controllo per un elemento segnaposto, è necessario solo il pattern di controllo [VirtualizedItem.](uiauto-implementingvirtualizeditem.md)
-   Il provider può invalidare un elemento segnaposto precedente quando viene chiamato di nuovo [**IItemContainerProvider::FindItemByProperty.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) Se un client deve realizzare l'elemento segnaposto, deve farlo immediatamente. In caso contrario, l'elemento può essere invalidato se **FindItemByProperty** viene chiamato di nuovo o se il viewport cambia per qualsiasi motivo.
-   Le azioni dell'interfaccia utente, ad esempio lo scorrimento o il ridimensionamento, possono causare la modifica del riquadro di visualizzazione del contenitore e la visualizzazione di un nuovo set di elementi figlio. In questo caso, gli elementi segnaposto recuperati in precedenza potrebbero non essere disponibili nell'Automazione interfaccia utente albero.
-   Il provider non deve virtualizzare gli elementi dell'interfaccia utente disponibili sullo schermo nel riquadro di visualizzazione dell'oggetto contenitore.

## <a name="required-members-for-iitemcontainerprovider"></a>Membri obbligatori per IItemContainerProvider

Il metodo seguente è necessario per implementare [**l'interfaccia IItemContainerProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider)



| Membri obbligatori                                                               | Tipo di membro | Note |
|--------------------------------------------------------------------------------|-------------|-------|
| [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) | Metodo      | Nessuno  |



 

Il **pattern di controllo ItemContainer** non ha proprietà o eventi associati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di controllo e pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> <dt>

[Pattern di controllo VirtualizedItem](uiauto-implementingvirtualizeditem.md)
</dt> </dl>

 

 





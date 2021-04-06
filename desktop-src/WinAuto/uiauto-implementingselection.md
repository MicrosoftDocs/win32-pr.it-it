---
title: Pattern di controllo Selection
description: Descrive le linee guida e le convenzioni per l'implementazione di ISelectionProvider, incluse informazioni su proprietà, metodi ed eventi.
ms.assetid: 9371e656-6f93-4a43-bd0c-c6977348b16a
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo Selection
- Automazione interfaccia utente, pattern di controllo Selection
- Automazione interfaccia utente, ISelectionProvider
- ISelectionProvider
- implementazione di pattern di controllo Selection di automazione interfaccia utente
- Pattern di controllo Selection
- pattern di controllo, ISelectionProvider
- pattern di controllo, implementazione della selezione di automazione interfaccia utente
- pattern di controllo, selezione
- interfacce, ISelectionProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad6950302373494f307c91c0aadaeab1db0132a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044773"
---
# <a name="selection-control-pattern"></a>Pattern di controllo Selection

Descrive le linee guida e le convenzioni per l'implementazione di [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider), incluse informazioni su proprietà, metodi ed eventi. Il pattern di controllo **Selection** viene usato per supportare i controlli che fungono da contenitori per una raccolta di elementi figlio selezionabili. Gli elementi figlio di questo elemento devono implementare [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).

Per esempi di controlli che implementano questo pattern di controllo, vedere [tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md).

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **ISelectionProvider**](#required-members-for-iselectionprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern di controllo **Selection** , tenere presenti le linee guida e le convenzioni seguenti:

-   I controlli che implementano [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) consentono la selezione di uno o più elementi figlio. Ad esempio, le caselle di riepilogo, le visualizzazioni elenco e le visualizzazioni ad albero supportano selezioni multiple, mentre le caselle combinate, i dispositivi di scorrimento e i gruppi di pulsanti di opzione supportano la selezione singola.
-   I controlli che hanno un intervallo minimo, massimo e continuo, ad esempio il controllo dispositivo di scorrimento del **volume** di un lettore multimediale, devono implementare [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) anziché [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).
-   I controlli a selezione singola che gestiscono i controlli figlio che implementano [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), ad esempio il dispositivo di scorrimento **risoluzione schermo** nella finestra di dialogo **proprietà di visualizzazione** per Windows o il controllo selezione selezione **colori** da Microsoft Word (vedere l'immagine seguente), devono implementare [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider); i relativi elementi figlio devono implementare sia [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) che [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).

    ![immagine che mostra un esempio di mapping delle stringhe dei campioni colore](images/uia-valuepattern-colorpicker.jpg)

-   I menu non supportano il pattern di controllo **Selection** . Se si usano voci di menu che includono sia grafica che testo (ad esempio gli elementi del **riquadro di anteprima** nel menu **Visualizza** in Microsoft Outlook) ed è necessario indicare lo stato, è necessario implementare [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider).

## <a name="required-members-for-iselectionprovider"></a>Membri obbligatori per **ISelectionProvider**

Le proprietà, i metodi e gli eventi seguenti sono obbligatori per l'implementazione dell'interfaccia [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) .



| Membri obbligatori                                                                                | Tipo di membro | Note                                                                       |
|-------------------------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------|
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)                        | Proprietà    | nessuno                                                                        |
| [**IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired)                    | Proprietà    | nessuno                                                                        |
| [**GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection)                                  | Metodo      | nessuno                                                                        |
| [**\_InvalidatedEventId selezione \_ UIA**](uiauto-event-ids.md) | Evento       | Generare questo evento quando una selezione in un contenitore è cambiata in modo significativo. |



 

Le proprietà [**ISelectionProvider:: IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) e [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple) possono essere dinamiche. Ad esempio, lo stato iniziale di un controllo potrebbe non includere elementi selezionati per impostazione predefinita, a indicare che **IsSelectionRequired** è false. Tuttavia, dopo aver selezionato un elemento, il controllo deve sempre avere almeno un elemento selezionato. Analogamente, in casi rari, un controllo potrebbe consentire la selezione di più elementi durante l'inizializzazione e successivamente consentire solo selezioni singole.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Pattern di controllo SelectionItem](uiauto-implementingselectionitem.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> </dl>

 

 





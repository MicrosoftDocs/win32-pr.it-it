---
title: Pattern di controllo Selection
description: Descrive le linee guida e le convenzioni per l'implementazione di ISelectionProvider, incluse le informazioni su proprietà, metodi ed eventi.
ms.assetid: 9371e656-6f93-4a43-bd0c-c6977348b16a
keywords:
- Automazione interfaccia utente,implementazione del pattern di controllo Selection
- Automazione interfaccia utente,Pattern di controllo Selection
- Automazione interfaccia utente,ISelectionProvider
- ISelectionProvider
- Implementazione Automazione interfaccia utente pattern di controllo Selection
- Pattern di controllo di selezione
- pattern di controllo, ISelectionProvider
- pattern di controllo, implementazione Automazione interfaccia utente Selection
- pattern di controllo, selezione
- interfacce, ISelectionProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2d0578dcdcfa9d381272afaa474338a54caa1f4b17989f2461f9aec5086bc18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098321"
---
# <a name="selection-control-pattern"></a>Pattern di controllo Selection

Vengono descritte le linee guida e le convenzioni per [**l'implementazione di ISelectionProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)incluse informazioni su proprietà, metodi ed eventi. Il **pattern di** controllo Selection viene usato per supportare i controlli che fungono da contenitori per una raccolta di elementi figlio selezionabili. Gli elementi figlio di questo elemento devono implementare [**ISelectionItemProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)

Per esempi di controlli che implementano questo pattern di controllo, vedere [Tipi di controllo e pattern di controllo supportati.](uiauto-controlpatternmapping.md)

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **ISelectionProvider**](#required-members-for-iselectionprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern **di controllo Selection,** tenere presente le linee guida e le convenzioni seguenti:

-   I controlli che [**implementano ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) consentono la selezione di uno o più elementi figlio. Ad esempio, le caselle di riepilogo, le visualizzazioni elenco e le visualizzazioni albero supportano più selezioni, mentre le caselle combinate, i dispositivi di scorrimento e i gruppi di pulsanti di opzione supportano la selezione singola.
-   I controlli con un intervallo minimo, massimo e continuo, ad esempio il dispositivo di scorrimento **Volume** di un lettore multimediale, devono implementare [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) anziché [**ISelectionProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)
-   I controlli a selezione singola che gestiscono controlli figlio che  implementano [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), ad esempio il dispositivo di scorrimento Risoluzione dello schermo nella finestra di dialogo **Proprietà dello schermo** per Windows o il controllo di selezione **Selezione colori** da Microsoft Word (vedere l'immagine seguente), devono implementare [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider); i relativi elementi figlio devono implementare [**sia IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) che [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).

    ![Immagine che mostra un esempio di mapping di stringhe di controllo colore](images/uia-valuepattern-colorpicker.jpg)

-   I menu non supportano il **pattern di controllo Selection.** Se si lavora con voci di menu che includono  sia grafica che testo (ad esempio le voci del riquadro di anteprima nel **menu** Visualizza in Microsoft Outlook) ed è necessario comunicare lo stato, è necessario implementare [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider).

## <a name="required-members-for-iselectionprovider"></a>Membri obbligatori per **ISelectionProvider**

Le proprietà, i metodi e gli eventi seguenti sono necessari per l'implementazione [**dell'interfaccia ISelectionProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)



| Membri obbligatori                                                                                | Tipo di membro | Note                                                                       |
|-------------------------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------|
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)                        | Proprietà    | Nessuno                                                                        |
| [**IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired)                    | Proprietà    | Nessuno                                                                        |
| [**GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection)                                  | Metodo      | Nessuno                                                                        |
| [**UIA \_ Selection \_ InvalidatedEventId**](uiauto-event-ids.md) | Event       | Generare questo evento quando una selezione in un contenitore viene modificata in modo significativo. |



 

Le [**proprietà ISelectionProvider::IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) e [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple) possono essere dinamiche. Ad esempio, lo stato iniziale di un controllo potrebbe non avere elementi selezionati per impostazione predefinita, a indicare che **IsSelectionRequired** è false. Tuttavia, dopo aver selezionato un elemento, il controllo deve sempre avere almeno un elemento selezionato. Analogamente, in casi rari, un controllo potrebbe consentire la selezione di più elementi durante l'inizializzazione e successivamente consentire solo selezioni singole.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di controllo e pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Pattern di controllo SelectionItem](uiauto-implementingselectionitem.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> </dl>

 

 





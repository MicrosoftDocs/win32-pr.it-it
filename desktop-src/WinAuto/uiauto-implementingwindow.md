---
title: Pattern di controllo Window
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di IWindowProvider, incluse informazioni su proprietà, metodi ed eventi. Il pattern di controllo Window supporta i controlli che forniscono funzionalità fondamentali basate su finestra all'interno di un'interfaccia utente grafica tradizionale.
ms.assetid: bfd37d27-fcec-4d25-841c-63e14e48c6c8
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo Window
- Automazione interfaccia utente, pattern di controllo Window
- Automazione interfaccia utente, IWindowProvider
- IWindowProvider
- implementazione di pattern di controllo Window di automazione interfaccia utente
- Pattern di controllo Window
- pattern di controllo, IWindowProvider
- pattern di controllo, implementazione della finestra di automazione interfaccia utente
- pattern di controllo, finestra
- interfacce, IWindowProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3c4f0d862a14fee35f8d1982c7870e2be031c61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332420"
---
# <a name="window-control-pattern"></a>Pattern di controllo Window

Vengono descritte le linee guida e le convenzioni per l'implementazione di [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider), incluse informazioni su proprietà, metodi ed eventi. Il pattern di controllo **Window** supporta i controlli che forniscono funzionalità fondamentali basate su finestra all'interno di un'interfaccia utente grafica tradizionale.

Esempi di controlli che devono implementare questo pattern di controllo sono le finestre dell'applicazione di primo livello, le finestre figlio dell'interfaccia a documenti multipli (MDI), i controlli del riquadro suddiviso ridimensionabili, le finestre di dialogo modali e le finestre della guida del fumetto. Per esempi di controlli che implementano questo pattern di controllo, vedere [Control Pattern Mapping for UI Automation Clients](uiauto-controlpatternmapping.md).

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **IWindowProvider**](#required-members-for-iwindowprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern di controllo **Window** , tenere presenti le linee guida e le convenzioni seguenti:

-   Per supportare la possibilità di modificare le dimensioni della finestra e la posizione dello schermo usando l'automazione interfaccia utente Microsoft, un controllo deve implementare [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) oltre a [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).
-   I controlli che contengono barre del titolo ed elementi della barra del titolo che consentono di spostare, ridimensionare, ingrandire, ridurre a icona o chiudere il controllo sono in genere necessari per implementare [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).
-   I controlli quali popup della descrizione comando e elenchi a discesa della casella combinata o dei menu non implementano in genere [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).
-   Le finestre della Guida per i fumetti si differenziano dai popup di descrizione comando di base tramite il provisioning di un pulsante **Chiudi** simile a una finestra.
-   La modalità schermo intero non è supportata da [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) perché è specifica della funzionalità per un'applicazione e non è un comportamento tipico delle finestre.

## <a name="required-members-for-iwindowprovider"></a>Membri obbligatori per **IWindowProvider**

Le proprietà, i metodi e gli eventi seguenti sono obbligatori per l'implementazione dell'interfaccia [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) .



| Membri obbligatori                                                                            | Tipo di membro | Note                                                                       |
|---------------------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------|
| [**WindowInteractionState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_windowinteractionstate)             | Proprietà    | Non è garantito che sia **WindowInteractionState \_ ReadyForUserInteraction** |
| [**IsModal**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_ismodal)                                           | Proprietà    | nessuno                                                                        |
| [**IsTopmost**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_istopmost)                                       | Proprietà    | nessuno                                                                        |
| [**CanMaximize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_canmaximize)                                   | Proprietà    | nessuno                                                                        |
| [**CanMinimize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_canminimize)                                   | Proprietà    | nessuno                                                                        |
| [**WindowVisualState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_windowvisualstate)                       | Proprietà    | nessuno                                                                        |
| [**Chiudi**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-close)                                               | Metodo      | nessuno                                                                        |
| [**SetVisualState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-setvisualstate)                             | Metodo      | nessuno                                                                        |
| [**WaitForInputIdle**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-waitforinputidle)                         | Metodo      | nessuno                                                                        |
| [**\_WindowClosedEventId finestra \_ UIA**](uiauto-event-ids.md) | Evento       | nessuno                                                                        |
| [**\_WindowOpenedEventId finestra \_ UIA**](uiauto-event-ids.md) | Evento       | nessuno                                                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Mapping dei pattern di controllo per i client di automazione interfaccia utente](uiauto-controlpatternmapping.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> </dl>

 

 





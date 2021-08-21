---
title: Pattern di controllo MultipleView
description: Descrive le linee guida e le convenzioni per l'implementazione di IMultipleViewProvider, incluse le informazioni su proprietà e metodi.
ms.assetid: c67e7e4f-d2c7-4fca-8e8a-9b6565afa4ed
keywords:
- Automazione interfaccia utente,implementazione del pattern di controllo MultipleView
- Automazione interfaccia utente,Pattern di controllo MultipleView
- Automazione interfaccia utente,IMultipleViewProvider
- IMultipleViewProvider
- Implementazione Automazione interfaccia utente pattern di controllo MultipleView
- Pattern di controllo MultipleView
- pattern di controllo, IMultipleViewProvider
- pattern di controllo, implementazione Automazione interfaccia utente MultipleView
- pattern di controllo, MultipleView
- interfacce, IMultipleViewProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a5848a521da45470854bd860d3ee9c582e18fc84783ca8072ad552fd91a8d1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115004"
---
# <a name="multipleview-control-pattern"></a>Pattern di controllo MultipleView

Descrive le linee guida e le convenzioni per l'implementazione [**di IMultipleViewProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider)incluse le informazioni su proprietà e metodi. Alla fine della panoramica sono elencati collegamenti ad altro materiale di riferimento. Il **pattern di controllo MultipleView** viene usato per supportare i controlli che forniscono e sono in grado di alternare più rappresentazioni delle stesse informazioni o dello stesso set di controlli figlio.

Esempi di controlli che possono presentare più visualizzazioni includono la visualizzazione elenco (che può visualizzarne il contenuto come anteprime, riquadri, icone o dettagli), i grafici Microsoft Excel (a torta, a linee, a barre, il valore della cella con una formula), i documenti Microsoft Word (normale, layout Web, layout di stampa, layout di lettura, struttura), il calendario di Microsoft Outlook (anno, mese, settimana, giorno) e le interfaccia di Microsoft Windows Media Player. Le visualizzazioni supportate sono determinate dallo sviluppatore del controllo e sono specifiche di ogni controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **IMultipleViewProvider**](#required-members-for-imultipleviewprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern **di controllo MultipleView,** tenere presenti le linee guida e le convenzioni seguenti:

-   [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) deve essere implementato anche in un contenitore che gestisce la visualizzazione corrente se è diversa da un controllo che fornisce la visualizzazione corrente. Ad esempio, Windows Explorer contiene un controllo elenco per il contenuto della cartella corrente, mentre la visualizzazione per il controllo viene gestita dall'applicazione Windows Explorer.
-   Un controllo in grado di ordinare il relativo contenuto non supporta più visualizzazioni.
-   La raccolta di visualizzazioni deve essere identica tra istanze.
-   I nomi delle view devono essere adatti per l'uso in sintesi vocale, Braille e altre applicazioni leggibili dall'utente.

## <a name="required-members-for-imultipleviewprovider"></a>Membri obbligatori per **IMultipleViewProvider**

Per implementare l'interfaccia [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) sono necessari i metodi e le proprietà seguenti.



| Membri obbligatori                                                            | Tipo di membro | Note |
|-----------------------------------------------------------------------------|-------------|-------|
| [**Currentview**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-get_currentview)             | Proprietà    | Nessuno  |
| [**GetSupportedViews**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-getsupportedviews) | Metodo      | Nessuno  |
| [**GetViewName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-getviewname)             | Metodo      | Nessuno  |
| [**SetCurrentView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-setcurrentview)       | Metodo      | Nessuno  |



 

Questo pattern di controllo non è associato a eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di controllo e pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> <dt>

[Pattern di controllo ExpandCollapse](uiauto-implementingexpandcollapse.md)
</dt> </dl>

 

 





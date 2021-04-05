---
title: Pattern di controllo Scroll
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di IScrollProvider, incluse informazioni su proprietà e metodi. Il pattern di controllo Scroll viene usato per supportare un controllo che funge da contenitore scorrevole per una raccolta di oggetti figlio.
ms.assetid: baf8012a-52d5-4465-b26d-aa3d7f550b54
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo Scroll
- Automazione interfaccia utente, pattern di controllo Scroll
- Automazione interfaccia utente, IScrollProvider
- IScrollProvider
- implementazione di pattern di controllo Scroll di automazione interfaccia utente
- Pattern di controllo Scroll
- pattern di controllo, IScrollProvider
- pattern di controllo, implementazione dello scorrimento di automazione interfaccia utente
- pattern di controllo, scorrimento
- interfacce, IScrollProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b525c77a7f89f7adc95a3d90d999f8b243cfcdb6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712172"
---
# <a name="scroll-control-pattern"></a>Pattern di controllo Scroll

Vengono descritte le linee guida e le convenzioni per l'implementazione di [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider), incluse informazioni su proprietà e metodi. Il pattern di controllo **Scroll** viene usato per supportare un controllo che funge da contenitore scorrevole per una raccolta di oggetti figlio.

Il controllo non è necessario per usare le barre di scorrimento per supportare la funzionalità di scorrimento, sebbene in genere. La figura seguente mostra un controllo scorrevole che non usa barre di scorrimento. Per esempi di controlli che implementano questo pattern di controllo, vedere [tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md).

![screenshot che mostra un controllo di scorrimento senza barre di scorrimento](images/uia-scrollpattern-without-scrollbars.jpg)

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **IScrollProvider**](#required-members-for-iscrollprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern di controllo **Scroll** , tenere presenti le linee guida e le convenzioni seguenti:

-   Gli elementi figlio di questo controllo devono implementare [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider).
-   Le barre di scorrimento di un controllo contenitore non supportano il pattern di controllo **Scroll** . Devono invece supportare il pattern di controllo [RangeValue](uiauto-implementingrangevalue.md) .
-   Quando lo scorrimento è misurato in percentuali, tutti i valori o gli importi relativi alla scala di scorrimento devono essere normalizzati in base a un intervallo compreso tra 0 e 100.
-   La proprietà [**IScrollProvider:: HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) e la proprietà [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) sono indipendenti dalla proprietà **IsEnabled** .
-   Se la proprietà [**IScrollProvider:: HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) è **false**, la proprietà [**HorizontalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalviewsize) deve essere impostata su 100 (100%) e la proprietà [**HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) deve essere impostata su **UIA \_ ScrollPatternNoScroll** (-1). Analogamente, se la proprietà [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) è **false**, la proprietà [**VerticalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalviewsize) deve essere impostata su 100 (100%) e la proprietà [**VerticalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalscrollpercent) deve essere impostata su **UIA \_ ScrollPatternNoScroll** (-1). In questo modo un client di automazione interfaccia utente Microsoft può usare questi valori di proprietà all'interno del metodo [**SetScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-setscrollpercent) , evitando una race condition se una direzione che il client non è interessata allo scorrimento viene attivata.
-   La proprietà [**IScrollProvider:: HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) è specifica delle impostazioni locali. Impostando **HorizontalScrollPercent** su 100 è necessario impostare la posizione di scorrimento del controllo sull'equivalente della posizione all'estrema destra per le lingue, ad esempio l'inglese, lette da sinistra a destra. In alternativa, per lingue quali l'arabo che legge da destra a sinistra, impostando **HorizontalScrollPercent** su 100 è necessario impostare la posizione di scorrimento sulla posizione più a sinistra.

## <a name="required-members-for-iscrollprovider"></a>Membri obbligatori per **IScrollProvider**

Le proprietà e i metodi seguenti sono necessari per implementare l'interfaccia [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider) .



| Membri obbligatori                                                                  | Tipo di membro | Note |
|-----------------------------------------------------------------------------------|-------------|-------|
| [**HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) | Proprietà    | nessuno  |
| [**VerticalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalscrollpercent)     | Proprietà    | nessuno  |
| [**HorizontalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalviewsize)           | Proprietà    | nessuno  |
| [**VerticalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalviewsize)               | Proprietà    | nessuno  |
| [**HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable)   | Proprietà    | nessuno  |
| [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable)       | Proprietà    | nessuno  |
| [**Scorrimento**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-scroll)                                   | Metodo      | nessuno  |
| [**SetScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-setscrollpercent)               | Metodo      | nessuno  |



 

Questo pattern di controllo non è associato a eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> </dl>

 

 





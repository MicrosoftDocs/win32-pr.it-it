---
title: Pattern di controllo Scroll
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di IScrollProvider, incluse informazioni su proprietà e metodi. Il pattern di controllo Scroll viene usato per supportare un controllo che funge da contenitore scorrevole per una raccolta di oggetti figlio.
ms.assetid: baf8012a-52d5-4465-b26d-aa3d7f550b54
keywords:
- Automazione interfaccia utente,implementazione del pattern di controllo Scroll
- Automazione interfaccia utente,Pattern di controllo Scroll
- Automazione interfaccia utente,IScrollProvider
- IScrollProvider
- Implementazione di Automazione interfaccia utente di controllo Scroll
- Pattern di controllo di scorrimento
- pattern di controllo, IScrollProvider
- pattern di controllo, implementazione Automazione interfaccia utente Scroll
- pattern di controllo,scorrimento
- interfacce, IScrollProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1d1cf3c04be18f362a64e619ec4659fac58923f29e6105174057b18a580f8d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118324396"
---
# <a name="scroll-control-pattern"></a>Pattern di controllo Scroll

Vengono descritte le linee guida e le convenzioni per [**l'implementazione di IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider), incluse informazioni su proprietà e metodi. Il **pattern di** controllo Scroll viene usato per supportare un controllo che funge da contenitore scorrevole per una raccolta di oggetti figlio.

Il controllo non è necessario per usare le barre di scorrimento per supportare la funzionalità di scorrimento, anche se in genere lo fa. L'immagine seguente mostra un controllo di scorrimento che non usa barre di scorrimento. Per esempi di controlli che implementano questo pattern di controllo, vedere [Tipi di controllo e pattern di controllo supportati.](uiauto-controlpatternmapping.md)

![Screenshot che mostra un controllo di scorrimento senza barre di scorrimento](images/uia-scrollpattern-without-scrollbars.jpg)

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **IScrollProvider**](#required-members-for-iscrollprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il **pattern di controllo Scroll,** tenere presente le linee guida e le convenzioni seguenti:

-   Gli elementi figlio di questo controllo devono implementare [**IScrollItemProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)
-   Le barre di scorrimento di un controllo contenitore non supportano il **pattern di controllo Scroll.** Devono invece supportare il [pattern di controllo RangeValue.](uiauto-implementingrangevalue.md)
-   Quando lo scorrimento è misurato in percentuali, tutti i valori o gli importi relativi alla scala di scorrimento devono essere normalizzati in base a un intervallo compreso tra 0 e 100.
-   La [**proprietà IScrollProvider::HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) e [**la proprietà VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) sono indipendenti dalla **proprietà IsEnabled.**
-   Se la proprietà [**IScrollProvider::HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) è **FALSE,** la proprietà [**HorizontalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalviewsize) deve essere impostata su 100 (100%) e la proprietà [**HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) deve essere impostata su **UIA \_ ScrollPatternNoScroll** (-1). Analogamente, se la proprietà [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) è **FALSE,** la proprietà [**VerticalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalviewsize) deve essere impostata su 100 (100%) e la proprietà [**VerticalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalscrollpercent) deve essere impostata su **UIA \_ ScrollPatternNoScroll** (-1). Ciò consente a un client Microsoft Automazione interfaccia utente di usare questi valori di proprietà all'interno del metodo [**SetScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-setscrollpercent) evitando un race condition se viene attivata una direzione che il client non è interessato allo scorrimento.
-   La [**proprietà IScrollProvider::HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) è specifica delle impostazioni locali. **L'impostazione di HorizontalScrollPercent** su 100 deve impostare la posizione di scorrimento del controllo sull'equivalente della posizione più a destra per lingue come l'inglese che leggono da sinistra a destra. In alternativa, per lingue come l'arabo che leggono da destra a sinistra, l'impostazione **di HorizontalScrollPercent** su 100 deve impostare la posizione di scorrimento all'estrema sinistra.

## <a name="required-members-for-iscrollprovider"></a>Membri obbligatori per **IScrollProvider**

Le proprietà e i metodi seguenti sono necessari per l'implementazione [**dell'interfaccia IScrollProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)



| Membri obbligatori                                                                  | Tipo di membro | Note |
|-----------------------------------------------------------------------------------|-------------|-------|
| [**HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) | Proprietà    | Nessuno  |
| [**VerticalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalscrollpercent)     | Proprietà    | Nessuno  |
| [**HorizontalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalviewsize)           | Proprietà    | Nessuno  |
| [**VerticalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalviewsize)               | Proprietà    | Nessuno  |
| [**HorizontalScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable)   | Proprietà    | Nessuno  |
| [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable)       | Proprietà    | Nessuno  |
| [**Scorrimento**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-scroll)                                   | Metodo      | Nessuno  |
| [**SetScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-setscrollpercent)               | Metodo      | Nessuno  |



 

Questo pattern di controllo non è associato a eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di controllo e relativi pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> </dl>

 

 





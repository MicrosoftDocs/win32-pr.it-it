---
title: Pattern di controllo ScrollItem
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di IScrollItemProvider, incluse informazioni sui metodi.
ms.assetid: ea0d7438-218c-4925-b24c-a8011f305b9d
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo ScrollItem
- Automazione interfaccia utente, pattern di controllo ScrollItem
- Automazione interfaccia utente, IScrollItemProvider
- IScrollItemProvider
- implementazione di pattern di controllo ScrollItem di automazione interfaccia utente
- Pattern di controllo ScrollItem
- pattern di controllo, IScrollItemProvider
- pattern di controllo, implementazione dell'automazione interfaccia utente ScrollItem
- pattern di controllo, ScrollItem
- interfacce, IScrollItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7233dfe649d166a3172ff2dda3122895f259abcc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221568"
---
# <a name="scrollitem-control-pattern"></a>Pattern di controllo ScrollItem

Vengono descritte le linee guida e le convenzioni per l'implementazione di [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider), incluse informazioni sui metodi. Il pattern di controllo **ScrollItem** viene usato per supportare singoli controlli figlio di contenitori che implementano [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider). L'esistenza del pattern di controllo **ScrollItem** in un controllo non implica che il relativo contenitore o qualsiasi predecessore debba implementare il pattern di controllo **Scroll** .

Quando il contenitore implementa il pattern di controllo **Scroll** , il pattern di controllo **ScrollItem** funge da canale di comunicazione tra un controllo figlio e il relativo contenitore per garantire che il contenitore possa modificare il contenuto o l'area attualmente visibile all'interno del viewport per visualizzare il controllo figlio. Per esempi di controlli che implementano questo pattern di controllo, vedere [tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md).

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **IScrollItemProvider**](#required-members-for-iscrollitemprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern di controllo **ScrollItem** , tenere presenti le linee guida e le convenzioni seguenti:

-   Gli elementi contenuti in una [finestra](uiauto-supportwindowcontroltype.md) o in un controllo **Canvas** non sono necessari per implementare l'interfaccia [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) . In alternativa, tuttavia, devono esporre un percorso valido per la proprietà [**IUIAutomationElement:: CurrentBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentboundingrectangle) (o [**CachedBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedboundingrectangle)). Ciò consentirà a un'applicazione client di automazione interfaccia utente Microsoft di usare i metodi del pattern di controllo [**IUIAutomationScrollPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationscrollpattern) sul contenitore per visualizzare l'elemento figlio.

## <a name="required-members-for-iscrollitemprovider"></a>Membri obbligatori per **IScrollItemProvider**

Il metodo seguente è necessario per implementare l'interfaccia [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) .



| Membri obbligatori                                                    | Tipo di membro | Note |
|---------------------------------------------------------------------|-------------|-------|
| [**ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollitemprovider-scrollintoview) | Metodo      | nessuno  |



 

Questo pattern di controllo non è associato a proprietà o eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Pattern di controllo Selection](uiauto-implementingselection.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> </dl>

 

 





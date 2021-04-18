---
title: Pattern di controllo Transform
description: Descrive le linee guida e le convenzioni per l'implementazione di ITransformProvider e ITransformProvider2, incluse informazioni su proprietà e metodi.
ms.assetid: e1d862a0-8085-42b4-9710-cf11e1a467cf
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo Transform
- Automazione interfaccia utente, pattern di controllo Transform
- Automazione interfaccia utente, ITransformProvider
- ITransformProvider
- implementazione di pattern di controllo Transform di automazione interfaccia utente
- Pattern di controllo Transform
- pattern di controllo, ITransformProvider
- pattern di controllo, implementazione della trasformazione automazione interfaccia utente
- pattern di controllo, trasformazione
- interfacce, ITransformProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eae752b34ed0b64fd2c0a7b476377fd1142f9b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516959"
---
# <a name="transform-control-pattern"></a>Pattern di controllo Transform

Descrive le linee guida e le convenzioni per l'implementazione di [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) e [**ITransformProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itransformprovider2), incluse informazioni su proprietà e metodi. Il pattern di controllo Transform viene usato per supportare i controlli che possono essere spostati, ridimensionati o ruotati in uno spazio bidimensionale.

Per esempi di controlli che implementano questo pattern di controllo, vedere [tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md).

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **ITransformProvider**](#required-members-for-itransformprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern di controllo **Transform** , tenere presenti le linee guida e le convenzioni seguenti:

-   Il supporto per questo pattern di controllo non è limitato agli oggetti sul desktop. Questo pattern di controllo deve essere supportato dagli elementi figlio di un oggetto contenitore se gli elementi figlio possono essere spostati, ridimensionati o ruotati all'interno dei limiti del contenitore.
-   Un oggetto non può essere spostato, ridimensionato o ruotato in modo che la posizione risultante sullo schermo potrebbe essere completamente esterna alle coordinate del relativo contenitore e pertanto inaccessibile per la tastiera o il mouse (ad esempio, quando una finestra di primo livello viene spostata fuori schermo o un oggetto figlio viene spostato fuori dai limiti del riquadro di visualizzazione del contenitore). In questi casi, l'oggetto viene posizionato il più vicino possibile alle coordinate richieste dello schermo rispetto alle coordinate in alto e a sinistra entro i limiti del contenitore.
-   Per sistemi con più monitor, se un oggetto viene spostato, ridimensionato o ruotato completamente al di fuori delle coordinate combinate dello schermo desktop, l'oggetto viene posizionato sul monitor principale il più vicino possibile alle coordinate richieste.
-   Tutti i parametri e i valori delle proprietà sono assoluti e indipendenti dalle impostazioni locali.

## <a name="required-members-for-itransformprovider"></a>Membri obbligatori per **ITransformProvider**

Per l'implementazione dell'interfaccia [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) sono necessari i metodi e le proprietà seguenti.



| Membri obbligatori                                         | Tipo di membro | Note |
|----------------------------------------------------------|-------------|-------|
| [**CanMove**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canmove)     | Proprietà    | nessuno  |
| [**CanResize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canresize) | Proprietà    | nessuno  |
| [**CanRotate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canrotate) | Proprietà    | nessuno  |
| [**Spostare**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-move)           | Metodo      | nessuno  |
| [**Ridimensionamento**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-resize)       | Metodo      | nessuno  |
| [**Ruota**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-rotate)       | Metodo      | nessuno  |



 

Per l'implementazione dell'interfaccia [**ITransformProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) sono necessari i metodi e le proprietà aggiuntive seguenti.



| Membri obbligatori                                              | Tipo di membro | Note |
|---------------------------------------------------------------|-------------|-------|
| [**CanZoom**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider2-get_canzoom)     | Proprietà    | nessuno  |
| [**Zoom**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider2-zoom)           | Metodo      | nessuno  |
| [**ZoomByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-zoombyunit)   | Metodo      | nessuno  |
| [**ZoomLevel**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoomlevel)     | Proprietà    | nessuno  |
| [**ZoomMaximum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoommaximum) | Proprietà    | nessuno  |
| [**ZoomMinimum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoomminimum) | Proprietà    | nessuno  |



 

Questo pattern di controllo non è associato a eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> </dl>

 

 
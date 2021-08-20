---
title: Pattern di controllo RangeValue
description: Descrive le linee guida e le convenzioni per l'implementazione di IRangeValueProvider, incluse le informazioni su proprietà e metodi. Il pattern di controllo RangeValue viene usato per supportare i controlli che possono essere impostati su un valore all'interno di un intervallo.
ms.assetid: e5c1104c-4b20-4fdd-bd12-dfc27cb73ac5
keywords:
- Automazione interfaccia utente,implementazione del pattern di controllo RangeValue
- Automazione interfaccia utente,Pattern di controllo RangeValue
- Automazione interfaccia utente,IRangeValueProvider
- IRangeValueProvider
- Implementazione Automazione interfaccia utente pattern di controllo RangeValue
- Pattern di controllo RangeValue
- pattern di controllo, IRangeValueProvider
- pattern di controllo, implementazione Automazione interfaccia utente RangeValue
- pattern di controllo, RangeValue
- interfacce, IRangeValueProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae87ca25fd1ada2f57ce77412fb589875792541fd2b5d31d6eb0aa86192dee36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114862"
---
# <a name="rangevalue-control-pattern"></a>Pattern di controllo RangeValue

Descrive le linee guida e le convenzioni per l'implementazione [**di IRangeValueProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)incluse le informazioni su proprietà e metodi. Il **pattern di controllo RangeValue** viene usato per supportare i controlli che possono essere impostati su un valore all'interno di un intervallo.

Per esempi di controlli che implementano questo pattern di controllo, vedere [Tipi di controllo e pattern di controllo supportati.](uiauto-controlpatternmapping.md)

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **IRangeValueProvider**](#required-members-for-irangevalueprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern **di controllo RangeValue,** tenere presente le linee guida e le convenzioni seguenti:

-   I controlli consentono la ricalibrazione delle relative proprietà supportate in base alle preferenze utente o alle impostazioni locali. Un esempio di questo è un controllo termometro che può essere impostato per visualizzare la temperatura in gradi Fahrenheit o Celsius.
-   I controlli che dispongono di valori di intervallo ambigui, ad esempio le barre di avanzamento o i dispositivi di scorrimento, devono avere questi valori normalizzati.

## <a name="required-members-for-irangevalueprovider"></a>Membri obbligatori per **IRangeValueProvider**

Le proprietà e i metodi seguenti sono necessari per l'implementazione [**dell'interfaccia IRangeValueProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)



| Membri obbligatori                                              | Tipo di membro | Note |
|---------------------------------------------------------------|-------------|-------|
| [**IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_isreadonly)   | Proprietà    | Nessuno  |
| [**Valore**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value)             | Proprietà    | Nessuno  |
| [**Largechange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_largechange) | Proprietà    | Nessuno  |
| [**Smallchange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_smallchange) | Proprietà    | Nessuno  |
| [**Massimo**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)         | Proprietà    | Nessuno  |
| [**Minimo**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)         | Proprietà    | Nessuno  |
| [**SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-setvalue)       | Metodo      | Nessuno  |



 

Questo pattern di controllo non è associato a eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di controllo e pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> </dl>

 

 





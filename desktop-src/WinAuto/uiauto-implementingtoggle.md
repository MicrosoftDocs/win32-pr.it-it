---
title: Mostra/Nascondi pattern di controllo
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di IToggleProvider, incluse informazioni su proprietà e metodi. Il pattern di controllo di alternanza viene usato per supportare i controlli che possono scorrere un insieme di Stati e gestire uno stato una volta impostato.
ms.assetid: 9fd1232b-199a-41e6-81b0-667c7e463d09
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo di attivazione
- Automazione interfaccia utente, controllo interruttore
- Automazione interfaccia utente, IToggleProvider
- IToggleProvider
- implementazione di pattern di controllo di automazione interfaccia utente
- Imposta/Nascondi pattern di controllo
- pattern di controllo, IToggleProvider
- pattern di controllo, implementazione dell'attivazione di automazione interfaccia utente
- pattern di controllo, interruttore
- interfacce, IToggleProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723d45326fdf9942682a318282ce4a9784df489c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395610"
---
# <a name="toggle-control-pattern"></a>Mostra/Nascondi pattern di controllo

Vengono descritte le linee guida e le convenzioni per l'implementazione di [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider), incluse informazioni su proprietà e metodi. Il pattern di controllo di **alternanza** viene usato per supportare i controlli che possono scorrere un insieme di Stati e gestire uno stato una volta impostato.

Per esempi di controlli che implementano questo pattern di controllo, vedere [tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md).

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **IToggleProvider**](#required-members-for-itoggleprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern di controllo di **attivazione** , tenere presenti le linee guida e le convenzioni seguenti:

-   I controlli che non mantengono lo stato quando vengono attivati, ad esempio pulsanti, pulsanti della barra degli strumenti e collegamenti ipertestuali, devono invece implementare [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) .
-   Un controllo deve scorrere i relativi stati di attivazione/disattivazione ([**ToggleState**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate)) nell'ordine seguente: **ToggleState \_ on**, **ToggleState \_ off** e, se supportato, **ToggleState \_ indeterminato**.
-   L' **attivazione/disattivazione** non fornisce un metodo di stato set a causa di problemi relativi all'impostazione diretta di una casella di controllo a tre stati senza eseguire il ciclo della sequenza [**ToggleState**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) appropriata.
-   Il controllo pulsante di opzione non implementa [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider), perché non è in grado di eseguire il Cycling negli stati validi.

## <a name="required-members-for-itoggleprovider"></a>Membri obbligatori per **IToggleProvider**

Le proprietà e i metodi seguenti sono necessari per implementare l'interfaccia [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) .



| Membri obbligatori                                          | Tipo di membro | Note |
|-----------------------------------------------------------|-------------|-------|
| [**Interruttore**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itoggleprovider-toggle)           | Metodo      | nessuno  |
| [**ToggleState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itoggleprovider-get_togglestate) | Proprietà    | nessuno  |



 

Questo pattern di controllo non è associato a eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> </dl>

 

 





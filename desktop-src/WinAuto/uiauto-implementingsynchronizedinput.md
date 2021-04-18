---
title: Pattern di controllo SynchronizedInput
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di ISynchronizedInputProvider, incluse informazioni su proprietà e metodi.
ms.assetid: 3e2d65ea-8093-4e65-b43e-28478ec74607
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo SynchronizedInput
- Automazione interfaccia utente, pattern di controllo SynchronizedInput
- Automazione interfaccia utente, ISynchronizedInputProvider
- ISynchronizedInputProvider
- implementazione di pattern di controllo SynchronizedInput di automazione interfaccia utente
- Pattern di controllo SynchronizedInput
- pattern di controllo, ISynchronizedInputProvider
- pattern di controllo, implementazione dell'automazione interfaccia utente SynchronizedInput
- pattern di controllo, SynchronizedInput
- interfacce, ISynchronizedInputProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 105e75163fdac742adaad6b778c251b4b7b8ae70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298615"
---
# <a name="synchronizedinput-control-pattern"></a>Pattern di controllo SynchronizedInput

Vengono descritte le linee guida e le convenzioni per l'implementazione di [**ISynchronizedInputProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider), incluse informazioni su proprietà e metodi. Il pattern di controllo **SynchronizedInput** consente alle applicazioni client di automazione interfaccia utente Microsoft di indirizzare l'input del mouse o della tastiera a un elemento specifico dell'interfaccia utente.

Questo pattern di controllo viene in genere usato negli script di test automatizzati per inviare l'input del mouse o della tastiera a un elemento dell'interfaccia utente specifico e quindi verificare che l'elemento abbia ricevuto l'input.

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **ISynchronizedInputProvider**](#required-members-for-isynchronizedinputprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern di controllo **SynchronizedInput** , tenere presenti le linee guida e le convenzioni seguenti:

-   Quando viene chiamato il metodo [**ISynchronizedInputProvider:: StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) , il provider di automazione interfaccia utente deve iniziare a controllare l'input del tipo specificato e quindi eseguire una delle azioni seguenti:
    -   Quando viene trovato un input corrispondente per l'elemento, il provider deve generare l'evento [**\_ InputReachedTargetEventId di UIA**](uiauto-event-ids.md) .
    -   Quando viene trovato un input corrispondente, ma è stato raggiunto un elemento diverso, il provider deve generare l'evento [**\_ InputReachedOtherElementEventId di UIA**](uiauto-event-ids.md) .
    -   Quando viene trovato un input non corrispondente, il provider deve eliminare l'input e generare l' [**evento \_ InputDiscardedEventId**](uiauto-event-ids.md) di gestione dei servizi.
-   Il provider di automazione interfaccia utente deve eliminare l'input se è per un elemento diverso dall'elemento corrente.
-   Quando l'elemento riceve l'input o quando viene chiamato il metodo [**ISynchronizedInputProvider:: Cancel**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel) , il provider interrompe il controllo dell'input e continua normalmente.
-   Se [**ISynchronizedInputProvider:: StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) viene chiamato quando il provider è già in ascolto per l'input, il provider deve restituire l'oggetto [**UIA \_ E \_ INVALIDOPERATION**](uiauto-error-codes.md).

## <a name="required-members-for-isynchronizedinputprovider"></a>Membri obbligatori per **ISynchronizedInputProvider**

Le proprietà, i metodi e gli eventi seguenti sono obbligatori per l'implementazione dell'interfaccia [**ISynchronizedInputProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider) .



| Membri obbligatori                                                                         | Tipo di membro | Note |
|------------------------------------------------------------------------------------------|-------------|-------|
| [**StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening)               | Metodo      | nessuno  |
| [**Annulla**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel)                               | Metodo      | nessuno  |
| [**\_INPUTREACHEDTARGETEVENTID UIA**](uiauto-event-ids.md) | Evento       | nessuno  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 





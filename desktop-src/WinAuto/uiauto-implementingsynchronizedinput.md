---
title: Pattern di controllo SynchronizedInput
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di ISynchronizedInputProvider, incluse le informazioni su proprietà e metodi.
ms.assetid: 3e2d65ea-8093-4e65-b43e-28478ec74607
keywords:
- Automazione interfaccia utente,implementazione del pattern di controllo SynchronizedInput
- Automazione interfaccia utente, pattern di controllo SynchronizedInput
- Automazione interfaccia utente,ISynchronizedInputProvider
- ISynchronizedInputProvider
- implementazione di Automazione interfaccia utente di controllo SynchronizedInput
- Pattern di controllo SynchronizedInput
- pattern di controllo, ISynchronizedInputProvider
- pattern di controllo, implementazione Automazione interfaccia utente SynchronizedInput
- pattern di controllo, SynchronizedInput
- interfacce, ISynchronizedInputProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91aa4ad93a30be26ebcbc463ade3a27d896d61727508965a86d1ed229b7d79be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114852"
---
# <a name="synchronizedinput-control-pattern"></a>Pattern di controllo SynchronizedInput

Vengono descritte le linee guida e le convenzioni per [**l'implementazione di ISynchronizedInputProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider)incluse le informazioni su proprietà e metodi. Il **pattern di controllo SynchronizedInput** consente a Microsoft Automazione interfaccia utente applicazioni client di indirizzare l'input del mouse o della tastiera a un elemento dell'interfaccia utente specifico.

Questo pattern di controllo viene in genere usato negli script di test automatizzati per inviare l'input del mouse o della tastiera a un elemento specifico dell'interfaccia utente e quindi verificare che l'elemento ha ricevuto l'input.

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **ISynchronizedInputProvider**](#required-members-for-isynchronizedinputprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern **di controllo SynchronizedInput,** tenere presente le linee guida e le convenzioni seguenti:

-   Quando viene chiamato il metodo [**ISynchronizedInputProvider::StartListening,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) il provider Automazione interfaccia utente deve iniziare a cercare l'input del tipo specificato e quindi eseguire una delle azioni seguenti:
    -   Quando viene trovato un input corrispondente per l'elemento, il provider deve generare l'evento [**\_ UiA InputReachedTargetEventId.**](uiauto-event-ids.md)
    -   Quando viene trovato l'input corrispondente, ma ha raggiunto un elemento diverso, il provider deve generare l'evento [**\_ UiA InputReachedOtherElementEventId.**](uiauto-event-ids.md)
    -   Quando viene trovato un input non corrispondente, il provider deve rimuovere l'input e generare l'evento [**\_ UiA InputDiscardedEventId.**](uiauto-event-ids.md)
-   Il provider Automazione interfaccia utente deve rimuovere l'input se è per un elemento diverso dall'elemento corrente.
-   Quando l'elemento riceve l'input o quando viene chiamato il metodo [**ISynchronizedInputProvider::Cancel,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel) il provider interrompe il controllo dell'input e continua come di consueto.
-   Se [**ISynchronizedInputProvider::StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) viene chiamato quando il provider è già in ascolto dell'input, il provider deve restituire [**UIA \_ E \_ INVALIDOPERATION**](uiauto-error-codes.md).

## <a name="required-members-for-isynchronizedinputprovider"></a>Membri obbligatori per **ISynchronizedInputProvider**

Le proprietà, i metodi e gli eventi seguenti sono necessari per l'implementazione [**dell'interfaccia ISynchronizedInputProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider)



| Membri obbligatori                                                                         | Tipo di membro | Note |
|------------------------------------------------------------------------------------------|-------------|-------|
| [**Elenco di avvio**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening)               | Metodo      | Nessuno  |
| [**Annulla**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel)                               | Metodo      | Nessuno  |
| [**UIA \_ InputReachedTargetEventId**](uiauto-event-ids.md) | Event       | Nessuno  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 





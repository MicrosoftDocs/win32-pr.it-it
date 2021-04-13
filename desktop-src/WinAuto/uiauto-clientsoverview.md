---
title: Panoramica dei client di automazione interfaccia utente
description: In questo argomento vengono descritte le attività principali relative all'implementazione di un'applicazione client di automazione interfaccia utente Microsoft.
ms.assetid: 536ccf03-2f52-49e5-a95f-ea56cf821779
keywords:
- Automazione interfaccia utente, panoramica dei client
- client, informazioni
- client, elementi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d4705d75a0a80c114e2b83f9625f827c75503b9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399112"
---
# <a name="ui-automation-clients-overview"></a>Panoramica dei client di automazione interfaccia utente

In questo argomento vengono descritte le attività principali relative all'implementazione di un'applicazione client di automazione interfaccia utente Microsoft.

Un client di automazione interfaccia utente è un'applicazione che usa l'API di automazione interfaccia utente per accedere alle informazioni sugli elementi dell'interfaccia utente o per controllare le applicazioni attraverso la manipolazione a livello di codice degli elementi dell'interfaccia utente. I client di automazione interfaccia utente includono applicazioni di Assistive Technology, quali utilità per la lettura dello schermo, che recuperano informazioni sugli elementi dell'interfaccia utente e presentano le informazioni in un modo utilizzabile per gli utenti con particolari esigenze. Includono anche applicazioni quali programmi di riconoscimento vocale e strumenti di test del software, che usano l'automazione dell'interfaccia utente anziché il mouse e la tastiera per "guidare" altre applicazioni.

Dal punto di vista dell'automazione interfaccia utente, le attività principali che un'applicazione client di automazione interfaccia utente deve eseguire sono le seguenti:

1.  **Ottenere un'istanza dell'oggetto CUIAutomation.**

    Le informazioni sugli elementi dell'interfaccia utente e l'accesso alle funzionalità degli elementi dell'interfaccia utente sono esposte ai client dai provider di automazione interfaccia utente. Tuttavia, le applicazioni client non funzionano direttamente con i provider. Al contrario, un servizio di base risiede tra il client e il provider. Quando un client chiama l'API di automazione interfaccia utente, chiama effettivamente il servizio di base di automazione interfaccia utente che, a sua volta, effettua chiamate alle interfacce implementate dal provider.

    Per ottenere l'accesso al servizio di automazione interfaccia utente principale, è necessario che un client crei un'istanza dell'oggetto [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) e recuperi un puntatore all'interfaccia [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) per l'oggetto. Il puntatore **IUIAutomation** è la chiave del client per accedere a tutte le funzionalità di automazione interfaccia utente disponibili per il client. Per ulteriori informazioni, vedere [creazione dell'oggetto CUIAutomation](uiauto-creatingcuiautomation.md).

2.  **Recupera le interfacce IUIAutomationElement per gli elementi dell'interfaccia utente dall'albero di automazione interfaccia utente.**

    Automazione interfaccia utente espone singoli elementi dell'interfaccia utente come oggetti che implementano l'interfaccia [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) . Le informazioni su un elemento sono disponibili per i client tramite le proprietà esposte dall'interfaccia **IUIAutomationElement** dell'elemento, insieme all'accesso ai pattern di controllo dell'elemento. Le proprietà e i metodi esposti dalle interfacce del pattern di controllo forniscono l'accesso a informazioni e funzionalità specifiche del controllo.

    Gli oggetti elemento di automazione interfaccia utente vengono forniti ai client in una struttura ad albero gerarchica chiamata albero di automazione interfaccia utente. I client usano i metodi esposti dall'interfaccia [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) per recuperare le interfacce [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) per gli elementi dell'interfaccia utente nell'albero e per recuperare altre interfacce usate per cercare gli elementi che corrispondono a un determinato set di criteri nell'albero. Per altre informazioni, vedere [acquisizione di elementi di automazione interfaccia utente](uiauto-obtainingelements.md).

    Quando si recuperano gli elementi dell'interfaccia utente, i client possono migliorare le prestazioni del sistema usando le funzionalità di memorizzazione nella cache di automazione interfaccia utente. La memorizzazione nella cache consente a un client di specificare un set di proprietà e pattern di controllo da recuperare insieme all'elemento. In una singola chiamata interprocesso, l'automazione interfaccia utente recupera l'elemento e le proprietà e i pattern di controllo specificati e li archivia nella cache. Senza la memorizzazione nella cache, è necessaria una chiamata di interprocesso separata per recuperare ogni proprietà o pattern di controllo. Per altre informazioni, vedere [memorizzazione nella cache delle proprietà e dei pattern di controllo di automazione interfaccia utente](uiauto-cachingforclients.md).

3.  **Recuperare le proprietà degli elementi dell'interfaccia utente e richiamare la funzionalità dell'elemento dell'interfaccia utente**

    I client usano l'interfaccia [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) per recuperare le proprietà e i pattern di controllo di un elemento. L'interfaccia include due versioni di ogni metodo di recupero delle proprietà: una versione recupera la proprietà dalla cache, l'altra recupera la proprietà dal provider. Per altre informazioni, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).

4.  **Rispondere agli eventi di automazione interfaccia utente.**

    I provider di automazione interfaccia utente inviano notifiche ai client di modifiche o importanti occorrenze nell'interfaccia utente tramite la generazione di eventi. I client devono determinare gli eventi necessari e quindi implementare e registrare le interfacce di gestione degli eventi per ricevere ed elaborare tali eventi. Per altre informazioni, vedere [sottoscrizione di eventi di automazione interfaccia utente](uiauto-eventsforclients.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> <dt>

[Cenni preliminari sulle proprietà di automazione interfaccia utente](uiauto-propertiesoverview.md)
</dt> <dt>

[Cenni preliminari sugli eventi di automazione interfaccia utente](uiauto-eventsoverview.md)
</dt> </dl>

 

 
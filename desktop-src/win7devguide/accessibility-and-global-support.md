---
title: Accessibilità e supporto globale
description: La piattaforma Windows 7 semplifica la creazione di soluzioni accessibili a più utenti e che soddisfino o superino gli standard di conformità per l'accessibilità.
ms.assetid: bcad2f00-7885-461c-a2dc-0a0a176962b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea7f710850f419493c5a8435626d163361c8a03
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118183"
---
# <a name="accessibility-and-global-support"></a>Accessibilità e supporto globale

La piattaforma Windows 7 semplifica la creazione di soluzioni accessibili a più utenti e che soddisfino o superino gli standard di conformità per l'accessibilità. La community del fornitore di Assistive Technology (ATV) può ora creare soluzioni per un'ampia gamma di applicazioni client e gli sviluppatori di applicazioni troveranno più semplice creare e convalidare interfacce utente accessibili.

Windows 7 rende inoltre più semplice il supporto di più linguaggi globali rispetto alle versioni precedenti di Windows. Dal momento in cui un utente seleziona una lingua e una località, Windows 7 presenta date, numeri, calendari, regole di confronto e altre informazioni usando le convenzioni culturali che i clienti si aspettano.

## <a name="windows-automation"></a>Automazione di Windows

Windows 7 offre un livello di automazione avanzato e basato su standard, esteso per le applicazioni native. Si basa su Microsoft Active Accessibility e automazione interfaccia utente Microsoft. È anche progettato per funzionare con gli standard del settore, ad esempio la W3C Web ARIA (applicazione Internet avanzata accessibile) e le *specifiche della sezione 508*.

Automazione interfaccia utente offre prestazioni migliori grazie all'introduzione di proxy di automazione non gestiti più veloci per i controlli Win32 Microsoft e le applicazioni Microsoft Active Accessibility (*MSAA*) legacy, nonché registrazioni di eventi e proxy di automazione interfaccia utente migliori e più veloci. Le nuove funzionalità di estensibilità estendono i pattern di controllo, le proprietà e gli eventi personalizzati. (Vedere [API di automazione Windows: Panoramica](../winauto/windows-automation-api-overview.md)).

## <a name="accessibility-support-tools"></a>Strumenti di supporto per l'accessibilità

Il controllo di accessibilità dell'interfaccia utente è un pratico strumento di interfaccia utente grafica che consente agli sviluppatori e ai tester di verificare rapidamente se la loro interfaccia utente è conforme ai requisiti di accessibilità principali, ad esempio *MSAA* (che verifica le relazioni padre-figlio o i rettangoli di delimitazione) e l'accesso a livello di codice all'automazione interfaccia utente, alla generazione di eventi Vedere [controllo dell'accessibilità dell'interfaccia utente](https://www.codeplex.com/AccCheck).

La verifica di UIA è un Framework di automazione di test che facilita il test manuale e automatizzato dell'implementazione del provider di automazione interfaccia utente di un controllo o di un'applicazione. Questi due nuovi strumenti consentono agli sviluppatori di testare le implementazioni e le funzionalità di accessibilità nelle applicazioni che utilizzano *MSAA* o l'automazione interfaccia utente. Entrambi gli strumenti sono disponibili tramite [codeplex](https://www.codeplex.com/), un sito Web creato da Microsoft per ospitare progetti open source e per offrire una migliore gestione alla community di sviluppatori. Vedere [Framework di automazione di test di automazione interfaccia utente](https://uiautomationverify.codeplex.com/).

## <a name="improved-multi-language-user-interface-support-and-linguistic-services"></a>Miglioramento del supporto dell'interfaccia utente multilingue e dei servizi linguistici

Windows 7 offre agli sviluppatori un metodo standard per preparare le proprie applicazioni per il mercato internazionale offrendo un supporto migliorato per l'interfaccia utente multilingue e i servizi linguistici che possono usare nelle applicazioni.

Extended Linguistic Services è una nuova funzionalità di Windows 7 che consente agli sviluppatori di utilizzare lo stesso set di API per sfruttare una vasta gamma di funzionalità linguistiche avanzate. Grazie all'utilizzo di ServicesAPIs linguistici estesi in Windows 7, gli sviluppatori possono rilevare automaticamente il linguaggio di qualsiasi testo Unicode e utilizzare tali informazioni per migliorare le scelte di esperienza utente per i clienti in tutto il mondo. Servizi linguistici estesi offre anche il supporto per la traslitterazione incorporato che converte il testo da un sistema di scrittura a un altro. Ad esempio, gli sviluppatori possono ora convertire automaticamente il testo tra il cinese semplificato e quello tradizionale per aiutare gli utenti a comunicare tra loro attraverso i confini linguistici. Grazie all'utilizzo di ServicesAPIs linguistici estesi, gli sviluppatori saranno in grado di utilizzare servizi linguistici estesi esistenti, nonché di prelevare nuovi servizi in futuro senza dover imparare nuovo codice. (Vedere [servizi linguistici estesi](../intl/extended-linguistic-services.md)).

 

 
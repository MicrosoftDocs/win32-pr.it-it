---
title: Accessibilità e supporto globale
description: La Windows 7 semplifica la creazione di soluzioni accessibili a più utenti e che soddisfino o superino gli standard di conformità di accessibilità.
ms.assetid: bcad2f00-7885-461c-a2dc-0a0a176962b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 320f6e52dba4f2a6d9c89a7bdea287e948a1bca048b0d3e88a2a8978e8085d0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118709118"
---
# <a name="accessibility-and-global-support"></a>Accessibilità e supporto globale

La Windows 7 semplifica la creazione di soluzioni accessibili a più utenti e che soddisfino o superino gli standard di conformità di accessibilità. La community di assistive technology (ATV) può ora creare soluzioni per una più ampia gamma di applicazioni client e gli sviluppatori di applicazioni troveranno più facile creare e convalidare interfacce utente accessibili.

Windows 7 semplifica anche il supporto di più lingue globali rispetto alle versioni precedenti di Windows. Dal momento in cui un utente seleziona una lingua e una posizione, Windows 7 presenta date, numeri, calendari, regole di confronto e altre informazioni usando le convenzioni culturali previste dai clienti.

## <a name="windows-automation"></a>Windows Automazione

Windows 7 offre un livello di automazione esteso e basato su standard esteso alle applicazioni native. Si basa su Microsoft Active Accessibility e Microsoft Automazione interfaccia utente. È progettato anche per funzionare con gli standard del settore, ad esempio W3C Web ARIA (Accessible Rich Internet Application) e *Section 508 Specifications.*

Automazione interfaccia utente offre prestazioni migliori grazie all'introduzione di proxy di automazione non gestiti più veloci per i controlli Microsoft Win32 e le applicazioni legacy Microsoft Active Accessibility *(MSAA)* e di registrazioni di eventi e proxy Automazione interfaccia utente migliori e più veloci. Le nuove funzionalità di estendibilità estendono pattern di controllo, proprietà ed eventi personalizzati. Vedere API [Windows: Panoramica.](../winauto/windows-automation-api-overview.md)

## <a name="accessibility-support-tools"></a>Strumenti di supporto per l'accessibilità

Controllo accessibilità interfaccia utente è un pratico strumento dell'interfaccia utente grafica che consente a sviluppatori e tester di verificare rapidamente se l'interfaccia utente è conforme ai requisiti di accessibilità dei tasti, ad esempio *MSAA* (che verifica le relazioni padre-figlio o i rettangoli di delimitazione) e l'accesso Automazione interfaccia utente livello di codice, la generazione di eventi, il layout e lo spostamento tramite tastiera. Vedere Ui [Accessibility Checker (Controllo accessibilità interfaccia](https://www.codeplex.com/AccCheck)utente).

UiA Verify è un framework di automazione dei test che facilita i test manuali e automatizzati dell'implementazione del provider Automazione interfaccia utente di un controllo o di un'applicazione. Questi due nuovi strumenti consentono agli sviluppatori di testare le implementazioni e le funzionalità di accessibilità nelle applicazioni che usano *MSAA* o Automazione interfaccia utente. Entrambi gli strumenti sono disponibili tramite [CodePlex,](https://www.codeplex.com/)un sito Web creato da Microsoft per ospitare progetti open source e servire al meglio la community di sviluppatori. Vedere verifica [Automazione interfaccia utente test (uia verify) del framework di automazione](https://uiautomationverify.codeplex.com/)dei test.

## <a name="improved-multi-language-user-interface-support-and-linguistic-services"></a>Miglioramento del supporto multilingue Interfaccia utente e dei servizi linguistici

Windows 7 offre agli sviluppatori un metodo standard per preparare le applicazioni per il mercato internazionale offrendo un supporto migliorato per l'interfaccia utente multilingue e servizi linguistici che possono essere utilizzati nelle proprie applicazioni.

Servizi linguistici estesi è una nuova funzionalità di Windows 7 che consente agli sviluppatori di usare lo stesso piccolo set di API per sfruttare un'ampia gamma di funzionalità linguistiche avanzate. Usando i Servizi linguistici estesiAPIs in Windows 7, gli sviluppatori possono rilevare automaticamente la lingua di qualsiasi parte del testo Unicode e usare queste informazioni per consentire ai clienti di tutto il mondo di scegliere un'esperienza utente più intelligente. Servizi linguistici estesi offre anche il supporto incorporato per la traslitterazione che converte il testo da un sistema di scrittura a un altro. Ad esempio, gli sviluppatori possono ora convertire automaticamente il testo tra il cinese semplificato e il cinese tradizionale per consentire alle persone di comunicare tra loro attraverso limiti linguistici. Usando i Servizi linguistici estesiARTI, gli sviluppatori potranno usare i servizi linguistici estesi esistenti e scegliere nuovi servizi in futuro senza apprendere nuovo codice. Vedere [Servizi linguistici estesi.](../intl/extended-linguistic-services.md)

 

 
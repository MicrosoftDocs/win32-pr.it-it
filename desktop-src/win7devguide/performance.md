---
title: Prestazioni (Guida per sviluppatori di Windows 7)
description: Windows 7 ottimizza la scalabilità e l'efficienza energetica hardware mantenendo al tempo stesso prestazioni elevate.
ms.assetid: db48aa8f-749e-4a56-8a91-ac9b81d6e8c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 752f66e80265bf7d6b3ea26e7baabdc6550ce921
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104339942"
---
# <a name="performance-windows-7-developer-guide"></a>Prestazioni (Guida per sviluppatori di Windows 7)

Windows 7 ottimizza la scalabilità e l'efficienza energetica hardware mantenendo al tempo stesso prestazioni elevate. L'efficienza energetica è migliorata grazie a un'attività in background ridotta e a un nuovo supporto per l'avvio del trigger dei servizi di sistema. Windows 7 offre anche miglioramenti nel kernel di Windows che consentono alle applicazioni e ai servizi di ridimensionarsi in modo efficiente tra le piattaforme. Le prestazioni di molte funzionalità e API sono migliorate in Windows 7 rispetto a Windows Vista. Ad esempio, le prestazioni dei driver sui server sono ottimizzate dalle nuove API della topologia in modalità utente e kernel. Il rendering della grafica è molto più semplice e rapido. Anche le prestazioni di accessibilità sono molto più veloci di quelle precedenti.

## <a name="building-power-efficient-applications"></a>Compilazione di applicazioni Power-Efficient

La creazione di applicazioni efficienti a consumo energetico che sfruttano le tecnologie di risparmio energia più recenti è una sfida significativa che gli sviluppatori stanno affrontando oggi. In genere, il processore e i produttori di dispositivi ottengono tutte le attenzioni che vengono misurate e valutate in base alle ultime offerte. Tuttavia, una singola applicazione può facilmente impedire che la generazione più recente di hardware renda conto del potenziale di efficienza energetica. Ad esempio, una singola applicazione che aumenta la risoluzione del timer della piattaforma può ridurre il 10 percento della durata della batteria.

Le operazioni estese sull'alimentazione a batteria e l'uso di tecnologie efficienti energetiche sono requisiti essenziali per gli sviluppatori attuali. Windows 7 riduce notevolmente il numero di attività eseguite dal sistema operativo che impediscono l'utilizzo di modalità di risparmio energia. Supporta inoltre il trigger-avvio dei servizi di sistema per consentire ai processori di diventare inattivi più spesso e rimanere inattivi più a lungo, riducendo così il consumo di energia. Inoltre, Windows 7 sfrutta i vantaggi dell'hardware più recente a consumo energetico, tra cui schede di rete, dispositivi di archiviazione e schede grafiche.

Windows 7 fornisce l'infrastruttura e gli strumenti che consentono agli sviluppatori di determinare con facilità l'effetto energetico delle proprie applicazioni. Un set di callback di evento consente alle applicazioni di ridurre l'attività quando il sistema è alimentato a batteria e viene scalato automaticamente quando il sistema si trova in una *rete elettrica.* Per le applicazioni che coinvolgono un processo in background o un servizio, Windows 7 offre una nuova infrastruttura per abilitare automaticamente le attività in background quando più appropriato per ottimizzare l'efficienza energetica. Vedere Panoramica di [whdc performance Central](https://www.microsoft.com/whdc/system/sysperf/default.mspx) and [Power Management in Windows 7](https://www.climatesaverscomputing.org/wordpress/wp-content/uploads/2011/06/Power_Management_in_Windows_7_Overview.pdf).

## <a name="service-control-manager"></a>Gestione controllo servizi

Windows 7Service Control Manager (SCM) è stato esteso in modo da consentire l'avvio e l'arresto automatici di un servizio quando si verifica un evento di sistema o un trigger specifico nel sistema. Funzionalità di avvio trigger rimuovere la necessità che i servizi vengano avviati automaticamente all'avvio del computer e quindi eseguire il polling o attendere che si verifichi un evento, ad esempio l'arrivo del dispositivo. Gli eventi trigger comuni per i servizi includono:

-   Arrivo interfaccia di classe dispositivo: avviare un servizio solo quando è presente un determinato tipo di dispositivo o collegato al sistema.
-   Aggiunta a un dominio: avviare un servizio solo se il sistema è aggiunto a un dominio Windows.
-   Modifica di criteri di gruppo: avviare un servizio automaticamente quando i criteri di gruppo vengono aggiornati nel sistema.
-   Indirizzo IP arrivo: avviare un servizio solo quando il sistema è connesso alla rete.

Gli sviluppatori di software possono usare i tipi di trigger predefiniti per Windows 7 e le opzioni di configurazione per abilitare la funzionalità di avvio del trigger. Windows 7SCM espone un nuovo set di API che consentono a un servizio di registrarsi per eventi trigger personalizzati specifici. (Vedere [Gestione controllo servizi](../services/service-control-manager.md)).

## <a name="windows-troubleshooting-platform"></a>Piattaforma di risoluzione dei problemi Windows

Windows 7 offre una piattaforma di risoluzione dei problemi completa ed estendibile che usa un meccanismo basato su PowerShell per la risoluzione dei problemi e la risoluzione dei problemi. I componenti principali della piattaforma di risoluzione dei problemi includono un pacchetto di risoluzione dei problemi, un motore per la risoluzione dei problemi e la procedura guidata per la risoluzione dei problemi Troubleshooting Pack è una raccolta di script di PowerShell e di metadati pertinenti. Il motore di risoluzione dei problemi avvia un runtime di PowerShell per eseguire un pacchetto di risoluzione dei problemi ed espone un set di interfacce per controllare la risoluzione dei problemi di esecuzione del pacchetto.

La procedura guidata per la risoluzione dei problemi offre un'esperienza coerente per la risoluzione dei problemi relativi ai pacchetti, comunicando con il motore di risoluzione dei problemi per risolvere i problemi specificati in un pacchetto di risoluzione dei problemi. L'esecuzione di un pacchetto di risoluzione dei problemi può essere controllata anche tramite un set di *cmdlet* di PowerShell.

La piattaforma per la risoluzione dei problemi si integra perfettamente con il centro soluzioni 7PC di Windows, consentendo ad altre applicazioni di eseguire la diagnostica in modo analogo come parte del regime di gestione dei PC. La piattaforma per la risoluzione dei problemi può essere configurata dai professionisti IT tramite *criteri di gruppo* per l'utilizzo all'interno dell'organizzazione. è inoltre disponibile un Toolkit per la risoluzione dei problemi di Windows che consente agli sviluppatori di creare pacchetti di risoluzione dei problemi. Vedere la pagina relativa alla piattaforma per la [risoluzione dei problemi di Windows](/previous-versions/windows/desktop/wintt/windows-troubleshooting-toolkit-portal).

![risoluzione dei problemi dell'interfaccia utente della piattaforma](images/windows7-devguide-troubleshoot.jpg)

La piattaforma per la risoluzione dei problemi si integra facilmente con il centro soluzioni Windows 7PC

 

 

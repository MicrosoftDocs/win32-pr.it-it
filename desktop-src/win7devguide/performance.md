---
title: Prestazioni (Windows 7 Guida per sviluppatori)
description: Windows 7 ottimizza l'efficienza e la scalabilità dell'hardware mantenendo al tempo stesso prestazioni elevate.
ms.assetid: db48aa8f-749e-4a56-8a91-ac9b81d6e8c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5636b6cb7178fa660381196f44b811c905478c1bcd31e0580ea631955b13c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118032054"
---
# <a name="performance-windows-7-developer-guide"></a>Prestazioni (Windows 7 Guida per sviluppatori)

Windows 7 ottimizza l'efficienza e la scalabilità dell'hardware mantenendo al tempo stesso prestazioni elevate. L'efficienza energetica è migliorata grazie alla riduzione delle attività in background e al nuovo supporto per l'avvio del trigger dei servizi di sistema. Windows 7 offre anche miglioramenti nel kernel Windows che consentono alle applicazioni e ai servizi di scalare in modo efficiente tra le piattaforme. Le prestazioni di molte funzionalità e API sono migliorate in Windows 7 rispetto Windows Vista. Ad esempio, le prestazioni dei driver nei server sono ottimizzate dalle nuove API di topologia in modalità utente e kernel. Il rendering della grafica è notevolmente più uniforme e veloce. Anche le prestazioni di accessibilità sono notevolmente più veloci rispetto a prima.

## <a name="building-power-efficient-applications"></a>Compilazione Power-Efficient applicazioni

La creazione di applicazioni efficienti dal punto di vista energetico che sfruttano le tecnologie di risparmio energia più recenti è una sfida significativa che gli sviluppatori devono affrontare oggi. In genere, i produttori di processori e dispositivi ottengono tutta l'attenzione quando le offerte più recenti vengono misurate e valutate. Tuttavia, una singola applicazione può facilmente impedire all'ultima generazione di hardware di realizzare il proprio potenziale di efficienza energetica. Ad esempio, una singola applicazione che aumenta la risoluzione del timer della piattaforma può ridurre la durata della batteria del 10%.

Il funzionamento esteso dell'alimentazione a batteria e l'uso di tecnologie efficienti dal punto di vista energetico sono requisiti chiave per gli sviluppatori di oggi. Windows 7 riduce notevolmente il numero di attività eseguite dal sistema operativo che impediscono l'uso delle modalità di risparmio energia. Supporta anche l'avvio trigger dei servizi di sistema per consentire ai processori di diventare inattivi più spesso e rimanere inattivi più a lungo, con una riduzione del consumo di energia. Inoltre, Windows 7 sfrutta l'hardware più efficiente dal punto di vista energetico, tra cui schede di rete, dispositivi di archiviazione e schede grafiche.

Windows 7 offre l'infrastruttura e gli strumenti che semplificano agli sviluppatori la determinazione dell'impatto energetico delle applicazioni. Un set di callback di eventi consente alle applicazioni di ridurre l'attività quando il sistema è alimentato a batteria e di aumentare automaticamente le prestazioni quando il sistema è alimentato *da* ca. Per le applicazioni che coinvolgono un processo o un servizio in background, Windows 7 offre una nuova infrastruttura per abilitare automaticamente le attività in background quando più appropriato per ottimizzare l'efficienza energetica. Vedere LA [PANORAMICA DI WHDC Performance Central](https://www.microsoft.com/whdc/system/sysperf/default.mspx) and Power Management in Windows 7 Overview (Panoramica di WHDC Performance Central e Power [Management)](https://www.climatesaverscomputing.org/wordpress/wp-content/uploads/2011/06/Power_Management_in_Windows_7_Overview.pdf)

## <a name="service-control-manager"></a>Gestione controllo servizi

Il Windows 7Servizio Control Manager (SCM) è stato esteso in modo che un servizio possa essere avviato e arrestato automaticamente quando si verifica un evento di sistema specifico, o trigger, nel sistema. Le funzionalità di avvio trigger eliminano la necessità di avviare automaticamente i servizi all'avvio del computer e quindi di eseguire il polling o attendere che si verifichi un evento, ad esempio l'arrivo del dispositivo. Gli eventi trigger comuni per i servizi includono:

-   Arrivo dell'interfaccia di classe del dispositivo: avviare un servizio solo quando un determinato tipo di dispositivo è presente o collegato nel sistema.
-   Aggiunta a un dominio: avviare un servizio solo se il sistema è aggiunto a un Windows dominio.
-   Modifica di Criteri di gruppo: avviare automaticamente un servizio quando i criteri di gruppo vengono aggiornati nel sistema.
-   Arrivo dell'indirizzo IP: avviare un servizio solo quando il sistema è connesso alla rete.

Gli sviluppatori di software possono usare i tipi di trigger predefiniti per Windows 7 e le opzioni di configurazione per abilitare la funzionalità trigger-start. La Windows 7SCM espone un nuovo set di API che consentono a un servizio di registrarsi per eventi trigger personalizzati specifici. Vedere [Gestione controllo servizi.](../services/service-control-manager.md)

## <a name="windows-troubleshooting-platform"></a>Piattaforma di risoluzione dei problemi Windows

Windows 7 offre una piattaforma di risoluzione dei problemi completa ed estendibile che usa un meccanismo basato su PowerShell per risolvere i problemi. I componenti principali della piattaforma di risoluzione dei problemi includono un pacchetto di risoluzione dei problemi, un motore di risoluzione dei problemi e una procedura guidata per la risoluzione dei problemi. Il pacchetto di risoluzione dei problemi è una raccolta di script di PowerShell e metadati pertinenti. Il motore di risoluzione dei problemi avvia un runtime di PowerShell per eseguire un pacchetto di risoluzione dei problemi ed espone un set di interfacce per controllare la risoluzione dei problemi di esecuzione del pacchetto.

La procedura guidata per la risoluzione dei problemi offre un'esperienza coerente tra i pacchetti di risoluzione dei problemi, comunicando con il motore di risoluzione dei problemi per risolvere i problemi specificati in un pacchetto di risoluzione dei problemi. L'esecuzione di un pacchetto di risoluzione dei problemi può essere controllata anche tramite un set di *commandlet di* PowerShell.

La piattaforma di risoluzione dei problemi si integra perfettamente con il centro soluzioni Windows 7PC, consentendo ad altre applicazioni di eseguire la diagnostica in modo simile come parte del proprio regime di gestione dei PC. La piattaforma di risoluzione dei problemi è configurabile dai professionisti IT tramite *Criteri di gruppo* per l'uso all'interno dell'azienda e è disponibile anche un Toolkit di risoluzione dei problemi Windows che consente agli sviluppatori di creare pacchetti di risoluzione dei problemi. Vedere la [Windows risoluzione dei problemi della piattaforma](/previous-versions/windows/desktop/wintt/windows-troubleshooting-toolkit-portal).

![risoluzione dei problemi relativi all'interfaccia utente della piattaforma](images/windows7-devguide-troubleshoot.jpg)

La piattaforma di risoluzione dei problemi si integra perfettamente con il centro soluzioni Windows 7PC

 

 

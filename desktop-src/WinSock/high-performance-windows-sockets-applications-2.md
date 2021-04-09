---
description: I componenti di rete di Microsoft Windows sono stati sviluppati per prestazioni e scalabilità.
ms.assetid: 2160b93e-c126-4592-972c-d9cc14eec745
title: Applicazioni Windows Sockets a prestazioni elevate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0496198ef3a8f11e6a840fd75d0083899d23d5a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049486"
---
# <a name="high-performance-windows-sockets-applications"></a>Applicazioni Windows Sockets a prestazioni elevate

I componenti di rete di Microsoft Windows sono stati sviluppati per prestazioni e scalabilità. Questo consente alle applicazioni di ottimizzare la larghezza di banda di rete disponibile. Windows Sockets e lo stack di protocolli TCP/IP di Windows sono stati ottimizzati e ottimizzati. Di conseguenza, le applicazioni Windows scritte correttamente possono ottenere velocità effettiva e prestazioni eccezionali, come illustrato nei seguenti fatti:

-   Windows è in grado di gestire più di 200.000 connessioni TCP simultanee.
-   In un test eseguito da SPECWeb96, Internet Information Server su Windows ha gestito oltre 25.000 richieste HTTP al secondo.
-   Windows ha impostato un record di trasmissione di oltre 750Mbps in una rete Gigabit transcontinentale costituita da 10 hop.

Questi risultati mostrano che Windows TCP/IP elabora i dati molto rapidamente. Molte applicazioni, tuttavia, non sfruttano le funzionalità delle prestazioni Windows, TCP/IP e Windows Sockets, perché inconsapevolmente implementano tecniche che ostacolano le prestazioni.

In questa guida si apprenderà come identificare gli errori di programmazione comuni e come evitarli. Si apprenderanno quindi le tecniche che consentono alle applicazioni Windows Sockets di funzionare in modo ottimale. Questa guida è presentata in sei sezioni. L'ordine delle sezioni è intenzionale. per ottenere il massimo da questa guida, leggerlo nell'ordine. Nella tabella seguente vengono forniti i collegamenti a ogni sezione, oltre a una breve descrizione di ogni argomento.



| Argomento                                                                                            | Descrizione                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Terminologia di rete](network-terminology-2.md)                                                 | Definisce la terminologia e le metriche di rete necessarie per comprendere le prestazioni di un'applicazione di rete.                                     |
| [Dimensioni prestazioni](performance-dimensions-2.md)                                           | Illustra le dimensioni delle prestazioni che influiscono sulle prestazioni di rete percepite ed effettive di un'applicazione.                                        |
| [Caratteristiche TCP/IP](tcp-ip-characteristics-2.md)                                           | Definisce le caratteristiche del protocollo TCP/IP che possono causare problemi di prestazioni per un'applicazione scritta in modo non corretto.                                     |
| [Comportamento dell'applicazione](application-behavior-2.md)                                               | Viene illustrato come riconoscere i segni di un'applicazione di rete con prestazioni scarse.                                                                     |
| [Miglioramento di un'applicazione lenta](improving-a-slow-application-2.md)                               | Fornisce esempi di problemi di progettazione di applicazioni che contribuiscono a un'applicazione con prestazioni scarse e apporta modifiche al codice per migliorare le prestazioni. |
| [Procedure consigliate per le applicazioni interattive](best-practices-for-interactive-applications-2.md) | Vengono elencate le procedure consigliate da utilizzare per lo sviluppo di applicazioni di rete interattive ottimali.                                                         |



 

 

 




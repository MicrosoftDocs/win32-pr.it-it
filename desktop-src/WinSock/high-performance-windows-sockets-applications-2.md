---
description: Microsoft Windows componenti di rete sono stati sviluppati per prestazioni e scalabilità.
ms.assetid: 2160b93e-c126-4592-972c-d9cc14eec745
title: Applicazioni socket Windows prestazioni elevate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9df2b050ac45bf0bf7788a356f4fdba98197d481dd99180f99f7dbf8cdfb5b7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117927870"
---
# <a name="high-performance-windows-sockets-applications"></a>Applicazioni socket Windows prestazioni elevate

Microsoft Windows componenti di rete sono stati sviluppati per prestazioni e scalabilità. Ciò consente alle applicazioni di ottimizzare la larghezza di banda di rete disponibile. Windows I socket e lo Windows stack del protocollo TCP/IP sono stati ottimizzati e semplificati. Di conseguenza, le applicazioni Windows correttamente scritte possono ottenere prestazioni e velocità effettiva eccezionali, come illustrato nei fatti seguenti:

-   Windows è in grado di eseguire più di 200.000 connessioni TCP simultanee.
-   In un test eseguito da SPECWeb96, Internet Information Server su Windows ha eseguito più di 25.000 richieste HTTP al secondo.
-   Windows un record di trasmissione di oltre 750 Mbps in una rete gigabit transcontinentale costituita da 10 hop.

Questi obiettivi illustrano che Windows TCP/IP elabora i dati molto rapidamente. Molte applicazioni, tuttavia, non sfruttano le funzionalità di prestazioni Windows, TCP/IP e Windows Sockets perché implementano inconsapevolmente tecniche che ostacolano le prestazioni.

In questa guida si apprenderà come identificare gli errori di programmazione comuni e come evitarli. Si apprenderanno quindi le tecniche che consentono alle Windows Sockets di ottenere prestazioni ottimali. Questa guida è presentata in sei sezioni. L'ordine delle sezioni è intenzionale. Per ottenere il massimo da questa guida, leggerla nell'ordine indicato. La tabella seguente include collegamenti a ogni sezione e una breve descrizione di ogni argomento.



| Argomento                                                                                            | Descrizione                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Terminologia della rete](network-terminology-2.md)                                                 | Definisce la terminologia e le metriche di rete necessarie per comprendere le prestazioni di un'applicazione di rete.                                     |
| [Dimensioni delle prestazioni](performance-dimensions-2.md)                                           | Vengono illustrate le dimensioni delle prestazioni che influiscono sulle prestazioni di rete percepite ed effettive di un'applicazione.                                        |
| [Caratteristiche TCP/IP](tcp-ip-characteristics-2.md)                                           | Definisce le caratteristiche del protocollo TCP/IP che possono causare problemi di prestazioni per un'applicazione scritta in modo non necessario.                                     |
| [Comportamento dell'applicazione](application-behavior-2.md)                                               | Spiega come riconoscere i segnali di un'applicazione di rete con prestazioni scarse.                                                                     |
| [Miglioramento di un'applicazione lenta](improving-a-slow-application-2.md)                               | Vengono forniti esempi di problemi di progettazione delle applicazioni che contribuiscono a un'applicazione con prestazioni scarse e vengono apportate modifiche al codice per migliorare le prestazioni. |
| [Procedure consigliate per le applicazioni interattive](best-practices-for-interactive-applications-2.md) | Elenca le procedure consigliate da usare per lo sviluppo di applicazioni di rete interattive ottimali.                                                         |



 

 

 




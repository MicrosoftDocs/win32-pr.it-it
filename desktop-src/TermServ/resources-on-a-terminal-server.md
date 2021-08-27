---
title: Risorse in un server host Desktop remoto sessione
description: Più utenti possono accedere contemporaneamente a un singolo server Host sessione Desktop remoto(Host sessione Desktop remoto), condividendo le risorse hardware e software del server.
ms.assetid: ab193a9f-7424-42bf-8cea-28628096edc6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46ba87ea7569b8ef9daeccb54890bb8882d423621b414fdd8df28c0c4e67b750
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009191"
---
# <a name="resources-on-a-remote-desktop-session-host-server"></a>Risorse in un server host Desktop remoto sessione

In un Servizi Desktop remoto, più utenti possono accedere contemporaneamente a un singolo server Host sessione Desktop remoto (host sessione Desktop remoto) (precedentemente noto come server terminal). Di conseguenza, gli utenti condividono le risorse hardware e software del server, che possono creare le seguenti aree di problemi:

-   Tempo CPU. Ogni utente ha un ambiente desktop e può eseguire tutte le applicazioni disponibili per tale desktop. Tuttavia, tutte le applicazioni eseguite da tutti gli utenti si contendono le risorse centrali della CPU disponibili nel server Host sessione Desktop remoto. Se un utente esegue un'applicazione a elevato utilizzo di CPU scritta in modo non ottimale, altri utenti potrebbero verificarsi una perdita di prestazioni visibile.
-   Accesso al disco. Gli utenti si contendono l'accesso alle applicazioni e ai file di programma correlati. Inoltre, gli utenti si contendono l'accesso al disco dal sistema operativo server, ad esempio il caricamento di DLL o lo scambio di memoria tra il file di paging e la memoria fisica.
-   Memoria ad accesso casuale (RAM). Ogni applicazione eseguita da ogni utente è in contesa per le risorse di RAM disponibili nel server Host sessione Desktop remoto. Se un utente esegue un'applicazione a elevato utilizzo di memoria, altri utenti potrebbero verificarsi una perdita di prestazioni.
-   Accesso alla rete. L'accesso alla rete è essenziale in un ambiente Servizi Desktop remoto perché tutte le attività desktop, ovvero output grafico e input da mouse/tastiera, passano attraverso i collegamenti di rete tra il desktop client e il server. Inoltre, le applicazioni degli utenti in esecuzione nel server Host sessione Desktop remoto si contendono l'accesso ad altre risorse di rete.
-   Hardware del server. I componenti hardware come CD-ROM, unità disco floppy, porte seriali e porte parallele sono spesso basati su server, non su client. La condivisione di questi componenti tradizionalmente non condivisi crea nuove considerazioni per gli utenti e per le applicazioni che accedono a questi componenti hardware. Per altre informazioni, vedere [Peripheral Hardware Guidelines](peripheral-hardware-guidelines.md).
-   Accesso a oggetti e risorse globali. In un Servizi Desktop remoto, gli utenti non eseguono singole copie di Windows: alcuni dei moduli principali vengono clonati, ma i moduli rimanenti vengono condivisi tra gli utenti. Di conseguenza, gli utenti sono in competizione per l'accesso al Registro di sistema, al file di paging, ai servizi di sistema e ad altri oggetti e risorse globali.

Molti dei punti di contenti precedenti possono essere mitigati ridimensionando il server Host sessione Desktop remoto con risorse sufficienti di CPU, memoria e disco per gestire la richiesta del client. Ad esempio, una configurazione con più processori può ottimizzare la disponibilità della CPU. La disponibilità della memoria può essere ottimizzata installando memoria fisica aggiuntiva. L'aumento dei limiti di memoria per le edizioni Enterprise, Datacenter o a 64 bit di Windows Server può essere utile. Infine, le prestazioni di accesso al disco possono essere ottimizzate configurando più canali e distribuendo i carichi del sistema operativo e dell'applicazione in unità fisiche diverse. La configurazione corretta di un server Host sessione Desktop remoto è un elemento fondamentale delle prestazioni percepite dell'applicazione.

Anche se il ridimensionamento dell'hardware è una parte importante della creazione di un ambiente Servizi Desktop remoto scalabile, le considerazioni sul software sono ugualmente importanti. In realtà, l'ottimizzazione di un'applicazione spesso può fare molto per ridurre la concorrenza delle risorse e migliorare le prestazioni percepite dell'applicazione.

Per altre informazioni sull'ambiente Servizi Desktop remoto, vedere gli argomenti seguenti:

-   [Servizi Desktop remoto di programmazione](terminal-services-programming-guidelines.md)
-   [Rilevamento dell'ambiente Servizi Desktop remoto](detecting-the-terminal-services-environment.md)
-   [Rilevamento dell'installazione Servizi Desktop remoto ruolo di distribuzione](detecting-whether-terminal-services-is-installed.md)
-   [Servizi Desktop remoto sessioni](terminal-services-sessions.md)

 

 





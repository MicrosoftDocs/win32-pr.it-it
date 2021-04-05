---
title: Risorse in un server di host sessione Desktop remoto
description: Più utenti possono accedere simultaneamente a un singolo server di host sessione Desktop remoto (host sessione Desktop remoto), condividendo le risorse hardware e software del server.
ms.assetid: ab193a9f-7424-42bf-8cea-28628096edc6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81e099787ae3d0acd9028405b244f7fbc2e2117e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711419"
---
# <a name="resources-on-a-remote-desktop-session-host-server"></a>Risorse in un server di host sessione Desktop remoto

In un ambiente di Servizi Desktop remoto, più utenti possono accedere simultaneamente a un singolo server di host sessione Desktop remoto (host sessione Desktop remoto), noto in precedenza come Terminal Server. Di conseguenza, gli utenti condividono le risorse hardware e software del server, che può creare le seguenti aree di contesa:

-   Tempo CPU. Ogni utente dispone di un ambiente desktop ed è in grado di eseguire tutte le applicazioni disponibili per il desktop. Tuttavia, tutte le applicazioni eseguite da tutti gli utenti si contendono le risorse della CPU centrale disponibili sul server Host sessione Desktop remoto. Se un utente esegue un'applicazione con utilizzo intensivo della CPU, altri utenti potrebbero subire una perdita di prestazioni visibile.
-   Accesso al disco. Gli utenti si contendono l'accesso alle applicazioni e ai file di programma correlati. Inoltre, gli utenti si contendono gli accessi al disco dal sistema operativo server, ad esempio il caricamento di dll o lo scambio di memoria tra il file di paging e la memoria fisica.
-   Memoria ad accesso casuale (RAM). Ogni applicazione eseguita da ogni utente sta tendendo alle risorse RAM disponibili nel server Host sessione Desktop remoto. Se un utente esegue un'applicazione con utilizzo intensivo della memoria, altri utenti potrebbero subire una perdita di prestazioni.
-   Accesso alla rete. L'accesso alla rete è essenziale in un ambiente Servizi Desktop remoto perché tutte le attività desktop, ovvero output grafico e input da tastiera e mouse, passano attraverso i collegamenti di rete tra il desktop client e il server. Inoltre, le applicazioni degli utenti in esecuzione nel server Host sessione Desktop remoto contendono l'accesso ad altre risorse di rete.
-   Hardware del server. I componenti hardware, ad esempio CD-ROM, unità disco floppy, porte seriali e porte parallele, sono spesso basati su server, non su client. La condivisione di questi componenti tradizionalmente non condivisi crea nuove considerazioni per gli utenti e per le applicazioni che accedono a questi componenti hardware. Per ulteriori informazioni, vedere [linee guida hardware periferiche](peripheral-hardware-guidelines.md).
-   Accesso a oggetti e risorse globali. In un ambiente di Servizi Desktop remoto, gli utenti non eseguono copie singole di Windows: alcuni dei moduli principali vengono clonati, ma i moduli rimanenti sono condivisi tra gli utenti. Pertanto, gli utenti sono in competizione per l'accesso al registro di sistema, il file di paging, i servizi di sistema e altri oggetti e risorse globali.

Molti dei punti precedenti della contesa possono essere attenuati ridimensionando il server Host sessione Desktop remoto con CPU, memoria e risorse disco sufficienti per gestire la richiesta del client. Una configurazione a più processori, ad esempio, può ottimizzare la disponibilità della CPU. È possibile ingrandire la disponibilità di memoria installando memoria fisica aggiuntiva (i limiti di memoria maggiori per le edizioni Enterprise, Datacenter o 64 bit di Windows Server possono essere utili). Infine, le prestazioni di accesso al disco possono essere ingrandite configurando più canali e distribuendo i carichi del sistema operativo e dell'applicazione in unità fisiche diverse. La corretta configurazione di un server Host sessione Desktop remoto è un elemento fondamentale delle prestazioni percepite dell'applicazione.

Sebbene il dimensionamento hardware sia una parte importante della creazione di un ambiente Servizi Desktop remoto scalabile, le considerazioni sul software sono ugualmente importanti. In realtà, l'ottimizzazione di un'applicazione spesso può fare molto per ridurre la concorrenza delle risorse e migliorare le prestazioni percepite dell'applicazione.

Per ulteriori informazioni sull'ambiente Servizi Desktop remoto, vedere gli argomenti seguenti:

-   [Linee guida per la programmazione Servizi Desktop remoto](terminal-services-programming-guidelines.md)
-   [Rilevamento dell'ambiente Servizi Desktop remoto](detecting-the-terminal-services-environment.md)
-   [Rilevamento dell'installazione del ruolo Servizi Desktop remoto](detecting-whether-terminal-services-is-installed.md)
-   [Sessioni di Servizi Desktop remoto](terminal-services-sessions.md)

 

 





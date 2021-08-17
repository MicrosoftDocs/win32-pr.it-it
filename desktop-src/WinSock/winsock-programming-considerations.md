---
description: Windows Sockets 2 estende la funzionalità di Windows Sockets 1.1 in diverse aree. La tabella seguente riepiloga alcune delle principali modifiche apportate alle funzionalità.
ms.assetid: 26bfb614-5700-44d3-b4fb-1002d757d15e
title: Considerazioni sulla programmazione winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8451601f92f0fbf7b85532fc5a63479fe2bec26adc1984c74fc1cd7d750a04aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739860"
---
# <a name="winsock-programming-considerations"></a>Considerazioni sulla programmazione winsock

Windows Sockets 2 estende la funzionalità di Windows Sockets 1.1 in diverse aree. La tabella seguente riepiloga alcune delle principali modifiche apportate alle funzionalità.



| Funzionalità                                                                                                           | Descrizione                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Windows Architettura di Sockets 2](windows-sockets-2-architecture-2.md)                                             | Descrizione dell'architettura Windows Sockets 2.                                                                                                                                                                                                                                           |
| [Handle di socket](socket-handles-2.md)                                                                             | Un handle socket può facoltativamente essere un handle di file in Windows Sockets 2. È possibile usare handle socket con funzioni di I/O Windows file standard.                                                                                                                                           |
| [Accesso simultaneo a più protocolli di trasporto](simultaneous-access-to-multiple-transport-protocols-2.md)   | Consente a un'applicazione di usare l'interfaccia socket nota per ottenere l'accesso simultaneo a una serie di protocolli di trasporto installati.                                                                                                                                                        |
| [Risoluzione dei nomi indipendente dal protocollo](protocol-independent-name-resolution-2.md)                                 | Include un set standardizzato di funzioni per l'esecuzione di query e l'uso di una miriade di domini di risoluzione dei nomi attualmente esistenti ,ad esempio DNS, SAP e X.500.                                                                                                                                  |
| [Multicast e multipoint indipendenti dal protocollo](protocol-independent-multicast-and-multipoint-2.md)               | Le applicazioni individuano il tipo di funzionalità multipoint o multicast fornite da un trasporto e usano queste funzionalità in modo generico.                                                                                                                                                     |
| [I/O sovrapposto](overlapped-i-o-and-event-objects-2.md)                                                           | Incorpora il paradigma sovrapposto per l'I/O socket seguendo il modello stabilito in Windows ambienti.                                                                                                                                                                                   |
| [I/O a dispersione/raccolta](scatter-gather-i-o-2.md)                                                                     | Incorpora le funzionalità di dispersione/raccolta con il paradigma sovrapposto per l'I/O del socket, seguendo il modello stabilito in Windows virtuali.                                                                                                                                                 |
| [Qualità del servizio](flow-specification-quality-of-service-2.md) (QoS)                                            | Stabilisce le convenzioni usate dalle applicazioni per negoziare i livelli di servizio necessari per parametri quali larghezza di banda e latenza. Altri miglioramenti correlati a QoS includono meccanismi per le estensioni quality of service specifiche della rete.                                                         |
| [Meccanismo di estensione specifico del provider](provider-specific-extension-mechanism-2.md)                               | La [**funzione WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) consente ai provider di servizi di offrire estensioni di funzionalità specifiche del provider.                                                                                                                                                                           |
| [Socket condivisi](shared-sockets-2.md)                                                                             | La [**funzione WSADuplicateSocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa) è stata introdotta per abilitare la condivisione dei socket tra processi.                                                                                                                                                                       |
| [Configurazione e rimozione della connessione](connection-setup-and-teardown-2.md)                                               | Un'applicazione può ottenere informazioni sul chiamante, ad esempio l'identificatore del chiamante e la qualità del servizio prima di decidere se accettare una richiesta di connessione in ingresso. È anche possibile (per i protocolli che lo supportano) scambiare dati utente tra gli endpoint in fase di rimozione della connessione. |
| [Arresto normale, opzioni Linger e chiusura socket](graceful-shutdown-linger-options-and-socket-closure-2.md) | Un'applicazione ha diverse opzioni per arrestare una connessione socket (sequenza di arresto).                                                                                                                                                                                                  |
| [Dati fuori banda indipendenti dal protocollo](protocol-independent-out-of-band-data-2.md)                               | L'astrazione del socket di flusso include la nozione di dati fuori banda (OOB).                                                                                                                                                                                                                   |
| [Funzionalità di debug e traccia](debug-and-trace-facilities-2.md)                                                     | Windows Sockets 2 supporta una versione appositamente concepita del32.dll Ws2 \_ e una DLL di debug/traccia separata.                                                                                                                                                                                      |
| [Windows Problemi di compatibilità dei socket](windows-sockets-compatibility-issues-2.md)                                 | Windows Sockets 2 continua a supportare tutte le semantiche e le chiamate di funzione Windows Sockets 1.1, ad eccezione di quelle che gestiscono pseudo-blocco.                                                                                                                                              |
| [Gestione degli errori Winsock](handling-winsock-errors.md)                                                             | Modalità di recupero e gestione degli errori winsock da parte di un'applicazione.                                                                                                                                                                                                                             |



 

 

 




---
description: Windows Sockets 2 estende le funzionalità di Windows Sockets 1,1 in diverse aree. Nella tabella seguente sono riepilogate alcune delle principali modifiche apportate alle funzionalità.
ms.assetid: 26bfb614-5700-44d3-b4fb-1002d757d15e
title: Considerazioni sulla programmazione Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfaee2cd04f03afe050ca539190b51e66c0abff9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130402"
---
# <a name="winsock-programming-considerations"></a>Considerazioni sulla programmazione Winsock

Windows Sockets 2 estende le funzionalità di Windows Sockets 1,1 in diverse aree. Nella tabella seguente sono riepilogate alcune delle principali modifiche apportate alle funzionalità.



| Funzionalità                                                                                                           | Descrizione                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Architettura di Windows Sockets 2](windows-sockets-2-architecture-2.md)                                             | Descrizione dell'architettura di Windows Sockets 2.                                                                                                                                                                                                                                           |
| [Handle socket](socket-handles-2.md)                                                                             | Un handle di socket può facoltativamente essere un handle di file in Windows Sockets 2. È possibile utilizzare handle di socket con le funzioni di I/O dei file di Windows standard.                                                                                                                                           |
| [Accesso simultaneo a più protocolli di trasporto](simultaneous-access-to-multiple-transport-protocols-2.md)   | Consente a un'applicazione di utilizzare l'interfaccia socket familiare per ottenere l'accesso simultaneo a diversi protocolli di trasporto installati.                                                                                                                                                        |
| [Risoluzione dei nomi indipendente dal protocollo](protocol-independent-name-resolution-2.md)                                 | Include un set standardizzato di funzioni per l'esecuzione di query e l'utilizzo di innumerevoli domini di risoluzione dei nomi attualmente esistenti, ad esempio DNS, SAP e X. 500.                                                                                                                                  |
| [Multicast e MultiPoint indipendenti dal protocollo](protocol-independent-multicast-and-multipoint-2.md)               | Le applicazioni individuano il tipo di funzionalità multipoint o multicast fornite da un trasporto e utilizzano queste funzioni in modo generico.                                                                                                                                                     |
| [I/O sovrapposti](overlapped-i-o-and-event-objects-2.md)                                                           | Incorpora il paradigma sovrapposto per I/O socket che segue il modello stabilito negli ambienti Windows.                                                                                                                                                                                   |
| [I/O a dispersione/raccolta](scatter-gather-i-o-2.md)                                                                     | Incorpora le funzionalità di dispersione/raccolta con il paradigma sovrapposto per I/O socket, seguendo il modello stabilito negli ambienti Windows.                                                                                                                                                 |
| [Qualità del servizio](flow-specification-quality-of-service-2.md) (QoS)                                            | Stabilisce le convenzioni utilizzate dalle applicazioni per negoziare i livelli di servizio necessari per parametri quali larghezza di banda e latenza. Altri miglioramenti correlati a QoS includono meccanismi per la qualità delle estensioni del servizio specifiche per la rete.                                                         |
| [Meccanismo di estensione specifico del provider](provider-specific-extension-mechanism-2.md)                               | La funzione [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) consente ai provider di servizi di offrire estensioni di funzionalità specifiche del provider.                                                                                                                                                                           |
| [Socket condivisi](shared-sockets-2.md)                                                                             | La funzione [**WSADuplicateSocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa) è stata introdotta per abilitare la condivisione dei socket tra i processi.                                                                                                                                                                       |
| [Configurazione della connessione e teardown](connection-setup-and-teardown-2.md)                                               | Un'applicazione può ottenere informazioni sul chiamante, ad esempio l'identificatore del chiamante e la qualità del servizio, prima di decidere se accettare una richiesta di connessione in ingresso. È anche possibile (per i protocolli che lo supportano) per scambiare dati utente tra gli endpoint al momento della connessione teardown. |
| [Arresto normale, opzioni Linger e chiusura del socket](graceful-shutdown-linger-options-and-socket-closure-2.md) | Un'applicazione dispone di diverse opzioni per l'arresto di una connessione socket (sequenza di arresto).                                                                                                                                                                                                  |
| [Dati fuori banda indipendenti dal protocollo](protocol-independent-out-of-band-data-2.md)                               | L'astrazione del socket di flusso include il concetto di dati fuori banda (OOB).                                                                                                                                                                                                                   |
| [Funzionalità di debug e di traccia](debug-and-trace-facilities-2.md)                                                     | Windows Sockets 2 supporta una versione appositamente concepita del \_32.dll WS2 e una DLL di debug/traccia separata.                                                                                                                                                                                      |
| [Problemi di compatibilità di Windows Sockets](windows-sockets-compatibility-issues-2.md)                                 | Windows Sockets 2 continua a supportare tutte le chiamate di funzione e la semantica di Windows Sockets 1,1, ad eccezione di quelle che si occupano di pseudo-blocco.                                                                                                                                              |
| [Gestione degli errori Winsock](handling-winsock-errors.md)                                                             | Come è possibile recuperare e gestire gli errori Winsock da un'applicazione.                                                                                                                                                                                                                             |



 

 

 




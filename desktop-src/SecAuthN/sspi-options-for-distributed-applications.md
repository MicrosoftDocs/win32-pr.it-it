---
description: Opzioni SSPI per le applicazioni distribuite
ms.assetid: e67cc054-7e48-43e7-a4b0-d1d90e9511f2
title: Opzioni SSPI per le applicazioni distribuite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed7729b3c479c69b674120fe1fc9827f5edfd878
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878526"
---
# <a name="sspi-options-for-distributed-applications"></a>Opzioni SSPI per le applicazioni distribuite

Gli sviluppatori hanno molte opzioni per la creazione di applicazioni distribuite. [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) fornisce un livello di astrazione tra i protocolli a livello di applicazione e i [*protocolli di sicurezza*](../secgloss/s-gly.md). Le applicazioni possono sfruttare i protocolli di sicurezza SSPI in diversi modi:

-   Chiamare le routine SSPI direttamente (per le applicazioni tradizionali basate su socket).

    Le routine utilizzano i messaggi di richiesta/risposta per implementare il [*protocollo dell'applicazione*](../secgloss/a-gly.md) che contiene dati correlati alla sicurezza SSPI.

-   Usare COM per chiamare le opzioni di sicurezza implementate tramite la RPC autenticata e SSPI a livelli inferiori.

    Queste applicazioni non chiamano direttamente le funzioni SSPI.

-   Usare [Windows Sockets 2](../winsock/windows-sockets-start-page-2.md) (Winsock) con l'interfaccia Winsock estesa per consentire ai provider di trasporto di usare le funzionalità di sicurezza.

    Questo approccio integra il [*Security Support Provider*](../secgloss/s-gly.md) (SSP) nello stack di rete e fornisce servizi di sicurezza e trasporto tramite un'interfaccia comune.

-   Utilizzare l' [API Windows Internet Extensions](../wininet/portal.md) (WinInet) e un'interfaccia progettata per supportare protocolli di sicurezza Internet, ad esempio il protocollo [*Secure Sockets Layer*](../secgloss/s-gly.md) (SSL).

    Le applicazioni utilizzano l'interfaccia SSPI per il provider di sicurezza del [canale sicuro](secure-channel.md) (Schannel) per implementare la sicurezza di WinInet. Schannel è l'implementazione Microsoft di SSL.

Diverse funzioni SSPI restituiscono indicatori temporali che rappresentano la durata di diversi oggetti. I [*pacchetti di sicurezza*](../secgloss/s-gly.md) possono mantenere l'ora e fornire timestamp in modi diversi, ma l'utilizzo dell'ora locale semplifica il lavoro di applicazioni che utilizzano funzioni SSPI.

 

 

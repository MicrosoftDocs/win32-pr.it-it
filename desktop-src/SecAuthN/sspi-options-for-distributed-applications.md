---
description: Opzioni SSPI per applicazioni distribuite
ms.assetid: e67cc054-7e48-43e7-a4b0-d1d90e9511f2
title: Opzioni SSPI per applicazioni distribuite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdfeef5cb52494c50b8b16911f70de238a7a86493297ec59bf6d46637810bf26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118916791"
---
# <a name="sspi-options-for-distributed-applications"></a>Opzioni SSPI per applicazioni distribuite

Gli sviluppatori hanno molte opzioni per la creazione di applicazioni distribuite. [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) fornisce un livello di astrazione tra protocolli a livello di applicazione e [*protocolli di sicurezza*](../secgloss/s-gly.md). Le applicazioni possono sfruttare i protocolli di sicurezza SSPI in diversi modi:

-   Chiamare direttamente le routine SSPI (per le applicazioni tradizionali basate su socket).

    Le routine usano messaggi di richiesta/risposta per implementare il [*protocollo dell'applicazione*](../secgloss/a-gly.md) che contiene dati correlati alla sicurezza SSPI.

-   Usare COM per chiamare le opzioni di sicurezza implementate tramite RPC autenticato e SSPI a livelli inferiori.

    Queste applicazioni non chiamano direttamente le funzioni SSPI.

-   Usare [Windows Sockets 2](../winsock/windows-sockets-start-page-2.md) (WinSock) con l'interfaccia WinSock estesa per consentire ai provider di trasporto di usare le funzionalità di sicurezza.

    Questo approccio integra il [*provider di supporto per la*](../secgloss/s-gly.md) sicurezza (SSP) nello stack di rete e fornisce servizi di sicurezza e trasporto tramite un'interfaccia comune.

-   Usare [l Windows API (Internet Extensions API)](../wininet/portal.md) e un'interfaccia progettata per supportare protocolli di sicurezza Internet come [*il protocollo Secure Sockets Layer*](../secgloss/s-gly.md) (SSL).

    Le applicazioni usano l'interfaccia SSPI per il provider di sicurezza Schannel [(Secure Channel)](secure-channel.md) per implementare la sicurezza WinInet. Schannel è l'implementazione Microsoft di SSL.

Diverse funzioni SSPI restituiscono timestamp che rappresentano l'intervallo di vita di vari oggetti. [*I pacchetti di*](../secgloss/s-gly.md) sicurezza possono mantenere l'ora e fornire timestamp in modi diversi, ma l'uso dell'ora locale semplifica il lavoro delle applicazioni che usano funzioni SSPI.

 

 

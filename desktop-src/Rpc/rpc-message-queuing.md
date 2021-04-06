---
title: Accodamento messaggi RPC
description: Accodamento messaggi (MSMQ) consente agli utenti di comunicare tra reti e sistemi indipendentemente dallo stato corrente delle applicazioni e dei sistemi che comunicano.
ms.assetid: f1c8665b-3754-4c2e-b3ac-bba1f4b329e1
keywords:
- RPC (Remote Procedure Call), descritto, Accodamento messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b72e9e35ec2aa1cc440c0d0356c681c4fe8548c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045128"
---
# <a name="rpc-message-queuing"></a>Accodamento messaggi RPC

Accodamento messaggi (MSMQ) consente agli utenti di comunicare tra reti e sistemi indipendentemente dallo stato corrente delle applicazioni e dei sistemi che comunicano. Le applicazioni inviano e ricevono messaggi tramite le code di messaggi gestite da MSMQ. Le code di messaggi continuano a funzionare anche quando l'applicazione client o server non è in esecuzione. Accodamento messaggi fornisce:

-   **Messaggistica asincrona.** Con la messaggistica asincrona MSMQ, un'applicazione client può inviare un messaggio a un server e restituire immediatamente un messaggio, anche se il computer di destinazione o il programma server non risponde.
-   **Recapito di messaggi garantito.** Quando un'applicazione invia un messaggio tramite MSMQ, il messaggio raggiungerà la destinazione anche se l'applicazione di destinazione non è in esecuzione nello stesso momento o se le reti e i sistemi sono offline.
-   **Routing e configurazione dinamica.** MSMQ fornisce un routing flessibile su reti eterogenee. La configurazione di tali reti può essere modificata dinamicamente senza modifiche sostanziali a sistemi e reti.
-   **Messaggistica senza connessione.** Le applicazioni che usano MSMQ non devono configurare sessioni dirette con le applicazioni di destinazione.
-   [Sicurezza](security.md). MSMQ fornisce comunicazioni sicure basate sulla sicurezza di Windows e sull'API di crittografia (CryptoAPI) per la crittografia e le firme digitali.
-   **Messaggistica con priorità.** MSMQ trasferisce i messaggi tra le reti in base alla priorità, consentendo una comunicazione più rapida per le applicazioni critiche.

Microsoft RPC estende il modello Open Software Foundation-Data Communications Equipment (OSF-DCE) per le chiamate di procedura remota consentendo alle applicazioni distribuite di usare MSMQ come trasporto e di controllare molte delle relative funzionalità. Questa funzionalità è disponibile sia per le applicazioni RPC convenzionali sia per le applicazioni COM tramite l'interfaccia **IRPCOptions** .

> [!Note]  
> Accodamento messaggi RPC è disponibile solo in Windows 2000. Le versioni successive di Windows non supportano l'accodamento dei messaggi RPC.

 

Negli argomenti seguenti viene fornita una panoramica di Accodamento messaggi:

-   [Panoramica dell'architettura dei servizi di Accodamento messaggi](overview-of-message-queuing-services-architecture.md)
-   [Proprietà Message e Message Queue](message-and-message-queue-properties.md)
-   [Utilizzo di MSMQ come trasporto RPC](using-msmq-as-an-rpc-transport.md)
-   [Requisiti di sistema per \_ le applicazioni di Accodamento messaggi RPC](system-requirements-for-rpc-message-queuing-applications.md)
-   [Sviluppo di applicazioni di Accodamento RPC-Message](developing-rpc-message-queuing-applications.md)
-   [Servizi di sicurezza MSMQ](msmq-security-services.md)

 

 





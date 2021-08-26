---
title: Accodamento messaggi RPC
description: Accodamento messaggi (MSMQ) consente agli utenti di comunicare tra reti e sistemi indipendentemente dallo stato corrente delle applicazioni e dei sistemi che comunicano.
ms.assetid: f1c8665b-3754-4c2e-b3ac-bba1f4b329e1
keywords:
- RPC Remote Procedure Call, descritto, accodamento messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c44296068087dc2fd4423dbb3294c3c7a417e8a983ec958c2ad765ff87ea81e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120018381"
---
# <a name="rpc-message-queuing"></a>Accodamento messaggi RPC

Accodamento messaggi (MSMQ) consente agli utenti di comunicare tra reti e sistemi indipendentemente dallo stato corrente delle applicazioni e dei sistemi che comunicano. Le applicazioni inviano e ricevono messaggi tramite code di messaggi gestite da MSMQ. Le code di messaggi continuano a funzionare anche quando l'applicazione client o server non è in esecuzione. Accodamento messaggi offre:

-   **Messaggistica asincrona.** Con la messaggistica asincrona MSMQ, un'applicazione client può inviare un messaggio a un server e restituire immediatamente un messaggio, anche se il computer o il programma server di destinazione non risponde.
-   **Recapito garantito dei messaggi.** Quando un'applicazione invia un messaggio tramite MSMQ, il messaggio raggiunge la destinazione anche se l'applicazione di destinazione non è in esecuzione contemporaneamente o se le reti e i sistemi sono offline.
-   **Routing e configurazione dinamica.** MSMQ offre un routing flessibile su reti eterogenee. La configurazione di tali reti può essere modificata in modo dinamico senza modifiche importanti ai sistemi e alle reti stesse.
-   **Messaggistica senza connessione.** Le applicazioni che usano MSMQ non devono configurare sessioni dirette con applicazioni di destinazione.
-   [Sicurezza](security.md). MSMQ fornisce comunicazioni protette basate Windows sicurezza e sull'API crittografica (CryptoAPI) per la crittografia e le firme digitali.
-   **Messaggistica classificata in ordine di priorità.** MSMQ trasferisce i messaggi tra reti in base alla priorità, consentendo comunicazioni più veloci per le applicazioni critiche.

Microsoft RPC estende il modello OSF-DCE (Open Software Foundation-Data Communications Equipment) per le chiamate di procedura remota consentendo alle applicazioni distribuite di usare MSMQ come trasporto e di controllare molte delle relative funzionalità. Questa funzionalità è disponibile sia per le applicazioni RPC convenzionali che, tramite **l'interfaccia IRPCOptions,** per le applicazioni COM.

> [!Note]  
> Accodamento messaggi RPC è disponibile solo in Windows 2000. Le versioni successive Windows non supportano l'accodamento dei messaggi RPC.

 

Negli argomenti seguenti viene fornita una panoramica dell'accodamento dei messaggi:

-   [Panoramica dell'architettura dei servizi di accodamento messaggi](overview-of-message-queuing-services-architecture.md)
-   [Proprietà di message e message queue](message-and-message-queue-properties.md)
-   [Utilizzo di MSMQ come trasporto RPC](using-msmq-as-an-rpc-transport.md)
-   [Requisiti di sistema per le applicazioni \_ di accodamento messaggi RPC](system-requirements-for-rpc-message-queuing-applications.md)
-   [Sviluppo RPC-Message applicazioni di accodamento](developing-rpc-message-queuing-applications.md)
-   [Servizi di sicurezza MSMQ](msmq-security-services.md)

 

 





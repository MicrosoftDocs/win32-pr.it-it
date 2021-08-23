---
description: Il protocollo Kerberos definisce il modo in cui i client interagiscono con un servizio di autenticazione di rete \[ Platform Software Development Kit (SDK). \]
ms.assetid: e7870e72-1386-4818-bf6f-73430ae942a8
title: Microsoft Kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 680a55581394d9d36da5b54cb2365d07384893069e26f9787163209daf2eabd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921793"
---
# <a name="microsoft-kerberos"></a>Microsoft Kerberos

Il [*protocollo Kerberos definisce*](../secgloss/k-gly.md) il modo in cui i client interagiscono con un servizio di autenticazione di rete. I client ottengono ticket dal centro di distribuzione chiave Kerberos (KDC, Kerberos Key Distribution Center) e quindi presentano questi ticket ai server durante la procedura di connessione. I ticket Kerberos rappresentano le credenziali di rete [*del client.*](../secgloss/c-gly.md)

Le informazioni contenute in questa sezione forniscono informazioni teoriche sull'uso del protocollo Kerberos in un processo di autenticazione. Si tratta di informazioni di base che possono aggiungere alla comprensione da parte dello sviluppatore di ciò che accade dietro le quinte in un processo SSPI che usa il protocollo Kerberos versione 5.

Il protocollo di autenticazione Kerberos fornisce un meccanismo per l'autenticazione reciproca tra entità prima che venga stabilita una connessione di rete sicura. In questa documentazione le due entità vengono chiamate client e server anche se è possibile eseguire connessioni di rete protette tra i server. Sia il client che il server possono essere definiti anche entità [*di sicurezza*](../secgloss/s-gly.md).

Il protocollo Kerberos presuppone che le transazioni tra client e server si sferrino in una rete aperta in cui la maggior parte dei client e molti server non sono fisicamente sicuri e i pacchetti che viaggiano lungo la rete possono essere monitorati e modificati a pedaggi. L'ambiente assunto è simile a Internet di oggi, in cui un utente malintenzionato può facilmente rappresentare un client o un server e può intercettare o manomettere facilmente le comunicazioni tra client legittimi e server.

In questa sezione vengono fornite le informazioni seguenti:

-   [Concetti relativi all'autenticazione di base](basic-authentication-concepts.md)
-   [Sottoprotocol Kerberos](kerberos-subprotocols.md)
-   [Modello Kerberos](kerberos-components.md)
-   [Interoperabilità SSPI/Kerberos con GSSAPI](sspi-kerberos-interoperability-with-gssapi.md)

L'applicazione non deve accedere direttamente al pacchetto [*di sicurezza*](../secgloss/s-gly.md) Kerberos. deve invece usare il pacchetto di sicurezza [*Negotiate.*](../secgloss/n-gly.md) Negotiate consente all'applicazione di sfruttare i protocolli [*di*](../secgloss/s-gly.md) sicurezza più avanzati se sono supportati dai sistemi coinvolti nell'autenticazione. Attualmente, il pacchetto di sicurezza Negotiate seleziona tra [*Kerberos*](../secgloss/k-gly.md) e NTLM. Negotiate seleziona Kerberos a meno che non possa essere usato da uno dei sistemi coinvolti nell'autenticazione.

 

 

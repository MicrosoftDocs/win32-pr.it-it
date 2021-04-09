---
description: Il protocollo Kerberos definisce il modo in cui i client interagiscono con un SDK (Network Authentication Service \[ Platform Software Development Kit) \] .
ms.assetid: e7870e72-1386-4818-bf6f-73430ae942a8
title: Microsoft Kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03787bcc65959838ea02c49958d9ca4e0405649
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966626"
---
# <a name="microsoft-kerberos"></a>Microsoft Kerberos

Il [*protocollo Kerberos*](../secgloss/k-gly.md) definisce il modo in cui i client interagiscono con un servizio di autenticazione di rete. I client ottengono ticket dal centro di distribuzione chiave Kerberos (KDC, Kerberos Key Distribution Center) e quindi presentano questi ticket ai server durante la procedura di connessione. I ticket Kerberos rappresentano le [*credenziali*](../secgloss/c-gly.md)di rete del client.

Le informazioni contenute in questa sezione forniscono un background teorico sull'uso del protocollo Kerberos in un processo di autenticazione. Si tratta di informazioni complementari che consentono agli sviluppatori di comprendere cosa accade dietro le quinte in un processo SSPI che usa il protocollo Kerberos versione 5.

Il protocollo di autenticazione Kerberos fornisce un meccanismo per l'autenticazione reciproca tra le entità prima che venga stabilita una connessione di rete protetta. In questa documentazione, le due entità sono denominate client e server anche se è possibile stabilire connessioni di rete sicure tra i server. Sia il client che il server possono anche essere denominati [*entità di sicurezza*](../secgloss/s-gly.md).

Il protocollo Kerberos presuppone che le transazioni tra client e server avvengano in una rete aperta in cui la maggior parte dei client e di molti server non siano fisicamente protetti e che i pacchetti che viaggino lungo la rete possano essere monitorati e modificati in base alle proprie dipendenze. L'ambiente ipotizzato è come Internet odierno, in cui un utente malintenzionato può facilmente fungere da client o server e può intercettare o manomettere le comunicazioni tra client e server legittimi.

In questa sezione vengono fornite le seguenti informazioni:

-   [Concetti di base sull'autenticazione](basic-authentication-concepts.md)
-   [Sottoprotocolli Kerberos](kerberos-subprotocols.md)
-   [Modello Kerberos](kerberos-components.md)
-   [Interoperabilità SSPI/Kerberos con GSSAPI](sspi-kerberos-interoperability-with-gssapi.md)

L'applicazione non deve accedere direttamente al [*pacchetto di sicurezza*](../secgloss/s-gly.md) Kerberos. deve invece usare il pacchetto di sicurezza [*Negotiate*](../secgloss/n-gly.md) . Negotiate consente all'applicazione di sfruttare i protocolli di [*sicurezza*](../secgloss/s-gly.md) più avanzati se sono supportati dai sistemi interessati dall'autenticazione. Attualmente, il pacchetto di sicurezza Negotiate seleziona tra [*Kerberos*](../secgloss/k-gly.md) e NTLM. Negotiate seleziona Kerberos a meno che non possa essere usato da uno dei sistemi interessati dall'autenticazione.

 

 

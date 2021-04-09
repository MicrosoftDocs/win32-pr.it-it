---
description: La semantica per i contesti di datagramma o senza connessione è leggermente diversa da quella per i contesti orientati alla connessione.
ms.assetid: f312796c-cbe6-4be9-9886-52fdb34ced6b
title: Contesti di datagramma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d233a0ba397e67a13b1c25588cf81b6f12c31d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129927"
---
# <a name="datagram-contexts"></a>Contesti di datagramma

La semantica per i contesti di [*datagramma*](/windows/desktop/SecGloss/d-gly)o senza connessione è leggermente diversa da quella per i contesti orientati alla connessione. Nel [*contesto*](/windows/desktop/SecGloss/c-gly)senza connessione di un datagramma, un server non è in grado di determinare quando il client è stato arrestato o ha interrotto la connessione. In altre parole, nessun avviso di terminazione viene passato dall'applicazione di trasporto al server come avviene in un contesto orientato alla connessione.

Per usare un contesto di datagramma, un client imposta il \_ flag del datagramma di ISC req \_ nella chiamata alla funzione [**InitializeSecurityContext (generale)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) .

> [!IMPORTANT]
> Il pacchetto [Microsoft Kerberos](microsoft-kerberos.md) non supporta i contesti di datagramma in modalità utente-utente.

 

Per supportare meglio alcuni modelli, in particolare RPC di tipo DCE, le regole seguenti si applicano quando il client usa un contesto di datagramma:

-   Il [*pacchetto di sicurezza*](/windows/desktop/SecGloss/s-gly) non produce un [*BLOB*](/windows/desktop/SecGloss/b-gly) di autenticazione (oggetto binario di grandi dimensioni) nella prima chiamata a [**InitializeSecurityContext (generale)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta). Tuttavia, il client può usare il contesto di sicurezza restituito in una chiamata alla funzione [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) per generare una firma per un messaggio.
-   Il pacchetto di sicurezza deve consentire il ristabilimento del contesto più volte per consentire al server di eliminare la connessione senza preavviso. Ciò implica che le chiavi utilizzate nelle funzioni [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) e [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) possono essere reimpostate su uno [*stato*](/windows/desktop/SecGloss/s-gly)coerente.
-   Il pacchetto di sicurezza consente al chiamante di specificare le informazioni sulla sequenza e fornisce le informazioni sulla sequenza sul lato ricevente. In aggiunta alle informazioni sulle sequenze gestite dal pacchetto.

Un pacchetto di sicurezza imposta il \_ \_ flag datagramma del flag SECPKG per indicare che supporta la semantica del datagramma.

 

 

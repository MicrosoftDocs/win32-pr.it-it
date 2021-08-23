---
description: La semantica per i contesti datagrammi o senza connessione è leggermente diversa da quella per i contesti orientati alla connessione.
ms.assetid: f312796c-cbe6-4be9-9886-52fdb34ced6b
title: Contesti di datagrammi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51cade151c77b9ceec037de57e08bcc3a90638ddeb56f27764d5ad2799abc523
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008649"
---
# <a name="datagram-contexts"></a>Contesti di datagrammi

La semantica [*per i contesti datagrammi*](/windows/desktop/SecGloss/d-gly)o senza connessione è leggermente diversa da quella per i contesti orientati alla connessione. Nel contesto senza connessione [](/windows/desktop/SecGloss/c-gly)di un datagramma, un server non è in grado di determinare quando il client è stato arrestato o in caso contrario ha terminato la connessione. In altre parole, non viene passata alcuna notifica di terminazione dall'applicazione di trasporto al server come si verificherebbe in un contesto orientato alla connessione.

Per usare un contesto di datagramma, un client imposta il flag ISC REQ DATAGRAM nella chiamata alla funzione \_ \_ [**InitializeSecurityContext (Generale).**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)

> [!IMPORTANT]
> Il [pacchetto Kerberos Microsoft](microsoft-kerberos.md) non supporta contesti di datagrammi in modalità da utente a utente.

 

Per supportare al meglio alcuni modelli, in particolare RPC di tipo DCE, quando il client usa un contesto di datagramma si applicano le regole seguenti:

-   Il [*pacchetto di sicurezza*](/windows/desktop/SecGloss/s-gly) non produce un [*BLOB*](/windows/desktop/SecGloss/b-gly) di autenticazione (oggetto binario di grandi dimensioni) alla prima chiamata a [**InitializeSecurityContext (Generale).**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) Tuttavia, il client può usare il contesto di sicurezza restituito in una chiamata alla [**funzione MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) per generare una firma per un messaggio.
-   Il pacchetto di sicurezza deve consentire al contesto di essere nuovamente stabilito più volte per consentire al server di eliminare la connessione senza preavviso. Ciò implica che qualsiasi chiave usata nelle [**funzioni MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) e [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) può essere reimpostata su uno stato [*coerente.*](/windows/desktop/SecGloss/s-gly)
-   Il pacchetto di sicurezza consente al chiamante di specificare le informazioni sulla sequenza e fornisce le informazioni sulla sequenza sul lato ricevitore. Si tratta di un'operazione che si aggiunge a qualsiasi informazione di sequenza gestita dal pacchetto.

Un pacchetto di sicurezza imposta il \_ flag SECPKG FLAG \_ DATAGRAM per indicare che supporta la semantica dei datagrammi.

 

 

---
description: Vengono illustrate le differenze tra provider di servizi condivisi/provider di servizi condivisi e provider di servizi condivisi.
ms.assetid: 0ed4291b-6562-440f-b892-4e6e5b4b49c8
title: Provider di servizi condivisi/provider di servizi condivisi e provider di servizi condivisi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c471e529a478cadbfcc385a1b0d699a4539e7bc80beeb2d40e01e2f7e9f428d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917267"
---
# <a name="sspaps-vs-ssps"></a>Provider di servizi condivisi/provider di servizi condivisi e provider di servizi condivisi

[*I pacchetti*](../secgloss/s-gly.md) di sicurezza vengono distribuiti in uno dei tipi seguenti di librerie a collegamento dinamico (DLL):

-   [Provider di servizi condivisi/provider di servizi condivisi](#sspaps-vs-ssps)
-   [SSP](#sspaps-vs-ssps)

Se un pacchetto di sicurezza si[](../secgloss/a-gly.md) trova in un provider di supporto per la sicurezza/pacchetto di autenticazione (SSP/AP) o in una DLL del provider di supporto per la sicurezza (SSP) è determinato dai tipi di servizi di sicurezza forniti e dalla misura in cui richiede l'integrazione con l'autorità di sicurezza locale (LSA). [](../secgloss/s-gly.md) [](../secgloss/l-gly.md) Queste differenze determinano anche l'API implementata in un pacchetto di sicurezza personalizzato.

## <a name="sspaps"></a>Provider di servizi condivisi/provider di servizi condivisi

Un provider di servizi condivisi è una [](../secgloss/s-gly.md) DLL che contiene uno o più pacchetti di [](authentication-packages.md) sicurezza e può funzionare come provider di servizi condivisi per le applicazioni client/server e come pacchetto di autenticazione per le applicazioni di accesso. Per funzionare in entrambi questi ruoli, I provider di servizi condivisi/provider di servizi di accesso vengono caricati nello spazio di elaborazione LSA all'avvio del sistema e possono essere caricati anche nei processi dell'applicazione client/server.

I pacchetti di sicurezza SSP/AP personalizzati devono implementare sia le funzioni implementate da [SSP/APs](authentication-functions.md)in modalità utente che le funzioni implementate da [SSP/APs.](authentication-functions.md) Queste implementazioni di funzione possono usare le funzioni di supporto LSA per offrire funzionalità di sicurezza avanzate, ad esempio la creazione di [*token,*](../secgloss/s-gly.md) il supporto delle credenziali supplementari e l'autenticazione pass-through.

Se un pacchetto di sicurezza SSP/AP [](../secgloss/i-gly.md) personalizzato fornisce l'intera gamma di funzioni di privacy e integrità dei messaggi, implementerà anche le funzioni implementate da provider di [servizi condivisi/provider di](authentication-functions.md)servizi di accesso in modalità utente.

## <a name="ssps"></a>SSP

Un provider di servizi condivisi è una DLL che contiene uno o più pacchetti di sicurezza che forniscono servizi autenticati di connessione, integrità dei messaggi e crittografia dei messaggi alle applicazioni client/server. Gli SSP implementano le funzioni SSPI [(Security Support Provider Interface).](sspi.md) Le applicazioni possono accedere ai pacchetti di sicurezza in un provider di servizi condivisi chiamando direttamente le funzioni SSPI. Gli SSP vengono caricati nei processi client e server. non sono integrati con l'LSA.

 

 

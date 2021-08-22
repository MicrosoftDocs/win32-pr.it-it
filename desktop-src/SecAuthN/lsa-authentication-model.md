---
description: Illustra il modello di autenticazione LSA.
ms.assetid: 0b2b868f-51a7-4f74-be4f-5f8db04d43ad
title: Modello di autenticazione LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3762595332252c22141aebdc7f3ecbe168e49a83795830a0cb03e49eb5da73ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140944"
---
# <a name="lsa-authentication-model"></a>Modello di autenticazione LSA

Il modello di autenticazione LSA [*(Local Security Authority)*](../secgloss/l-gly.md) include le funzionalità seguenti:

-   L'autenticazione LSA supporta pacchetti [di autenticazione personalizzati.](authentication-packages.md) Ciò consente ai clienti finali e ai fornitori di software indipendenti (ISV) di personalizzare o sostituire le routine di autenticazione per soddisfare requisiti diversi da quelli forniti dai pacchetti di autenticazione Microsoft standard. Mentre i pacchetti di autenticazione forniti da Microsoft richiedono un nome utente e una password di accesso, un pacchetto di autenticazione personalizzato può assumere altre forme di dati di accesso, ad esempio le informazioni sulla scheda ATM e un numero di identificazione personale (PIN). È anche possibile usare un pacchetto di autenticazione personalizzato per implementare un nuovo [*protocollo di sicurezza.*](../secgloss/s-gly.md)
-   LSA supporta pacchetti di sicurezza personalizzati, che funzionano come provider di supporto per la sicurezza per le applicazioni distribuite e come pacchetti di autenticazione per le applicazioni che richiedono servizi di autenticazione. È possibile accedere alla funzionalità di autenticazione usando la stessa interfaccia di un pacchetto di autenticazione autonomo, mentre la funzionalità del provider di supporto per la sicurezza è accessibile tramite [Security Support Provider Interface](sspi.md) (SSPI). Il set di funzioni di supporto LSA disponibili per i pacchetti di sicurezza personalizzati consente loro di fornire funzionalità di sicurezza avanzate, ad esempio la creazione di token e la gestione [*delle credenziali supplementari.*](../secgloss/s-gly.md)
-   LSA supporta la gestione eterogenea delle credenziali per l'interfaccia con prodotti non Microsoft, ad esempio reti e database. Poiché tali prodotti hanno spesso credenziali di sicurezza proprie, l'LSA fornisce funzioni che i pacchetti di autenticazione possono usare per associare le credenziali non Microsoft ai Windows processi. I pacchetti di autenticazione personalizzati possono fornire servizi per l'esecuzione di query su queste credenziali quando necessario, ad esempio quando un redirector di rete tenta di stabilire una connessione a un sistema remoto.
-   Ogni classe di dispositivo di accesso installata in un sistema può avere un proprio processo di accesso. Le classi di dispositivi includono in genere dispositivi come smart card lettori; Tuttavia, ai fini dell'autenticazione [*LSA,*](../secgloss/l-gly.md) anche le reti connesse vengono considerate dispositivi. Per impostazione predefinita, il Windows sistema operativo fornisce il processo di accesso che supporta gli accessi con nome utente e password tramite tastiera. Gli sviluppatori possono aggiungere il supporto per altri dispositivi, [*ad*](../secgloss/s-gly.md) esempio smart card [*lettori.*](../secgloss/r-gly.md) Per altre informazioni sulle smart card, vedere [Autenticazione smart card.](smart-card-authentication.md) Per altre informazioni sul supporto dei dispositivi di accesso, vedere [Winlogon e GINA.](winlogon-and-gina.md)

 

 

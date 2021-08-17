---
description: Un'applicazione server fornisce servizi ai client.
ms.assetid: 8301ed4f-9458-410b-af19-4f055656005a
title: Controllo di accesso client/server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c943d9d1e1f1cc5dcc405f49ab200aa30618f7eefb86c7f26342f005f23249fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782726"
---
# <a name="clientserver-access-control"></a>Controllo di accesso client/server

Un'applicazione server fornisce servizi ai client. Ad esempio, un server può eseguire i servizi seguenti per conto di un client:

-   Salvare e recuperare informazioni da un database privato
-   Accedere alle risorse di rete
-   Avviare [*i*](/windows/desktop/SecGloss/p-gly) processi nel contesto di [*sicurezza del*](/windows/desktop/SecGloss/s-gly) client nel computer del server

Un server protetto controlla l'accesso ai relativi servizi. Windows offre il supporto per la sicurezza che consente a un server di eseguire le operazioni seguenti:

-   Rappresenta il contesto di sicurezza di un [*client,*](/windows/desktop/SecGloss/s-gly)che [](/windows/desktop/SecGloss/p-gly) fa sì che il sistema eserviti la maggior parte dei controlli di accesso e dei privilegi rispetto al [*token*](/windows/desktop/SecGloss/a-gly) di accesso del client anziché a quello del server
-   Accedere a un client nel computer del server
-   Connessione alle risorse di rete usando il contesto di sicurezza del client
-   Creare [*descrittori di sicurezza per*](/windows/desktop/SecGloss/s-gly) proteggere gli oggetti privati
-   Determinare se un descrittore di sicurezza consente l'accesso a un client
-   Determinare se un set di privilegi è abilitato nel token di un client
-   Generare messaggi di controllo nel registro eventi di sicurezza per registrare i tentativi da parte di un client di accedere agli oggetti o usare i privilegi

 

 

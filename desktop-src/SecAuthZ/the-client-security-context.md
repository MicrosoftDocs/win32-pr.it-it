---
description: Come tutti i processi, un server protetto ha un token di accesso primario che ne descrive il contesto di sicurezza.
ms.assetid: 4e6393b2-4a71-49e4-b1e7-f34bf317d60d
title: Contesto di sicurezza client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af57c11c7b0452003498b88b0be24c880e2875fec459fb80e3cd87ef01bdd493
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907121"
---
# <a name="the-client-security-context"></a>Contesto di sicurezza client

Come tutti [*i processi*](/windows/desktop/SecGloss/p-gly), un server protetto ha un token di [*accesso primario*](/windows/desktop/SecGloss/p-gly) che ne descrive il contesto [*di sicurezza.*](/windows/desktop/SecGloss/s-gly) Quando un client si connette a un server protetto, è possibile che il server voglia eseguire azioni usando il contesto di sicurezza del client anziché il contesto di sicurezza del server. Ad esempio, quando un client in una conversazione DDE (Dynamic Data Exchange) richiede informazioni a un server DDE, il server deve verificare che al client sia consentito l'accesso alle informazioni.

Un server può agire in due modi nel contesto di sicurezza del client:

-   Un thread del processo server può rappresentare il client. In questo caso, il thread del server ha un [*token*](/windows/desktop/SecGloss/a-gly) di accesso di rappresentazione che identifica il client, i gruppi del client e i privilegi [*del*](/windows/desktop/SecGloss/p-gly)client. Per altre informazioni, vedere [Rappresentazione client](client-impersonation.md).
-   Il server può ottenere le credenziali [*del*](/windows/desktop/SecGloss/c-gly) client e accedere al computer del server. Verrà creata una nuova sessione [*di accesso*](/windows/desktop/SecGloss/s-gly) e verrà generato un token di accesso primario per il client. Il server può quindi usare il token di accesso del client per rappresentare il client o per avviare un nuovo processo eseguito nel contesto di sicurezza del client. Per altre informazioni, vedere [Sessioni di accesso client](client-logon-sessions.md).

Nella maggior parte dei casi, la rappresentazione del client è sufficiente. La rappresentazione consente al server di controllare l'accesso del client agli oggetti a protezione diretta, controllare i privilegi del client e generare audit trail che identificano il client. In genere, un server deve avviare una sessione di accesso client solo se deve usare il contesto di sicurezza del client per accedere alle risorse di rete.

 

 

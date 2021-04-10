---
description: Come tutti i processi, un server protetto dispone di un token di accesso primario che ne descrive il contesto di sicurezza.
ms.assetid: 4e6393b2-4a71-49e4-b1e7-f34bf317d60d
title: Contesto di sicurezza del client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb3d3b4522aa90ade89e2130742346956a396f15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966815"
---
# <a name="the-client-security-context"></a>Contesto di sicurezza del client

Come tutti i [*processi*](/windows/desktop/SecGloss/p-gly), un server protetto dispone di un [*token di accesso primario*](/windows/desktop/SecGloss/p-gly) che ne descrive il [*contesto di sicurezza*](/windows/desktop/SecGloss/s-gly). Quando un client si connette a un server protetto, il server potrebbe voler eseguire azioni utilizzando il contesto di sicurezza del client anziché il contesto di sicurezza del server. Ad esempio, quando un client in una conversazione DDE (Dynamic Data Exchange) richiede informazioni da un server DDE, il server deve verificare che il client sia autorizzato ad accedere alle informazioni.

Un server può agire nel contesto di sicurezza del client in due modi:

-   Un thread del processo server può rappresentare il client. In questo caso, il thread del server dispone di un token di [*accesso*](/windows/desktop/SecGloss/a-gly) di rappresentazione che identifica il client, i gruppi del client e i [*privilegi*](/windows/desktop/SecGloss/p-gly)del client. Per ulteriori informazioni, vedere [rappresentazione client](client-impersonation.md).
-   Il server può ottenere le [*credenziali*](/windows/desktop/SecGloss/c-gly) del client e registrare il client nel computer del server. Viene creata una nuova [*sessione*](/windows/desktop/SecGloss/s-gly) di accesso e viene generato un token di accesso primario per il client. Il server può quindi usare il token di accesso del client per rappresentare il client o per avviare un nuovo processo eseguito nel contesto di sicurezza del client. Per ulteriori informazioni, vedere [sessioni di accesso client](client-logon-sessions.md).

Nella maggior parte dei casi, è sufficiente rappresentare il client. La rappresentazione consente al server di controllare l'accesso del client agli oggetti a protezione diretta, controllare i privilegi del client e generare audit trail voci che identificano il client. In genere, un server deve avviare una sessione di accesso client solo se è necessario usare il contesto di sicurezza del client per accedere alle risorse di rete.

 

 

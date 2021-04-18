---
description: Un'applicazione server fornisce servizi ai client.
ms.assetid: 8301ed4f-9458-410b-af19-4f055656005a
title: Controllo di accesso client/server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92b1d349abb2d55f00b9801c9bb493437fa858eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308654"
---
# <a name="clientserver-access-control"></a>Controllo di accesso client/server

Un'applicazione server fornisce servizi ai client. Ad esempio, un server può eseguire i servizi seguenti per conto di un client:

-   Salvare e recuperare informazioni da un database privato
-   Accedere alle risorse di rete
-   Avviare i [*processi*](/windows/desktop/SecGloss/p-gly) nel contesto di [*sicurezza*](/windows/desktop/SecGloss/s-gly) del client nel computer del server

Un server protetto controlla l'accesso ai servizi. Windows fornisce supporto per la sicurezza che consente a un server di eseguire le operazioni seguenti:

-   Rappresenta il [*contesto di sicurezza*](/windows/desktop/SecGloss/s-gly)di un client, che fa in modo che il sistema esegua la maggior parte dei controlli di accesso e dei [*privilegi*](/windows/desktop/SecGloss/p-gly) rispetto al [*token di accesso*](/windows/desktop/SecGloss/a-gly) del client anziché al server
-   Registrare un client nel computer del server
-   Connettersi alle risorse di rete usando il contesto di sicurezza del client
-   Creare [*descrittori di sicurezza*](/windows/desktop/SecGloss/s-gly) per proteggere gli oggetti privati
-   Determinare se un descrittore di sicurezza consente l'accesso a un client
-   Determinare se un set di privilegi è abilitato nel token di un client
-   Generare messaggi di controllo nel registro eventi di sicurezza per registrare i tentativi da parte di un client di accedere agli oggetti o utilizzare i privilegi

 

 

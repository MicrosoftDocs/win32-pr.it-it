---
description: Per ridurre il traffico dei controller di dominio e migliorare le prestazioni, il lato client di Microsoft Digest memorizza nella cache le informazioni ricevute dopo il completamento dell'autenticazione con un server.
ms.assetid: cd928266-889a-494c-a94b-4ea7b1dcc241
title: Gestione del contesto di sicurezza tra le connessioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeb450dde789f17f46397cb56fe74b94adcf8ea6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347146"
---
# <a name="maintaining-the-security-context-between-connections"></a>Gestione del contesto di sicurezza tra le connessioni

Per ridurre il traffico dei controller di dominio e migliorare le prestazioni, il lato client di Microsoft Digest memorizza nella cache le informazioni ricevute dopo il completamento dell'autenticazione con un server. Per le applicazioni client è necessario memorizzare nella cache l'handle solo per il [*contesto di sicurezza*](../secgloss/s-gly.md) stabilito. Nella tabella seguente vengono descritte le informazioni memorizzate nella cache dal pacchetto di sicurezza.



| Informazioni                                                       | Descrizione                                                                                                                                         |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Nome server                                                       | Server in cui è stato creato correttamente un contesto di sicurezza per l'utente.                                                                           |
| Area di autenticazione/dominio                                                      | Nome di dominio utilizzato per l'autenticazione riuscita.                                                                                              |
| [*Nonce*](../secgloss/n-gly.md) | Parametro nonce del server associato all'autenticazione riuscita.                                                                               |
| Conteggio nonce                                                       | Il numero di volte in cui il client ha incluso il parametro nonce nelle richieste al server. Viene utilizzato per il rilevamento della riproduzione.                                 |
| Valore opaco                                                      | Valore restituito per la direttiva opaca dopo un'autenticazione riuscita. Questo valore contiene un riferimento al contesto di sicurezza dell'utente. |



 

Quando un client invia un messaggio a un server, il server deve determinare se il client dispone di un contesto di sicurezza esistente. A tale scopo, il server passa ogni richiesta client alla funzione [**AcceptSecurityContext (generale)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) . Questa funzione estrae il valore della direttiva Opaque dalla richiesta, se presente, e la usa per cercare il contesto di sicurezza del client. Se viene trovato il contesto di sicurezza, l'handle del contesto viene restituito al server. Per informazioni correlate, vedere [autenticazione delle richieste successive](authenticating-subsequent-requests-using-microsoft-digest.md).

Come mezzo per rilevare gli attacchi di spoofing e riproduzione, il client chiama la funzione [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) che usa un contesto di sicurezza per firmare un messaggio. Quando i messaggi vengono protetti tramite la funzione **MakeSignature** , il server utilizza la funzione [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) con il contesto memorizzato nella cache per verificare l'origine e l' [*integrità*](../secgloss/i-gly.md)del messaggio. Per ulteriori informazioni, vedere la pagina relativa alla [protezione dei messaggi](protecting-messages-using-microsoft-digest.md).

 

 

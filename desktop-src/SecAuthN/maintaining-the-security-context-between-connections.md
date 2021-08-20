---
description: Per ridurre il traffico del controller di dominio e migliorare le prestazioni, il lato client Microsoft Digest memorizza nella cache le informazioni ricevute dopo l'autenticazione con un server.
ms.assetid: cd928266-889a-494c-a94b-4ea7b1dcc241
title: Gestione del contesto di sicurezza tra le connessioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d36b28d1db96efd6c41b3532b8021db7e6f8cf206e0df0bedf62b5775d2ba7de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117787048"
---
# <a name="maintaining-the-security-context-between-connections"></a>Gestione del contesto di sicurezza tra le connessioni

Per ridurre il traffico del controller di dominio e migliorare le prestazioni, il lato client Microsoft Digest memorizza nella cache le informazioni ricevute dopo l'autenticazione con un server. Le applicazioni client devono memorizzare nella cache solo l'handle nel [*contesto di*](../secgloss/s-gly.md) sicurezza stabilito. Nella tabella seguente vengono descritte le informazioni memorizzate nella cache dal pacchetto di sicurezza.



| Informazioni                                                       | Descrizione                                                                                                                                         |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Nome server                                                       | Server che ha creato correttamente un contesto di sicurezza per l'utente.                                                                           |
| Area di autenticazione/dominio                                                      | Nome di dominio utilizzato nell'autenticazione riuscita.                                                                                              |
| [*Nonce*](../secgloss/n-gly.md) | Server nonce associato all'autenticazione riuscita.                                                                               |
| Conteggio nonce                                                       | Numero di volte in cui il client ha incluso il nonce nelle richieste al server. Viene usato per il rilevamento della riproduzione.                                 |
| Valore opaco                                                      | Valore restituito per la direttiva opaca dopo un'autenticazione riuscita. Questo valore contiene un riferimento al contesto di sicurezza dell'utente. |



 

Quando un client invia un messaggio a un server, il server deve determinare se il client dispone di un contesto di sicurezza esistente. A tale scopo, il server passa ogni richiesta client alla [**funzione AcceptSecurityContext (Generale).**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) Questa funzione estrae il valore della direttiva opaca dalla richiesta, se presente, e la usa per cercare il contesto di sicurezza del client. Se viene trovato il contesto di sicurezza, l'handle del contesto viene restituito al server. Per informazioni correlate, vedere [Autenticazione delle richieste successive.](authenticating-subsequent-requests-using-microsoft-digest.md)

Per rilevare attacchi di spoofing e riproduzione, il client chiama la [**funzione MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) che usa un contesto di sicurezza per firmare un messaggio. Quando i messaggi vengono protetti tramite la **funzione MakeSignature,** il server usa la [**funzione VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) con il contesto memorizzato nella cache per verificare l'origine e l'integrità [*del messaggio.*](../secgloss/i-gly.md) Per altre informazioni, vedere [Protezione dei messaggi](protecting-messages-using-microsoft-digest.md).

 

 

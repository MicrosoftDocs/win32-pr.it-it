---
description: Viene illustrato come proteggere i messaggi utilizzando Microsoft Digest.
ms.assetid: 15509d51-80c0-4d5c-aa24-4dc17de3f12c
title: Protezione dei messaggi mediante Microsoft Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 573eafcf66e23188546abd3acd316095ec100187
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313724"
---
# <a name="protecting-messages-using-microsoft-digest"></a>Protezione dei messaggi mediante Microsoft Digest

## <a name="http-and-sasl"></a>HTTP e SASL

Come mezzo per rilevare determinati tipi di violazioni della sicurezza, il client e il server utilizzano le funzioni di [*integrità*](../secgloss/i-gly.md) dei messaggi SSPI ( [Security Support Provider Interface](sspi.md) ) [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) e [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) per proteggere i messaggi.

Un client chiama la funzione [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) per firmare un messaggio utilizzando il relativo [*contesto di sicurezza*](../secgloss/s-gly.md). Il server utilizza la funzione [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) per verificare l'origine del messaggio. Oltre a verificare la [*firma*](../secgloss/d-gly.md) che accompagna il messaggio, la funzione **VerifySignature** verifica anche che il numero di [*nonce*](../secgloss/n-gly.md) (specificato dalla direttiva NC) sia maggiore di quello dell'ultimo numero inviato per il parametro nonce. In caso contrario, la funzione **VerifySignature** restituisce un \_ \_ codice di errore di sequenza al secondo \_ .

## <a name="sasl-only"></a>Solo SASL

Le funzioni [**EncryptMessage (generale)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) e [**DecryptMessage (generale)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) forniscono la riservatezza per i messaggi di post-autenticazione scambiati tra client e server.

Per utilizzare le funzioni di riservatezza dei messaggi, è necessario che il server e il client abbiano stabilito un [*contesto di sicurezza*](../secgloss/s-gly.md) con gli attributi seguenti:

-   La qualità della protezione, specificata dalla direttiva qop, deve essere "auth-conf".
-   Un meccanismo di crittografia deve essere stato specificato mediante la direttiva di crittografia.

 

 

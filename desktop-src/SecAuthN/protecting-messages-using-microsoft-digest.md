---
description: Viene illustrato come proteggere i messaggi usando Microsoft Digest.
ms.assetid: 15509d51-80c0-4d5c-aa24-4dc17de3f12c
title: Protezione dei messaggi tramite Microsoft Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dab0add351287b6c90cfe0781151c0378da56f309214b03ed12d1325a6e55d88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118920740"
---
# <a name="protecting-messages-using-microsoft-digest"></a>Protezione dei messaggi tramite Microsoft Digest

## <a name="http-and-sasl"></a>HTTP e SASL

Per rilevare determinati tipi di violazioni della sicurezza, il client e il server [](../secgloss/i-gly.md) usano le funzioni di integrità dei messaggi SSPI [(Security Support Provider Interface)](sspi.md) [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) e [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) per proteggere i messaggi.

Un client chiama la [**funzione MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) per firmare un messaggio usando il contesto [*di sicurezza*](../secgloss/s-gly.md). Il server usa la [**funzione VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) per verificare l'origine del messaggio. Oltre a verificare [](../secgloss/d-gly.md) la firma che accompagna il messaggio, la funzione **VerifySignature** verifica anche che il conteggio dei nonce (specificato dalla direttiva nc) sia maggiore di uno rispetto all'ultimo conteggio inviato per il [*parametro nonce.*](../secgloss/n-gly.md) In caso contrario, la funzione **VerifySignature** restituisce un codice di errore SEC \_ OUT OF \_ \_ SEQUENCE.

## <a name="sasl-only"></a>Solo SASL

Le [**funzioni EncryptMessage (Generale)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) e [**DecryptMessage (Generale)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) forniscono riservatezza per i messaggi post-autenticazione s scambiati tra client e server.

Per usare le funzioni di riservatezza dei messaggi, il server e il client devono avere stabilito un contesto [*di sicurezza*](../secgloss/s-gly.md) con gli attributi seguenti:

-   La qualità della protezione, specificata dalla direttiva qop, deve essere "auth-conf".
-   Un meccanismo di crittografia deve essere stato specificato tramite la direttiva di crittografia .

 

 

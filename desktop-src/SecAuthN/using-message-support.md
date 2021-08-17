---
description: Viene illustrato come utilizzare il supporto dei messaggi SSPI.
ms.assetid: 14d4813e-413e-4ef9-85f0-96986c3c1eca
title: Uso del supporto messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08c6a14c28cc9eb9e1b606574659412a22f375ad935ee0d7d1bdd898781c230d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785921"
---
# <a name="using-message-support"></a>Uso del supporto messaggi

Dopo aver completato un handshake e stabilito una connessione sicura, un'applicazione può usare le funzioni [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature), [**EncryptMessage (Generale),**](/windows/win32/api/sspi/nf-sspi-encryptmessage) [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature)e [**DecryptMessage (Generale)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) per scambiare dati dell'applicazione firmati o crittografati con il computer remoto.

Gli esempi che usano queste funzioni dopo [*aver stabilito un contesto*](../secgloss/s-gly.md) di sicurezza sono illustrati nelle sezioni seguenti:

-   [Firma di un messaggio](signing-a-message.md)
-   [Verifica di un messaggio](verifying-a-message.md)
-   [Crittografia di un messaggio](encrypting-a-message.md)
-   [Decrittografia di un messaggio](decrypting-a-message.md)

 

 

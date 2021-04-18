---
description: Viene illustrato come utilizzare il supporto di messaggi SSPI.
ms.assetid: 14d4813e-413e-4ef9-85f0-96986c3c1eca
title: Utilizzo del supporto per i messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d75a2475609afed1647d99552a3719479d84fbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315855"
---
# <a name="using-message-support"></a>Utilizzo del supporto per i messaggi

Dopo che è stato completato un handshake ed è stata stabilita una connessione protetta, un'applicazione può utilizzare le funzioni [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature), [**EncryptMessage (generale)**](/windows/win32/api/sspi/nf-sspi-encryptmessage), [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature)e [**DecryptMessage (generale)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) per scambiare dati dell'applicazione firmati o crittografati con il computer remoto.

Le sezioni seguenti illustrano alcuni esempi che usano queste funzioni dopo aver stabilito un [*contesto di sicurezza*](../secgloss/s-gly.md) .

-   [Firma di un messaggio](signing-a-message.md)
-   [Verifica di un messaggio](verifying-a-message.md)
-   [Crittografia di un messaggio](encrypting-a-message.md)
-   [Decrittografia di un messaggio](decrypting-a-message.md)

 

 

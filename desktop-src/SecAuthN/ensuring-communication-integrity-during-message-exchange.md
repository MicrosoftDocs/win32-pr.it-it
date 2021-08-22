---
description: Dopo aver stabilito un contesto di sicurezza, l'applicazione può usare le funzioni di supporto dei messaggi per trasmettere messaggi anti-manomissione.
ms.assetid: 43d7b940-1816-429f-be6e-40978efed278
title: Garantire l'integrità della comunicazione durante l'Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 394f78fcc1e5becf4bdfc7c67db52e1af177a7f3aa427d1c6182a080f0ae87bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008259"
---
# <a name="ensuring-communication-integrity-during-message-exchange"></a>Garantire l'integrità della comunicazione durante l'Exchange

Dopo aver [*stabilito un contesto di*](/windows/desktop/SecGloss/s-gly) sicurezza, l'applicazione può usare le funzioni di [supporto](authentication-functions.md) dei messaggi per trasmettere messaggi anti-manomissione.

Il client o il server passa il contesto di sicurezza e un messaggio alla [**funzione MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) per generare una firma sicura che impedisce la modifica del messaggio durante il transito. Il ricevitore del messaggio chiama la [**funzione VerifySignature.**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) **VerifySignature** usa le informazioni nella firma per verificare che il messaggio ricevuto non sia stato modificato durante la trasmissione. Il client e il server possono anche scambiare messaggi crittografati usando [**EncryptMessage (Generale)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) e [**DecryptMessage (Generale).**](/windows/win32/api/sspi/nf-sspi-decryptmessage)

Il server in una connessione autenticata può anche stabilire connessioni con altri computer remoti nel nome del client dopo aver chiamato [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext).

 

 

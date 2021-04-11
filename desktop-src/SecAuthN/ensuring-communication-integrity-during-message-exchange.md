---
description: Una volta stabilito un contesto di sicurezza, l'applicazione può utilizzare le funzioni di supporto dei messaggi per trasmettere messaggi resistenti alle manomissioni.
ms.assetid: 43d7b940-1816-429f-be6e-40978efed278
title: Verifica dell'integrità della comunicazione durante lo scambio di messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70545abf11a933cd3bb6d0c32f3312637fcccbe2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128806"
---
# <a name="ensuring-communication-integrity-during-message-exchange"></a>Verifica dell'integrità della comunicazione durante lo scambio di messaggi

Una volta stabilito un [*contesto di sicurezza*](/windows/desktop/SecGloss/s-gly) , l'applicazione può utilizzare le funzioni di [supporto dei messaggi](authentication-functions.md) per trasmettere messaggi resistenti alle manomissioni.

Il client o il server passa il contesto di sicurezza e un messaggio alla funzione [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) per generare una firma sicura che impedisce che il messaggio venga modificato durante il transito. Il ricevitore del messaggio chiama la funzione [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) . **VerifySignature** utilizza le informazioni nella firma per verificare che il messaggio ricevuto non sia stato modificato durante la trasmissione. Il client e il server possono anche scambiare messaggi crittografati tramite [**EncryptMessage (generale)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) e [**DecryptMessage (generale)**](/windows/win32/api/sspi/nf-sspi-decryptmessage).

Il server in una connessione autenticata può inoltre stabilire connessioni con altri computer remoti nel nome del client dopo aver chiamato [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext).

 

 

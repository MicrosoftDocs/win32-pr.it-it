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
# <a name="ensuring-communication-integrity-during-message-exchange"></a><span data-ttu-id="aa8bf-103">Verifica dell'integrità della comunicazione durante lo scambio di messaggi</span><span class="sxs-lookup"><span data-stu-id="aa8bf-103">Ensuring Communication Integrity During Message Exchange</span></span>

<span data-ttu-id="aa8bf-104">Una volta stabilito un [*contesto di sicurezza*](/windows/desktop/SecGloss/s-gly) , l'applicazione può utilizzare le funzioni di [supporto dei messaggi](authentication-functions.md) per trasmettere messaggi resistenti alle manomissioni.</span><span class="sxs-lookup"><span data-stu-id="aa8bf-104">After a [*security context*](/windows/desktop/SecGloss/s-gly) is established, the application can use the [message support](authentication-functions.md) functions to transmit tamper-resistant messages.</span></span>

<span data-ttu-id="aa8bf-105">Il client o il server passa il contesto di sicurezza e un messaggio alla funzione [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) per generare una firma sicura che impedisce che il messaggio venga modificato durante il transito.</span><span class="sxs-lookup"><span data-stu-id="aa8bf-105">The client or server passes the security context and a message to the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) function to generate a secure signature that prevents the message from being modified while in transit.</span></span> <span data-ttu-id="aa8bf-106">Il ricevitore del messaggio chiama la funzione [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) .</span><span class="sxs-lookup"><span data-stu-id="aa8bf-106">The receiver of the message calls the [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) function.</span></span> <span data-ttu-id="aa8bf-107">**VerifySignature** utilizza le informazioni nella firma per verificare che il messaggio ricevuto non sia stato modificato durante la trasmissione.</span><span class="sxs-lookup"><span data-stu-id="aa8bf-107">**VerifySignature** uses the information in the signature to verify that the message received was not modified during transmission.</span></span> <span data-ttu-id="aa8bf-108">Il client e il server possono anche scambiare messaggi crittografati tramite [**EncryptMessage (generale)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) e [**DecryptMessage (generale)**](/windows/win32/api/sspi/nf-sspi-decryptmessage).</span><span class="sxs-lookup"><span data-stu-id="aa8bf-108">The client and server can also exchange encrypted messages using [**EncryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) and [**DecryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage).</span></span>

<span data-ttu-id="aa8bf-109">Il server in una connessione autenticata può inoltre stabilire connessioni con altri computer remoti nel nome del client dopo aver chiamato [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext).</span><span class="sxs-lookup"><span data-stu-id="aa8bf-109">The server in an authenticated connection can also make connections with other remote computers in the name of the client after calling [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext).</span></span>

 

 

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
# <a name="protecting-messages-using-microsoft-digest"></a><span data-ttu-id="7cb84-103">Protezione dei messaggi mediante Microsoft Digest</span><span class="sxs-lookup"><span data-stu-id="7cb84-103">Protecting Messages Using Microsoft Digest</span></span>

## <a name="http-and-sasl"></a><span data-ttu-id="7cb84-104">HTTP e SASL</span><span class="sxs-lookup"><span data-stu-id="7cb84-104">HTTP and SASL</span></span>

<span data-ttu-id="7cb84-105">Come mezzo per rilevare determinati tipi di violazioni della sicurezza, il client e il server utilizzano le funzioni di [*integrità*](../secgloss/i-gly.md) dei messaggi SSPI ( [Security Support Provider Interface](sspi.md) ) [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) e [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) per proteggere i messaggi.</span><span class="sxs-lookup"><span data-stu-id="7cb84-105">As a means of detecting certain types of security violations, the client and server use the [security support provider interface](sspi.md) (SSPI) message [*integrity*](../secgloss/i-gly.md) functions [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) and [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) to protect messages.</span></span>

<span data-ttu-id="7cb84-106">Un client chiama la funzione [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) per firmare un messaggio utilizzando il relativo [*contesto di sicurezza*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="7cb84-106">A client calls the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) function to sign a message using its [*security context*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="7cb84-107">Il server utilizza la funzione [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) per verificare l'origine del messaggio.</span><span class="sxs-lookup"><span data-stu-id="7cb84-107">The server uses the [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) function to verify the message's origin.</span></span> <span data-ttu-id="7cb84-108">Oltre a verificare la [*firma*](../secgloss/d-gly.md) che accompagna il messaggio, la funzione **VerifySignature** verifica anche che il numero di [*nonce*](../secgloss/n-gly.md) (specificato dalla direttiva NC) sia maggiore di quello dell'ultimo numero inviato per il parametro nonce.</span><span class="sxs-lookup"><span data-stu-id="7cb84-108">In addition to verifying the [*signature*](../secgloss/d-gly.md) that accompanies the message, the **VerifySignature** function also checks that the [*nonce*](../secgloss/n-gly.md) count (specified by the nc directive) is one greater than the last count sent for the nonce.</span></span> <span data-ttu-id="7cb84-109">In caso contrario, la funzione **VerifySignature** restituisce un \_ \_ codice di errore di sequenza al secondo \_ .</span><span class="sxs-lookup"><span data-stu-id="7cb84-109">If this is not the case, the **VerifySignature** function returns an SEC\_OUT\_OF\_SEQUENCE error code.</span></span>

## <a name="sasl-only"></a><span data-ttu-id="7cb84-110">Solo SASL</span><span class="sxs-lookup"><span data-stu-id="7cb84-110">SASL Only</span></span>

<span data-ttu-id="7cb84-111">Le funzioni [**EncryptMessage (generale)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) e [**DecryptMessage (generale)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) forniscono la riservatezza per i messaggi di post-autenticazione scambiati tra client e server.</span><span class="sxs-lookup"><span data-stu-id="7cb84-111">The [**EncryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) and [**DecryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) functions supply confidentiality for post-authentication messages exchanged between client and server.</span></span>

<span data-ttu-id="7cb84-112">Per utilizzare le funzioni di riservatezza dei messaggi, è necessario che il server e il client abbiano stabilito un [*contesto di sicurezza*](../secgloss/s-gly.md) con gli attributi seguenti:</span><span class="sxs-lookup"><span data-stu-id="7cb84-112">In order to use the message confidentiality functions, the server and client must have established a [*security context*](../secgloss/s-gly.md) with the following attributes:</span></span>

-   <span data-ttu-id="7cb84-113">La qualità della protezione, specificata dalla direttiva qop, deve essere "auth-conf".</span><span class="sxs-lookup"><span data-stu-id="7cb84-113">Quality of protection, specified by the qop directive, must be "auth-conf".</span></span>
-   <span data-ttu-id="7cb84-114">Un meccanismo di crittografia deve essere stato specificato mediante la direttiva di crittografia.</span><span class="sxs-lookup"><span data-stu-id="7cb84-114">An encryption mechanism must have been specified by means of the cipher directive.</span></span>

 

 

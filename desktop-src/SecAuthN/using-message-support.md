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
# <a name="using-message-support"></a><span data-ttu-id="eb98e-103">Utilizzo del supporto per i messaggi</span><span class="sxs-lookup"><span data-stu-id="eb98e-103">Using Message Support</span></span>

<span data-ttu-id="eb98e-104">Dopo che è stato completato un handshake ed è stata stabilita una connessione protetta, un'applicazione può utilizzare le funzioni [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature), [**EncryptMessage (generale)**](/windows/win32/api/sspi/nf-sspi-encryptmessage), [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature)e [**DecryptMessage (generale)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) per scambiare dati dell'applicazione firmati o crittografati con il computer remoto.</span><span class="sxs-lookup"><span data-stu-id="eb98e-104">After a handshake has been completed and a secure connection has been established, an application can use the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature), [**EncryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-encryptmessage), [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature), and [**DecryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) functions to exchange signed or encrypted application data with the remote computer.</span></span>

<span data-ttu-id="eb98e-105">Le sezioni seguenti illustrano alcuni esempi che usano queste funzioni dopo aver stabilito un [*contesto di sicurezza*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="eb98e-105">Examples that use these functions after a [*security context*](../secgloss/s-gly.md) has been established are demonstrated in the following sections:</span></span>

-   [<span data-ttu-id="eb98e-106">Firma di un messaggio</span><span class="sxs-lookup"><span data-stu-id="eb98e-106">Signing a Message</span></span>](signing-a-message.md)
-   [<span data-ttu-id="eb98e-107">Verifica di un messaggio</span><span class="sxs-lookup"><span data-stu-id="eb98e-107">Verifying a Message</span></span>](verifying-a-message.md)
-   [<span data-ttu-id="eb98e-108">Crittografia di un messaggio</span><span class="sxs-lookup"><span data-stu-id="eb98e-108">Encrypting a Message</span></span>](encrypting-a-message.md)
-   [<span data-ttu-id="eb98e-109">Decrittografia di un messaggio</span><span class="sxs-lookup"><span data-stu-id="eb98e-109">Decrypting a Message</span></span>](decrypting-a-message.md)

 

 

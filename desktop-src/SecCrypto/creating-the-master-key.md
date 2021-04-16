---
description: Una chiave master è un materiale dati chiave da cui derivano altre chiavi.
ms.assetid: c8445f74-659a-470b-9007-07ea98d36dcd
title: Creazione della chiave master
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b35a6aef52525bdce622355ede4ae9723f7cd8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525740"
---
# <a name="creating-the-master-key"></a><span data-ttu-id="949d4-103">Creazione della chiave master</span><span class="sxs-lookup"><span data-stu-id="949d4-103">Creating the Master Key</span></span>

<span data-ttu-id="949d4-104">Una [*chiave master*](../secgloss/m-gly.md) è un materiale dati chiave da cui derivano altre chiavi.</span><span class="sxs-lookup"><span data-stu-id="949d4-104">A [*master key*](../secgloss/m-gly.md) is key data material from which other keys are derived.</span></span> <span data-ttu-id="949d4-105">A seconda del protocollo e del pacchetto di crittografia utilizzati, la chiave master può avere una lunghezza compresa tra 5 e 48 byte.</span><span class="sxs-lookup"><span data-stu-id="949d4-105">Depending on the protocol and cipher suite used, the master key can be from 5 to 48 bytes in length.</span></span> <span data-ttu-id="949d4-106">Per il [](../secgloss/r-gly.md) / CSP [*Schannel*](../secgloss/s-gly.md) RSA, la chiave master viene creata dal lato client e trasferita al server in una busta RSA.</span><span class="sxs-lookup"><span data-stu-id="949d4-106">For the [*RSA*](../secgloss/r-gly.md)/[*Schannel*](../secgloss/s-gly.md) CSP, the master key is created by the client-side and transferred to the server in an RSA envelope.</span></span> <span data-ttu-id="949d4-107">Per un CSP/SChannel di [*Diffie-Hellman*](../secgloss/d-gly.md), la chiave master viene creata eseguendo uno scambio di chiave Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="949d4-107">For a [*Diffie-Hellman*](../secgloss/d-gly.md)/Schannel CSP, the master key is created by performing a Diffie-Hellman key exchange.</span></span>

<span data-ttu-id="949d4-108">Il codice per la creazione e lo scambio di chiavi master è illustrato in:</span><span class="sxs-lookup"><span data-stu-id="949d4-108">Code for creating and exchanging master keys is demonstrated in:</span></span>

-   [<span data-ttu-id="949d4-109">Codice client Diffie-Hellman per la creazione della chiave master</span><span class="sxs-lookup"><span data-stu-id="949d4-109">Diffie-Hellman Client Code for Creating the Master Key</span></span>](diffie-hellman-client-code-for-creating-the-master-key.md)
-   [<span data-ttu-id="949d4-110">Codice server Diffie-Hellman per la creazione della chiave master</span><span class="sxs-lookup"><span data-stu-id="949d4-110">Diffie-Hellman Server Code for Creating the Master Key</span></span>](diffie-hellman-server-code-for-creating-the-master-key.md)
-   [<span data-ttu-id="949d4-111">Codice client RSA per la creazione della chiave master</span><span class="sxs-lookup"><span data-stu-id="949d4-111">RSA Client Code for Creating the Master Key</span></span>](rsa-client-code-for-creating-the-master-key.md)
-   [<span data-ttu-id="949d4-112">Codice server RSA per la creazione della chiave master</span><span class="sxs-lookup"><span data-stu-id="949d4-112">RSA Server Code for Creating the Master Key</span></span>](rsa-server-code-for-creating-the-master-key.md)
-   [<span data-ttu-id="949d4-113">Specifica degli algoritmi</span><span class="sxs-lookup"><span data-stu-id="949d4-113">Specifying the Algorithms</span></span>](specifying-the-algorithms.md)

 

 

---
description: Le credenziali utente sono necessarie per Microsoft Digest; sia il client che il server devono presentare credenziali valide prima di poter stabilire un contesto di sicurezza per lo scambio di messaggi. Gli handle delle credenziali vengono utilizzati per ottenere e presentare le credenziali.
ms.assetid: f97bdaf6-40a8-414e-a561-d3cb953d0bab
title: Acquisizione di Microsoft Digest credenziali SSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c61895ecc8e49713665af4542689729bc491d9e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484709"
---
# <a name="obtaining-microsoft-digest-ssp-credentials"></a><span data-ttu-id="661bb-104">Acquisizione di Microsoft Digest credenziali SSP</span><span class="sxs-lookup"><span data-stu-id="661bb-104">Obtaining Microsoft Digest SSP Credentials</span></span>

<span data-ttu-id="661bb-105">Le [*credenziali*](../secgloss/c-gly.md) utente sono necessarie per Microsoft Digest; sia il client che il server devono presentare credenziali valide prima di poter stabilire un [*contesto di sicurezza*](../secgloss/s-gly.md) per lo scambio di messaggi.</span><span class="sxs-lookup"><span data-stu-id="661bb-105">User [*credentials*](../secgloss/c-gly.md) are required by Microsoft Digest; both client and server must present valid credentials before they can establish a [*security context*](../secgloss/s-gly.md) for message exchange.</span></span> <span data-ttu-id="661bb-106">Gli handle delle credenziali vengono utilizzati per ottenere e presentare le credenziali.</span><span class="sxs-lookup"><span data-stu-id="661bb-106">Credentials handles are used to obtain and present credentials.</span></span>

<span data-ttu-id="661bb-107">Poiché l'handle delle credenziali viene utilizzato per archiviare le informazioni di configurazione, non è possibile utilizzare lo stesso handle sia per le operazioni sul lato client che sul lato server.</span><span class="sxs-lookup"><span data-stu-id="661bb-107">Because the credential handle is used to store configuration information, the same handle cannot be used for both client-side and server-side operations.</span></span> <span data-ttu-id="661bb-108">Ciò significa che le applicazioni che supportano le connessioni client e server devono ottenere almeno due handle di credenziali.</span><span class="sxs-lookup"><span data-stu-id="661bb-108">This means that applications that support both client and server connections must obtain a minimum of two credentials handles.</span></span>

<span data-ttu-id="661bb-109">Per ottenere un handle per le credenziali richieste da Microsoft Digest, chiamare la funzione [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) .</span><span class="sxs-lookup"><span data-stu-id="661bb-109">To get a handle to the credentials required by Microsoft Digest, call the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function.</span></span>

<span data-ttu-id="661bb-110">Negli esempi di linguaggio C seguenti viene illustrato come ottenere le credenziali.</span><span class="sxs-lookup"><span data-stu-id="661bb-110">The following C language examples demonstrate obtaining credentials.</span></span>

-   [<span data-ttu-id="661bb-111">Recupero delle credenziali del digest predefinite</span><span class="sxs-lookup"><span data-stu-id="661bb-111">Obtaining Default Digest Credentials</span></span>](obtaining-default-digest-credentials.md)
-   [<span data-ttu-id="661bb-112">Acquisizione di credenziali del digest alternative</span><span class="sxs-lookup"><span data-stu-id="661bb-112">Obtaining Alternate Digest Credentials</span></span>](obtaining-alternate-digest-credentials.md)

 

 

---
description: Quando viene avviato, un client seleziona un pacchetto di sicurezza per le transazioni con un server e quindi contatta tale server. Un server seleziona uno o più pacchetti di sicurezza ed è in attesa di una connessione client.
ms.assetid: eaed162b-ef07-4295-93d9-6be91232a82e
title: Ottenere informazioni sui pacchetti di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca690575ff7f46ef5a5b1d971b1ab9fdd91f95e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129923"
---
# <a name="getting-information-about-security-packages"></a><span data-ttu-id="38bd5-104">Ottenere informazioni sui pacchetti di sicurezza</span><span class="sxs-lookup"><span data-stu-id="38bd5-104">Getting Information About Security Packages</span></span>

<span data-ttu-id="38bd5-105">Quando viene avviato, un client seleziona un [*pacchetto di sicurezza*](/windows/desktop/SecGloss/s-gly) per le transazioni con un server e quindi contatta tale server.</span><span class="sxs-lookup"><span data-stu-id="38bd5-105">When a client begins, it selects a [*security package*](/windows/desktop/SecGloss/s-gly) for its transactions with a server and then contacts that server.</span></span> <span data-ttu-id="38bd5-106">Un server seleziona uno o più pacchetti di sicurezza ed è in attesa di una connessione client.</span><span class="sxs-lookup"><span data-stu-id="38bd5-106">A server selects one or more security packages and waits for a client connection.</span></span>

<span data-ttu-id="38bd5-107">Per informazioni specifiche sui pacchetti di sicurezza SSPI disponibili con un particolare SSP, è possibile chiamare la funzione [**EnumerateSecurityPackages**](/windows/desktop/api/Sspi/nf-sspi-enumeratesecuritypackagesa) per recuperare una struttura [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) .</span><span class="sxs-lookup"><span data-stu-id="38bd5-107">For specific information about the SSPI security packages available with a particular SSP, the [**EnumerateSecurityPackages**](/windows/desktop/api/Sspi/nf-sspi-enumeratesecuritypackagesa) function can be called to retrieve a [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) structure.</span></span>

<span data-ttu-id="38bd5-108">Per recuperare la struttura di output, il chiamante passa alla funzione l'indirizzo di un puntatore al tipo della struttura restituita.</span><span class="sxs-lookup"><span data-stu-id="38bd5-108">To retrieve the output structure, the caller passes to the function the address of a pointer to the type of the return structure.</span></span> <span data-ttu-id="38bd5-109">La funzione alloca memoria e restituisce i dati al chiamante assegnando l'indirizzo del buffer dei dati restituiti all'argomento.</span><span class="sxs-lookup"><span data-stu-id="38bd5-109">The function allocates memory and returns the data to the caller by assigning the address of the return data buffer to the argument.</span></span> <span data-ttu-id="38bd5-110">La convenzione SSPI è che la funzione alloca memoria per la struttura e l'applicazione chiamante libera tale memoria utilizzando [**FreeContextBuffer**](/windows/desktop/api/Sspi/nf-sspi-freecontextbuffer).</span><span class="sxs-lookup"><span data-stu-id="38bd5-110">The SSPI convention is that the function allocates memory for the structure, and the calling application frees that memory using [**FreeContextBuffer**](/windows/desktop/api/Sspi/nf-sspi-freecontextbuffer).</span></span>

<span data-ttu-id="38bd5-111">La chiamata della funzione [**QuerySecurityPackageInfo**](/windows/desktop/api/Sspi/nf-sspi-querysecuritypackageinfoa) recupera gli attributi di un [*pacchetto di sicurezza*](/windows/desktop/SecGloss/s-gly).</span><span class="sxs-lookup"><span data-stu-id="38bd5-111">Calling the [**QuerySecurityPackageInfo**](/windows/desktop/api/Sspi/nf-sspi-querysecuritypackageinfoa) function retrieves the attributes of a [*security package*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="38bd5-112">Sia il server che il client possono chiamare la funzione **QuerySecurityPackageInfo** per ottenere la lunghezza massima del token di sicurezza dal membro **CbMaxToken** della struttura [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) .</span><span class="sxs-lookup"><span data-stu-id="38bd5-112">Both server and client can call the **QuerySecurityPackageInfo** function to get the maximum length of the security token from the **cbMaxToken** member of the [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) structure.</span></span> <span data-ttu-id="38bd5-113">Per un esempio, vedere la chiamata alla funzione **QuerySecurityPackageInfo** illustrata in [uso di SSPI con un server Windows Sockets](using-sspi-with-a-windows-sockets-server.md).</span><span class="sxs-lookup"><span data-stu-id="38bd5-113">For an example, see the call to the **QuerySecurityPackageInfo** function shown in [Using SSPI with a Windows Sockets Server](using-sspi-with-a-windows-sockets-server.md).</span></span>

<span data-ttu-id="38bd5-114">Per ulteriori informazioni sulle funzioni del pacchetto, vedere [Gestione pacchetti](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="38bd5-114">For more information on package functions, see [Package Management](authentication-functions.md).</span></span>

 

 

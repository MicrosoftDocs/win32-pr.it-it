---
description: Microsoft Negotiate è un Security Support Provider che funge da livello di applicazione tra l'interfaccia del provider di supporto della sicurezza e gli altri SSP.
ms.assetid: 3aa7e979-8b55-416d-bed1-28296055d38e
title: Negoziazione Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7ce57a8f8924120dcce51e50e05de90fd6774b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966625"
---
# <a name="microsoft-negotiate"></a><span data-ttu-id="63822-103">Negoziazione Microsoft</span><span class="sxs-lookup"><span data-stu-id="63822-103">Microsoft Negotiate</span></span>

<span data-ttu-id="63822-104">Microsoft Negotiate è un [*Security Support Provider*](../secgloss/s-gly.md) (SSP) che funge da livello di applicazione tra [*Security Support Provider Interface*](../secgloss/s-gly.md) ([SSPI](sspi.md)) e gli altri SSP.</span><span class="sxs-lookup"><span data-stu-id="63822-104">Microsoft Negotiate is a [*security support provider*](../secgloss/s-gly.md) (SSP) that acts as an application layer between [*Security Support Provider Interface*](../secgloss/s-gly.md) ([SSPI](sspi.md)) and the other SSPs.</span></span> <span data-ttu-id="63822-105">Un'applicazione che chiama l'interfaccia SSPI per accedere a una rete può specificare un provider SSP per l'elaborazione della richiesta.</span><span class="sxs-lookup"><span data-stu-id="63822-105">When an application calls into SSPI to log on to a network, it can specify an SSP to process the request.</span></span> <span data-ttu-id="63822-106">Se l'applicazione specifica Negotiate, Negotiate analizza la richiesta e sceglie il provider SSP migliore per gestire la richiesta in base ai criteri di sicurezza configurati dal cliente.</span><span class="sxs-lookup"><span data-stu-id="63822-106">If the application specifies Negotiate, Negotiate analyzes the request and picks the best SSP to handle the request based on customer-configured security policy.</span></span>

<span data-ttu-id="63822-107">Attualmente, il pacchetto di sicurezza Negotiate seleziona tra [Kerberos](microsoft-kerberos.md) e [NTLM](microsoft-ntlm.md).</span><span class="sxs-lookup"><span data-stu-id="63822-107">Currently, the Negotiate security package selects between [Kerberos](microsoft-kerberos.md) and [NTLM](microsoft-ntlm.md).</span></span> <span data-ttu-id="63822-108">Negotiate seleziona Kerberos, a meno che non possa essere utilizzato da uno dei sistemi interessati dall'autenticazione o se l'applicazione chiamante non ha fornito informazioni sufficienti per l'utilizzo di Kerberos.</span><span class="sxs-lookup"><span data-stu-id="63822-108">Negotiate selects Kerberos unless it cannot be used by one of the systems involved in the authentication or the calling application did not provide sufficient information to use Kerberos.</span></span>

<span data-ttu-id="63822-109">Per consentire a Negotiate di selezionare il provider di sicurezza [Kerberos](microsoft-kerberos.md) , l'applicazione client deve fornire un [*nome dell'entità servizio*](../secgloss/s-gly.md) (SPN), un nome dell'entità utente (UPN) o un nome di account NetBIOS come nome di destinazione.</span><span class="sxs-lookup"><span data-stu-id="63822-109">To allow Negotiate to select the [Kerberos](microsoft-kerberos.md) security provider, the client application must provide a [*service principal name*](../secgloss/s-gly.md) (SPN), a user principal name (UPN), or a NetBIOS account name as the target name.</span></span> <span data-ttu-id="63822-110">In caso contrario, Negotiate seleziona sempre il provider di sicurezza [NTLM](microsoft-ntlm.md) .</span><span class="sxs-lookup"><span data-stu-id="63822-110">Otherwise, Negotiate always selects the [NTLM](microsoft-ntlm.md) security provider.</span></span>

<span data-ttu-id="63822-111">Un server che utilizza il pacchetto Negotiate è in grado di rispondere alle applicazioni client che selezionano in modo specifico il provider di sicurezza [Kerberos](microsoft-kerberos.md) o [NTLM](microsoft-ntlm.md) .</span><span class="sxs-lookup"><span data-stu-id="63822-111">A server that uses the Negotiate package is able to respond to client applications that specifically select either the [Kerberos](microsoft-kerberos.md) or [NTLM](microsoft-ntlm.md) security provider.</span></span> <span data-ttu-id="63822-112">È tuttavia necessario che un'applicazione client sappia che un server supporta il pacchetto Negotiate per richiedere l'autenticazione tramite Negotiate.</span><span class="sxs-lookup"><span data-stu-id="63822-112">However, a client application must know that a server supports the Negotiate package to request authentication using Negotiate.</span></span> <span data-ttu-id="63822-113">Un server che non supporta Negotiate non è sempre in grado di rispondere alle richieste provenienti dai client che specificano Negotiate come SSP.</span><span class="sxs-lookup"><span data-stu-id="63822-113">A server that does not support Negotiate cannot always respond to requests from clients that specify Negotiate as the SSP.</span></span>

## <a name="reasons-to-use-the-negotiate-package"></a><span data-ttu-id="63822-114">Motivi per utilizzare il pacchetto Negotiate</span><span class="sxs-lookup"><span data-stu-id="63822-114">Reasons to Use the Negotiate Package</span></span>

-   <span data-ttu-id="63822-115">Consente al sistema di utilizzare il protocollo più sicuro disponibile.</span><span class="sxs-lookup"><span data-stu-id="63822-115">Allows the system to use the strongest (most secure) available protocol.</span></span>
-   <span data-ttu-id="63822-116">Garantisce la compatibilità con le edizioni con le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="63822-116">Ensures forward compatibility for your application.</span></span>
-   <span data-ttu-id="63822-117">Garantisce che l'applicazione mostri il comportamento in base ai criteri di sicurezza impostati dal cliente.</span><span class="sxs-lookup"><span data-stu-id="63822-117">Ensures that your application exhibits behavior that is in accordance with the security policy set by the customer.</span></span>

 

 

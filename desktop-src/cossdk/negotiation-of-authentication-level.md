---
description: Negoziazione del livello di autenticazione
ms.assetid: 31353d02-bfe2-48ac-81a1-0e38895a8a75
title: Negoziazione del livello di autenticazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38b9983bd2a2df1d85cc6df4bfc0ba2a757b200f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305322"
---
# <a name="negotiation-of-authentication-level"></a><span data-ttu-id="97102-103">Negoziazione del livello di autenticazione</span><span class="sxs-lookup"><span data-stu-id="97102-103">Negotiation of Authentication Level</span></span>

<span data-ttu-id="97102-104">Sia il client che il server devono partecipare all'autenticazione e ogni entità indica che desidera eseguire un determinato livello di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="97102-104">Both client and server must participate in authentication, and each party indicates that it wants to perform a certain level of authentication.</span></span> <span data-ttu-id="97102-105">All'inizio di una chiamata, il livello di autenticazione viene negoziato tra le due parti, viene scelto un servizio appropriato e la chiamata viene autenticata e procede con la possibile crittografia, a seconda del livello di autenticazione scelto.</span><span class="sxs-lookup"><span data-stu-id="97102-105">At the beginning of a call, the authentication level is negotiated between the two parties, an appropriate service is chosen, and the call is authenticated and proceeds (with possible encryption, depending on the authentication level chosen).</span></span> <span data-ttu-id="97102-106">Il livello di autenticazione negoziato tra il client e il server è determinato come massimo (*preferenza client*, *preferenza server*).</span><span class="sxs-lookup"><span data-stu-id="97102-106">The authentication level negotiated between client and server is determined as Maximum(*Client preference*, *Server preference*).</span></span> <span data-ttu-id="97102-107">L'effetto di questo significa che il server può sempre stabilire un livello minimo di autenticazione con cui è confortevole; ovvero l'autenticazione può essere dettata amministrativamente dal server.</span><span class="sxs-lookup"><span data-stu-id="97102-107">The effect of this means that the server can always dictate a minimum level of authentication that it is comfortable with; that is, authentication can be administratively dictated from the server.</span></span>

<span data-ttu-id="97102-108">Il client specifica che desidera eseguire l'autenticazione a un determinato livello come con qualsiasi applicazione COM.</span><span class="sxs-lookup"><span data-stu-id="97102-108">The client specifies that it wants to perform authentication at a certain level as with any COM application.</span></span> <span data-ttu-id="97102-109">Il livello di autenticazione client può essere indicato come segue:</span><span class="sxs-lookup"><span data-stu-id="97102-109">The client authentication level can be indicated as follows:</span></span>

-   <span data-ttu-id="97102-110">Per ogni computer client, con il livello di autenticazione COM a livello di computer impostato utilizzando [DCOMCNFG](/windows/desktop/com/setting-machine-wide-security-using-dcomcnfg) o lo strumento di amministrazione Servizi componenti.</span><span class="sxs-lookup"><span data-stu-id="97102-110">Per client machine, with the machine-wide COM authentication level set by using either [DCOMCNFG](/windows/desktop/com/setting-machine-wide-security-using-dcomcnfg) or the Component Services administrative tool.</span></span>
-   <span data-ttu-id="97102-111">Per applicazione client amministrativa, utilizzando [DCOMCNFG](/windows/desktop/com/setting-processwide-security-using-dcomcnfg) o lo strumento di amministrazione Servizi componenti se il client deve essere un'applicazione com+.</span><span class="sxs-lookup"><span data-stu-id="97102-111">Per client application administratively, using [DCOMCNFG](/windows/desktop/com/setting-processwide-security-using-dcomcnfg) or using the Component Services administrative tool if the client should be a COM+ application.</span></span>
-   <span data-ttu-id="97102-112">Per processo client a livello di codice, con [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="97102-112">Per client process programmatically, with [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>
-   <span data-ttu-id="97102-113">In qualsiasi momento a livello di codice, usando [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="97102-113">At any point programmatically, using [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

<span data-ttu-id="97102-114">L'applicazione server COM+ specifica un livello di autenticazione amministrativo utilizzando lo strumento di amministrazione Servizi componenti (o tramite uno script amministrativo).</span><span class="sxs-lookup"><span data-stu-id="97102-114">The COM+ server application specifies an authentication level administratively by using the Component Services administrative tool (or through an administrative script).</span></span>

<span data-ttu-id="97102-115">La negoziazione dell'autenticazione per una chiamata procede nella sequenza seguente:</span><span class="sxs-lookup"><span data-stu-id="97102-115">Negotiating authentication for a call proceeds in the following sequence:</span></span>

1.  <span data-ttu-id="97102-116">Il livello di autenticazione viene scelto come MAX (*client*, *Server*).</span><span class="sxs-lookup"><span data-stu-id="97102-116">Authentication level is chosen as MAX(*client*, *server*).</span></span>
2.  <span data-ttu-id="97102-117">Negoziazione del protocollo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="97102-117">Negotiation of authentication protocol.</span></span>
3.  <span data-ttu-id="97102-118">Il server autentica l'identità del client.</span><span class="sxs-lookup"><span data-stu-id="97102-118">Server authenticates client identity.</span></span>
4.  <span data-ttu-id="97102-119">Facoltativamente, il client autentica l'identità del server, a seconda del protocollo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="97102-119">Optionally, client authenticates server identity, depending on the authentication protocol.</span></span>
5.  <span data-ttu-id="97102-120">Le chiamate al metodo vengono comunicate con il livello di autenticazione scelto.</span><span class="sxs-lookup"><span data-stu-id="97102-120">Method calls are communicated with the chosen level of authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97102-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="97102-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97102-122">Autenticazione client</span><span class="sxs-lookup"><span data-stu-id="97102-122">Client Authentication</span></span>](client-authentication.md)
</dt> </dl>

 

 

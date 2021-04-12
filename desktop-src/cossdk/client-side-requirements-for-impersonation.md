---
description: Client-Side requisiti per la rappresentazione
ms.assetid: c2d20233-93c6-4d2d-946d-8abccbeb3c5e
title: Client-Side requisiti per la rappresentazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c3c188f3c03e46a0e6e414efc66c5fdd2366d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342411"
---
# <a name="client-side-requirements-for-impersonation"></a><span data-ttu-id="71fa0-103">Client-Side requisiti per la rappresentazione</span><span class="sxs-lookup"><span data-stu-id="71fa0-103">Client-Side Requirements for Impersonation</span></span>

<span data-ttu-id="71fa0-104">È possibile specificare le due impostazioni seguenti rispetto alla rappresentazione sul lato client:</span><span class="sxs-lookup"><span data-stu-id="71fa0-104">The following two settings can be specified relative to impersonation on the client side:</span></span>

-   <span data-ttu-id="71fa0-105">Livello di rappresentazione, che indica la volontà del client di usare la propria identità del server.</span><span class="sxs-lookup"><span data-stu-id="71fa0-105">Impersonation level, which indicates the client's willingness to have the server use its identity.</span></span>
-   <span data-ttu-id="71fa0-106">Impostazione nel servizio Active Directory tramite la quale l'account client può essere contrassegnato come "account è sensibile e non può essere delegato", che disabilita la delega.</span><span class="sxs-lookup"><span data-stu-id="71fa0-106">A setting in the Active Directory Service through which the client account can be marked "Account is sensitive and cannot be delegated," which will disable delegation.</span></span>

<span data-ttu-id="71fa0-107">Il livello di rappresentazione può essere impostato in diversi modi.</span><span class="sxs-lookup"><span data-stu-id="71fa0-107">The impersonation level can be set in a variety of ways.</span></span> <span data-ttu-id="71fa0-108">Se il client non indica un livello di rappresentazione, il valore predefinito a livello di computer verrà utilizzato da COM.</span><span class="sxs-lookup"><span data-stu-id="71fa0-108">If the client does not indicate an impersonation level, the machine-wide default will be used by COM.</span></span> <span data-ttu-id="71fa0-109">Il valore predefinito a livello di computer può essere impostato utilizzando lo strumento di amministrazione Servizi componenti o Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="71fa0-109">The machine-wide default can be set using either the Component Services administrative tool or Dcomcnfg.exe.</span></span> <span data-ttu-id="71fa0-110">Il client può anche indicare un livello di rappresentazione preferito in maniera amministrativa con Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="71fa0-110">The client can also indicate a preferred impersonation level administratively with Dcomcnfg.exe.</span></span>

<span data-ttu-id="71fa0-111">Il client può indicare il livello di rappresentazione a livello di codice, utilizzando [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), equivalente a [**IClientSecurity:: seblankt**](/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket), che può essere chiamato ogni volta che è necessario, o [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), che può essere chiamato una volta per processo.</span><span class="sxs-lookup"><span data-stu-id="71fa0-111">The client can indicate the impersonation level programmatically, using either [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)—equivalent to [**IClientSecurity::SetBlanket**](/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket), which can be called as often as necessary—or [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), which can be called once per process.</span></span>

<span data-ttu-id="71fa0-112">Se il client indica una rappresentazione a livello di delegato, ovvero l'autorità più ampia che può concedere al server, il client deve essere in esecuzione con un'identità configurata correttamente nel servizio Active Directory per consentire la delega dell'identità.</span><span class="sxs-lookup"><span data-stu-id="71fa0-112">If the client indicates delegate-level impersonation—the broadest authority it can grant to the server—the client should be running under an identity that is properly configured in the Active Directory Service to enable its identity to be delegated.</span></span>

<span data-ttu-id="71fa0-113">Per informazioni più dettagliate sui livelli di rappresentazione e sui requisiti per il funzionamento della delega, vedere [delega e rappresentazione](/windows/desktop/com/delegation-and-impersonation).</span><span class="sxs-lookup"><span data-stu-id="71fa0-113">For more detail regarding impersonation levels and the requirements for delegation to work, see [Delegation and Impersonation](/windows/desktop/com/delegation-and-impersonation).</span></span>

<span data-ttu-id="71fa0-114">Naturalmente, le applicazioni COM+ possono fungere sempre da client.</span><span class="sxs-lookup"><span data-stu-id="71fa0-114">COM+ applications can always act as clients, of course.</span></span> <span data-ttu-id="71fa0-115">Quando l'applicazione COM+ effettua una chiamata a un'altra applicazione o risorsa, esprime un livello di rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="71fa0-115">When the COM+ application makes a call to another application or resource, it expresses an impersonation level.</span></span> <span data-ttu-id="71fa0-116">Per le applicazioni server COM+, è possibile impostare un livello di rappresentazione in modo amministrativo.</span><span class="sxs-lookup"><span data-stu-id="71fa0-116">For COM+ server applications, you can set an impersonation level administratively.</span></span> <span data-ttu-id="71fa0-117">Le applicazioni della libreria COM+ non possono impostare il proprio livello di rappresentazione; usano invece quello del processo host.</span><span class="sxs-lookup"><span data-stu-id="71fa0-117">COM+ library applications cannot set their own impersonation level; they use that of the host process instead.</span></span> <span data-ttu-id="71fa0-118">Per informazioni su come impostare la rappresentazione per un'applicazione COM+, vedere [impostazione di un livello di rappresentazione](setting-an-impersonation-level.md).</span><span class="sxs-lookup"><span data-stu-id="71fa0-118">To learn how to set impersonation for a COM+ application, see [Setting an Impersonation Level](setting-an-impersonation-level.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="71fa0-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="71fa0-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71fa0-120">Rappresentazione e delega client</span><span class="sxs-lookup"><span data-stu-id="71fa0-120">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="71fa0-121">Cloaking</span><span class="sxs-lookup"><span data-stu-id="71fa0-121">Cloaking</span></span>](cloaking.md)
</dt> <dt>

[<span data-ttu-id="71fa0-122">Requisiti lato server per la rappresentazione</span><span class="sxs-lookup"><span data-stu-id="71fa0-122">Server-Side Requirements for Impersonation</span></span>](server-side-requirements-for-impersonation.md)
</dt> </dl>

 

 

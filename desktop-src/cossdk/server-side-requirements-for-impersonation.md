---
description: Server-Side requisiti per la rappresentazione
ms.assetid: f6128688-dfd8-40ff-83ec-99d740b9152c
title: Server-Side requisiti per la rappresentazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e30edbebd37035ab7a7f4ca09e1cff73c2afbabe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304808"
---
# <a name="server-side-requirements-for-impersonation"></a><span data-ttu-id="5de40-103">Server-Side requisiti per la rappresentazione</span><span class="sxs-lookup"><span data-stu-id="5de40-103">Server-Side Requirements for Impersonation</span></span>

<span data-ttu-id="5de40-104">Il server esegue la rappresentazione a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="5de40-104">The server performs impersonation programmatically.</span></span> <span data-ttu-id="5de40-105">Presuppone in modo esplicito le credenziali di sicurezza del client usando [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient).</span><span class="sxs-lookup"><span data-stu-id="5de40-105">It explicitly assumes the client's security credentials by using [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient).</span></span> <span data-ttu-id="5de40-106">Quando il client ha concesso al server un'autorità sufficiente, questo ha l'effetto di sostituire le credenziali di sicurezza del client con il token del thread del server, al posto del token di processo.</span><span class="sxs-lookup"><span data-stu-id="5de40-106">When the client has granted the server sufficient authority, this has the effect of substituting the client's security credentials with the server thread token, in place of the process token.</span></span>

<span data-ttu-id="5de40-107">Al termine di questa operazione, il server può, ad esempio, usare il token client per accedere alle risorse sorvegliate con un descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="5de40-107">When this has been done, the server can, for example, use the client token to access resources guarded with a security descriptor.</span></span> <span data-ttu-id="5de40-108">In alternativa, può effettuare chiamate sotto l'identità del client, se il mascheramento è abilitato.</span><span class="sxs-lookup"><span data-stu-id="5de40-108">Or it can make calls under the client identity, if cloaking is enabled.</span></span>

<span data-ttu-id="5de40-109">Il server può impostare in modo esplicito il mascheramento a livello di codice oppure può basarsi su un'impostazione amministrativa.</span><span class="sxs-lookup"><span data-stu-id="5de40-109">The server can explicitly set cloaking programmatically, or it can rely on an administrative setting.</span></span> <span data-ttu-id="5de40-110">Per impostazione predefinita, le applicazioni COM+ sono configurate per l'utilizzo del mascheramento dinamico.</span><span class="sxs-lookup"><span data-stu-id="5de40-110">By default, COM+ applications are configured to use dynamic cloaking.</span></span> <span data-ttu-id="5de40-111">Per informazioni dettagliate, vedere [mascheramento](cloaking.md).</span><span class="sxs-lookup"><span data-stu-id="5de40-111">For more detail, see [Cloaking](cloaking.md).</span></span>

<span data-ttu-id="5de40-112">Se il server sta implementando la delega per conto del client, utilizzando l'identità client sulla rete, l'identità del processo server deve essere contrassegnata come "trusted per la delega" nel servizio Active Directory; in caso contrario, la delega avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="5de40-112">If the server is implementing delegation on behalf of the client—using the client identity over network—the server process identity must be marked as "Trusted for delegation" in the Active Directory Service; otherwise, delegation will fail.</span></span>

<span data-ttu-id="5de40-113">Al termine dell'utilizzo dell'identità del client, il server può ripristinare il proprio token di processo utilizzando [**CoRevertToSelf**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself).</span><span class="sxs-lookup"><span data-stu-id="5de40-113">When it has finished using the client's identity, the server can revert to its own process token using [**CoRevertToSelf**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself).</span></span>

<span data-ttu-id="5de40-114">Per informazioni dettagliate sull'implementazione della rappresentazione e della delega, vedere [delega e rappresentazione](/windows/desktop/com/delegation-and-impersonation).</span><span class="sxs-lookup"><span data-stu-id="5de40-114">For details on implementing impersonation and delegation, see [Delegation and Impersonation](/windows/desktop/com/delegation-and-impersonation).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5de40-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5de40-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5de40-116">Rappresentazione e delega client</span><span class="sxs-lookup"><span data-stu-id="5de40-116">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="5de40-117">Requisiti lato client per la rappresentazione</span><span class="sxs-lookup"><span data-stu-id="5de40-117">Client-Side Requirements for Impersonation</span></span>](client-side-requirements-for-impersonation.md)
</dt> <dt>

[<span data-ttu-id="5de40-118">Cloaking</span><span class="sxs-lookup"><span data-stu-id="5de40-118">Cloaking</span></span>](cloaking.md)
</dt> </dl>

 

 

---
title: Sicurezza Server-Side
description: Sicurezza Server-Side
ms.assetid: 6c1d210e-daf0-490a-a6b9-65d99b9e1d7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77501c395c3ae1f14c8451d4691e7e776545e756
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963493"
---
# <a name="server-side-security"></a><span data-ttu-id="62672-103">Sicurezza Server-Side</span><span class="sxs-lookup"><span data-stu-id="62672-103">Server-Side Security</span></span>

<span data-ttu-id="62672-104">Il server può recuperare le informazioni di sicurezza relative a un chiamante o rappresentare il chiamante utilizzando i metodi di [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity).</span><span class="sxs-lookup"><span data-stu-id="62672-104">The server can retrieve security information about a caller or impersonate the caller by using the methods of [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity).</span></span> <span data-ttu-id="62672-105">Un'implementazione di **IServerSecurity** viene fornita da com nell'oggetto Context per la chiamata corrente quando viene utilizzato il marshalling standard.</span><span class="sxs-lookup"><span data-stu-id="62672-105">An implementation of **IServerSecurity** is supplied by COM on the context object for the current call when standard marshaling is used.</span></span> <span data-ttu-id="62672-106">Questa interfaccia potrebbe tuttavia essere assente per alcune interfacce con marshalling personalizzato.</span><span class="sxs-lookup"><span data-stu-id="62672-106">However, this interface may be absent for some custom-marshaled interfaces.</span></span>

<span data-ttu-id="62672-107">Quando arriva una chiamata al server, il server può chiamare [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) per ottenere un puntatore all'interfaccia [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) .</span><span class="sxs-lookup"><span data-stu-id="62672-107">When a call arrives at the server, the server can call [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) to obtain a pointer to the [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) interface.</span></span> <span data-ttu-id="62672-108">Con questo puntatore, i metodi **IServerSecurity** possono essere chiamati dal server per individuare le impostazioni di autenticazione del client e per rappresentare il client, se necessario.</span><span class="sxs-lookup"><span data-stu-id="62672-108">With this pointer, **IServerSecurity** methods can be called by the server to find out what the client's authentication settings are and to impersonate the client, if needed.</span></span> <span data-ttu-id="62672-109">L'oggetto **IServerSecurity** è valido in qualsiasi thread nell'Apartment finché la chiamata rappresentata da **IServerSecurity** non viene completata.</span><span class="sxs-lookup"><span data-stu-id="62672-109">The **IServerSecurity** object is valid on any thread in the apartment until the call represented by **IServerSecurity** completes.</span></span> <span data-ttu-id="62672-110">Per ulteriori informazioni sulla rappresentazione, vedere [rappresentazione](impersonation.md) e [mascheramento](cloaking.md).</span><span class="sxs-lookup"><span data-stu-id="62672-110">For more information about impersonation, see [Impersonation](impersonation.md) and [Cloaking](cloaking.md).</span></span>

<span data-ttu-id="62672-111">Sono disponibili anche le funzioni di supporto seguenti che si basano sull'implementazione dell'interfaccia [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) dell'oggetto contesto di chiamata:</span><span class="sxs-lookup"><span data-stu-id="62672-111">The following helper functions that rely on the call context object's [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) interface implementation are also available:</span></span>

-   [<span data-ttu-id="62672-112">**CoQueryClientBlanket**</span><span class="sxs-lookup"><span data-stu-id="62672-112">**CoQueryClientBlanket**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket)
-   [<span data-ttu-id="62672-113">**CoImpersonateClient**</span><span class="sxs-lookup"><span data-stu-id="62672-113">**CoImpersonateClient**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)
-   [<span data-ttu-id="62672-114">**CoRevertToSelf**</span><span class="sxs-lookup"><span data-stu-id="62672-114">**CoRevertToSelf**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself)

## <a name="related-topics"></a><span data-ttu-id="62672-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="62672-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62672-116">Sicurezza in COM</span><span class="sxs-lookup"><span data-stu-id="62672-116">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 
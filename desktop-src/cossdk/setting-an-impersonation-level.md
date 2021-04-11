---
description: Quando si imposta un livello di rappresentazione per un'applicazione, si determina il grado di autorità che l'applicazione concede ad altre applicazioni per utilizzarne l'identità quando viene chiamata.
ms.assetid: 5b5b2c2d-dc3d-4edd-9e13-e6cb13022ceb
title: Impostazione di un livello di rappresentazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1075ac3b10380892cdfdf770543a2dcbb32d56c8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127014"
---
# <a name="setting-an-impersonation-level"></a><span data-ttu-id="1bcb0-103">Impostazione di un livello di rappresentazione</span><span class="sxs-lookup"><span data-stu-id="1bcb0-103">Setting an Impersonation Level</span></span>

<span data-ttu-id="1bcb0-104">Quando si imposta un livello di rappresentazione per un'applicazione, si determina il grado di autorità che l'applicazione concede ad altre applicazioni per utilizzarne l'identità quando viene chiamata.</span><span class="sxs-lookup"><span data-stu-id="1bcb0-104">When you set an impersonation level for an application, you determine what degree of authority the application grants other applications to use its identity when it calls them.</span></span> <span data-ttu-id="1bcb0-105">È possibile impostare questa impostazione solo per le applicazioni server COM+: le applicazioni di libreria vengono eseguite con l'identità del processo di hosting e utilizzano il livello di rappresentazione specificato.</span><span class="sxs-lookup"><span data-stu-id="1bcb0-105">You can set this only for COM+ server applications—library applications run under the identity of the hosting process and use the impersonation level that it specifies.</span></span> <span data-ttu-id="1bcb0-106">Per informazioni dettagliate, vedere [livelli di rappresentazione](/windows/desktop/com/impersonation-levels).</span><span class="sxs-lookup"><span data-stu-id="1bcb0-106">For more detail, see [Impersonation Levels](/windows/desktop/com/impersonation-levels).</span></span>

<span data-ttu-id="1bcb0-107">**Per selezionare un livello di rappresentazione**</span><span class="sxs-lookup"><span data-stu-id="1bcb0-107">**To select an impersonation level**</span></span>

1.  <span data-ttu-id="1bcb0-108">Fare clic con il pulsante destro del mouse sull'applicazione COM+ per cui si imposta la rappresentazione e quindi scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="1bcb0-108">Right-click the COM+ application for which you are setting impersonation, and then click **Properties**.</span></span>

2.  <span data-ttu-id="1bcb0-109">Nella finestra di dialogo Proprietà applicazione fare clic sulla scheda **sicurezza** .</span><span class="sxs-lookup"><span data-stu-id="1bcb0-109">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="1bcb0-110">Nella casella **livello di rappresentazione** selezionare il livello appropriato.</span><span class="sxs-lookup"><span data-stu-id="1bcb0-110">In the **Impersonation level** box, select the appropriate level.</span></span> <span data-ttu-id="1bcb0-111">I livelli sono i seguenti, ordinati dalla concessione di almeno all'autorità più grande:</span><span class="sxs-lookup"><span data-stu-id="1bcb0-111">The levels are as follows, ordered from granting least to greatest authority:</span></span>

    -   <span data-ttu-id="1bcb0-112">**Anonimo**.</span><span class="sxs-lookup"><span data-stu-id="1bcb0-112">**Anonymous**.</span></span> <span data-ttu-id="1bcb0-113">Il client è anonimo per il server.</span><span class="sxs-lookup"><span data-stu-id="1bcb0-113">The client is anonymous to the server.</span></span> <span data-ttu-id="1bcb0-114">Il server può rappresentare il client, ma il token di rappresentazione (credenziale locale) non contiene informazioni sul client.</span><span class="sxs-lookup"><span data-stu-id="1bcb0-114">The server can impersonate the client, but the impersonation token (a local credential) does not contain any information about the client.</span></span>
    -   <span data-ttu-id="1bcb0-115">**Identificare**.</span><span class="sxs-lookup"><span data-stu-id="1bcb0-115">**Identify**.</span></span> <span data-ttu-id="1bcb0-116">Il server può ottenere l'identità del client e può rappresentare il client per eseguire controlli ACL.</span><span class="sxs-lookup"><span data-stu-id="1bcb0-116">The server can obtain the client's identity and can impersonate the client to do ACL checks.</span></span>
    -   <span data-ttu-id="1bcb0-117">**Rappresenta**.</span><span class="sxs-lookup"><span data-stu-id="1bcb0-117">**Impersonate**.</span></span> <span data-ttu-id="1bcb0-118">Il server può rappresentare il client mentre agisce per suo conto, sebbene con restrizioni.</span><span class="sxs-lookup"><span data-stu-id="1bcb0-118">The server can impersonate the client while acting on its behalf, although with restrictions.</span></span> <span data-ttu-id="1bcb0-119">Il server può accedere alle risorse nello stesso computer del client.</span><span class="sxs-lookup"><span data-stu-id="1bcb0-119">The server can access resources on the same computer as the client.</span></span> <span data-ttu-id="1bcb0-120">Se il server si trova nello stesso computer del client, può accedere alle risorse di rete come client.</span><span class="sxs-lookup"><span data-stu-id="1bcb0-120">If the server is on the same computer as the client, it can access network resources as the client.</span></span> <span data-ttu-id="1bcb0-121">Se il server si trova in un computer diverso da quello del client, può accedere solo alle risorse che si trovano nello stesso computer del server.</span><span class="sxs-lookup"><span data-stu-id="1bcb0-121">If the server is on a computer different from the client, it can access only resources that are on the same computer as the server.</span></span> <span data-ttu-id="1bcb0-122">Si tratta dell'impostazione predefinita per le applicazioni server COM+.</span><span class="sxs-lookup"><span data-stu-id="1bcb0-122">This is the default setting for COM+ server applications.</span></span>
    -   <span data-ttu-id="1bcb0-123">**Delegato**.</span><span class="sxs-lookup"><span data-stu-id="1bcb0-123">**Delegate**.</span></span> <span data-ttu-id="1bcb0-124">Il server può rappresentare il client mentre agisce per suo conto, sia nello stesso computer del client.</span><span class="sxs-lookup"><span data-stu-id="1bcb0-124">The server can impersonate the client while acting on its behalf, whether on the same computer as the client.</span></span> <span data-ttu-id="1bcb0-125">Durante la rappresentazione, le credenziali del client, sia quelle con la validità locale che quella con la validità della rete, possono essere passate a un numero qualsiasi di computer.</span><span class="sxs-lookup"><span data-stu-id="1bcb0-125">During impersonation, the client's credentials (both those with local and those with network validity) can be passed to any number of machines.</span></span>

4.  <span data-ttu-id="1bcb0-126">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="1bcb0-126">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1bcb0-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1bcb0-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bcb0-128">Configurazione della sicurezza Role-Based</span><span class="sxs-lookup"><span data-stu-id="1bcb0-128">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="1bcb0-129">Configurazione dei criteri di restrizione software</span><span class="sxs-lookup"><span data-stu-id="1bcb0-129">Configuring the Software Restriction Policy</span></span>](configuring-the-software-restriction-policy.md)
</dt> <dt>

[<span data-ttu-id="1bcb0-130">Abilitazione dell'autenticazione per un'applicazione di libreria</span><span class="sxs-lookup"><span data-stu-id="1bcb0-130">Enabling Authentication for a Library Application</span></span>](enabling-authentication-for-a-library-application.md)
</dt> <dt>

[<span data-ttu-id="1bcb0-131">Impostazione di un livello di autenticazione per un'applicazione server</span><span class="sxs-lookup"><span data-stu-id="1bcb0-131">Setting an Authentication Level for a Server Application</span></span>](setting-an-authentication-level-for-a-server-application.md)
</dt> </dl>

 

 

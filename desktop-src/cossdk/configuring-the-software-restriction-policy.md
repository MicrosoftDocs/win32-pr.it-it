---
description: Configurazione dei criteri di restrizione software
ms.assetid: 22c1897a-abb5-4ce9-9d09-21b6aed4f1d8
title: Configurazione dei criteri di restrizione software
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 522f216af6957ebd23bc9f17c70f61cab2cabc5c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049261"
---
# <a name="configuring-the-software-restriction-policy"></a><span data-ttu-id="fbcb6-103">Configurazione dei criteri di restrizione software</span><span class="sxs-lookup"><span data-stu-id="fbcb6-103">Configuring the Software Restriction Policy</span></span>

<span data-ttu-id="fbcb6-104">Quando si impostano in modo esplicito i livelli di attendibilità dei criteri di restrizione software di un'applicazione COM+, viene eseguito l'override delle impostazioni predefinite di a livello.</span><span class="sxs-lookup"><span data-stu-id="fbcb6-104">When you explicitly set the software restriction policy trust levels of a COM+ application, you are overriding the default systemwide settings.</span></span> <span data-ttu-id="fbcb6-105">Questa operazione è spesso necessaria per le applicazioni server COM+ perché il livello di attendibilità a livello è impostato sullo stesso per tutte le applicazioni server (perché tutti vengono eseguiti nello stesso file, dllhost.exe).</span><span class="sxs-lookup"><span data-stu-id="fbcb6-105">This is often necessary for COM+ server applications because the systemwide trust level is set the same for all server applications (because they all run in the same file, dllhost.exe).</span></span> <span data-ttu-id="fbcb6-106">Tuttavia, quando si imposta il livello di attendibilità dei criteri di restrizione software di un'applicazione libreria COM+, si influisce sulla configurazione di a livello per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fbcb6-106">However, when you set the software restriction policy trust level of a COM+ library application, you are affecting the systemwide configuration for that application.</span></span> <span data-ttu-id="fbcb6-107">Per informazioni sull'utilizzo dei criteri di restrizione software in COM+, vedere [utilizzo dei criteri di restrizione software in com+](using-the-software-restriction-policy-in-com-.md).</span><span class="sxs-lookup"><span data-stu-id="fbcb6-107">For a discussion of how to use the software restriction policy in COM+, see [Using the Software Restriction Policy in COM+](using-the-software-restriction-policy-in-com-.md).</span></span>

<span data-ttu-id="fbcb6-108">**Per impostare i criteri di restrizione software**</span><span class="sxs-lookup"><span data-stu-id="fbcb6-108">**To set the software restriction policy**</span></span>

1.  <span data-ttu-id="fbcb6-109">Fare clic con il pulsante destro del mouse sull'applicazione COM+ per la quale si stanno impostando i criteri di restrizione software, quindi scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="fbcb6-109">Right-click the COM+ application for which you are setting the software restriction policy, and then click **Properties**.</span></span>

2.  <span data-ttu-id="fbcb6-110">Nella finestra di dialogo Proprietà applicazione fare clic sulla scheda **sicurezza** .</span><span class="sxs-lookup"><span data-stu-id="fbcb6-110">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="fbcb6-111">In **Criteri restrizione software** selezionare la casella di controllo **Applica criteri di restrizione software** ; in questo modo è possibile impostare il livello di attendibilità.</span><span class="sxs-lookup"><span data-stu-id="fbcb6-111">Under **Software Restriction Policy**, select the **Apply software restriction policy** check box; this enables you to set the trust level.</span></span> <span data-ttu-id="fbcb6-112">Se si deseleziona la casella di controllo, COM+ utilizzerà la configurazione a livello dei criteri di restrizione software per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fbcb6-112">Clearing the check box will cause COM+ to use the systemwide configuration of the software restriction policy for the application.</span></span> <span data-ttu-id="fbcb6-113">Questa casella di controllo corrisponde alla proprietà SRPEnabled della raccolta di [**applicazioni**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="fbcb6-113">This check box corresponds to the SRPEnabled property of the [**Applications**](applications.md) collection.</span></span>

4.  <span data-ttu-id="fbcb6-114">Nella casella **livello di restrizione** selezionare il livello appropriato.</span><span class="sxs-lookup"><span data-stu-id="fbcb6-114">In the **Restriction Level** box, select the appropriate level.</span></span> <span data-ttu-id="fbcb6-115">Questa casella di riepilogo a discesa corrisponde alla proprietà SRPTrustLevel della raccolta di [**applicazioni**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="fbcb6-115">This drop-down box corresponds to the SRPTrustLevel property of the [**Applications**](applications.md) collection.</span></span> <span data-ttu-id="fbcb6-116">I livelli sono i seguenti, ordinati dal minimo al più attendibile:</span><span class="sxs-lookup"><span data-stu-id="fbcb6-116">The levels are as follows, ordered from least to most trusted:</span></span>

    -   <span data-ttu-id="fbcb6-117">Non **consentito**.</span><span class="sxs-lookup"><span data-stu-id="fbcb6-117">**Disallowed**.</span></span> <span data-ttu-id="fbcb6-118">L'applicazione non è consentita per l'utilizzo dei privilegi completi dell'utente.</span><span class="sxs-lookup"><span data-stu-id="fbcb6-118">The application is disallowed from using the full privileges of the user.</span></span> <span data-ttu-id="fbcb6-119">È possibile caricare i componenti con un livello di attendibilità.</span><span class="sxs-lookup"><span data-stu-id="fbcb6-119">Components with any trust level can be loaded into it.</span></span>
    -   <span data-ttu-id="fbcb6-120">**Senza restrizioni**.</span><span class="sxs-lookup"><span data-stu-id="fbcb6-120">**Unrestricted**.</span></span> <span data-ttu-id="fbcb6-121">L'applicazione dispone di accesso illimitato ai privilegi dell'utente.</span><span class="sxs-lookup"><span data-stu-id="fbcb6-121">The application has unrestricted access to the user's privileges.</span></span> <span data-ttu-id="fbcb6-122">Al suo interno possono essere caricati solo i componenti con un livello di attendibilità illimitato.</span><span class="sxs-lookup"><span data-stu-id="fbcb6-122">Only components with an Unrestricted trust level can be loaded into it.</span></span>

5.  <span data-ttu-id="fbcb6-123">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="fbcb6-123">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fbcb6-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fbcb6-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fbcb6-125">Configurazione della sicurezza Role-Based</span><span class="sxs-lookup"><span data-stu-id="fbcb6-125">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="fbcb6-126">Abilitazione dell'autenticazione per un'applicazione di libreria</span><span class="sxs-lookup"><span data-stu-id="fbcb6-126">Enabling Authentication for a Library Application</span></span>](enabling-authentication-for-a-library-application.md)
</dt> <dt>

[<span data-ttu-id="fbcb6-127">Impostazione di un livello di autenticazione per un'applicazione server</span><span class="sxs-lookup"><span data-stu-id="fbcb6-127">Setting an Authentication Level for a Server Application</span></span>](setting-an-authentication-level-for-a-server-application.md)
</dt> <dt>

[<span data-ttu-id="fbcb6-128">Impostazione di un livello di rappresentazione</span><span class="sxs-lookup"><span data-stu-id="fbcb6-128">Setting an Impersonation Level</span></span>](setting-an-impersonation-level.md)
</dt> </dl>

 

 




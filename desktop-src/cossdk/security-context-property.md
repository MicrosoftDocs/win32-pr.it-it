---
description: Proprietà del contesto di sicurezza
ms.assetid: 7ffae145-be13-4a2c-beb1-eaa1d11ad9a7
title: Proprietà del contesto di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b061ef7c0d0d0c146b626c11fd550c48ab488a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225773"
---
# <a name="security-context-property"></a><span data-ttu-id="8eb0b-103">Proprietà del contesto di sicurezza</span><span class="sxs-lookup"><span data-stu-id="8eb0b-103">Security Context Property</span></span>

<span data-ttu-id="8eb0b-104">Come per ogni servizio automatico fornito da COM+, il controllo automatico dei ruoli è basato sulle proprietà incluse nel contesto dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8eb0b-104">As with every automatic service provided by COM+, automatic role checking is based on properties included on the object context.</span></span> <span data-ttu-id="8eb0b-105">Per determinare se è necessario eseguire un controllo di sicurezza in una chiamata a un componente, si basa sulla proprietà di sicurezza nel contesto dell'oggetto creato quando viene creata un'istanza del componente configurato.</span><span class="sxs-lookup"><span data-stu-id="8eb0b-105">The determination of whether a security check must be carried out on a call into a component is based on the security property on the object context created when the configured component is instantiated.</span></span>

<span data-ttu-id="8eb0b-106">In genere non è necessario preoccuparsi di questa proprietà. viene utilizzato direttamente da COM+, non dall'utente.</span><span class="sxs-lookup"><span data-stu-id="8eb0b-106">You generally don't need to be concerned with this property; it is used directly by COM+, not you.</span></span> <span data-ttu-id="8eb0b-107">In alcuni casi, tuttavia, potrebbe essere necessario un controllo rigoroso sull'attivazione di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="8eb0b-107">However, in some circumstances, you might want strict control over the activation of an object.</span></span> <span data-ttu-id="8eb0b-108">In questo caso, la proprietà di sicurezza può influire sul contesto in cui è attivato l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8eb0b-108">In this case, the security property can affect which context your object is activated in.</span></span> <span data-ttu-id="8eb0b-109">Ovvero, se un oggetto dispone di una configurazione incompatibile con il contesto del relativo creatore, verrà attivata nel relativo contesto.</span><span class="sxs-lookup"><span data-stu-id="8eb0b-109">That is, if an object has a configuration incompatible with the context of its creator, it will be activated in its own context.</span></span> <span data-ttu-id="8eb0b-110">La proprietà di sicurezza può influenzare questo, così come qualsiasi proprietà del contesto dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8eb0b-110">The security property can influence this, as can any property on the object context.</span></span>

<span data-ttu-id="8eb0b-111">Se non si vuole che le impostazioni di sicurezza influiscano sull'attivazione, è possibile scegliere solo il controllo di accesso a livello di processo.</span><span class="sxs-lookup"><span data-stu-id="8eb0b-111">If you don't want security settings to influence activation, you can choose process-level access checking only.</span></span> <span data-ttu-id="8eb0b-112">In questo modo viene eliminata la proprietà di sicurezza nel contesto dell'oggetto, anche se il controllo basato sui ruoli viene disabilitato e le [informazioni sul contesto delle chiamate di sicurezza](security-call-context-information.md) non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="8eb0b-112">This suppresses the security property on the object context, although it effectively disables role-based checking and makes [security call context information](security-call-context-information.md) unavailable.</span></span>

<span data-ttu-id="8eb0b-113">Per ulteriori informazioni sui controlli di accesso a livello di processo, vedere [limiti di sicurezza](security-boundaries.md).</span><span class="sxs-lookup"><span data-stu-id="8eb0b-113">For more information about process-level access checks, see [Security Boundaries](security-boundaries.md).</span></span> <span data-ttu-id="8eb0b-114">Per informazioni su come impostare la sicurezza a livello di processo, vedere [impostazione di un livello di sicurezza per i controlli di accesso](setting-a-security-level-for-access-checks.md).</span><span class="sxs-lookup"><span data-stu-id="8eb0b-114">To see how to set process-level security, see [Setting a Security Level for Access Checks](setting-a-security-level-for-access-checks.md).</span></span>

<span data-ttu-id="8eb0b-115">Per ulteriori informazioni sul contesto dell'oggetto, vedere [contesti](com--contexts.md).</span><span class="sxs-lookup"><span data-stu-id="8eb0b-115">For more information about object context, see [Contexts](com--contexts.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8eb0b-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8eb0b-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8eb0b-117">Progettazione efficace dei ruoli</span><span class="sxs-lookup"><span data-stu-id="8eb0b-117">Designing Roles Effectively</span></span>](designing-roles-effectively.md)
</dt> <dt>

[<span data-ttu-id="8eb0b-118">Limiti di sicurezza</span><span class="sxs-lookup"><span data-stu-id="8eb0b-118">Security Boundaries</span></span>](security-boundaries.md)
</dt> <dt>

[<span data-ttu-id="8eb0b-119">Informazioni sul contesto delle chiamate di sicurezza</span><span class="sxs-lookup"><span data-stu-id="8eb0b-119">Security Call Context Information</span></span>](security-call-context-information.md)
</dt> <dt>

[<span data-ttu-id="8eb0b-120">Utilizzo dei ruoli per l'autorizzazione client</span><span class="sxs-lookup"><span data-stu-id="8eb0b-120">Using Roles for Client Authorization</span></span>](using-roles-for-client-authorization.md)
</dt> </dl>

 

 




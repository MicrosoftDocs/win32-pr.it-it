---
description: Informazioni sul contesto delle chiamate di sicurezza
ms.assetid: 8b170c17-f095-4c25-9ee2-480681b7e5f6
title: Informazioni sul contesto delle chiamate di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 213e21d684d004ed18e5b9aa536e03ae8292307e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225775"
---
# <a name="security-call-context-information"></a><span data-ttu-id="aaf3f-103">Informazioni sul contesto delle chiamate di sicurezza</span><span class="sxs-lookup"><span data-stu-id="aaf3f-103">Security Call Context Information</span></span>

<span data-ttu-id="aaf3f-104">La protezione basata sui ruoli si basa su un meccanismo generale che consente di recuperare le informazioni di sicurezza relative a tutti i chiamanti upstream nella catena di chiamate al componente.</span><span class="sxs-lookup"><span data-stu-id="aaf3f-104">Role-based security is built on a general mechanism that enables you to retrieve security information regarding all upstream callers in the chain of calls to your component.</span></span> <span data-ttu-id="aaf3f-105">Queste informazioni sono disponibili solo quando è abilitato il controllo del ruolo a livello di componente.</span><span class="sxs-lookup"><span data-stu-id="aaf3f-105">This information is available only when you have component-level role checking enabled.</span></span> <span data-ttu-id="aaf3f-106">Per informazioni dettagliate su come impostare la sicurezza a livello di componente, vedere [impostazione di un livello di sicurezza per i controlli di accesso](setting-a-security-level-for-access-checks.md).</span><span class="sxs-lookup"><span data-stu-id="aaf3f-106">For details about how to set component-level security, see [Setting a Security Level for Access Checks](setting-a-security-level-for-access-checks.md).</span></span>

<span data-ttu-id="aaf3f-107">È possibile usare l'interfaccia [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) per accedere alle informazioni di contesto delle chiamate di sicurezza a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="aaf3f-107">You can use the [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) interface to access security call context information programmatically.</span></span> <span data-ttu-id="aaf3f-108">Per una descrizione, vedere [sicurezza dei componenti programmatici](programmatic-component-security.md).</span><span class="sxs-lookup"><span data-stu-id="aaf3f-108">For a description, see [Programmatic Component Security](programmatic-component-security.md).</span></span>

<span data-ttu-id="aaf3f-109">Il contesto della chiamata di sicurezza viene passato ogni volta che viene superato un limite di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="aaf3f-109">Security call context is passed along every time a security boundary is crossed.</span></span> <span data-ttu-id="aaf3f-110">Per le chiamate tra i componenti all'interno di un'applicazione, che si trovano all'interno dello stesso limite di sicurezza, non vengono passate informazioni sul contesto di chiamata.</span><span class="sxs-lookup"><span data-stu-id="aaf3f-110">For calls between components within an application, which reside within the same security boundary, no call context information is passed.</span></span> <span data-ttu-id="aaf3f-111">Per le chiamate tra i processi o tra le applicazioni all'interno di un processo, le informazioni sul contesto di chiamata scorrono lungo.</span><span class="sxs-lookup"><span data-stu-id="aaf3f-111">For calls between processes or between applications within a process, call context information flows along.</span></span>

<span data-ttu-id="aaf3f-112">Questa funzionalità è particolarmente utile se si desidera eseguire operazioni di controllo e registrazione dettagliate.</span><span class="sxs-lookup"><span data-stu-id="aaf3f-112">This facility is particularly useful if you wish to do detailed auditing and logging.</span></span> <span data-ttu-id="aaf3f-113">È possibile recuperare e registrare le informazioni di sicurezza per ogni chiamante upstream.</span><span class="sxs-lookup"><span data-stu-id="aaf3f-113">You can retrieve and record security information for every upstream caller.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aaf3f-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="aaf3f-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aaf3f-115">Progettazione efficace dei ruoli</span><span class="sxs-lookup"><span data-stu-id="aaf3f-115">Designing Roles Effectively</span></span>](designing-roles-effectively.md)
</dt> <dt>

[<span data-ttu-id="aaf3f-116">Limiti di sicurezza</span><span class="sxs-lookup"><span data-stu-id="aaf3f-116">Security Boundaries</span></span>](security-boundaries.md)
</dt> <dt>

[<span data-ttu-id="aaf3f-117">Proprietà del contesto di sicurezza</span><span class="sxs-lookup"><span data-stu-id="aaf3f-117">Security Context Property</span></span>](security-context-property.md)
</dt> <dt>

[<span data-ttu-id="aaf3f-118">Utilizzo dei ruoli per l'autorizzazione client</span><span class="sxs-lookup"><span data-stu-id="aaf3f-118">Using Roles for Client Authorization</span></span>](using-roles-for-client-authorization.md)
</dt> </dl>

 

 




---
description: Se l'applicazione COM+ usa la sicurezza basata sui ruoli, è necessario completare diverse attività.
ms.assetid: f53b9945-cd34-4afc-a03a-dd72b0af160d
title: Configurazione della sicurezza Role-Based
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eafa71430dfa13f497b0e4f7f7cea45229a422e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342141"
---
# <a name="configuring-role-based-security"></a><span data-ttu-id="c6890-103">Configurazione della sicurezza Role-Based</span><span class="sxs-lookup"><span data-stu-id="c6890-103">Configuring Role-Based Security</span></span>

<span data-ttu-id="c6890-104">Se l'applicazione COM+ usa la sicurezza basata sui ruoli, è necessario completare diverse attività.</span><span class="sxs-lookup"><span data-stu-id="c6890-104">If your COM+ application uses role-based security, there are several tasks that need to be completed.</span></span> <span data-ttu-id="c6890-105">Quando si progettano i componenti nell'applicazione, si definiscono i ruoli necessari per proteggere l'accesso a tali componenti.</span><span class="sxs-lookup"><span data-stu-id="c6890-105">When designing the components in your application, you define the roles that are necessary to help protect access to those components.</span></span> <span data-ttu-id="c6890-106">Si decidono inoltre i ruoli da assegnare ai componenti, alle interfacce e ai metodi dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c6890-106">You also decide which roles to assign to the application's components, interfaces, and methods.</span></span> <span data-ttu-id="c6890-107">Durante l'integrazione dell'applicazione, si utilizza lo strumento di amministrazione Servizi componenti per aggiungere i ruoli definiti all'applicazione e assegnare ogni ruolo ai componenti, alle interfacce e ai metodi appropriati.</span><span class="sxs-lookup"><span data-stu-id="c6890-107">During application integration, you use the Component Services administrative tool to add the defined roles to the application and assign each role to the appropriate components, interfaces, and methods.</span></span>

<span data-ttu-id="c6890-108">Per la configurazione della sicurezza basata sui ruoli, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="c6890-108">In configuring role-based security, you perform the following steps:</span></span>

1.  <span data-ttu-id="c6890-109">Abilitare i controlli di accesso a livello di applicazione.</span><span class="sxs-lookup"><span data-stu-id="c6890-109">Enable access checks at the application level.</span></span> <span data-ttu-id="c6890-110">Per attivare il controllo di sicurezza per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c6890-110">To turn on security checking for an application.</span></span> <span data-ttu-id="c6890-111">Per informazioni dettagliate su come eseguire questo passaggio, vedere [Abilitazione dei controlli di accesso per un'applicazione](enabling-access-checks-for-an-application.md) .</span><span class="sxs-lookup"><span data-stu-id="c6890-111">See [Enabling Access Checks for an Application](enabling-access-checks-for-an-application.md) for details on how to perform this step.</span></span>
2.  <span data-ttu-id="c6890-112">Imposta il livello di sicurezza per i controlli di accesso.</span><span class="sxs-lookup"><span data-stu-id="c6890-112">Set security level for access checks.</span></span> <span data-ttu-id="c6890-113">Per impostare la sicurezza a livello di processo o di componente.</span><span class="sxs-lookup"><span data-stu-id="c6890-113">To set security either at process or at process and component level.</span></span> <span data-ttu-id="c6890-114">Per informazioni dettagliate su come eseguire questo passaggio, vedere [impostazione di un livello di sicurezza per i controlli di accesso](setting-a-security-level-for-access-checks.md) .</span><span class="sxs-lookup"><span data-stu-id="c6890-114">See [Setting a Security Level for Access Checks](setting-a-security-level-for-access-checks.md) for details on how to perform this step.</span></span>
3.  <span data-ttu-id="c6890-115">Abilitare i controlli di accesso a livello di componente.</span><span class="sxs-lookup"><span data-stu-id="c6890-115">Enable access checks at the component level.</span></span> <span data-ttu-id="c6890-116">Per attivare il controllo di sicurezza a livello di componente, interfaccia e metodo.</span><span class="sxs-lookup"><span data-stu-id="c6890-116">To turn on security checking at the component, interface, and method levels.</span></span> <span data-ttu-id="c6890-117">Per informazioni dettagliate su come eseguire questo passaggio, vedere [Abilitazione dei controlli di accesso a livello di componente](enabling-access-checks-at-the-component-level.md) .</span><span class="sxs-lookup"><span data-stu-id="c6890-117">See [Enabling Access Checks at the Component Level](enabling-access-checks-at-the-component-level.md) for details on how to perform this step.</span></span>
4.  <span data-ttu-id="c6890-118">Definire i ruoli per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c6890-118">Define roles for an application.</span></span> <span data-ttu-id="c6890-119">Per creare ruoli per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c6890-119">To create roles for an application.</span></span> <span data-ttu-id="c6890-120">Per informazioni dettagliate su come eseguire questo passaggio, vedere [definizione dei ruoli per un'applicazione](defining-roles-for-an-application.md) .</span><span class="sxs-lookup"><span data-stu-id="c6890-120">See [Defining Roles for an Application](defining-roles-for-an-application.md) for details on how to perform this step.</span></span>
5.  <span data-ttu-id="c6890-121">Assegnare ruoli a componenti, interfacce o metodi.</span><span class="sxs-lookup"><span data-stu-id="c6890-121">Assign roles to components, interfaces, or methods.</span></span> <span data-ttu-id="c6890-122">Per assegnare ruoli a risorse specifiche all'interno di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c6890-122">To assign roles to specific resources within an application.</span></span> <span data-ttu-id="c6890-123">Per informazioni dettagliate su come eseguire questo passaggio [, vedere Assegnazione di ruoli a componenti, interfacce o metodi](assigning-roles-to-components--interfaces--or-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="c6890-123">See [Assigning Roles to Components, Interfaces, or Methods](assigning-roles-to-components--interfaces--or-methods.md) for details on how to perform this step.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6890-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c6890-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6890-125">Configurazione dei criteri di restrizione software</span><span class="sxs-lookup"><span data-stu-id="c6890-125">Configuring the Software Restriction Policy</span></span>](configuring-the-software-restriction-policy.md)
</dt> <dt>

[<span data-ttu-id="c6890-126">Impostazione di un livello di rappresentazione</span><span class="sxs-lookup"><span data-stu-id="c6890-126">Setting an Impersonation Level</span></span>](setting-an-impersonation-level.md)
</dt> </dl>

 

 




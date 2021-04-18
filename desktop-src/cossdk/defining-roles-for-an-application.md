---
description: Per determinare i criteri di sicurezza per un'applicazione, è necessario definire i privilegi di sicurezza necessari.
ms.assetid: 0348684f-aebd-4d2d-a69b-85fea551c0cd
title: Definizione dei ruoli per un'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8e46eb2cb857a2b2dee2aabe41cb571e12ed98
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304627"
---
# <a name="defining-roles-for-an-application"></a><span data-ttu-id="84883-103">Definizione dei ruoli per un'applicazione</span><span class="sxs-lookup"><span data-stu-id="84883-103">Defining Roles for an Application</span></span>

<span data-ttu-id="84883-104">Per determinare i criteri di sicurezza per un'applicazione, è necessario definire i privilegi di sicurezza necessari.</span><span class="sxs-lookup"><span data-stu-id="84883-104">You determine a security policy for an application by defining the security privileges that it requires.</span></span> <span data-ttu-id="84883-105">A tale scopo, è necessario dichiarare un livello simbolico di privilegio come ruolo, ovvero definire il ruolo per l'applicazione, quindi [assegnare il ruolo](assigning-roles-to-components--interfaces--or-methods.md) a risorse specifiche all'interno dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="84883-105">To do this you declare a symbolic level of privilege as a role—that is, define the role for the application—and then [assign the role](assigning-roles-to-components--interfaces--or-methods.md) to specific resources within the application.</span></span> <span data-ttu-id="84883-106">Questa progettazione viene soddisfatta quando viene distribuita l'applicazione e gli amministratori di sistema popolano il ruolo con utenti e gruppi di utenti effettivi.</span><span class="sxs-lookup"><span data-stu-id="84883-106">This design is fulfilled when the application is deployed and system administrators populate the role with actual users and user groups.</span></span> <span data-ttu-id="84883-107">Per maggiori dettagli, vedere [amministrazione della sicurezza basata sui ruoli](role-based-security-administration.md).</span><span class="sxs-lookup"><span data-stu-id="84883-107">For greater detail, see [Role-Based Security Administration](role-based-security-administration.md).</span></span>

<span data-ttu-id="84883-108">**Per aggiungere un ruolo a un'applicazione**</span><span class="sxs-lookup"><span data-stu-id="84883-108">**To add a role to an application**</span></span>

1.  <span data-ttu-id="84883-109">Nell'albero della console dello strumento di amministrazione Servizi componenti individuare l'applicazione COM+ a cui si desidera aggiungere il ruolo.</span><span class="sxs-lookup"><span data-stu-id="84883-109">In the console tree of the Component Services administrative tool, locate the COM+ application to which you want to add the role.</span></span> <span data-ttu-id="84883-110">Espandere l'albero per visualizzare le cartelle per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="84883-110">Expand the tree to view the folders for the application.</span></span>

2.  <span data-ttu-id="84883-111">Fare clic con il pulsante destro del mouse sulla cartella **ruoli** per l'applicazione, scegliere **nuovo**, quindi fare clic su **ruolo**.</span><span class="sxs-lookup"><span data-stu-id="84883-111">Right-click the **Roles** folder for the application, point to **New**, and then click **Role**.</span></span>

3.  <span data-ttu-id="84883-112">Nella finestra di dialogo **ruolo** Digitare il nome del nuovo ruolo nella casella specificata.</span><span class="sxs-lookup"><span data-stu-id="84883-112">In the **Role** dialog box, type the name of the new role in the box provided.</span></span>

4.  <span data-ttu-id="84883-113">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="84883-113">Click **OK**.</span></span>

> [!Note]  
> <span data-ttu-id="84883-114">Dopo aver aggiunto i ruoli all'applicazione, è necessario assicurarsi di assegnare i ruoli ai componenti, alle interfacce e ai metodi appropriati.</span><span class="sxs-lookup"><span data-stu-id="84883-114">After adding roles to the application, you must be sure to assign the roles to the appropriate components, interfaces, and methods.</span></span> <span data-ttu-id="84883-115">In caso contrario, se è stata scelta e abilitata la sicurezza basata sui ruoli e se i ruoli sono stati aggiunti ma non assegnati, tutte le chiamate all'applicazione avranno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="84883-115">Otherwise, if role-based security has been chosen and enabled and if roles have been added but not assigned, all calls to the application will fail.</span></span> <span data-ttu-id="84883-116">Per ulteriori informazioni, vedere [assegnazione di ruoli a componenti, interfacce o metodi](assigning-roles-to-components--interfaces--or-methods.md).</span><span class="sxs-lookup"><span data-stu-id="84883-116">For more information, see [Assigning Roles to Components, Interfaces, or Methods](assigning-roles-to-components--interfaces--or-methods.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="84883-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="84883-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84883-118">Assegnazione di ruoli a componenti, interfacce o metodi</span><span class="sxs-lookup"><span data-stu-id="84883-118">Assigning Roles to Components, Interfaces, or Methods</span></span>](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[<span data-ttu-id="84883-119">Configurazione della sicurezza Role-Based</span><span class="sxs-lookup"><span data-stu-id="84883-119">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="84883-120">Abilitazione dei controlli di accesso per un'applicazione</span><span class="sxs-lookup"><span data-stu-id="84883-120">Enabling Access Checks for an Application</span></span>](enabling-access-checks-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="84883-121">Abilitazione dei controlli di accesso a livello di componente</span><span class="sxs-lookup"><span data-stu-id="84883-121">Enabling Access Checks at the Component Level</span></span>](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[<span data-ttu-id="84883-122">Impostazione di un livello di sicurezza per i controlli di accesso</span><span class="sxs-lookup"><span data-stu-id="84883-122">Setting a Security Level for Access Checks</span></span>](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 




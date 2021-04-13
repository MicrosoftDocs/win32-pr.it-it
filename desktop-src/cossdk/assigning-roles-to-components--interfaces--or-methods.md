---
description: Assegnazione di ruoli a componenti, interfacce o metodi
ms.assetid: 687d5692-4a83-4de8-b99d-859aaaddd16d
title: Assegnazione di ruoli a componenti, interfacce o metodi
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5efb66c9de865cbfcdc6e9cb047af92c95f6bc0a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401470"
---
# <a name="assigning-roles-to-components-interfaces-or-methods"></a><span data-ttu-id="39177-103">Assegnazione di ruoli a componenti, interfacce o metodi</span><span class="sxs-lookup"><span data-stu-id="39177-103">Assigning Roles to Components, Interfaces, or Methods</span></span>

<span data-ttu-id="39177-104">È possibile assegnare in modo esplicito un ruolo a qualsiasi elemento all'interno di un'applicazione COM+ visibile mediante lo strumento di amministrazione Servizi componenti.</span><span class="sxs-lookup"><span data-stu-id="39177-104">You can explicitly assign a role to any item within a COM+ application that is visible through the Component Services administrative tool.</span></span> <span data-ttu-id="39177-105">In questo modo si garantisce che a tutti gli utenti membri del ruolo verrà consentito l'accesso a tale elemento e a tutti gli altri elementi in esso contenuti.</span><span class="sxs-lookup"><span data-stu-id="39177-105">Doing so ensures that any users that are members of the role will be permitted access to that item and any other items that it contains.</span></span> <span data-ttu-id="39177-106">Se, ad esempio, si assegna il ruolo "Readers" a un componente, qualsiasi membro di "Readers" potrà accedere a tale componente e alle interfacce e ai metodi esposti.</span><span class="sxs-lookup"><span data-stu-id="39177-106">For example, if you assign the role "Readers" to a component, any member of "Readers" is allowed access to that component and any interfaces and methods it exposes.</span></span> <span data-ttu-id="39177-107">"Readers" viene visualizzato come ruolo ereditato per le interfacce e i metodi.</span><span class="sxs-lookup"><span data-stu-id="39177-107">"Readers" will show up as an Inherited role for any of those interfaces and methods.</span></span>

<span data-ttu-id="39177-108">Un metodo è accessibile ai chiamanti solo se si assegna un ruolo, assegnando esplicitamente il ruolo direttamente al metodo o assegnando un ruolo all'interfaccia del metodo o al componente del metodo, nel qual caso il ruolo verrà ereditato dal metodo.</span><span class="sxs-lookup"><span data-stu-id="39177-108">A method is accessible to callers only if you assign a role to it, either by explicitly assigning the role directly to the method or by assigning a role to the method's interface or the method's component, in which case the role will be inherited by the method.</span></span> <span data-ttu-id="39177-109">Se non viene assegnato alcun ruolo e se sono abilitati i controlli di accesso, tutte le chiamate al metodo avranno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="39177-109">If no role is assigned and if access checks are enabled, all calls to the method will fail.</span></span>

<span data-ttu-id="39177-110">Prima di poter assegnare un ruolo, è necessario [definirlo](defining-roles-for-an-application.md) per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="39177-110">Before you can assign a role, you must [define](defining-roles-for-an-application.md) it for the application.</span></span> <span data-ttu-id="39177-111">Tutti i ruoli definiti per l'applicazione verranno visualizzati nei **ruoli impostati in modo esplicito per la finestra elementi selezionati** nella scheda **sicurezza** per qualsiasi componente, metodo e interfaccia all'interno dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="39177-111">All roles defined for the application will appear in the **Roles explicitly set for selected item(s)** window on the **Security** tab for any components, methods, and interfaces within the application.</span></span>

<span data-ttu-id="39177-112">**Per assegnare ruoli a un componente, a un metodo o a un'interfaccia**</span><span class="sxs-lookup"><span data-stu-id="39177-112">**To assign roles to a component, method, or interface**</span></span>

1.  <span data-ttu-id="39177-113">Nell'albero della console dello strumento di amministrazione Servizi componenti individuare l'applicazione COM+ per la quale è stato definito il ruolo.</span><span class="sxs-lookup"><span data-stu-id="39177-113">In the console tree of the Component Services administrative tool, locate the COM+ application for which the role has been defined.</span></span> <span data-ttu-id="39177-114">Espandere l'albero per visualizzare i componenti, le interfacce o i metodi dell'applicazione, a seconda di ciò a cui viene assegnato il ruolo.</span><span class="sxs-lookup"><span data-stu-id="39177-114">Expand the tree to view the application's components, interfaces, or methods, depending on what you are assigning the role to.</span></span>

2.  <span data-ttu-id="39177-115">Fare clic con il pulsante destro del mouse sull'elemento a cui si desidera assegnare il ruolo, quindi scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="39177-115">Right-click the item to which you want to assign the role, and then click **Properties**.</span></span>

3.  <span data-ttu-id="39177-116">Nella finestra di dialogo Proprietà fare clic sulla scheda **sicurezza** .</span><span class="sxs-lookup"><span data-stu-id="39177-116">In the properties dialog box, click the **Security** tab.</span></span>

4.  <span data-ttu-id="39177-117">Nella casella **ruoli impostati in modo esplicito per gli elementi selezionati** selezionare i ruoli che si desidera assegnare all'elemento.</span><span class="sxs-lookup"><span data-stu-id="39177-117">In the **Roles explicitly set for selected item(s)** box, select the roles that you want to assign to the item.</span></span>

5.  <span data-ttu-id="39177-118">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="39177-118">Click **OK**.</span></span>

<span data-ttu-id="39177-119">Tutti i ruoli impostati in modo esplicito per un elemento verranno ereditati da tutti gli elementi di livello inferiore che contiene e verranno visualizzati nella finestra **ruoli ereditati da elementi selezionati** per tali elementi.</span><span class="sxs-lookup"><span data-stu-id="39177-119">Any roles that you have explicitly set for an item will be inherited by any lower-level items it contains and will show up in the **Roles inherited by selected item(s)** window for those items.</span></span>

## <a name="related-topics"></a><span data-ttu-id="39177-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="39177-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39177-121">Configurazione della sicurezza Role-Based</span><span class="sxs-lookup"><span data-stu-id="39177-121">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="39177-122">Definizione dei ruoli per un'applicazione</span><span class="sxs-lookup"><span data-stu-id="39177-122">Defining Roles for an Application</span></span>](defining-roles-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="39177-123">Abilitazione dei controlli di accesso per un'applicazione</span><span class="sxs-lookup"><span data-stu-id="39177-123">Enabling Access Checks for an Application</span></span>](enabling-access-checks-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="39177-124">Abilitazione dei controlli di accesso a livello di componente</span><span class="sxs-lookup"><span data-stu-id="39177-124">Enabling Access Checks at the Component Level</span></span>](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[<span data-ttu-id="39177-125">Impostazione di un livello di sicurezza per i controlli di accesso</span><span class="sxs-lookup"><span data-stu-id="39177-125">Setting a Security Level for Access Checks</span></span>](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 




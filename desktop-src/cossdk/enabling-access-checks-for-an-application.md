---
description: L'esecuzione di questo passaggio consente di controllare l'accesso ai processi o la sicurezza completa basata sui ruoli, a seconda del livello di sicurezza selezionato e se si Abilita il controllo degli accessi per i singoli componenti.
ms.assetid: 266bdac1-41be-45a5-a8c7-f9c6fe08445c
title: Abilitazione dei controlli di accesso per un'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3d64a32b23467f85c368e088a870ebe5e4d683e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304617"
---
# <a name="enabling-access-checks-for-an-application"></a><span data-ttu-id="406fb-103">Abilitazione dei controlli di accesso per un'applicazione</span><span class="sxs-lookup"><span data-stu-id="406fb-103">Enabling Access Checks for an Application</span></span>

<span data-ttu-id="406fb-104">L'esecuzione di questo passaggio consente di controllare l'accesso ai processi o la sicurezza completa basata sui ruoli, a seconda del livello di sicurezza selezionato e se si Abilita il controllo degli accessi per i singoli componenti.</span><span class="sxs-lookup"><span data-stu-id="406fb-104">Performing this step enables either process access checks or full role-based security, depending on what security level you select and whether you enable access checking for individual components.</span></span>

<span data-ttu-id="406fb-105">**Per abilitare i controlli di accesso per un'applicazione**</span><span class="sxs-lookup"><span data-stu-id="406fb-105">**To enable access checks for an application**</span></span>

1.  <span data-ttu-id="406fb-106">Nell'albero della console dello strumento di amministrazione Servizi componenti fare clic con il pulsante destro del mouse sull'applicazione COM+ per cui si desidera abilitare i controlli di accesso, quindi scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="406fb-106">In the console tree of the Component Services administrative tool, right-click the COM+ application for which you want to enable access checks, and then click **Properties**.</span></span>

2.  <span data-ttu-id="406fb-107">Nella finestra di dialogo Proprietà applicazione fare clic sulla scheda **sicurezza** .</span><span class="sxs-lookup"><span data-stu-id="406fb-107">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="406fb-108">Selezionare la casella **di controllo applica verifiche di accesso per l'applicazione** .</span><span class="sxs-lookup"><span data-stu-id="406fb-108">Select the **Enforce access checks for this application** check box.</span></span>

4.  <span data-ttu-id="406fb-109">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="406fb-109">Click **OK**.</span></span>

> [!Note]  
> <span data-ttu-id="406fb-110">A partire da Windows Server 2003, i controlli di accesso sono abilitati per impostazione predefinita quando si crea un'applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="406fb-110">As of Windows Server 2003, access checks are enabled by default when creating a COM+ application.</span></span> <span data-ttu-id="406fb-111">I controlli di accesso sono abilitati per impostazione predefinita a livello di applicazione e disabilitati per impostazione predefinita a livello di componente.</span><span class="sxs-lookup"><span data-stu-id="406fb-111">Access checks are enabled by default at the application level and disabled by default at the component level.</span></span> <span data-ttu-id="406fb-112">In precedenza, i controlli di accesso erano disabilitati per impostazione predefinita a livello di applicazione e abilitati per impostazione predefinita a livello di componente.</span><span class="sxs-lookup"><span data-stu-id="406fb-112">Previously, access checks were disabled by default at the application level and enabled by default at the component level.</span></span>

 

<span data-ttu-id="406fb-113">Dopo aver abilitato i controlli di accesso, è necessario selezionare il livello di sicurezza appropriato.</span><span class="sxs-lookup"><span data-stu-id="406fb-113">After enabling access checks, you should select the appropriate security level.</span></span> <span data-ttu-id="406fb-114">Vedere [impostazione di un livello di sicurezza per i controlli di accesso](setting-a-security-level-for-access-checks.md).</span><span class="sxs-lookup"><span data-stu-id="406fb-114">See [Setting a Security Level for Access Checks](setting-a-security-level-for-access-checks.md).</span></span> <span data-ttu-id="406fb-115">Inoltre, è necessario assicurarsi di definire i ruoli e aggiungerli all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="406fb-115">Also, you must be sure to define roles and add them to the application.</span></span> <span data-ttu-id="406fb-116">Se i controlli di accesso sono abilitati ma non sono stati aggiunti ruoli, tutte le chiamate all'applicazione avranno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="406fb-116">If access checks are enabled but no roles have been added, all calls to the application will fail.</span></span> <span data-ttu-id="406fb-117">Vedere [definizione dei ruoli per un'applicazione](defining-roles-for-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="406fb-117">See [Defining Roles for an Application](defining-roles-for-an-application.md).</span></span>

> [!Note]  
> <span data-ttu-id="406fb-118">Quando si esegue il debug dell'applicazione, potrebbe essere utile disabilitare la sicurezza in modo da potersi concentrare su altri aspetti del comportamento e della progettazione del programma.</span><span class="sxs-lookup"><span data-stu-id="406fb-118">When debugging your application, it might be helpful to disable security so that you can concentrate on other aspects of your program's behavior and design.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="406fb-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="406fb-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="406fb-120">Assegnazione di ruoli a componenti, interfacce o metodi</span><span class="sxs-lookup"><span data-stu-id="406fb-120">Assigning Roles to Components, Interfaces, or Methods</span></span>](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[<span data-ttu-id="406fb-121">Configurazione della sicurezza Role-Based</span><span class="sxs-lookup"><span data-stu-id="406fb-121">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="406fb-122">Definizione dei ruoli per un'applicazione</span><span class="sxs-lookup"><span data-stu-id="406fb-122">Defining Roles for an Application</span></span>](defining-roles-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="406fb-123">Abilitazione dei controlli di accesso a livello di componente</span><span class="sxs-lookup"><span data-stu-id="406fb-123">Enabling Access Checks at the Component Level</span></span>](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[<span data-ttu-id="406fb-124">Impostazione di un livello di sicurezza per i controlli di accesso</span><span class="sxs-lookup"><span data-stu-id="406fb-124">Setting a Security Level for Access Checks</span></span>](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 




---
description: Dopo aver abilitato i controlli di accesso, per l'applicazione COM+ è necessario selezionare il livello in cui si desidera che vengano eseguiti i controlli di accesso.
ms.assetid: 9c044add-7761-4378-b7eb-bf4e84e913b3
title: Impostazione di un livello di sicurezza per i controlli di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 646a49a4966bff7c593f12cb7481f4a4aad8859e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127395"
---
# <a name="setting-a-security-level-for-access-checks"></a><span data-ttu-id="cbad0-103">Impostazione di un livello di sicurezza per i controlli di accesso</span><span class="sxs-lookup"><span data-stu-id="cbad0-103">Setting a Security Level for Access Checks</span></span>

<span data-ttu-id="cbad0-104">Dopo aver abilitato i [controlli di accesso](enabling-access-checks-for-an-application.md), per l'applicazione com+ è necessario selezionare il livello in cui si desidera che vengano eseguiti i controlli di accesso.</span><span class="sxs-lookup"><span data-stu-id="cbad0-104">After you have enabled [access checks](enabling-access-checks-for-an-application.md), for your COM+ application, you must select the level at which you wish to have access checks performed.</span></span>

<span data-ttu-id="cbad0-105">**Per selezionare un livello di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="cbad0-105">**To select a security level**</span></span>

1.  <span data-ttu-id="cbad0-106">Nell'albero della console dello strumento di amministrazione Servizi componenti fare clic con il pulsante destro del mouse sull'applicazione COM+ per cui si desidera abilitare i controlli di accesso, quindi scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="cbad0-106">In the console tree of the Component Services administrative tool, right-click the COM+ application for which you want to enable access checks, and then click **Properties**.</span></span>

2.  <span data-ttu-id="cbad0-107">Nella finestra di dialogo Proprietà applicazione fare clic sulla scheda **sicurezza** .</span><span class="sxs-lookup"><span data-stu-id="cbad0-107">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="cbad0-108">In **livello di sicurezza**, selezionare una delle opzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cbad0-108">Under **Security level**, select one of the following:</span></span>

    -   <span data-ttu-id="cbad0-109">**Esegui controlli di accesso solo a livello di processo**: questa impostazione indica che gli utenti nei ruoli assegnati all'applicazione verranno aggiunti al descrittore di sicurezza del processo.</span><span class="sxs-lookup"><span data-stu-id="cbad0-109">**Perform access checks only at the process level**— This setting indicates that users in roles that are assigned to the application will be added to the process security descriptor.</span></span> <span data-ttu-id="cbad0-110">Ciò presenta gli effetti e le implicazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cbad0-110">This has the following effects and implications:</span></span>

        <span data-ttu-id="cbad0-111">Il controllo dei ruoli con granularità fine è disattivato a livello di componente, metodo e interfaccia.</span><span class="sxs-lookup"><span data-stu-id="cbad0-111">Fine-grained role checking is turned off at the component, method, and interface levels.</span></span> <span data-ttu-id="cbad0-112">I controlli di sicurezza vengono eseguiti solo a livello di applicazione.</span><span class="sxs-lookup"><span data-stu-id="cbad0-112">Security checks are performed only at the application level.</span></span>

        <span data-ttu-id="cbad0-113">La proprietà di sicurezza non è inclusa nel contesto per gli oggetti in esecuzione all'interno dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cbad0-113">The security property is not included on the context for any objects running within the application.</span></span> <span data-ttu-id="cbad0-114">Questo può influire potenzialmente sulla modalità di attivazione degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="cbad0-114">This can potentially affect how objects are activated.</span></span> <span data-ttu-id="cbad0-115">Vedere [proprietà del contesto di sicurezza](security-context-property.md).</span><span class="sxs-lookup"><span data-stu-id="cbad0-115">See [Security Context Property](security-context-property.md).</span></span>

        <span data-ttu-id="cbad0-116">Il contesto della chiamata di sicurezza non verrà reso disponibile.</span><span class="sxs-lookup"><span data-stu-id="cbad0-116">The security call context will not be made available.</span></span> <span data-ttu-id="cbad0-117">La sicurezza a livello di codice che si basa sulle informazioni sul contesto delle chiamate di sicurezza non funzionerà.</span><span class="sxs-lookup"><span data-stu-id="cbad0-117">Programmatic security that relies on security call context information will not function.</span></span> <span data-ttu-id="cbad0-118">Vedere [informazioni sul contesto delle chiamate di sicurezza](security-call-context-information.md).</span><span class="sxs-lookup"><span data-stu-id="cbad0-118">See [Security Call Context Information](security-call-context-information.md).</span></span>

    -   <span data-ttu-id="cbad0-119">**Eseguire i controlli di accesso a livello di processo e componente**: questa impostazione indica che verranno eseguiti i controlli dei descrittori di sicurezza a livello di processo e i controlli di sicurezza completi basati sui ruoli.</span><span class="sxs-lookup"><span data-stu-id="cbad0-119">**Perform access checks at the process and component level**—This setting indicates that process-level security descriptor checks and full role-based security checks will be performed.</span></span> <span data-ttu-id="cbad0-120">Ciò presenta gli effetti e le implicazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cbad0-120">This has the following effects and implications:</span></span>

        <span data-ttu-id="cbad0-121">Per abilitare il controllo dei ruoli per determinati componenti, è necessario [abilitare i controlli di accesso a livello di componente](enabling-access-checks-at-the-component-level.md).</span><span class="sxs-lookup"><span data-stu-id="cbad0-121">To enable role checking for particular components, you must [enable access checks at the component level](enabling-access-checks-at-the-component-level.md).</span></span>

        <span data-ttu-id="cbad0-122">La proprietà di sicurezza è inclusa nel contesto per qualsiasi oggetto in esecuzione all'interno dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cbad0-122">The security property is included on the context for any objects running within the application.</span></span> <span data-ttu-id="cbad0-123">Questo può influire potenzialmente sulla modalità di attivazione degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="cbad0-123">This can potentially affect how objects are activated.</span></span> <span data-ttu-id="cbad0-124">Vedere [proprietà del contesto di sicurezza](security-context-property.md).</span><span class="sxs-lookup"><span data-stu-id="cbad0-124">See [Security Context Property](security-context-property.md).</span></span>

        <span data-ttu-id="cbad0-125">Il contesto della chiamata di sicurezza è disponibile.</span><span class="sxs-lookup"><span data-stu-id="cbad0-125">The security call context is available.</span></span> <span data-ttu-id="cbad0-126">La sicurezza basata sui ruoli a livello di codice è abilitata.</span><span class="sxs-lookup"><span data-stu-id="cbad0-126">Programmatic role-based security is enabled.</span></span> <span data-ttu-id="cbad0-127">Vedere [informazioni sul contesto delle chiamate di sicurezza](security-call-context-information.md).</span><span class="sxs-lookup"><span data-stu-id="cbad0-127">See [Security Call Context Information](security-call-context-information.md).</span></span>

        > [!Note]  
        > <span data-ttu-id="cbad0-128">Per le applicazioni della libreria COM+, è necessario scegliere di controllare i livelli a livello di processo e di componente per eseguire il controllo di accesso significativo.</span><span class="sxs-lookup"><span data-stu-id="cbad0-128">For COM+ library applications, you must choose to check both at process and at component levels for any meaningful access checking to work.</span></span> <span data-ttu-id="cbad0-129">Le applicazioni di libreria si basano sul processo host per la sicurezza a livello di processo.</span><span class="sxs-lookup"><span data-stu-id="cbad0-129">Library applications rely on the host process for process-level security.</span></span> <span data-ttu-id="cbad0-130">È possibile determinare il modo in cui l'applicazione della libreria interagisce con l'autenticazione eseguita dal processo host [impostando l'autenticazione](enabling-authentication-for-a-library-application.md).</span><span class="sxs-lookup"><span data-stu-id="cbad0-130">You can determine how the library application interacts with authentication performed by the host process by [setting authentication](enabling-authentication-for-a-library-application.md).</span></span> <span data-ttu-id="cbad0-131">Per ulteriori informazioni, vedere la pagina relativa alla [sicurezza delle applicazioni di libreria](library-application-security.md).</span><span class="sxs-lookup"><span data-stu-id="cbad0-131">For more information, see [Library Application Security](library-application-security.md).</span></span>

         

4.  <span data-ttu-id="cbad0-132">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="cbad0-132">Click **OK**.</span></span>

<span data-ttu-id="cbad0-133">Al successivo avvio dell'applicazione, la sicurezza verrà controllata automaticamente al livello specificato.</span><span class="sxs-lookup"><span data-stu-id="cbad0-133">The next time the application is started, security will automatically be checked at the specified level.</span></span> <span data-ttu-id="cbad0-134">Solo agli utenti assegnati ai ruoli assegnati all'applicazione verrà concesso l'accesso all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cbad0-134">Only users assigned to roles assigned to the application will be given access to the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cbad0-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cbad0-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbad0-136">Assegnazione di ruoli a componenti, interfacce o metodi</span><span class="sxs-lookup"><span data-stu-id="cbad0-136">Assigning Roles to Components, Interfaces, or Methods</span></span>](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[<span data-ttu-id="cbad0-137">Configurazione della sicurezza Role-Based</span><span class="sxs-lookup"><span data-stu-id="cbad0-137">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="cbad0-138">Definizione dei ruoli per un'applicazione</span><span class="sxs-lookup"><span data-stu-id="cbad0-138">Defining Roles for an Application</span></span>](defining-roles-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="cbad0-139">Abilitazione dei controlli di accesso per un'applicazione</span><span class="sxs-lookup"><span data-stu-id="cbad0-139">Enabling Access Checks for an Application</span></span>](enabling-access-checks-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="cbad0-140">Abilitazione dei controlli di accesso a livello di componente</span><span class="sxs-lookup"><span data-stu-id="cbad0-140">Enabling Access Checks at the Component Level</span></span>](enabling-access-checks-at-the-component-level.md)
</dt> </dl>

 

 




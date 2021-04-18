---
description: Creazione di una nuova applicazione COM+
ms.assetid: eec4e871-36c2-4e60-9808-1400efcfc60c
title: Creazione di una nuova applicazione COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c09eb296ad0a5f2326b5d931f59a5075d001d89f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305224"
---
# <a name="creating-a-new-com-application"></a><span data-ttu-id="1ba20-103">Creazione di una nuova applicazione COM+</span><span class="sxs-lookup"><span data-stu-id="1ba20-103">Creating a New COM+ Application</span></span>

<span data-ttu-id="1ba20-104">Per la creazione di una nuova applicazione COM+ sono necessari due passaggi di base, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="1ba20-104">Creating a new COM+ application requires two basic steps, as follows:</span></span>

-   <span data-ttu-id="1ba20-105">Creazione di un'applicazione COM+ vuota (descritta di seguito).</span><span class="sxs-lookup"><span data-stu-id="1ba20-105">Creating an empty COM+ application (described below).</span></span>
-   <span data-ttu-id="1ba20-106">Aggiunta di componenti all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1ba20-106">Adding components to the application.</span></span> <span data-ttu-id="1ba20-107">Vedere [installazione di nuovi componenti](installing-new-components.md) e [importazione di componenti](importing-components.md).</span><span class="sxs-lookup"><span data-stu-id="1ba20-107">(See [Installing New Components](installing-new-components.md) and [Importing Components](importing-components.md).)</span></span>

<span data-ttu-id="1ba20-108">**Per creare un'applicazione COM+ vuota**</span><span class="sxs-lookup"><span data-stu-id="1ba20-108">**To create an empty COM+ application**</span></span>

1.  <span data-ttu-id="1ba20-109">Nell'albero della console dello strumento di amministrazione Servizi componenti selezionare il computer in cui si desidera creare un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1ba20-109">In the console tree of the Component Services administrative tool, select the computer on which you want to create an application.</span></span>

2.  <span data-ttu-id="1ba20-110">Selezionare la cartella **applicazioni com+** per il computer.</span><span class="sxs-lookup"><span data-stu-id="1ba20-110">Select the **COM+ Applications** folder for that computer.</span></span>

3.  <span data-ttu-id="1ba20-111">Scegliere **nuovo** dal menu **azione** , quindi fare clic su **applicazione**.</span><span class="sxs-lookup"><span data-stu-id="1ba20-111">On the **Action** menu, point to **New**, and then click **Application**.</span></span> <span data-ttu-id="1ba20-112">È anche possibile fare clic con il pulsante destro del mouse sulla cartella **applicazioni com+** , scegliere **nuovo**, quindi fare clic su **applicazione**.</span><span class="sxs-lookup"><span data-stu-id="1ba20-112">You can also right-click the **COM+ Applications** folder, point to **New**, and then click **Application**.</span></span>

4.  <span data-ttu-id="1ba20-113">Nella pagina **iniziale** dell'installazione guidata dell'applicazione com+, fare clic su **Avanti**, quindi nella finestra di dialogo **Installa o crea una nuova applicazione** fare clic su **Crea un'applicazione vuota**.</span><span class="sxs-lookup"><span data-stu-id="1ba20-113">On the **Welcome** page of the COM+ Application Install Wizard, click **Next**, and then in the **Install or Create a New Application** dialog box, click **Create an empty application**.</span></span>

5.  <span data-ttu-id="1ba20-114">Nella casella specificata digitare un nome per la nuova applicazione.</span><span class="sxs-lookup"><span data-stu-id="1ba20-114">In the box provided, type a name for the new application.</span></span> <span data-ttu-id="1ba20-115">Si noti che non è possibile utilizzare i seguenti caratteri speciali in un nome di applicazione: \\ ,/, ~,!, @, \# ,%, ^, &, \* , (,), \| ,}, {, \] , \[ ,', ", >, <,.,?,: e;.) In **tipo di attivazione** fare clic su applicazione **libreria** o **applicazione server**.</span><span class="sxs-lookup"><span data-stu-id="1ba20-115">(Note that the following special characters cannot be used in an application name: \\, /, ~, !, @, \#, %, ^, &, \*, (, ), \|, }, {, \], \[, ', ", >, <, ., ?, :, and ;.) Under **Activation type**, click **Library application** or **Server application**.</span></span> <span data-ttu-id="1ba20-116">Fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="1ba20-116">Click **Next**.</span></span>

    > [!Note]  
    > <span data-ttu-id="1ba20-117">Un'applicazione server viene eseguita in un proprio processo.</span><span class="sxs-lookup"><span data-stu-id="1ba20-117">A server application runs in its own process.</span></span> <span data-ttu-id="1ba20-118">Le applicazioni server possono supportare tutti i servizi COM+.</span><span class="sxs-lookup"><span data-stu-id="1ba20-118">Server applications can support all COM+ services.</span></span> <span data-ttu-id="1ba20-119">Un'applicazione di libreria viene eseguita nel processo del client che la crea.</span><span class="sxs-lookup"><span data-stu-id="1ba20-119">A library application runs in the process of the client that creates it.</span></span> <span data-ttu-id="1ba20-120">Le applicazioni di libreria possono usare la sicurezza basata sui ruoli, ma non supportano l'accesso remoto o i componenti in coda.</span><span class="sxs-lookup"><span data-stu-id="1ba20-120">Library applications can use role-based security but do not support remote access or queued components.</span></span>

     

6.  <span data-ttu-id="1ba20-121">Nella finestra di dialogo **Imposta identità applicazione** scegliere un'identità con cui eseguire l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1ba20-121">In the **Set Application Identity** dialog box, choose an identity under which the application will run.</span></span> <span data-ttu-id="1ba20-122">Se si seleziona **questo utente**, digitare il nome utente e la password.</span><span class="sxs-lookup"><span data-stu-id="1ba20-122">If you select **This user**, type the user name and password.</span></span> <span data-ttu-id="1ba20-123">È inoltre necessario digitare nuovamente la password nella casella **Conferma password** .</span><span class="sxs-lookup"><span data-stu-id="1ba20-123">You must also retype the password in the **Confirm password** box.</span></span> <span data-ttu-id="1ba20-124">Fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="1ba20-124">Click **Next**.</span></span> <span data-ttu-id="1ba20-125">La selezione predefinita per l'identità dell'applicazione è **utente interattivo**.</span><span class="sxs-lookup"><span data-stu-id="1ba20-125">(The default selection for application identity is **Interactive User**.</span></span> <span data-ttu-id="1ba20-126">L'utente interattivo è l'utente connesso al computer server in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="1ba20-126">The interactive user is the user logged on to the server computer at any given time.</span></span> <span data-ttu-id="1ba20-127">È possibile selezionare un utente diverso selezionando **l'utente** e immettendo un utente o un gruppo specifico.</span><span class="sxs-lookup"><span data-stu-id="1ba20-127">You can select a different user by selecting **This user** and entering a specific user or group.)</span></span>

    > [!Note]  
    > <span data-ttu-id="1ba20-128">La finestra di dialogo **Imposta identità applicazione** viene visualizzata solo se è stata selezionata l'opzione **applicazione server** per il tipo di attivazione della nuova applicazione nella finestra di dialogo precedente della procedura guidata di installazione dell'applicazione com.</span><span class="sxs-lookup"><span data-stu-id="1ba20-128">The **Set Application Identity** dialog box appears only if you selected **Server application** for the new application's activation type in the COM Application Install Wizard's preceding dialog box.</span></span> <span data-ttu-id="1ba20-129">La proprietà Identity non viene utilizzata per le applicazioni di libreria.</span><span class="sxs-lookup"><span data-stu-id="1ba20-129">The identity property is not used for library applications.</span></span>

     

7.  <span data-ttu-id="1ba20-130">Nella finestra di dialogo **Aggiungi ruoli applicazione** aggiungere i ruoli che si desidera associare all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1ba20-130">In the **Add Application Roles** dialog box, add any roles you want to associate with the application.</span></span> <span data-ttu-id="1ba20-131">Per impostazione predefinita, viene definito solo il ruolo **CreatorOwner** .</span><span class="sxs-lookup"><span data-stu-id="1ba20-131">By default, only the **CreatorOwner** role is defined.</span></span> <span data-ttu-id="1ba20-132">Per informazioni sui ruoli, vedere [amministrazione della sicurezza basata sui ruoli](role-based-security-administration.md).</span><span class="sxs-lookup"><span data-stu-id="1ba20-132">For information on roles, see [Role-Based Security Administration](role-based-security-administration.md).</span></span>

8.  <span data-ttu-id="1ba20-133">Nella finestra di dialogo **Aggiungi utenti ai ruoli** , popolare ogni ruolo creato nell'ultimo passaggio con gli utenti, i gruppi o le entità di sicurezza predefinite a cui si desidera concedere i privilegi associati a tale ruolo.</span><span class="sxs-lookup"><span data-stu-id="1ba20-133">In the **Add Users to Roles** dialog box, populate each role you created in the last step with the users, groups, or built-in security principals to which you want to grant the privileges associated with that role.</span></span> <span data-ttu-id="1ba20-134">Per impostazione predefinita, l'utente interattivo viene inserito nel ruolo **CreatorOwner** .</span><span class="sxs-lookup"><span data-stu-id="1ba20-134">By default, the interactive user is placed in the **CreatorOwner** role.</span></span>

9.  <span data-ttu-id="1ba20-135">Fare clic su **Fine**.</span><span class="sxs-lookup"><span data-stu-id="1ba20-135">Click **Finish**.</span></span>

<span data-ttu-id="1ba20-136">La nuova applicazione verrà ora visualizzata nella cartella **applicazioni com+** nell'albero della console dello strumento di amministrazione Servizi componenti.</span><span class="sxs-lookup"><span data-stu-id="1ba20-136">The new application will now be displayed under the **COM+ Applications** folder in the console tree of the Component Services administrative tool.</span></span>

> [!Note]  
> <span data-ttu-id="1ba20-137">A partire da Windows Server 2003, i controlli di accesso sono abilitati per impostazione predefinita quando si crea un'applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="1ba20-137">As of Windows Server 2003, access checks are enabled by default when creating a COM+ application.</span></span> <span data-ttu-id="1ba20-138">Nelle versioni precedenti, i controlli di accesso erano disabilitati per impostazione predefinita a livello di applicazione.</span><span class="sxs-lookup"><span data-stu-id="1ba20-138">In previous versions, access checks were disabled by default at the application level.</span></span> <span data-ttu-id="1ba20-139">Il risultato è che, per impostazione predefinita, l'accesso a un'applicazione COM+ è consentito solo agli utenti inclusi nei ruoli associati all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1ba20-139">The result is that by default, access to a COM+ application is allowed only to users that are in the roles associated with the application.</span></span> <span data-ttu-id="1ba20-140">(Vedere [amministrazione della sicurezza basata sui ruoli](role-based-security-administration.md)). In alternativa, è possibile consentire l'accesso a tutti gli utenti disabilitando i controlli di accesso in un'applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="1ba20-140">(See [Role-Based Security Administration](role-based-security-administration.md).) Alternatively, you can allow access to all users by disabling access checks on a COM+ application.</span></span> <span data-ttu-id="1ba20-141">Vedere [Abilitazione dei controlli di accesso per un'applicazione](enabling-access-checks-for-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="1ba20-141">(See [Enabling Access Checks for an Application](enabling-access-checks-for-an-application.md).)</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1ba20-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1ba20-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ba20-143">Copia di componenti</span><span class="sxs-lookup"><span data-stu-id="1ba20-143">Copying Components</span></span>](copying-components.md)
</dt> <dt>

[<span data-ttu-id="1ba20-144">Eliminazione di un'applicazione COM+</span><span class="sxs-lookup"><span data-stu-id="1ba20-144">Deleting a COM+ Application</span></span>](deleting-a-com--application.md)
</dt> <dt>

[<span data-ttu-id="1ba20-145">Importazione di componenti</span><span class="sxs-lookup"><span data-stu-id="1ba20-145">Importing Components</span></span>](importing-components.md)
</dt> <dt>

[<span data-ttu-id="1ba20-146">Installazione di nuovi componenti</span><span class="sxs-lookup"><span data-stu-id="1ba20-146">Installing New Components</span></span>](installing-new-components.md)
</dt> <dt>

[<span data-ttu-id="1ba20-147">Spostamento dei componenti</span><span class="sxs-lookup"><span data-stu-id="1ba20-147">Moving Components</span></span>](moving-components.md)
</dt> <dt>

[<span data-ttu-id="1ba20-148">Rimozione di un componente da un'applicazione COM+</span><span class="sxs-lookup"><span data-stu-id="1ba20-148">Removing a Component from a COM+ Application</span></span>](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 




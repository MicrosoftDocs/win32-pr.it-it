---
description: È possibile utilizzare lo strumento di amministrazione Servizi componenti per popolare un ruolo con gli account utente o i gruppi.
ms.assetid: 1cf7dc38-185a-4cc4-8f4c-44b6af4c5f4a
title: Assegnazione di un account utente o di un gruppo a un ruolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d53b37c9f0265e02c7abdf74eeaf81bd0b12e3d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305023"
---
# <a name="assigning-a-user-account-or-group-to-a-role"></a><span data-ttu-id="eb696-103">Assegnazione di un account utente o di un gruppo a un ruolo</span><span class="sxs-lookup"><span data-stu-id="eb696-103">Assigning a User Account or Group to a Role</span></span>

<span data-ttu-id="eb696-104">È possibile utilizzare lo strumento di amministrazione Servizi componenti per popolare un ruolo con gli account utente o i gruppi.</span><span class="sxs-lookup"><span data-stu-id="eb696-104">You can use the Component Services administrative tool to populate a role with user accounts or groups.</span></span> <span data-ttu-id="eb696-105">Il modo migliore per assegnare un account utente a un ruolo consiste nell'assegnare l'account utente a un gruppo e quindi assegnare il gruppo al ruolo.</span><span class="sxs-lookup"><span data-stu-id="eb696-105">The preferred way to assign a user account to a role is to assign the user account to a group and then assign the group to the role.</span></span> <span data-ttu-id="eb696-106">L'utilizzo di gruppi per popolare i ruoli semplifica la gestione di un numero elevato di utenti.</span><span class="sxs-lookup"><span data-stu-id="eb696-106">Using groups to populate roles makes it easier for you to manage large numbers of users.</span></span> <span data-ttu-id="eb696-107">Per ulteriori informazioni sulla creazione di gruppi o sull'assegnazione di un account utente a un gruppo, vedere l'argomento relativo a utenti e gruppi locali nella Guida in linea per lo strumento di amministrazione Gestione computer.</span><span class="sxs-lookup"><span data-stu-id="eb696-107">In the online help for the Computer Management administrative tool, see the topic "Local Users and Groups" for more information about creating groups or assigning a user account to a group.</span></span>

> [!Note]  
> <span data-ttu-id="eb696-108">Per consentire agli utenti di rete non autenticati di eseguire un'applicazione COM+, i ruoli applicazione devono includere l'utente anonimo.</span><span class="sxs-lookup"><span data-stu-id="eb696-108">To allow unauthenticated network users to run a COM+ application, the application roles must include the Anonymous user.</span></span> <span data-ttu-id="eb696-109">A partire da Windows Server 2003, per impostazione predefinita, l'utente anonimo non è incluso nel gruppo Everyone.</span><span class="sxs-lookup"><span data-stu-id="eb696-109">Starting with Windows Server 2003, by default, the Anonymous user is not included in the Everyone group.</span></span>

 

<span data-ttu-id="eb696-110">Dopo aver assegnato l'account utente al gruppo di Windows appropriato, attenersi alla procedura seguente per assegnare il gruppo di Windows al ruolo.</span><span class="sxs-lookup"><span data-stu-id="eb696-110">After you have assigned the user account to the appropriate Windows group, follow these steps to assign the Windows group to the role.</span></span>

<span data-ttu-id="eb696-111">**Per assegnare un gruppo di Windows a un ruolo di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="eb696-111">**To assign a Windows group to a security role**</span></span>

1.  <span data-ttu-id="eb696-112">Nell'albero della console dello strumento di amministrazione Servizi componenti individuare l'applicazione COM+ che contiene il ruolo a cui si desidera aggiungere l'account utente o il gruppo.</span><span class="sxs-lookup"><span data-stu-id="eb696-112">In the console tree of the Component Services administrative tool, locate the COM+ application that contains the role to which you want to add the user account or group.</span></span> <span data-ttu-id="eb696-113">Espandere la visualizzazione nell'albero della console fino a quando i ruoli dell'applicazione non sono visibili.</span><span class="sxs-lookup"><span data-stu-id="eb696-113">Expand the view in the console tree until the application's roles are visible.</span></span>

2.  <span data-ttu-id="eb696-114">Individuare il ruolo a cui si desidera aggiungere l'account utente o il gruppo.</span><span class="sxs-lookup"><span data-stu-id="eb696-114">Locate the role to which you want to add the user account or group.</span></span>

    > [!Note]  
    > <span data-ttu-id="eb696-115">Se il ruolo che si sta cercando non è presente nella cartella **roles** , il ruolo non è stato aggiunto all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="eb696-115">If the role you are looking for is not in the **Roles** folder, the role has not been added to the application.</span></span> <span data-ttu-id="eb696-116">Prima di poter assegnare gli account utente al ruolo, è necessario aggiungerlo all'applicazione dallo sviluppatore.</span><span class="sxs-lookup"><span data-stu-id="eb696-116">It must be added to the application by the developer before you can assign user accounts to the role.</span></span>

     

3.  <span data-ttu-id="eb696-117">Fare clic con il pulsante destro del mouse sulla cartella **utenti** del ruolo, scegliere **nuovo**, quindi fare clic su **utente**.</span><span class="sxs-lookup"><span data-stu-id="eb696-117">Right-click the **Users** folder in the role, point to **New**, and then click **User**.</span></span>

4.  <span data-ttu-id="eb696-118">Nella finestra **Seleziona utenti o gruppi** , nel riquadro inferiore, digitare il nome completo dell'utente o del gruppo che si desidera aggiungere.</span><span class="sxs-lookup"><span data-stu-id="eb696-118">In the **Select Users or Groups** window, in the bottom pane, type the fully qualified name of the user or group you want to add.</span></span> <span data-ttu-id="eb696-119">Se non si conosce il nome, fare clic sul pulsante **Avanzate** , quindi fare clic su **trova** per visualizzare un elenco di utenti e gruppi nel dominio selezionato.</span><span class="sxs-lookup"><span data-stu-id="eb696-119">If you do not know the name, click the **Advanced** button and then click **Find Now** to view a list of users and groups in the selected domain.</span></span> <span data-ttu-id="eb696-120">Selezionare un utente o un gruppo dall'elenco **nome (RDN)** , quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="eb696-120">Select a user or group from the **Name (RDN)** list, and click **OK**.</span></span>

5.  <span data-ttu-id="eb696-121">Per aggiungere altri account utente o gruppi, ripetere il passaggio 4.</span><span class="sxs-lookup"><span data-stu-id="eb696-121">To add more user accounts or groups, repeat step 4.</span></span>

6.  <span data-ttu-id="eb696-122">Al termine dell'aggiunta di account utente e gruppi al ruolo, fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="eb696-122">When you have finished adding user accounts and groups to the role, click **OK**.</span></span>

<span data-ttu-id="eb696-123">Per ogni account utente o gruppo assegnato al ruolo, viene visualizzata un'icona nella cartella **utenti** .</span><span class="sxs-lookup"><span data-stu-id="eb696-123">For each user account or group you have assigned to the role, an icon appears in the **Users** folder.</span></span> <span data-ttu-id="eb696-124">L'appartenenza al nuovo ruolo diventa effettiva al successivo avvio dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="eb696-124">The new role membership takes effect the next time the application is started.</span></span>

 

 




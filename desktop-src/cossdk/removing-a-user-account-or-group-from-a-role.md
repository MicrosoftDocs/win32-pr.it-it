---
description: Se un utente modifica i privilegi o se i ruoli vengono aggiunti a un'applicazione, è possibile spostare un account da un ruolo a un altro.
ms.assetid: 2d81a45a-9762-48b9-8395-3c3a4dcd5e8c
title: Rimozione di un account utente o di un gruppo da un ruolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 176272aef16af0d0a65d90f6a1d7628a5af232fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305211"
---
# <a name="removing-a-user-account-or-group-from-a-role"></a><span data-ttu-id="96c0e-103">Rimozione di un account utente o di un gruppo da un ruolo</span><span class="sxs-lookup"><span data-stu-id="96c0e-103">Removing a User Account or Group from a Role</span></span>

<span data-ttu-id="96c0e-104">Se i privilegi di un utente cambiano o se i ruoli vengono aggiunti a un'applicazione, è possibile spostare un account da un ruolo a un altro.</span><span class="sxs-lookup"><span data-stu-id="96c0e-104">If a user's privileges change or if roles are added to an application, you can move an account from one role to another role.</span></span> <span data-ttu-id="96c0e-105">Per spostare un account utente o un gruppo di utenti da un ruolo a un altro, è necessario rimuovere l'account utente o il gruppo dal ruolo corrente e quindi assegnarlo al nuovo ruolo.</span><span class="sxs-lookup"><span data-stu-id="96c0e-105">To move a user account or group of users from one role to another, you must remove the user account or group from its current role and then assign it to the new role.</span></span>

<span data-ttu-id="96c0e-106">**Per spostare un account utente o un gruppo da un ruolo a un altro**</span><span class="sxs-lookup"><span data-stu-id="96c0e-106">**To move a user account or group from one role to another**</span></span>

1.  <span data-ttu-id="96c0e-107">Rimuovere l'account utente o il gruppo dal ruolo a cui non deve più appartenere, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="96c0e-107">Remove the user account or group from the role that it should no longer belong to, as follows:</span></span>

    1.  <span data-ttu-id="96c0e-108">Nell'albero della console dello strumento di amministrazione Servizi componenti individuare l'applicazione COM+ che contiene il ruolo a cui si è interessati.</span><span class="sxs-lookup"><span data-stu-id="96c0e-108">In the console tree of the Component Services administrative tool, locate the COM+ application that contains the role you are interested in.</span></span> <span data-ttu-id="96c0e-109">Espandere la visualizzazione nell'albero della console fino a quando non saranno visibili gli utenti per il ruolo.</span><span class="sxs-lookup"><span data-stu-id="96c0e-109">Expand the view in the console tree until the users for the role are visible.</span></span>

    2.  <span data-ttu-id="96c0e-110">Fare clic con il pulsante destro del mouse sull'account utente o sul gruppo che si desidera rimuovere, quindi scegliere **Elimina**.</span><span class="sxs-lookup"><span data-stu-id="96c0e-110">Right-click the user account or group you want to remove, and then click **Delete**.</span></span>

    3.  <span data-ttu-id="96c0e-111">Quando richiesto dalla finestra di dialogo **Conferma eliminazione elemento** , fare clic su **Sì** per eliminare l'account utente o il gruppo.</span><span class="sxs-lookup"><span data-stu-id="96c0e-111">When prompted by the **Confirm Item Delete** dialog box, click **Yes** to delete the user account or group.</span></span>

    <span data-ttu-id="96c0e-112">L'account utente o il gruppo rimosso dal ruolo non viene più visualizzato nella cartella **utenti** .</span><span class="sxs-lookup"><span data-stu-id="96c0e-112">The user account or group that you have removed from the role no longer appears in the **Users** folder.</span></span>

2.  <span data-ttu-id="96c0e-113">Assegnare l'account utente o il gruppo rimosso ai ruoli a cui deve essere assegnato l'utente o il gruppo, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="96c0e-113">Assign the user account or group you have removed to the roles that the user or group should be assigned to, as follows:</span></span>

    1.  <span data-ttu-id="96c0e-114">Nell'albero della console dello strumento di amministrazione Servizi componenti individuare l'applicazione COM+ che contiene il ruolo a cui si desidera aggiungere l'account utente o il gruppo.</span><span class="sxs-lookup"><span data-stu-id="96c0e-114">In the console tree of the Component Services administrative tool, locate the COM+ application that contains the role to which you want to add the user account or group.</span></span> <span data-ttu-id="96c0e-115">Espandere la visualizzazione nell'albero della console fino a quando i ruoli dell'applicazione non sono visibili.</span><span class="sxs-lookup"><span data-stu-id="96c0e-115">Expand the view in the console tree until the application's roles are visible.</span></span>

    2.  <span data-ttu-id="96c0e-116">Individuare il ruolo a cui si desidera aggiungere l'account utente o il gruppo.</span><span class="sxs-lookup"><span data-stu-id="96c0e-116">Locate the role to which you want to add the user account or group.</span></span>

        > [!Note]  
        > <span data-ttu-id="96c0e-117">Se il ruolo che si sta cercando non è presente nella cartella **roles** , il ruolo non è stato aggiunto all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="96c0e-117">If the role you are looking for is not in the **Roles** folder, the role has not been added to the application.</span></span> <span data-ttu-id="96c0e-118">Prima di poter assegnare gli account utente al ruolo, è necessario aggiungerlo all'applicazione dallo sviluppatore.</span><span class="sxs-lookup"><span data-stu-id="96c0e-118">It must be added to the application by the developer before you can assign user accounts to the role.</span></span>

         

    3.  <span data-ttu-id="96c0e-119">Fare clic con il pulsante destro del mouse sulla cartella **utenti** del ruolo, scegliere **nuovo**, quindi fare clic su **utente**.</span><span class="sxs-lookup"><span data-stu-id="96c0e-119">Right-click the **Users** folder in the role, point to **New**, and then click **User**.</span></span>

    4.  <span data-ttu-id="96c0e-120">Nella finestra **Seleziona utenti o gruppi** , nel riquadro inferiore, digitare il nome completo dell'utente o del gruppo che si desidera aggiungere.</span><span class="sxs-lookup"><span data-stu-id="96c0e-120">In the **Select Users or Groups** window, in the bottom pane, type the fully qualified name of the user or group you want to add.</span></span> <span data-ttu-id="96c0e-121">Se non si conosce il nome, fare clic sul pulsante **Avanzate** , quindi fare clic su **trova** per visualizzare un elenco di utenti e gruppi nel dominio selezionato.</span><span class="sxs-lookup"><span data-stu-id="96c0e-121">If you do not know the name, click the **Advanced** button and then click **Find Now** to view a list of users and groups in the selected domain.</span></span> <span data-ttu-id="96c0e-122">Selezionare un utente o un gruppo dall'elenco **nome (RDN)** e fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="96c0e-122">Select a user or group from the **Name (RDN)** list and click **OK**.</span></span>

    5.  <span data-ttu-id="96c0e-123">Al termine dell'aggiunta dell'account utente o del gruppo al ruolo, fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="96c0e-123">When you have finished adding the user account or group to the role, click **OK**.</span></span>

    <span data-ttu-id="96c0e-124">Per ogni account utente o gruppo assegnato al ruolo, viene visualizzata un'icona nella cartella **utenti** .</span><span class="sxs-lookup"><span data-stu-id="96c0e-124">For each user account or group you have assigned to the role, an icon appears in the **Users** folder.</span></span>

<span data-ttu-id="96c0e-125">L'appartenenza al ruolo modificata per l'account utente o il gruppo diventa effettiva al successivo avvio dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="96c0e-125">The changed role membership for the user account or group takes effect the next time the application is started.</span></span>

 

 




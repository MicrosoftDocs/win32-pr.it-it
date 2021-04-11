---
description: È possibile rimuovere gli account utente o i gruppi da un ruolo quando agli utenti o ai membri dei gruppi non deve più essere concesso l'accesso alle risorse dell'applicazione a cui è assegnato il ruolo.
ms.assetid: d2cfa5cb-a143-41de-9aa2-7af7fce10ed7
title: Trasferimento di un account utente o di un gruppo a un ruolo diverso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2401d792066212269d4eaa4eb11eadfef6e2d73e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127406"
---
# <a name="moving-a-user-account-or-group-to-a-different-role"></a><span data-ttu-id="aead8-103">Trasferimento di un account utente o di un gruppo a un ruolo diverso</span><span class="sxs-lookup"><span data-stu-id="aead8-103">Moving a User Account or Group to a Different Role</span></span>

<span data-ttu-id="aead8-104">È possibile rimuovere gli account utente o i gruppi da un ruolo quando agli utenti o ai membri dei gruppi non deve più essere concesso l'accesso alle risorse dell'applicazione a cui è assegnato il ruolo.</span><span class="sxs-lookup"><span data-stu-id="aead8-104">You can remove user accounts or groups from a role when the users or members of the groups should no longer be given access to the application resources to which the role is assigned.</span></span>

<span data-ttu-id="aead8-105">**Per rimuovere un account utente o un gruppo da un ruolo**</span><span class="sxs-lookup"><span data-stu-id="aead8-105">**To remove a user account or group from a role**</span></span>

1.  <span data-ttu-id="aead8-106">Nell'albero della console dello strumento di amministrazione Servizi componenti individuare l'applicazione COM+ che contiene il ruolo a cui si è interessati.</span><span class="sxs-lookup"><span data-stu-id="aead8-106">In the console tree of the Component Services administrative tool, locate the COM+ application that contains the role you are interested in.</span></span> <span data-ttu-id="aead8-107">Espandere la visualizzazione nell'albero della console fino a quando non saranno visibili gli utenti per il ruolo.</span><span class="sxs-lookup"><span data-stu-id="aead8-107">Expand the view in the console tree until the users for the role are visible.</span></span>

2.  <span data-ttu-id="aead8-108">Fare clic con il pulsante destro del mouse sull'account utente o sul gruppo che si desidera rimuovere, quindi scegliere **Elimina**.</span><span class="sxs-lookup"><span data-stu-id="aead8-108">Right-click the user account or group you want to remove, and then click **Delete**.</span></span>

3.  <span data-ttu-id="aead8-109">Quando richiesto dalla finestra di dialogo **Conferma eliminazione elemento** , fare clic su **Sì** per eliminare l'account utente o il gruppo.</span><span class="sxs-lookup"><span data-stu-id="aead8-109">When prompted by the **Confirm Item Delete** dialog box, click **Yes** to delete the user account or group.</span></span>

<span data-ttu-id="aead8-110">L'account utente o il gruppo rimosso dal ruolo non viene più visualizzato nella cartella **utenti** .</span><span class="sxs-lookup"><span data-stu-id="aead8-110">The user account or group that you have removed from the role no longer appears in the **Users** folder.</span></span> <span data-ttu-id="aead8-111">L'appartenenza al nuovo ruolo diventa effettiva al successivo avvio dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="aead8-111">The new role membership takes effect the next time the application is started.</span></span> <span data-ttu-id="aead8-112">Se sono state apportate modifiche all' **applicazione di sistema**, è necessario riavviare il computer per rendere effettive le modifiche.</span><span class="sxs-lookup"><span data-stu-id="aead8-112">If you have made changes to the **System Application**, you must restart the computer for the changes to take effect.</span></span>

 

 




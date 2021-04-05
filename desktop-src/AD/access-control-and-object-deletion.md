---
title: Controllo di accesso e eliminazione di oggetti
description: Active Directory consente di eliminare un oggetto se si dispone dell'accesso DELETE per l'oggetto o ADS \_ Rights \_ DS \_ Delete \_ child Access per il tipo di oggetto nel contenitore padre.
ms.assetid: 87027c25-e3c9-4bad-8df3-cb6205e40ef6
ms.tgt_platform: multiple
keywords:
- Active Directory per il controllo di accesso e l'eliminazione di oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bddcd2b563e144743689f2a26c17bd417db14ee
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724375"
---
# <a name="access-control-and-object-deletion"></a><span data-ttu-id="e6ef6-104">Controllo di accesso e eliminazione di oggetti</span><span class="sxs-lookup"><span data-stu-id="e6ef6-104">Access Control and Object Deletion</span></span>

<span data-ttu-id="e6ef6-105">Active Directory Domain Services consentono di eliminare un oggetto se si dispone di uno dei seguenti diritti di accesso:</span><span class="sxs-lookup"><span data-stu-id="e6ef6-105">Active Directory Domain Services enable you to delete an object if you have one of the following access rights:</span></span>

-   <span data-ttu-id="e6ef6-106">Elimina accesso all'oggetto stesso</span><span class="sxs-lookup"><span data-stu-id="e6ef6-106">DELETE access to the object itself</span></span>
-   <span data-ttu-id="e6ef6-107">ADS \_ Rights \_ DS \_ eliminare l' \_ accesso figlio per quel tipo di oggetto nel contenitore padre</span><span class="sxs-lookup"><span data-stu-id="e6ef6-107">ADS\_RIGHT\_DS\_DELETE\_CHILD access for that object type on the parent container</span></span>

<span data-ttu-id="e6ef6-108">Tenere presente che il sistema verifica il descrittore di sicurezza sia per l'oggetto che per il relativo elemento padre prima di negare l'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="e6ef6-108">Be aware that the system verifies the security descriptor for both the object and its parent before denying the deletion.</span></span> <span data-ttu-id="e6ef6-109">Ciò significa che una voce ACE che nega in modo esplicito l'accesso DELETE a un utente non ha alcun effetto se l'utente dispone dell' \_ accesso figlio Delete nell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="e6ef6-109">This means that an ACE that explicitly denies DELETE access to a user has no effect if the user has DELETE\_CHILD access on the parent.</span></span> <span data-ttu-id="e6ef6-110">Analogamente, è possibile eseguire l'override di una voce ACE che nega l' \_ accesso figlio Delete nell'elemento padre se l'accesso DELETE è consentito per l'oggetto stesso.</span><span class="sxs-lookup"><span data-stu-id="e6ef6-110">Similarly, an ACE that denies DELETE\_CHILD access on the parent can be overridden if DELETE access is allowed on the object itself.</span></span>

<span data-ttu-id="e6ef6-111">Per eseguire un'operazione di eliminazione di una struttura ad albero, ad esempio usando il metodo [**IADsDeleteOps::D eleteobject**](/windows/desktop/api/iads/nf-iads-iadsdeleteops-deleteobject) , è necessario avere ads \_ Rights \_ DS \_ Delete \_ Tree Access all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e6ef6-111">To perform a tree-delete operation, for example using the [**IADsDeleteOps::DeleteObject**](/windows/desktop/api/iads/nf-iads-iadsdeleteops-deleteobject) method, you must have ADS\_RIGHT\_DS\_DELETE\_TREE access to the object.</span></span> <span data-ttu-id="e6ef6-112">Se si dispone di questo diritto di accesso, è possibile eliminare l'oggetto e tutti gli oggetti figlio indipendentemente dalle protezioni sugli oggetti figlio.</span><span class="sxs-lookup"><span data-stu-id="e6ef6-112">If you have this access right, you can delete the object and any child objects regardless of the protections on the child objects.</span></span> <span data-ttu-id="e6ef6-113">Per eliminare un albero se non si ha ADS \_ Rights \_ DS \_ Delete \_ Tree Access, è necessario attraversare in modo ricorsivo l'albero, eliminando singolarmente ogni oggetto.</span><span class="sxs-lookup"><span data-stu-id="e6ef6-113">To delete a tree if you do not have ADS\_RIGHT\_DS\_DELETE\_TREE access, you must recursively traverse the tree, deleting each object individually.</span></span> <span data-ttu-id="e6ef6-114">In questo caso, è necessario disporre dell'accesso figlio DELETE o DELETE necessario \_ per ogni oggetto nell'albero.</span><span class="sxs-lookup"><span data-stu-id="e6ef6-114">In this case, you must have the necessary DELETE or DELETE\_CHILD access for each object in the tree.</span></span>

> [!WARNING]
> <span data-ttu-id="e6ef6-115">Se gli utenti hanno ADS \_ Rights \_ DS \_ Delete \_ Tree Access per un oggetto, ciò consente di eliminare un intero sottoalbero, inclusi tutti gli oggetti figlio.</span><span class="sxs-lookup"><span data-stu-id="e6ef6-115">If users have ADS\_RIGHT\_DS\_DELETE\_TREE access for an object, this gives them the ability to delete a whole subtree, including all child objects.</span></span> <span data-ttu-id="e6ef6-116">Per questo motivo, è possibile prendere in considerazione la revoca dell'autorizzazione di accesso "Delete subtree" per tutti gli utenti in un contenitore padre.</span><span class="sxs-lookup"><span data-stu-id="e6ef6-116">For this reason, you may consider revoking "Delete Subtree" access permission for all users on a parent container.</span></span>

 

 

 
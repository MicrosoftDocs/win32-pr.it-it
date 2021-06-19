---
title: Gestire utenti
description: Informazioni sulla gestione degli utenti. Gli account utente vengono creati e archiviati come oggetti in Active Directory Domain Services.
ms.assetid: 57c83e4d-2d9f-4f22-97e2-27e2d277f014
ms.tgt_platform: multiple
keywords:
- Active Directory, uso, gestione degli utenti
- utenti AD
- utenti AD, gestione degli utenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8154dc9d062b86d10b0df6418b5b4cbb79b44d2
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395316"
---
# <a name="managing-users"></a><span data-ttu-id="14613-107">Gestire utenti</span><span class="sxs-lookup"><span data-stu-id="14613-107">Managing Users</span></span>

<span data-ttu-id="14613-108">Gli account utente vengono creati e archiviati come oggetti in Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="14613-108">User accounts are created and stored as objects in Active Directory Domain Services.</span></span> <span data-ttu-id="14613-109">Questi oggetti utente rappresentano utenti e computer.</span><span class="sxs-lookup"><span data-stu-id="14613-109">These user objects represent users and computers.</span></span> <span data-ttu-id="14613-110">Questa sezione definisce cosa sono gli utenti e come vengono usati e spiega come gestire gli utenti a livello di codice in Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="14613-110">This section defines what users are and how they are used, and explains how to programmatically manage users in Active Directory Domain Services.</span></span> <span data-ttu-id="14613-111">In questa sezione vengono illustrati gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="14613-111">This section discusses the following topics:</span></span>

-   [<span data-ttu-id="14613-112">Utenti in Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="14613-112">Users in Active Directory Domain Services</span></span>](users-in-active-directory-domain-services.md)
-   [<span data-ttu-id="14613-113">Entità di sicurezza</span><span class="sxs-lookup"><span data-stu-id="14613-113">Security Principals</span></span>](security-principals.md)
-   [<span data-ttu-id="14613-114">Che cos'è un utente?</span><span class="sxs-lookup"><span data-stu-id="14613-114">What is a User?</span></span>](what-is-a-user.md)
-   [<span data-ttu-id="14613-115">Codice di esempio per l'associazione al contenitore Users</span><span class="sxs-lookup"><span data-stu-id="14613-115">Example Code for Binding to the Users Container</span></span>](example-code-for-binding-to-the-users-container.md)
-   [<span data-ttu-id="14613-116">Attributi dell'oggetto utente</span><span class="sxs-lookup"><span data-stu-id="14613-116">User Object Attributes</span></span>](user-object-attributes.md)
-   [<span data-ttu-id="14613-117">Creazione di un utente</span><span class="sxs-lookup"><span data-stu-id="14613-117">Creating a User</span></span>](creating-a-user.md)
-   <span data-ttu-id="14613-118">Eliminazione di un utente.</span><span class="sxs-lookup"><span data-stu-id="14613-118">Deleting a user.</span></span> <span data-ttu-id="14613-119">Un utente viene eliminato nello stesso stato di qualsiasi altro oggetto in Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="14613-119">A user is deleted in the same was as any other object in Active Directory Domain Services.</span></span> <span data-ttu-id="14613-120">Per altre informazioni sull'eliminazione di oggetti, vedere [Creazione ed eliminazione di oggetti in Active Directory Domain Services](creating-and-deleting-objects-in-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="14613-120">For more information about deleting objects, see [Creating and Deleting Objects in Active Directory Domain Services](creating-and-deleting-objects-in-active-directory-domain-services.md).</span></span>
-   [<span data-ttu-id="14613-121">Enumerazione degli utenti</span><span class="sxs-lookup"><span data-stu-id="14613-121">Enumerating Users</span></span>](enumerating-users.md)
-   [<span data-ttu-id="14613-122">Esecuzione di query per gli utenti</span><span class="sxs-lookup"><span data-stu-id="14613-122">Querying for Users</span></span>](querying-for-users.md)
-   <span data-ttu-id="14613-123">Spostamento degli utenti.</span><span class="sxs-lookup"><span data-stu-id="14613-123">Moving users.</span></span> <span data-ttu-id="14613-124">Un utente viene spostato nello stesso stato di qualsiasi altro oggetto di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="14613-124">A user is moved in the same was as any other Active Directory object.</span></span> <span data-ttu-id="14613-125">Per altre informazioni sullo spostamento di oggetti Active Directory, vedere [Spostamento di oggetti](moving-objects.md).</span><span class="sxs-lookup"><span data-stu-id="14613-125">For more information about moving Active Directory objects, see [Moving Objects](moving-objects.md).</span></span>
-   [<span data-ttu-id="14613-126">Gestione degli utenti nei server membri e in Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="14613-126">Managing Users on Member Servers and Windows 2000 Professional</span></span>](managing-users-on-member-servers-and-windows-2000-professional.md)

 

 





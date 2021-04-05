---
title: Gestire utenti
description: Gli account utente vengono creati e archiviati come oggetti in Active Directory Domain Services.
ms.assetid: 57c83e4d-2d9f-4f22-97e2-27e2d277f014
ms.tgt_platform: multiple
keywords:
- Active Directory, utilizzo, gestione degli utenti
- utenti AD
- utenti AD, gestione utenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d1105132c6836e108a416331b2f4a6ad666c03d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855413"
---
# <a name="managing-users"></a><span data-ttu-id="ba514-106">Gestire utenti</span><span class="sxs-lookup"><span data-stu-id="ba514-106">Managing Users</span></span>

<span data-ttu-id="ba514-107">Gli account utente vengono creati e archiviati come oggetti in Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="ba514-107">User accounts are created and stored as objects in Active Directory Domain Services.</span></span> <span data-ttu-id="ba514-108">Questi oggetti utente rappresentano utenti e computer.</span><span class="sxs-lookup"><span data-stu-id="ba514-108">These user objects represent users and computers.</span></span> <span data-ttu-id="ba514-109">Questa sezione definisce gli utenti e il modo in cui vengono usati e spiega come gestire gli utenti a livello di codice in Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="ba514-109">This section defines what users are and how they are used, and explains how to programmatically manage users in Active Directory Domain Services.</span></span> <span data-ttu-id="ba514-110">In questa sezione vengono illustrati gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ba514-110">This section discusses the following topics:</span></span>

-   [<span data-ttu-id="ba514-111">Utenti in Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="ba514-111">Users in Active Directory Domain Services</span></span>](users-in-active-directory-domain-services.md)
-   [<span data-ttu-id="ba514-112">Entità di sicurezza</span><span class="sxs-lookup"><span data-stu-id="ba514-112">Security Principals</span></span>](security-principals.md)
-   [<span data-ttu-id="ba514-113">Che cos'è un utente?</span><span class="sxs-lookup"><span data-stu-id="ba514-113">What is a User?</span></span>](what-is-a-user.md)
-   [<span data-ttu-id="ba514-114">Codice di esempio per l'associazione al contenitore degli utenti</span><span class="sxs-lookup"><span data-stu-id="ba514-114">Example Code for Binding to the Users Container</span></span>](example-code-for-binding-to-the-users-container.md)
-   [<span data-ttu-id="ba514-115">Attributi dell'oggetto utente</span><span class="sxs-lookup"><span data-stu-id="ba514-115">User Object Attributes</span></span>](user-object-attributes.md)
-   [<span data-ttu-id="ba514-116">Creazione di un utente</span><span class="sxs-lookup"><span data-stu-id="ba514-116">Creating a User</span></span>](creating-a-user.md)
-   <span data-ttu-id="ba514-117">Eliminazione di un utente.</span><span class="sxs-lookup"><span data-stu-id="ba514-117">Deleting a user.</span></span> <span data-ttu-id="ba514-118">Un utente è stato eliminato allo stesso modo di qualsiasi altro oggetto in Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="ba514-118">A user is deleted in the same was as any other object in Active Directory Domain Services.</span></span> <span data-ttu-id="ba514-119">Per ulteriori informazioni sull'eliminazione di oggetti, vedere [creazione ed eliminazione di oggetti in Active Directory Domain Services](creating-and-deleting-objects-in-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="ba514-119">For more information about deleting objects, see [Creating and Deleting Objects in Active Directory Domain Services](creating-and-deleting-objects-in-active-directory-domain-services.md).</span></span>
-   [<span data-ttu-id="ba514-120">Enumerazione degli utenti</span><span class="sxs-lookup"><span data-stu-id="ba514-120">Enumerating Users</span></span>](enumerating-users.md)
-   [<span data-ttu-id="ba514-121">Esecuzione di query per gli utenti</span><span class="sxs-lookup"><span data-stu-id="ba514-121">Querying for Users</span></span>](querying-for-users.md)
-   <span data-ttu-id="ba514-122">Trasferimento degli utenti.</span><span class="sxs-lookup"><span data-stu-id="ba514-122">Moving users.</span></span> <span data-ttu-id="ba514-123">Un utente è stato spostato allo stesso modo di qualsiasi altro oggetto Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ba514-123">A user is moved in the same was as any other Active Directory object.</span></span> <span data-ttu-id="ba514-124">Per ulteriori informazioni sullo stato di Active Directory degli oggetti, vedere la pagina relativa al [trasferimento di oggetti](moving-objects.md).</span><span class="sxs-lookup"><span data-stu-id="ba514-124">For more information about moving Active Directory objects, see [Moving Objects](moving-objects.md).</span></span>
-   [<span data-ttu-id="ba514-125">Gestione degli utenti su server membri e Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ba514-125">Managing Users on Member Servers and Windows 2000 Professional</span></span>](managing-users-on-member-servers-and-windows-2000-professional.md)

 

 





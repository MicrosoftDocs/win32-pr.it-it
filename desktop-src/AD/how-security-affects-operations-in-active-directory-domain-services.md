---
title: Effetti della sicurezza sulle operazioni in Active Directory Domain Services
description: Active Directory Domain Services usare il controllo di accesso per concedere o negare l'accesso a oggetti, proprietà e operazioni in base all'identità dell'utente che esegue il tentativo di accesso.
ms.assetid: d5d53354-fa97-4e46-9632-20ac49f7db5a
ms.tgt_platform: multiple
keywords:
- Effetti della sicurezza in Active Directory Domain Services Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be628acd1709985aeaa9539bfa527de674732ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855422"
---
# <a name="how-security-affects-operations-in-active-directory-domain-services"></a><span data-ttu-id="2a74c-104">Effetti della sicurezza sulle operazioni in Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="2a74c-104">How Security Affects Operations in Active Directory Domain Services</span></span>

<span data-ttu-id="2a74c-105">Active Directory Domain Services usare il controllo di accesso per concedere o negare l'accesso a oggetti, proprietà e operazioni in base all'identità dell'utente che esegue il tentativo di accesso.</span><span class="sxs-lookup"><span data-stu-id="2a74c-105">Active Directory Domain Services use access control to grant or deny access to objects, properties, and operations based on the identity of the user performing the access attempt.</span></span> <span data-ttu-id="2a74c-106">Quando l'applicazione viene associata alla directory, viene associata a credenziali utente specifiche.</span><span class="sxs-lookup"><span data-stu-id="2a74c-106">When your application binds to the directory, it binds with specific user credentials.</span></span> <span data-ttu-id="2a74c-107">Una volta autenticate, queste credenziali determinano il contesto di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2a74c-107">When authenticated, these credentials determine your application's security context.</span></span> <span data-ttu-id="2a74c-108">Indipendentemente dal fatto che le credenziali siano quelle dell'utente connesso, un utente specificato, un account del servizio, un account computer o un utente non autenticato (Guest/Everyone), il Active Directory Server verifica il diritto dell'utente di accedere a un oggetto prima che venga eseguita un'operazione sull'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2a74c-108">Regardless of whether the credentials are those of the logged-on user, a specified user, a service account, a computer account, or an unauthenticated user (Guest/Everyone), the Active Directory server verifies the user's right to access an object before any operation is performed on that object.</span></span> <span data-ttu-id="2a74c-109">L'utente può, o meno, avere accesso a un particolare oggetto, ai relativi elementi figlio, alle relative proprietà o alle operazioni su tale oggetto, il che significa che l'applicazione deve gestire i potenziali errori causati dall'accesso negato.</span><span class="sxs-lookup"><span data-stu-id="2a74c-109">The user may, or may not, have access to a particular object, its children, its properties, or operations on that object, which means that your application must handle the potential errors caused by denied access.</span></span>

<span data-ttu-id="2a74c-110">Per ulteriori informazioni sui contesti di sicurezza e sugli effetti del controllo di accesso su varie operazioni, vedere:</span><span class="sxs-lookup"><span data-stu-id="2a74c-110">For more information about security contexts and the effects of access control on various operations, see:</span></span>

-   [<span data-ttu-id="2a74c-111">Controllo di accesso e operazioni di lettura</span><span class="sxs-lookup"><span data-stu-id="2a74c-111">Access Control and Read Operations</span></span>](access-control-and-read-operations.md)
-   [<span data-ttu-id="2a74c-112">Operazioni di scrittura e controllo di accesso</span><span class="sxs-lookup"><span data-stu-id="2a74c-112">Access Control and Write Operations</span></span>](access-control-and-write-operations.md)
-   [<span data-ttu-id="2a74c-113">Controllo di accesso e creazione di oggetti</span><span class="sxs-lookup"><span data-stu-id="2a74c-113">Access Control and Object Creation</span></span>](access-control-and-object-creation.md)
-   [<span data-ttu-id="2a74c-114">Controllo di accesso e eliminazione di oggetti</span><span class="sxs-lookup"><span data-stu-id="2a74c-114">Access Control and Object Deletion</span></span>](access-control-and-object-deletion.md)

 

 





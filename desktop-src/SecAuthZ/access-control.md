---
description: Il controllo di accesso si riferisce alle funzionalità di sicurezza che controllano gli utenti che possono accedere alle risorse nel sistema operativo. Le applicazioni chiamano funzioni di controllo di accesso per impostare gli utenti che possono accedere a risorse specifiche o controllare l'accesso alle risorse fornite dall'applicazione.
ms.assetid: d9ce4ec5-5c09-4b33-93a1-39638a925986
title: Controllo di accesso (autorizzazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31c0198f0ce0de77750e0587d9b54c1e20cee756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049894"
---
# <a name="access-control-authorization"></a><span data-ttu-id="b4d05-104">Controllo di accesso (autorizzazione)</span><span class="sxs-lookup"><span data-stu-id="b4d05-104">Access Control (Authorization)</span></span>

<span data-ttu-id="b4d05-105">Il controllo di accesso si riferisce alle funzionalità di sicurezza che controllano gli utenti che possono accedere alle risorse nel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b4d05-105">Access control refers to security features that control who can access resources in the operating system.</span></span> <span data-ttu-id="b4d05-106">Le applicazioni chiamano funzioni di controllo di accesso per impostare gli utenti che possono accedere a risorse specifiche o controllare l'accesso alle risorse fornite dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b4d05-106">Applications call access control functions to set who can access specific resources or control access to resources provided by the application.</span></span>

<span data-ttu-id="b4d05-107">In questa panoramica viene descritto il modello di sicurezza per controllare l'accesso agli oggetti di Windows, ad esempio i file, e per controllare l'accesso alle funzioni amministrative, ad esempio l'impostazione dell'ora di sistema o il controllo delle azioni dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b4d05-107">This overview describes the security model for controlling access to Windows objects, such as files, and for controlling access to administrative functions, such as setting the system time or auditing user actions.</span></span> <span data-ttu-id="b4d05-108">Nell'argomento [modello di controllo di accesso](access-control-model.md) viene fornita una descrizione di alto livello delle parti del controllo di accesso e del modo in cui interagiscono tra loro.</span><span class="sxs-lookup"><span data-stu-id="b4d05-108">The [Access Control Model](access-control-model.md) topic provides a high-level description of the parts of access control and how they interact with each other.</span></span>

<span data-ttu-id="b4d05-109">Negli argomenti seguenti viene descritto il controllo degli accessi:</span><span class="sxs-lookup"><span data-stu-id="b4d05-109">The following topics describe access control:</span></span>

-   [<span data-ttu-id="b4d05-110">Sicurezza a livello C2</span><span class="sxs-lookup"><span data-stu-id="b4d05-110">C2-level Security</span></span>](c2-level-security.md)
-   [<span data-ttu-id="b4d05-111">Modello di controllo di accesso</span><span class="sxs-lookup"><span data-stu-id="b4d05-111">Access Control Model</span></span>](access-control-model.md)
-   [<span data-ttu-id="b4d05-112">Linguaggio di definizione del descrittore di sicurezza</span><span class="sxs-lookup"><span data-stu-id="b4d05-112">Security Descriptor Definition Language</span></span>](security-descriptor-definition-language.md)
-   [<span data-ttu-id="b4d05-113">Privilegi</span><span class="sxs-lookup"><span data-stu-id="b4d05-113">Privileges</span></span>](privileges.md)
-   [<span data-ttu-id="b4d05-114">Generazione di controllo</span><span class="sxs-lookup"><span data-stu-id="b4d05-114">Audit Generation</span></span>](audit-generation.md)
-   [<span data-ttu-id="b4d05-115">Oggetti a protezione diretta</span><span class="sxs-lookup"><span data-stu-id="b4d05-115">Securable Objects</span></span>](securable-objects.md)
-   [<span data-ttu-id="b4d05-116">Controllo di accesso di basso livello</span><span class="sxs-lookup"><span data-stu-id="b4d05-116">Low-level Access Control</span></span>](low-level-access-control.md)

<span data-ttu-id="b4d05-117">Di seguito sono riportate le attività comuni di controllo di accesso:</span><span class="sxs-lookup"><span data-stu-id="b4d05-117">The following are common access control tasks:</span></span>

-   [<span data-ttu-id="b4d05-118">Come gli elenchi DACL controllano l'accesso a un oggetto</span><span class="sxs-lookup"><span data-stu-id="b4d05-118">How DACLs Control Access to an Object</span></span>](how-dacls-control-access-to-an-object.md)
-   [<span data-ttu-id="b4d05-119">Controllo della creazione di oggetti figlio in C++</span><span class="sxs-lookup"><span data-stu-id="b4d05-119">Controlling Child Object Creation in C++</span></span>](controlling-child-object-creation-in-c--.md)
-   [<span data-ttu-id="b4d05-120">ACE per controllare l'accesso alle proprietà di un oggetto</span><span class="sxs-lookup"><span data-stu-id="b4d05-120">ACEs to Control Access to an Object's Properties</span></span>](aces-to-control-access-to-an-object-s-properties.md)
-   [<span data-ttu-id="b4d05-121">Richiesta di diritti di accesso a un oggetto</span><span class="sxs-lookup"><span data-stu-id="b4d05-121">Requesting Access Rights to an Object</span></span>](requesting-access-rights-to-an-object.md)

<span data-ttu-id="b4d05-122">Negli argomenti seguenti viene fornito il codice di esempio per le attività di controllo di accesso:</span><span class="sxs-lookup"><span data-stu-id="b4d05-122">The following topics provide example code for access control tasks:</span></span>

-   [<span data-ttu-id="b4d05-123">Modifica degli ACL di un oggetto in C++</span><span class="sxs-lookup"><span data-stu-id="b4d05-123">Modifying the ACLs of an Object in C++</span></span>](modifying-the-acls-of-an-object-in-c--.md)
-   [<span data-ttu-id="b4d05-124">Creazione di un descrittore di sicurezza per un nuovo oggetto in C++</span><span class="sxs-lookup"><span data-stu-id="b4d05-124">Creating a Security Descriptor for a New Object in C++</span></span>](creating-a-security-descriptor-for-a-new-object-in-c--.md)
-   [<span data-ttu-id="b4d05-125">Controllo della creazione di oggetti figlio in C++</span><span class="sxs-lookup"><span data-stu-id="b4d05-125">Controlling Child Object Creation in C++</span></span>](controlling-child-object-creation-in-c--.md)
-   [<span data-ttu-id="b4d05-126">Abilitazione e disabilitazione dei privilegi in C++</span><span class="sxs-lookup"><span data-stu-id="b4d05-126">Enabling and Disabling Privileges in C++</span></span>](enabling-and-disabling-privileges-in-c--.md)
-   [<span data-ttu-id="b4d05-127">Ricerca di un SID in un token di accesso in C++</span><span class="sxs-lookup"><span data-stu-id="b4d05-127">Searching for a SID in an Access Token in C++</span></span>](searching-for-a-sid-in-an-access-token-in-c--.md)
-   [<span data-ttu-id="b4d05-128">Ricerca del proprietario di un oggetto file in C++</span><span class="sxs-lookup"><span data-stu-id="b4d05-128">Finding the Owner of a File Object in C++</span></span>](finding-the-owner-of-a-file-object-in-c--.md)
-   [<span data-ttu-id="b4d05-129">Assunzione della proprietà di un oggetto in C++</span><span class="sxs-lookup"><span data-stu-id="b4d05-129">Taking Object Ownership in C++</span></span>](taking-object-ownership-in-c--.md)
-   [<span data-ttu-id="b4d05-130">Creazione di un DACL</span><span class="sxs-lookup"><span data-stu-id="b4d05-130">Creating a DACL</span></span>](/windows/desktop/SecBP/creating-a-dacl)

 

 

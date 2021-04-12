---
title: Ereditarietà e delega dell'amministrazione
description: Viene descritto il supporto di servizi di dominio Active Directory per l'ereditarietà delle autorizzazioni nell'albero degli oggetti e anche l'ereditarietà specifica dell'oggetto.
ms.assetid: db9cf8d9-6831-4456-b2a5-9f5b4f3e9100
ms.tgt_platform: multiple
keywords:
- ereditarietà dell'amministrazione e delega Active Directory
- Active Directory Active Directory, ereditarietà delle autorizzazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d76db80497b54e71c806f3ccff9df549f9b2c1a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220933"
---
# <a name="inheritance-and-delegation-of-administration"></a><span data-ttu-id="2c9c6-105">Ereditarietà e delega dell'amministrazione</span><span class="sxs-lookup"><span data-stu-id="2c9c6-105">Inheritance and Delegation of Administration</span></span>

<span data-ttu-id="2c9c6-106">Active Directory Domain Services supporta l'ereditarietà delle autorizzazioni nell'albero degli oggetti per consentire l'esecuzione delle attività di amministrazione a livelli più elevati nell'albero.</span><span class="sxs-lookup"><span data-stu-id="2c9c6-106">Active Directory Domain Services supports the inheritance of permissions down the object tree to allow administration tasks to be performed at higher levels in the tree.</span></span> <span data-ttu-id="2c9c6-107">Ciò consente agli amministratori di configurare le autorizzazioni ereditabili sugli oggetti vicini alla radice, ad esempio le unità di dominio e organizzative, e di distribuire tali autorizzazioni a vari oggetti dell'albero.</span><span class="sxs-lookup"><span data-stu-id="2c9c6-107">This enables administrators to set up inheritable permissions on objects near the root, such as domain and organizational units, and have those permissions distributed to various objects in the tree.</span></span>

<span data-ttu-id="2c9c6-108">L'ereditarietà può essere impostata in base a ACE.</span><span class="sxs-lookup"><span data-stu-id="2c9c6-108">Inheritance can be set on a per-ACE basis.</span></span> <span data-ttu-id="2c9c6-109">Nella tabella seguente sono elencati i flag che è possibile specificare in **AceFlags** per controllare l'ereditarietà della voce ACE.</span><span class="sxs-lookup"><span data-stu-id="2c9c6-109">The following table lists flags that can be specified in the **AceFlags** to control inheritance of the ACE.</span></span>



| <span data-ttu-id="2c9c6-110">Flag</span><span class="sxs-lookup"><span data-stu-id="2c9c6-110">Flag</span></span>                                                     | <span data-ttu-id="2c9c6-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c9c6-111">Description</span></span>                                                                                                                                     |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c9c6-112">**ADS \_ ACEFLAG \_ eredita \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="2c9c6-112">**ADS\_ACEFLAG\_INHERIT\_ACE**</span></span><br/>                | <span data-ttu-id="2c9c6-113">Determina l'ereditarietà della voce ACE nell'albero.</span><span class="sxs-lookup"><span data-stu-id="2c9c6-113">Causes the ACE to be inherited down in the tree.</span></span><br/>                                                                                     |
| <span data-ttu-id="2c9c6-114">**ADS \_ ACEFLAG \_ No \_ propagate \_ eredita \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="2c9c6-114">**ADS\_ACEFLAG\_NO\_PROPAGATE\_INHERIT\_ACE**</span></span><br/> | <span data-ttu-id="2c9c6-115">Determina l'ereditarietà della voce ACE su un solo livello nell'albero.</span><span class="sxs-lookup"><span data-stu-id="2c9c6-115">Causes the ACE to be inherited down only one level in the tree.</span></span><br/>                                                                      |
| <span data-ttu-id="2c9c6-116">**ADS \_ ACEFLAG \_ ereditano \_ solo \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="2c9c6-116">**ADS\_ACEFLAG\_INHERIT\_ONLY\_ACE**</span></span><br/>          | <span data-ttu-id="2c9c6-117">Fa in modo che la voce ACE venga ignorata sull'oggetto su cui è specificato, che venga ereditata solo in basso ed è valida in cui è stata ereditata.</span><span class="sxs-lookup"><span data-stu-id="2c9c6-117">Causes the ACE to be ignored on the object it is specified on, only be inherited down, and be effective where it has been inherited.</span></span><br/> |



 

<span data-ttu-id="2c9c6-118">Oltre a impostare l'ereditarietà, Active Directory Domain Services supporta l'ereditarietà specifica dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2c9c6-118">In addition to setting inheritance, Active Directory Domain Services supports object-specific inheritance.</span></span> <span data-ttu-id="2c9c6-119">In questo modo, le voci ACE ereditabili possono essere ereditate dall'albero, ma sono valide solo per un tipo specifico di oggetto.</span><span class="sxs-lookup"><span data-stu-id="2c9c6-119">This allows the inheritable ACEs to be inherited down the tree, but be effective only on a specific type of object.</span></span> <span data-ttu-id="2c9c6-120">Questa operazione è estremamente utile per delegare l'amministrazione.</span><span class="sxs-lookup"><span data-stu-id="2c9c6-120">This is extremely useful in delegating administration.</span></span> <span data-ttu-id="2c9c6-121">Ad esempio, può essere usato per impostare una voce ACE ereditabile specifica dell'oggetto in un'unità organizzativa che consente a un gruppo di avere il controllo completo su tutti gli oggetti utente nell'unità organizzativa, ma nient'altro.</span><span class="sxs-lookup"><span data-stu-id="2c9c6-121">For example, this can be used to set an object-specific inheritable ACE at an organizational unit that enables a group to have full control on all user objects in the organizational unit, but nothing else.</span></span> <span data-ttu-id="2c9c6-122">In questo modo, la gestione degli utenti in tale unità organizzativa viene delegata agli utenti di tale gruppo.</span><span class="sxs-lookup"><span data-stu-id="2c9c6-122">Thereby, the management of users in that organizational unit gets delegated to the users in that group.</span></span>

### <a name="delegating-service-administration-with-security-groups"></a><span data-ttu-id="2c9c6-123">Delega dell'amministrazione del servizio con gruppi di sicurezza</span><span class="sxs-lookup"><span data-stu-id="2c9c6-123">Delegating Service Administration with Security Groups</span></span>

<span data-ttu-id="2c9c6-124">Usare i gruppi di sicurezza per definire e delegare i ruoli amministrativi associati al server applicazioni.</span><span class="sxs-lookup"><span data-stu-id="2c9c6-124">Use Security groups to define and delegate administrative roles associated with your application server.</span></span> <span data-ttu-id="2c9c6-125">Ad esempio, il servizio può essere associato a un gruppo amministratori di servizi.</span><span class="sxs-lookup"><span data-stu-id="2c9c6-125">For example, your service may be associated with a group MyService Administrators.</span></span> <span data-ttu-id="2c9c6-126">Gli utenti che sono identificati come amministratori del servizio verranno aggiunti al gruppo di amministratori del servizio.</span><span class="sxs-lookup"><span data-stu-id="2c9c6-126">Users who are identified as the MyService administrators will be added to MyService Administrators group.</span></span> <span data-ttu-id="2c9c6-127">Il programma di installazione per il servizio può impostare gli ACL nella directory per consentire agli amministratori del servizio di disporre di autorizzazioni sufficienti per la lettura/scrittura degli attributi correlati al servizio o per la creazione di oggetti specifici del servizio, ad esempio.</span><span class="sxs-lookup"><span data-stu-id="2c9c6-127">The setup program for MyService can set ACLs on the directory to enable MyService Administrators sufficient permissions to read/write MyService-related attributes or create MyService-specific objects for example.</span></span>

### <a name="roles-in-security-groups-for-computers-running-your-service"></a><span data-ttu-id="2c9c6-128">Ruoli nei gruppi di sicurezza per i computer che eseguono il servizio</span><span class="sxs-lookup"><span data-stu-id="2c9c6-128">Roles in Security Groups for Computers Running Your Service</span></span>

<span data-ttu-id="2c9c6-129">Usare i gruppi di sicurezza per definire il set di computer a cui viene concesso l'accesso agli oggetti del servizio nella directory.</span><span class="sxs-lookup"><span data-stu-id="2c9c6-129">Use security groups to define the set of computers that are granted access to your service's objects in the directory.</span></span> <span data-ttu-id="2c9c6-130">Ad esempio, il servizio può essere associato a un server Servizi di gruppo.</span><span class="sxs-lookup"><span data-stu-id="2c9c6-130">For example, your service may be associated with a group MyService Servers.</span></span> <span data-ttu-id="2c9c6-131">Tutti i computer in cui è in esecuzione il server di servizio vengono aggiunti al gruppo di server di servizio e a questo gruppo può essere concesso l'accesso alle parti della directory in cui i server dei servizi devono leggere/scrivere i dati.</span><span class="sxs-lookup"><span data-stu-id="2c9c6-131">All computers running the MyService server are added to MyService Servers group and this group can then be given access to parts of the directory where MyService servers need to read/write data.</span></span> <span data-ttu-id="2c9c6-132">Il programma di installazione per il servizio può impostare gli ACL nella directory per consentire ai server di servizi di disporre di autorizzazioni sufficienti per la lettura/scrittura degli attributi correlati al servizio o per la creazione di oggetti specifici del servizio, ad esempio.</span><span class="sxs-lookup"><span data-stu-id="2c9c6-132">The setup program for MyService can set ACLs on the directory to enable MyService Servers sufficient permissions to read/write MyService-related attributes or create MyService-specific objects for example.</span></span>

 

 





